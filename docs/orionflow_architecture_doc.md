# Documento de Arquitetura e Visão de Negócio — OrionFlow

> **Nota de Nomenclatura:** Projeto anteriormente denominado **OraZap**, renomeado provisoriamente para **OrionFlow** (sujeito a alterações futuras).

---

## 1. Resumo Executivo e Proposta de Valor

O **OrionFlow** é uma solução de software como serviço (SaaS) focada na automação inteligente de agendamentos via WhatsApp para profissionais solo e pequenas empresas (ex: barbearias). 

O sistema resolve a dor do empreendedor que perde receita por não conseguir responder clientes enquanto atende, entregando uma secretária virtual baseada em Inteligência Artificial com **onboarding simples (< 5 minutos)** e **experiência sem complexidade**.

---

## 2. Visão de Arquitetura Técnica

[ Cliente no WhatsApp ]
│
▼
[ API Oficial da Meta (Cloud API) ]
│  (1.000 conversas gratuitas/mês por WABA)
▼
[ Orquestrador n8n + LLM (OpenAI / Ollama) ]
│
├── (Protocolo MCP / API REST)
▼
[ Plataforma Web OrionFlow ]
│  (Gestão de Agenda, Clientes e Dashboard)
▼
[ Banco de Dados ]


### Componentes Principais

1. **Mensageria — API Oficial da Meta (Cloud API):**
   * Estabilidade total sem risco de banimento de chips.
   * Utilização da franquia de **1.000 conversas de atendimento (Service) gratuitas/mês** por conta do WhatsApp Business (WABA).

2. **Orquestração e Inteligência — n8n + LLM:**
   * **n8n:** Gerencia gatilhos de entrada, janelas de 24 horas e parsing de mensagens.
   * **LLM (OpenAI / Ollama):** Entende intenções em linguagem natural, trata exceções e extrai datas e horários.
     * **OpenAI (gpt-4.1-mini):** Opção gerenciada de alta precisão e baixo custo em nuvem.
     * **Ollama (Modelos Local/Self-hosted):** Opção local e independente para execução de modelos open-source (ex: Llama, Mistral, Qwen) reduzindo custos de API e garantindo privacidade total dos dados.

3. **Integração de Dados — Protocolo MCP (Model Context Protocol):**
   * Interface padronizada e segura entre a IA/n8n e o backend do OrionFlow.
   * Ferramentas expostas: consulta de disponibilidade (`get_slots`), criação de agendamento (`create_booking`), cancelamento (`cancel_booking`) e reagendamento (`reschedule_booking`).

4. **Aplicação Web — Plataforma OrionFlow:**
   * Painel de controle do barbeiro para acompanhamento da agenda em tempo real.
   * Histórico de conversas e transparência total de atendimento para garantir a segurança e controle do cliente.

---

## 3. Unidade Econômica (Unit Economics)

| Métrica | Valor Estimado (SaaS Cloud) | Valor Estimado (Ollama Self-hosted) |
| :--- | :--- | :--- |
| **Ticket Médio Mensal** | R$ 79,90 / mês | R$ 79,90 / mês |
| **Volume de Agendamentos (Barbeiro Solo)** | ~300 agendamentos / mês | ~300 agendamentos / mês |
| **Custo Meta API** | **R$ 0,00** (coberto pelas 1.000 grátis) | **R$ 0,00** (coberto pelas 1.000 grátis) |
| **Custo IA (OpenAI / Ollama)** | ~R$ 3,60 / mês | **R$ 0,00** (custo de API terceirizada) |
| **Custo de Hospedagem / Infra** | ~R$ 1,40 / mês | ~R$ 5,00 - R$ 10,00 / mês (servidor GPU/VPS) |
| **Custo Total por Cliente** | **~R$ 5,00 / mês** | **~R$ 5,00 - R$ 10,00 / mês** |
| **Margem Bruta** | **> 93% (~R$ 74,90)** | **> 87% (~R$ 69,90 - R$ 74,90)** |

---

## 4. Diretrizes Principais de Produto e Mitigação de Riscos

* **Mitigação do Risco R04 (Resistência do Cliente):**
  * Onboarding ultra-rápido (menos de 5 minutos).
  * Painel de transparência para visualizar histórico de mensagens do bot.
  * Resumos diários de agendamentos para reforçar o valor gerado.
* **Foco Inicial (MVP):**
  * Agendamento passivo em resposta às chamadas do cliente.
  * Sem disparos de lembretes automáticos ativos na fase 1 (mantendo o uso do WhatsApp 100% dentro da faixa gratuita de *Service*).

---

*Documento mantido para referência do projeto OrionFlow.*
