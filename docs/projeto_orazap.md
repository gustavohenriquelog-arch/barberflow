# 🚀 OraZap - Sistema de Agendamento Inteligente & Conversacional

O **OraZap** é uma plataforma de inteligência conversacional e agendamento automático via WhatsApp criada sob o conceito **minimalista e mobile-first**. O nosso objetivo é auxiliar pequenas e médias empresas (PMEs) e profissionais autônomos a modernizarem e automatizarem seus processos a um preço justo, permitindo que empreendedores tenham mais tempo para focar no crescimento do negócio.

Ao contrário de sistemas legados complexos e burocráticos, o OraZap remove toda a fricção: sem aplicativos pesados, sem cadastros longos para o cliente final e sem painéis administrativos inacessíveis pelo celular.

---

## 🎯 Nosso Posicionamento de Mercado (Ataque às Brechas)

Mapeamos os maiores concorrentes do mercado (*Trinks, HoraZap, SmartZaap, RobotiZap*) e projetamos o OraZap para atacar exatamente onde eles falham:

1.  **Fricção Zero para o Cliente Final:** Diferente do *Trinks* (que exige download de app ou login em portais), o cliente do OraZap agenda tudo conversando naturalmente no WhatsApp que já usa todo dia.
2.  **Agilidade Mobile-First:** Focado no profissional que não tem tempo de gerenciar ERPs em computadores. O setup leva menos de 5 minutos no celular:
    *   1️⃣ Conecta o WhatsApp via QR Code ou API Oficial.
    *   2️⃣ Configura os serviços, horários e duração.
    *   3️⃣ A IA assume o atendimento, agenda de forma autônoma e notifica o calendário nativo do celular do profissional.
3.  **Acessibilidade Financeira:** Frente a planos de multiatendimento caros (como *SmartZaap* a R$ 290/mês), o OraZap foca em democratizar o acesso para o microempreendedor individual (MEI) e prestadores de serviços autônomos com planos de entrada competitivos.

---

## 🛠️ Arquitetura Tecnológica & Conectividade

O OraZap adota uma infraestrutura híbrida, permitindo que o cliente escolha o melhor balanço entre custo e estabilidade de acordo com a maturidade do seu negócio.

### 🔌 1. Métodos de Conexão com o WhatsApp
*   **Conexão via QR Code (Instância Não Oficial):** Alternativa de baixo custo e ativação instantânea. Ideal para profissionais autônomos, testes rápidos, validação de MVP ou negócios com baixo orçamento inicial.
*   **Conexão via API Oficial Cloud (Meta Verified):** Conectividade direta e homologada pela Meta. Extremamente estável, escalável e segura contra o risco de banimento da linha de WhatsApp. Recomendada para clínicas e redes de alto volume de mensagens.

### 🧠 2. Motores de Inteligência Artificial (LLMs)
O sistema opera de forma modular, podendo alternar o motor de processamento de linguagem natural do robô de agendamento:
*   **GPT-5 (OpenAI):** IA de última geração baseada em nuvem para máxima precisão contextual, respostas ultra-humanizadas e entendimento perfeito de nuances conversacionais complexas.
*   **Ollama (Open-Source / Local LLM):** Integração com modelos de linguagem abertos rodando em servidores dedicados. Ideal para otimizar custos operacionais de escala de mensagens ou para clientes que exigem total privacidade de dados locais.

### 🎛️ 3. Orquestração de Fluxos com n8n
Toda a lógica de negócios, triagem de mensagens, controle de status, envio de notificações e integrações externas é orquestrada de forma visual e robusta pelo **n8n**.
*   Garante agilidade extrema no desenvolvimento e manutenção de fluxos de conversação.
*   Simplifica conexões futuras com CRMs, gateways de pagamento e planilhas de forma dinâmica.

---

## 📅 Sistema de Agendamento Independente

Diferente de integradores que dependem exclusivamente de plataformas terceiras de agenda, o OraZap conta com um **Sistema de Agendamento Independente nativo**, construído para ser a única fonte de verdade do estabelecimento.

### Principais Diferenciais:
*   **Sincronização Bidirecional Nativa:** Integração instantânea com o Google Calendar e Apple Calendar dos profissionais para bloquear horários ocupados de forma automatizada.
*   **Lista de Espera Inteligente:** Se um horário nobre for cancelado, a IA do OraZap detecta o buraco na agenda e oferece a vaga de forma proativa aos clientes que estavam na fila de espera no WhatsApp.
*   **Gestão Simplificada:** Painel mobile simplificado para o prestador de serviços gerenciar bloqueios manuais de horários, folgas e consultar o faturamento diário.

---

## 📂 Estrutura do Repositório

```text
├── .github/                  # Configurações do GitHub (Workflows, etc.)
├── docs/                     # Documentações adicionais e pesquisas de mercado
├── n8n-workflows/            # Arquivos JSON de exportação dos fluxos do n8n
├── src/                      # Código-fonte da aplicação (Frontend & Backend)
│   ├── calendar/             # Módulo do sistema de agendamento independente
│   ├── connection/           # Módulo de conexões (QR Code / API Cloud)
│   └── ai/                   # Integrações de LLM (GPT-5 / Ollama)
└── README.md                 # Documento principal
