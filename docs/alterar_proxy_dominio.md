# Tutorial de Migração: DuckDNS + Nginx Proxy Manager para Traefik + api.olyon.cloud

Este guia passo a passo demonstra como migrar uma aplicação hospedada em VPS (utilizada no projeto `barb-api-test`), saindo do domínio dinâmico (`duckdns.org`) com Nginx Proxy Manager e adotando o **Traefik** com roteamento seguro e certificado SSL automático para o novo domínio `api.olyon.cloud`.

---

## Passo 1: Configurar o DNS do novo domínio
Antes de alterar qualquer arquivo no servidor, o novo subdomínio precisa apontar diretamente para o IP do seu VPS.

1. Acesse o gerenciador de DNS do seu provedor de domínio (ex: Hostinger).
2. Crie ou ajuste um registro **A** com os seguintes parâmetros:
   * **Tipo:** `A`
   * **Nome / Host:** `api` (para que o endereço completo fique `api.olyon.cloud`)
   * **Aponta para (Destino / IP):** `187.77.242.6`
   * **TTL:** 5 minutos (ou padrão)
3. Salve as alterações e aguarde alguns minutos para a propagação global do DNS.

---

## Passo 2: Liberar as portas 80 e 443 do Nginx Proxy Manager
O Traefik precisa assumir obrigatoriamente as portas de entrada padrão da web (`80` para HTTP e `443` para HTTPS). Se o Nginx Proxy Manager estiver rodando nelas, haverá conflito de portas.

1. Acesse o painel do seu VPS (via Gerenciador Docker ou SSH).
2. **Pare e desative** o projeto do Nginx Proxy Manager para liberar as portas. 
   > *Dica: Certifique-se de salvar ou anotar informações de certificados ou configurações antigas caso precise consultá-las futuramente.*

---

## Passo 3: Implantar o Traefik
Com as portas padrão livres:

1. Inicie a instalação/implantação do Traefik no seu VPS.
2. Certifique-zse de que o Traefik está configurado para:
   * Utilizar as portas externas **80:80** e **443:443**.
   * Criar ou conectar-se à rede externa compartilhada chamada **`traefik-proxy`**.

---

## Passo 4: Atualizar o arquivo `.yaml` (Docker Compose) do projeto
Ajuste o arquivo de configuração do seu projeto (ex: `barb-api-test`) para remover o acesso direto por porta e integrá-lo ao ecossistema do Traefik através de labels.

```yaml
services:
  barb-api:
    build:
      context: ../../../*
      dockerfile: Dockerfile
    image: apexlone/barb-api:${BARB_API_IMAGE_TAG}
    container_name: barb-api-${ENV_NAME}
    user: root
    restart: always
    env_file:
      - ../../../env/.env.${ENV_NAME}
    networks:
      - apex-network
      - traefik-proxy
    labels:
      - "traefik.enable=true"
      - "traefik.docker.network=traefik-proxy"
      - "traefik.http.routers.barb-api-test.rule=Host(`api.olyon.cloud`)"
      - "traefik.http.routers.barb-api-test.entrypoints=websecure"
      - "traefik.http.routers.barb-api-test.tls.certresolver=letsencrypt"
      - "traefik.http.services.barb-api-test.loadbalancer.server.port=8081"
    healthcheck:
      test: ["CMD-SHELL", "curl -f http://localhost:${BARB_API_INTERNAL_PORT}/actuator/health || exit 1"]
      interval: 10s
      timeout: 5s
      retries: 5
      start_period: 30s

networks:
  apex-network:
    name: apex-network-${ENV_NAME}
    external: true
  traefik-proxy:
    external: true

### O que mudou nesta estrutura:

* **Remoção de portas diretas:** A linha de mapeamento de porta externa foi apagada (`ports: ...`). A API não expõe mais sua porta de forma isolada para fora do servidor.
* **Inclusão da rede:** Adicionada a rede externa `- traefik-proxy` para que o Traefik se comunique com o container.
* **Labels do Traefik:**
  * `rule=Host(api.olyon.cloud)`: Define o novo domínio de acesso.
  * `entrypoints=websecure`: Utiliza a porta segura (HTTPS).
  * `tls.certresolver=letsencrypt`: Solicita a geração automática do certificado SSL.
  * `loadbalancer.server.port=8081`: Direciona o tráfego para a porta interna correta da sua aplicação.

---

### Passo 5: Reimplantar e Validar

1. Salve o arquivo YAML atualizado no diretório do seu projeto ou painel de gerenciamento.
2. Reimplante / Atualize o container do projeto `barb-api-test`.
3. Monitore os logs do Traefik para garantir que ele reconheceu as novas labels e emitiu o certificado SSL Let's Encrypt com sucesso para `api.olyon.cloud`.
4. Acesse `https://api.olyon.cloud` pelo navegador ou faça uma requisição de teste para validar o fluxo completo.
