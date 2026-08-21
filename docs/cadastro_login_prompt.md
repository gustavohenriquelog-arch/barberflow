# PROMPT: Navegação + Telas de Login e Cadastro — OrionFlow (versão final)

Atue como um Engenheiro Front-end especialista em React/Tailwind, responsável por **criar do zero** as telas de Login (`/login`) e Cadastro (`/register`) do OrionFlow, além da navegação entre elas e a Landing Page, garantindo que **toda a identidade visual do projeto — Landing Page, Login e Cadastro — use a mesma paleta de cores**, sem exceções.

## IDENTIDADE VISUAL (única, para todo o projeto)

- Roxo Neon: `#A822FF`
- Gradiente Azul/Ciano: `#007BFF → #00C8FF`
- Gradiente primário: `linear-gradient(135deg, #A822FF 0%, #007BFF 100%)`

O painel esquerdo (logo + recursos) de `/login` e `/register` usa esse gradiente roxo→azul. Os botões principais ("Acessar", "Criar conta") também usam o gradiente primário do projeto — nada de verde.

### Cuidado de contraste
O gradiente é vibrante e pode reduzir a legibilidade de texto branco perto do ciano. No painel esquerdo:
- Escureça o gradiente em ~15-20%, ou
- Aplique overlay escuro sutil (`rgba(0,0,0,0.35)`) sobre o gradiente.
- Cards translúcidos de recursos: fundo `rgba(255,255,255,0.1)` com borda sutil funciona bem sobre esse fundo escurecido.

### Tabela de substituição de cores

| Elemento | Cor final |
|---|---|
| Painel esquerdo (fundo) | Gradiente `#A822FF → #007BFF` (escurecido ou com overlay) |
| Botão "Acessar" (login) | Gradiente primário do projeto |
| Botão "Criar conta" (cadastro) | Gradiente primário do projeto |
| Link "Esqueceu a senha?" | Roxo `#A822FF` ou azul `#007BFF` |
| Link "Registre-se" / "Faça login" | Roxo `#A822FF` ou azul `#007BFF` |

## MAPA DE ROTAS E NAVEGAÇÃO

| Origem | Elemento | Destino |
|---|---|---|
| Cabeçalho (Landing Page) | Botão "Teste grátis" | `/register` |
| Cabeçalho (Landing Page) | Link "Entrar" | `/login` |
| **Landing Page (todos os CTAs)** | **Todo botão de teste grátis em qualquer seção da página** — Hero ("Começar Teste Grátis"), Comparativo, Preço, Chamada Final, e qualquer outro com texto equivalente ("Começar Teste Grátis", "Garantir X Dias Grátis", etc.) | `/register` |
| `/register` | Link "Faça login" | `/login` |
| `/login` | Link "Registre-se" | `/register` |
| `/login` e `/register` | Botão "Voltar ao site" | `/` (Landing Page) |
| `/login` | Link "Esqueceu a senha?" | `/forgot-password` (**stub** — rota existe, sem lógica ainda; ver seção abaixo) |
| `/login` | Toggle "Acesso para Atendentes" | mesmo formulário de `/login`, ver seção abaixo |
| Login bem-sucedido | — | `/dashboard` |

Rotas via React Router (ou equivalente já usado no projeto), navegação client-side, sem reload de página.

**Importante:** varra TODA a Landing Page e identifique todo botão cujo texto seja de teste grátis (ex: "Começar Teste Grátis", "Garantir 14 Dias Grátis") — são pelo menos 5 ocorrências (Hero, Comparativo "Com vs Sem", Preço, Chamada Final, e o botão do Cabeçalho). Todos devem apontar para `/register`, sem exceção. Não assuma que só o botão do cabeçalho precisa de link.

## ROTA `/login` — ESTRUTURA DE 2 COLUNAS

### Lado esquerdo (painel com gradiente do projeto)
- Logo do OrionFlow.
- Título: "Automatize seu atendimento".
- Subtítulo curto (ex: "A plataforma completa para gestão de agendamentos e atendimento automatizado via WhatsApp").
- 4 cards translúcidos de recursos — **reaproveitar exatamente os mesmos 4 já usados em `/register`**.
- Mobile (`<768px`): colapsar para faixa superior compacta com logo, priorizando o formulário.

### Lado direito — Card de login

**Toggle "Dono do negócio" / "Atendente" no topo do card**, acima do título — alterna o contexto do mesmo formulário (não é tela separada, não muda os campos, só o contexto de permissão enviado no submit).

- Título centralizado: "Bem-vindo de volta!".
- Campo E-mail: rótulo "E-mail", placeholder `seu@email.com`, validação de formato, erro inline se inválido.
- Campo Senha: rótulo "Senha", tipo password, ícone de olho (`aria-label` alternando "Mostrar senha" / "Ocultar senha").
- Checkbox "Manter logado" à esquerda + link "Esqueceu a senha?" à direita.
- Botão principal "Acessar" com ícone de login, gradiente primário, estado de loading ("Entrando...") e disabled se campos vazios/inválidos.
- Erro de login: mensagem genérica acima do formulário ("E-mail ou senha incorretos"), sem indicar qual campo está errado.
- Divisor sutil "ou" — **remover o botão "Acesso para Atendentes" como bloco separado**, já que virou o toggle no topo do card.
- Rodapé: "Não tem uma conta? Registre-se" (link para `/register`).
- Enter no teclado submete o formulário.
- Ao logar com sucesso: redirecionar para `/dashboard`.

## ROTA `/forgot-password` (stub)

Criar a rota e o link funcional, mas sem lógica de envio real:
- Mesma estrutura de 2 colunas (painel esquerdo igual ao de `/login`).
- Card com título "Redefinir senha", campo de e-mail, botão "Enviar instruções" (desabilitado ou com toast "Funcionalidade em breve" ao clicar — não implementar envio real).
- Link "Voltar ao login" no rodapé do card.

## ROTA `/register` — ESTRUTURA DE 2 COLUNAS (criar do zero)

### Lado esquerdo
Mesmo painel de `/login` (logo, título, subtítulo, 4 cards translúcidos) — componente compartilhado entre as duas telas.

### Lado direito — Card "Crie sua conta"
- Título centralizado: "Crie sua conta".
- Campos Primeiro Nome e Último Nome (lado a lado em telas largas, empilhados no mobile), ambos obrigatórios.
- Campo Telefone com seletor de país (padrão `+55`), obrigatório.
- Campo Nome do estabelecimento, obrigatório, com texto de apoio "O nome do seu negócio, como seus clientes o conhecem."
- Campo E-mail, obrigatório, com texto de apoio "Este será o seu e-mail de acesso ao sistema."
- Campo Senha, tipo password com ícone de olho, obrigatório, mínimo de 8 caracteres, com texto de apoio indicando o requisito e validação inline.
- Botão "Criar conta" com ícone, gradiente primário do projeto, estado de loading e disabled se campos obrigatórios vazios/inválidos.
- Rodapé: "Já tem uma conta? Faça login" (link para `/login`, cor conforme tabela).
- Após cadastro bem-sucedido: redirecionar para `/dashboard`.

## REQUISITOS TÉCNICOS GERAIS

- Mobile-first: testar em 375px antes de expandir.
- Reaproveitar componentes idênticos entre `/login`, `/register` e `/forgot-password` (painel esquerdo, botão, inputs) — não duplicar código.
- Tipografia consistente com o projeto (Inter ou Plus Jakarta Sans).
- `<title>` e meta `noindex` em todas as rotas de autenticação.
- `focus-visible` em todos os campos e botões interativos.
- Apenas UI — sem lógica de autenticação real; estados de loading/erro/sucesso com dados mockados. `/dashboard` pode ser uma tela stub simples por enquanto (será especificada depois).
