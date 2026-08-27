# PADRONIZAÇÃO VISUAL — PALETA OLYON / ORIONFLOW

Quero atualizar exclusivamente a identidade de cores da aplicação para deixá-la visualmente consistente com a identidade visual atual do produto.

IMPORTANTE: NÃO altere layout, estrutura, componentes, textos, funcionalidades, navegação, espaçamentos, tipografia, tamanhos, responsividade ou comportamento da aplicação.

Apenas substitua e padronize as CORES em todas as páginas existentes.

## PÁGINAS QUE DEVEM SER ATUALIZADAS

A nova identidade visual deve ser aplicada de forma consistente em:

1. Página Principal / Landing Page
2. Página Criar Conta
3. Página Login

Todas devem parecer parte do mesmo produto e utilizar exatamente a mesma linguagem visual.

---

# NOVA PALETA DE CORES

## Cores principais

### Roxo Neon

HEX: #A822FF

Uso:

* Palavras de destaque
* Títulos estratégicos
* Ícones de destaque
* Badges
* Elementos de identidade visual
* Estados ativos
* Pequenos detalhes de destaque

### Azul

HEX: #007BFF

Uso:

* CTAs
* Links
* Elementos interativos
* Botões secundários
* Estados ativos

### Ciano Neon

HEX: #00C8FF

Uso:

* Destaques tecnológicos
* Gradientes
* Hover de elementos azuis
* Detalhes visuais
* Elementos de apoio

---

# GRADIENTE PRINCIPAL DA MARCA

Utilizar como gradiente principal:

linear-gradient(135deg, #A822FF 0%, #007BFF 100%)

Quando fizer sentido adicionar uma transição mais tecnológica entre azul e ciano, utilizar:

linear-gradient(135deg, #A822FF 0%, #007BFF 65%, #00C8FF 100%)

Não utilizar gradientes aleatórios.

A identidade visual deve transmitir:

* tecnologia
* inteligência artificial
* automação
* confiança
* modernidade
* simplicidade

---

# CORES DE FUNDO

### Fundo principal

#FFFFFF

### Fundo secundário

#F8F9FA

### Fundo de seções alternativas

#F3F4F6

Manter o estilo Light Mode.

Não transformar a aplicação em Dark Mode.

---

# TIPOGRAFIA

### Texto principal

#0D0E12

Alternativamente, quando necessário:
#111827

### Texto secundário

#4B5563

### Texto terciário / informações auxiliares

Utilizar uma variação neutra de cinza com contraste adequado.

Preservar completamente a tipografia atualmente utilizada.

NÃO trocar fonte, peso ou tamanho sem necessidade.

---

# BOTÕES E CTAs

Os botões principais devem utilizar a identidade visual da marca.

### CTA principal

Usar:

background:
linear-gradient(135deg, #A822FF 0%, #007BFF 100%)

Texto:
#FFFFFF

O botão deve ter alto contraste e aparência moderna.

### Hover

Criar uma variação visual sutil utilizando a mesma paleta.

Não utilizar verde, vermelho, laranja ou outras cores fora da identidade.

### Botões secundários

Utilizar:

* fundo branco ou transparente
* borda #A822FF ou #007BFF
* texto #A822FF ou #007BFF

Preservar o estilo atual dos componentes.

---

# LINKS

Links devem utilizar principalmente:

#007BFF

Em estados de destaque, pode utilizar:

#A822FF

Hover pode utilizar o gradiente da marca quando visualmente apropriado.

---

# BADGES / SELOS / TAGS

Utilizar a identidade roxo + azul.

Exemplo:

background:
rgba(168, 34, 255, 0.06)

border:
rgba(168, 34, 255, 0.25)

text:
#A822FF

Evitar cores muito saturadas no fundo.

---

# CARDS

Manter os cards atuais exatamente como estão estruturalmente.

Apenas adaptar:

* bordas
* ícones
* pequenos detalhes
* estados hover
* elementos de destaque

para a nova paleta.

Preferência:

background: #FFFFFF

border: #E5E7EB

Hover:
borda ou detalhe utilizando #A822FF / #007BFF.

---

# ÍCONES

Padronizar os ícones utilizando:

* #A822FF para destaque
* #007BFF para ações
* #00C8FF para detalhes tecnológicos
* #4B5563 para elementos neutros

Não utilizar cores aleatórias entre componentes.

---

# FORMULÁRIOS — CRIAR CONTA E LOGIN

Aplicar exatamente a mesma identidade visual da Landing Page.

### Inputs

Estado normal:

* fundo branco
* borda neutra
* texto #0D0E12
* placeholder #4B5563

Estado focus:
utilizar #007BFF ou #A822FF

Exemplo:

border-color: #007BFF

ou uma borda/efeito sutil utilizando o gradiente da marca.

### Botão de autenticação

Utilizar o mesmo estilo do CTA principal:

linear-gradient(135deg, #A822FF 0%, #007BFF 100%)

Texto branco.

### Links de autenticação

Utilizar #007BFF.

Estados de destaque podem utilizar #A822FF.

---

# CONSISTÊNCIA ENTRE AS PÁGINAS

Este é um requisito importante.

A Landing Page, Criar Conta e Login devem utilizar:

* mesma paleta
* mesmo gradiente
* mesma linguagem de botões
* mesma linguagem de bordas
* mesma linguagem de estados hover/focus
* mesma linguagem de ícones
* mesma hierarquia visual

O usuário deve sentir que está navegando dentro de um único produto.

Não criar uma paleta diferente para Login ou Criar Conta.

---

# REGRAS IMPORTANTES

1. Não alterar funcionalidades.
2. Não alterar lógica de negócio.
3. Não alterar rotas.
4. Não alterar textos.
5. Não alterar componentes existentes.
6. Não alterar estrutura HTML/React sem necessidade.
7. Não alterar espaçamentos.
8. Não alterar tamanhos.
9. Não alterar fontes.
10. Não alterar responsividade.
11. Não criar novos componentes apenas para modificar cores.
12. Não remover elementos existentes.
13. Não adicionar novas seções.
14. Não modificar o conteúdo da Landing Page.
15. Não utilizar verde como cor principal.
16. Não utilizar a antiga identidade visual em nenhuma das três páginas.
17. Evitar cores fora da paleta, exceto cores neutras necessárias para acessibilidade e feedback de sistema.
18. Manter aparência clean, premium, tecnológica e SaaS.
19. Garantir contraste adequado entre texto e fundo.
20. Centralizar a definição das cores em variáveis/tokens CSS quando a arquitetura atual permitir.

---

# TOKENS DE DESIGN

Se o projeto utilizar CSS Variables, Tailwind tokens ou outro sistema de design, criar/atualizar os tokens para evitar cores duplicadas e inconsistentes.

Utilizar conceitos equivalentes a:

--color-primary: #A822FF;
--color-secondary: #007BFF;
--color-accent: #00C8FF;
--color-background: #FFFFFF;
--color-background-secondary: #F8F9FA;
--color-background-tertiary: #F3F4F6;
--color-text-primary: #0D0E12;
--color-text-secondary: #4B5563;
--color-border: #E5E7EB;

--gradient-primary: linear-gradient(135deg, #A822FF 0%, #007BFF 100%);

Se o projeto utilizar Tailwind, adapte esses tokens ao sistema existente em vez de criar um sistema paralelo.

---

# RESULTADO ESPERADO

Quero que o resultado final tenha a aparência de um único produto SaaS moderno.

A identidade visual deve ser imediatamente reconhecível pela combinação:

ROXO NEON → AZUL → CIANO

com fundos claros, textos grafite e bastante espaço visual.

A Landing Page deve continuar exatamente com o mesmo design atual, porém utilizando a nova identidade de cores.

As páginas Criar Conta e Login devem seguir a mesma identidade visual da Landing Page.

Faça uma revisão final em TODAS as três páginas para garantir que não exista nenhuma cor antiga ou componente visual destoante.

IMPORTANTE:

Antes de modificar, analise os componentes e estilos existentes do projeto.

Faça a alteração de forma centralizada sempre que possível.

Não faça redesign.

É uma tarefa de BRANDING / COLOR SYSTEM, não de UI REDESIGN.
