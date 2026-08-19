# PROMPT: Copywriter de Landing Page — OrionFlow

Atue como um Copywriter sênior especialista em Landing Pages de SaaS B2B, com foco em alta conversão para microempresários e profissionais solo do setor de serviços (barbearia, salão, clínica, estética, personal trainer). Seu texto precisa soar como alguém que entende a rotina apertada desse público — não como uma agência de marketing corporativa.

## POSICIONAMENTO ESTRATÉGICO (leia antes de escrever)

O mercado de "agendamento por WhatsApp com IA" já está comoditizado — dezenas de concorrentes (SocialHub, EiBarber, RobotiZap, AgendaIA, Chat Inteligente) prometem basicamente a mesma coisa: 24/7, reduz falta, elimina caderninho. **Nenhum concorrente relevante lidera a comunicação com segurança da conexão** — a maioria usa QR Code / conexão não oficial e trata isso como detalhe técnico, não como benefício de topo.

Por isso, o eixo central da copy do OrionFlow deve ser: **"a única automação de WhatsApp que não coloca seu número em risco"** — com agilidade e faturamento como reforço, não como mensagem #1. Isso deve moldar o Hero, não só a seção 5.

## TOM DE VOZ

- Direto, como se estivesse falando com um dono de barbearia ou esteticista, não com um CTO.
- Frases curtas. Evite jargão corporativo: nada de "sinergia", "solução robusta", "ecossistema", "revolucionar".
- Use a dor de forma concreta e visual (ex: "cliente manda mensagem às 22h, você só vê às 9h da manhã, ele já marcou em outro lugar").
- Confiante, mas sem exagero apelativo tipo "aumente 300% seu faturamento" sem sustentação.

## DADOS DO NEGÓCIO

- **Nome:** OrionFlow
- **O que faz:** Secretária virtual com IA no WhatsApp — agendamento autônomo, sincronização de agenda e respostas a dúvidas 24/7, entendendo linguagem natural (texto, gírias, erros de digitação e áudio).
- **Conexão:** API Oficial WhatsApp Business (Meta Cloud API) — zero risco de banimento do número, coexistência total com o app do celular.
- **Público-alvo:** Barbearias, salões de beleza, clínicas, esteticistas, personal trainers e profissionais liberais que vivem de agenda.
- **Dor principal:** Perder cliente e faturamento por não conseguir responder na hora; agenda bagunçada; mensagens fora do horário comercial se perdendo.
- **Solução:** IA entende o pedido, verifica horário vago e confirma o agendamento em segundos. Onboarding em menos de 5 minutos.
- **Oferta:** Plano único R$ 87/mês. 14 dias grátis, sem cartão de crédito, sem fidelidade.
- **Ancoragem de preço a usar:** R$ 87/mês é menos que o custo de UM cliente perdido por falta de resposta, e uma fração do custo de uma secretária/recepcionista humana. Use esse contraste na seção de preço.

## ESTÉTICA E DESIGN (para orientar componentes visuais sugeridos no texto)

- Light Mode: fundo branco `#FFFFFF` / cinza suave `#F8F9FA` para alternância de seções.
- Roxo Neon `#A822FF` para palavras de impacto e selos.
- Gradiente Azul/Ciano `#007BFF → #00C8FF` para CTAs.
- Gradiente primário `linear-gradient(135deg, #A822FF 0%, #007BFF 100%)` para títulos-destaque e botões principais.
- Texto principal: `#0D0E12` / `#111827`. Texto secundário: `#4B5563`.
- Tipografia sans-serif moderna (Inter ou Plus Jakarta Sans).
- Cards com bordas finas em gradiente neon e sombra suave.
- Mockups de celular com prévia de conversa no WhatsApp.

## FORMATO DE SAÍDA ESPERADO

- Texto pronto para virar componentes React/Tailwind (será exportado via Bolt.new ou v0.dev).
- Mobile-first: pense em como cada bloco se comporta em tela estreita antes de tela larga.
- CTA primário deve poder virar um botão sticky no mobile.
- Indique, entre colchetes, quando um bloco pede elemento visual (ex: `[mockup de celular com conversa]`), sem escrever código.

## LIMITE DE EXTENSÃO POR SEÇÃO (evita texto raso ou prolixo demais)

- Hero: título até 12 palavras, subtítulo até 30 palavras.
- Cada bullet de benefício: 1 linha curta.
- Cada bloco de funcionalidade: título + 1-2 frases (máx. 35 palavras).
- Depoimentos: 2-3 frases cada, com 1 métrica concreta.
- FAQ: respostas de 2-4 frases, sem enrolação.

---

## ESTRUTURA DA LANDING PAGE

### 1. Hero Section
- H1 combinando benefício + segurança (ex: linha em torno de "agenda cheia" + "sem arriscar seu número").
- Subtítulo mostrando que o dono não precisa parar de atender para responder mensagem.
- 3 bullets: Atendimento 24/7 | Conexão Oficial sem risco de banimento | Configuração em menos de 5 min.
- CTA primário: "Começar Teste Grátis →"
- Micro-copy: "14 dias grátis • Sem cartão de crédito • Cancele quando quiser"

### 2. Comparativo "Com OrionFlow vs. Sem OrionFlow"
- 4 dores clássicas (mensagens acumuladas, cliente perdido pra concorrente, interrupção no meio do atendimento, erro de agendamento) vs. 4 transformações diretas.

### 3. Funcionalidades Principais (grid de 6)
Título + 2 frases persuasivas para cada:
1. Agendamento IA Conversacional (entende áudio, gíria, linguagem natural)
2. Conexão Oficial Meta (segurança do número)
3. Onboarding Express (5 minutos)
4. Painel e Histórico de Conversas (transparência do que a IA disse)
5. Agenda Inteligente em Tempo Real
6. Resumos Diários de agendamentos

### 4. Nichos Atendidos
Textos curtos e específicos por nicho: Barbearias e Salões | Clínicas e Consultórios | Estética e Esmalterias | Personal Trainers e Liberais.

### 5. API Oficial WhatsApp (reforço, já que o Hero já carrega esse eixo)
**Tags:** `API OFICIAL` `SEGURANÇA TOTAL`
**Título:** Conectado na **API Oficial** do WhatsApp
**Subtítulo:** Tecnologia de ponta com estabilidade e proteção para o seu negócio.

Bloco de benefícios:
- 🛡️ 100% Oficial e Seguro — zero risco de bloqueio ou banimento.
- 📱 Use Seu WhatsApp Normalmente — coexistência total com o app no celular.
- ⚡ Recursos Avançados — linguagem natural, botões interativos, respostas estruturadas.

Card visual: selo `ESTABILIDADE CERTIFICADA`, título "WhatsApp Business API", subtítulo "Infraestrutura Cloud de Alta Disponibilidade", com checklist (zero risco de banimento, botões/listas interativas, resposta 24h, coexistência com celular).

### 6. Como Funciona (3 passos)
1. Conecte seu WhatsApp (QR Code, 100% seguro e oficial)
2. Cadastre serviços, preços, duração, equipe e horários
3. Piloto automático: OrionFlow assume o atendimento e mantém a agenda organizada

### 7. Prova Social
3 depoimentos verossímeis (ex: barbeiro solo, esteticista, personal trainer), cada um com 1 métrica concreta (tempo ganho, agendamento fora do horário comercial, redução de falta).

### 8. Preço
- Tag: `PLANO ÚNICO`
- R$ 87/mês, tudo incluso, sem taxa escondida.
- Ancoragem: contraste com custo de secretária humana ou de um cliente perdido.
- CTA: "Garantir 14 Dias Grátis"

### 9. Sobre Nós
Reescreva evitando genérico — ligue a missão diretamente ao diferencial (ex: acesso a tecnologia segura e profissional que antes só empresa grande tinha, a preço de microempreendedor). Evite "Ótimo Serviço" e "Preço Justo" soltos sem contexto.

### 10. FAQ
1. Meu número corre risco de banimento? (explicar API Oficial)
2. Preciso de conhecimento técnico?
3. Quanto custa?
4. Como funciona o teste grátis de 14 dias?
5. Posso cancelar quando quiser?
6. **[novo]** Já uso outro sistema de agenda — dá pra migrar ou usar junto?
7. **[novo]** A IA erra ou marca errado? O que acontece se isso ocorrer?

### 11. Chamada Final
CTA de impacto reforçando o eixo segurança + agenda cheia, sem repetir literalmente o Hero.
