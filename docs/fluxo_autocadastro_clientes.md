# 🚀 Fluxo de Onboarding e Autocadastro de Clientes (OraZap)

Este documento especifica a jornada de integração automática do cliente (*Onboarding Self-Service*), detalhando como o estabelecimento ou profissional autônomo realiza o cadastro, ativa o período de teste e configura o **OraZap** sem necessidade de intervenção humana.

---

### 1. Visão Geral do Onboarding

Para manter a premissa de **Zero Fricção e Alta Conversão**, o processo de entrada do cliente é 100% automatizado através da Landing Page oficial do produto. A meta é permitir que o profissional saia do cadastro inicial para o primeiro agendamento via WhatsApp em menos de 5 minutos.

### 2. Etapas Detalhadas da Jornada do Cliente

#### Etapa 1: Acesso e Ativação do Trial (Landing Page)
1. O cliente acessa o link oficial da plataforma (`www.orazap.tech`).
2. Clica no botão de chamada para ação (*CTA*): **"Testar Grátis por 15 Dias"** ou **"Iniciar Teste Gratuito"**.
3. **Conversão de Baixo Atrito:** O cadastro inicial solicita apenas as informações essenciais para a criação do ambiente:
   * Nome do Responsável / Estabelecimento;
   * E-mail para login;
   * WhatsApp para contato e notificações;
   * Criação de senha.
4. **Sem Cartão de Crédito:** Não é solicitada nenhuma informação financeira ou meio de pagamento no momento da adesão. O período de degustação de 15 dias é liberado automaticamente após a confirmação.

#### Etapa 2: Setup Mobile-First das Regras de Negócio
Após a conclusão do cadastro, o usuário é direcionado para um assistente de configuração simplificado, projetado com foco total em telas de smartphones:

1. **Informações do Estabelecimento:**
   * Nome comercial que a IA utilizará para se apresentar (ex: *"Barbearia do Silva"*).
   * Endereço físico ou indicação de atendimento domiciliar/remoto.
   * Horários de funcionamento (dias da semana e intervalos de almoço/pausa).

2. **Cadastro de Serviços e Preços:**
   * Lista dos serviços oferecidos (ex: *Corte Social, Barba Completa, Combo*).
   * Duração estimada de cada procedimento (ex: *30 min, 45 min*).
   * Valores cobrados por cada item.

3. **Conexão da Agenda e WhatsApp:**
   * Conexão com a plataforma de agendamento Web.
   * Vinculação da instância de WhatsApp (via escaneamento de QR Code ou autenticação da API Cloud).

---

### 3. Proposta de Valor no Pós-Cadastro

Ao concluir esses 3 passos rápidos, a conta do **OraZap** entra em operação imediata.

> **Impacto na Rotina do Profissional:**  
> A partir do momento em que o cadastro é finalizado, o **OraZap** assume de forma autônoma e inteligente a gestão de horários, a triagem de mensagens e a confirmação de compromissos 24 horas por dia. O barbeiro ou prestador de serviços deixa de interromper o atendimento manual para responder mensagens no celular e passa a focar exclusivamente na execução do seu trabalho principal.

---

### 4. Regras do Período de Degustação (Trial de 15 Dias)

* **Acesso Total:** Durante os 15 dias, o cliente tem acesso irrestrito às funcionalidades do plano Starter (agendamentos por IA ilimitados e sincronização de agenda).
* **Régua de Reengajamento:** No 10º e 14º dia de teste, o sistema dispara lembretes via WhatsApp e e-mail informando sobre a conclusão do período gratuito.
* **Transição para Assinatura:** No 15º dia, é exibida a tela para inclusão do método de pagamento (Cartão de Crédito ou PIX Recorrente) no valor de R$ 87,90/mês para manter o serviço ativo sem interrupções.

---
*OraZap Pro — Documentação de Requisitos de Produto (PRD).*
