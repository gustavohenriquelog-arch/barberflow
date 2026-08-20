# PROMPT: Navegação + Telas de Login e Cadastro — OrionFlow (paleta unificada)

Atue como um Engenheiro Front-end especialista em React/Tailwind, responsável por implementar a navegação entre páginas e ajustar as telas de Login (`/login`) e Cadastro (`/register`) do OrionFlow, garantindo que **toda a identidade visual do projeto — Landing Page, Login e Cadastro — use a mesma paleta de cores**, sem exceções.

## CORREÇÃO IMPORTANTE DE IDENTIDADE VISUAL

Não existem duas paletas separadas no projeto. Landing Page, `/login` e `/register` usam a **mesma identidade**:

- Roxo Neon: `#A822FF`
- Gradiente Azul/Ciano: `#007BFF → #00C8FF`
- Gradiente primário: `linear-gradient(135deg, #A822FF 0%, #007BFF 100%)`

**O painel esquerdo (logo + recursos) de `/login` e `/register` deve trocar o verde escuro por esse gradiente roxo→azul.** Os botões principais ("Acessar", "Criar conta") também devem abandonar o verde `#22c55e` e usar o gradiente primário do projeto, para consistência com os CTAs da Landing Page.

### Cuidado de contraste (ajuste técnico necessário)
O gradiente `#A822FF → #007BFF` é vibrante e pode reduzir a legibilidade de texto branco em algumas áreas, especialmente perto do ciano. Para o painel esquerdo (fundo grande, com bastante texto):
- Use uma versão mais escura/saturada do gradiente (ex: escurecer os tons em ~15-20%), ou
- Aplique um overlay escuro sutil (`rgba(0,0,0,0.35)`) sobre o gradiente para garantir contraste AA com texto branco.
- Teste os cards translúcidos de recursos sobre esse fundo — eles precisam continuar legíveis (fundo `rgba(255,255,255,0.1)` com borda sutil costuma funcionar bem sobre gradiente escuro).

### Tabela de substituição de cores (referência rápida)

| Elemento | Antes (referência) | Depois (padrão OrionFlow) |
|---|---|---|
| Painel esquerdo (fundo) | Verde escuro sólido/gradiente | Gradiente `#A822FF → #007BFF` (versão escurecida ou com overlay) |
| Botão "Acessar" (login) | Verde `#22c55e` | Gradiente primário do projeto |
| Botão "Criar conta" (cadastro) | Verde `#22c55e` | Gradiente primário do projeto |
| Link "Esqueceu a senha?" | Verde | Roxo `#A822FF` ou azul `#007BFF` |
| Link "Registre-se" / "Faça login" | Verde | Roxo `#A822FF` ou azul `#007BFF` |

## MAPA DE ROTAS E NAVEGAÇÃO

| Origem | Elemento | Destino |
|---|---|---|
| Cabeçalho (Landing Page) | Botão "Teste grátis" | `/register` |
| Cabeçalho (Landing Page) | Link "Entrar" | `/login` |
| `/register` | Link "Faça login" | `/login` |
| `/login` | Link "Registre-se" | `/register` |
| `/login` e `/register` | Botão "Voltar ao site" | `/` (Landing Page) |
| `/login` | Link "Esqueceu a senha?" | `/forgot-password` (stub — sem especificação ainda) |
| `/login` | Botão "Acesso para Atendentes" | rota separada para login de equipe (confirmar se reaproveita `/login` com contexto ou é tela própria) |

Rotas via React Router (ou equivalente já usado no projeto), navegação client-side, sem reload de página.

## ROTA `/login` — ESTRUTURA DE 2 COLUNAS

### Lado esquerdo (painel com gradiente do projeto — ver correção acima)
- Logo do OrionFlow.
- Título: "Automatize seu atendimento".
- Subtítulo curto reforçando a proposta (ex: "A plataforma completa para gestão de agendamentos e atendimento automatizado via WhatsApp").
- 4 cards translúcidos de recursos — **reaproveitar exatamente os mesmos 4 já usados em `/register`**, para manter consistência entre as telas.
- Em mobile (`<768px`): colapsar para uma faixa superior compacta com logo, priorizando o formulário.

### Lado direito — Card "Bem-vindo de volta!"
- Título centralizado: "Bem-vindo de volta!".
- Campo E-mail: rótulo "E-mail", placeholder `seu@email.com`, validação de formato, erro inline se inválido.
- Campo Senha: rótulo "Senha", tipo password, ícone de olho (com `aria-label` alternando "Mostrar senha" / "Ocultar senha").
- Checkbox "Manter logado" à esquerda + link "Esqueceu a senha?" à direita (cor conforme tabela acima).
- Botão principal "Acessar" com ícone de login, gradiente primário do projeto, estado de loading ("Entrando...") e disabled se campos vazios/inválidos.
- Erro de login: mensagem genérica acima do formulário (ex: "E-mail ou senha incorretos"), sem indicar qual campo está errado.
- Divisor sutil "ou".
- Botão secundário "Acesso para Atendentes" (fundo claro, borda fina, ícone de usuário).
- Rodapé: "Não tem uma conta? Registre-se" (link para `/register`, cor conforme tabela).
- Enter no teclado submete o formulário.

## ROTA `/register` — AJUSTE DE PALETA (estrutura já existente, só cor muda)

Mantenha a estrutura atual (painel esquerdo com 4 cards, título "Crie sua conta", campos Primeiro Nome/Último Nome, Telefone com seletor de país, Nome do estabelecimento, E-mail, Senha com mínimo de 8 caracteres, botão "Criar conta", link "Já tem uma conta? Faça login") — só substitua as cores conforme a tabela acima. Não altere textos, campos ou ordem.

## REQUISITOS TÉCNICOS GERAIS

- Mobile-first: testar em 375px antes de expandir.
- Reaproveitar componentes idênticos entre `/login` e `/register` (painel esquerdo, botão, inputs) — não duplicar código.
- Tipografia consistente com o projeto (Inter ou Plus Jakarta Sans).
- `<title>` e meta `noindex` em ambas as rotas de autenticação.
- `focus-visible` em todos os campos e botões interativos.
- Apenas UI — sem lógica de autenticação real; estados de loading/erro/sucesso com dados mockados.

## PENDÊNCIAS A CONFIRMAR

1. "Acesso para Atendentes": tela separada com campos diferentes, ou `/login` com toggle de contexto?
2. `/forgot-password`: já tem especificação ou é só stub por enquanto?
3. Rota de destino após login bem-sucedido (ex: `/dashboard`)?
