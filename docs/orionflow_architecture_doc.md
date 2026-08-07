Documento de Arquitetura e Visão de Negócio — OrionFlow

Nota de Nomenclatura: Projeto anteriormente denominado OraZap, renomeado provisoriamente para OrionFlow (sujeito a alterações futuras).


1. Resumo Executivo e Proposta de Valor
O OrionFlow é uma solução de software como serviço (SaaS) focada na automação inteligente de agendamentos via WhatsApp para profissionais solo e pequenas empresas (ex: barbearias).
O sistema resolve a dor do empreendedor que perde receita por não conseguir responder clientes enquanto atende, entregando uma secretária virtual baseada em Inteligência Artificial com onboarding simples (< 5 minutos) e experiência sem complexidade.

2. Visão de Arquitetura Técnica
[ Cliente no WhatsApp ]
        │
        ▼
[ API Oficial da Meta (Cloud API) ]
        │  (1.000 conversas gratuitas/mês por WABA)
        ▼
[ Orquestrador n8n + LLM (OpenAI/Ollama) ]
        │
        ├── (Protocolo MCP / API REST)
        ▼
[ Plataforma Web OrionFlow ]
        │  (Gestão de Agenda, Clientes e Dashboard)
        ▼
[ Banco de Dados ]

Componentes Principais


Mensageria — API Oficial da Meta (Cloud API):

Estabilidade total sem risco de banimento de chips.
Utilização da franquia de 1.000 conversas de atendimento (Service) gratuitas/mês por conta do WhatsApp Business (WABA).



Orquestração e Inteligência — n8n + LLM:

n8n: Gerencia gatilhos de entrada, janelas de 24 horas e parsing de mensagens.
LLM (gpt-4.1-mini/Ollama): Entende intenções em linguagem natural, trata exceções e extrai datas e horários.



Integração de Dados — Protocolo MCP (Model Context Protocol):

Interface padronizada e segura entre a IA/n8n e o backend do OrionFlow.
Ferramentas expostas: consulta de disponibilidade (get_slots), criação de agendamento (create_booking), cancelamento (cancel_booking) e reagendamento (reschedule_booking).



Aplicação Web — Plataforma OrionFlow:

Painel de controle do barbeiro para acompanhamento da agenda em tempo real.
Histórico de conversas e transparência total de atendimento para garantir a segurança e controle do cliente.




3. Unidade Econômica (Unit Economics)

MétricaValor EstimadoTicket Médio MensalR$ 79,90 / mêsVolume de Agendamentos (Barbeiro Solo)~300 agendamentos / mêsCusto Meta APIR$ 0,00 (coberto pelas 1.000 conversas grátis)Custo IA (OpenAI gpt-4.1-mini)~R$ 3,60 / mêsCusto de Hospedagem / Infra~R$ 1,40 / mêsCusto Total por Cliente~R$ 5,00 / mêsMargem Bruta> 93% (~R$ 74,90 por cliente)


4. Diretrizes Principais de Produto e Mitigação de Riscos

Mitigação do Risco R04 (Resistência do Cliente):

Onboarding ultra-rápido (menos de 5 minutos).
Painel de transparência para visualizar histórico de mensagens do bot.
Resumos diários de agendamentos para reforçar o valor gerado.


Foco Inicial (MVP):

Agendamento passivo em resposta às chamadas do cliente.
Sem disparos de lembretes automáticos ativos na fase 1 (mantendo o uso do WhatsApp 100% dentro da faixa gratuita de Service).




Documento mantido para referência do projeto OrionFlow.
