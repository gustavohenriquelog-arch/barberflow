# ATUALIZAÇÃO DA IDENTIDADE VISUAL — ORIONFLOW

Quero atualizar a identidade visual de todo o projeto OrionFlow para que todas as páginas tenham **total conformidade visual com as cores do logo da marca**.

IMPORTANTE:

* NÃO alterar o layout existente.
* NÃO alterar a estrutura das páginas.
* NÃO alterar textos.
* NÃO alterar funcionalidades.
* NÃO alterar componentes ou fluxos.
* NÃO alterar espaçamentos, tamanhos ou responsividade, exceto quando uma alteração de cor exigir ajuste mínimo de contraste.
* NÃO criar uma nova identidade visual.
* NÃO utilizar a paleta roxa atual.
* NÃO utilizar roxo, violeta, magenta ou pink em nenhum elemento.
* A alteração solicitada é principalmente de **cores e identidade visual**.
* A mesma identidade visual deve ser aplicada de forma consistente em TODAS as páginas.

## 1. IDENTIDADE VISUAL OFICIAL

A identidade visual deve seguir exclusivamente a paleta do logo OrionFlow:

### Azul Elétrico

HEX: `#0050F8`
RGB: `0, 80, 248`

Uso:

* CTAs principais
* botões primários
* links importantes
* elementos de ação
* ícones de destaque
* estados ativos

### Azul Intermediário

HEX: `#0088F8`
RGB: `0, 136, 248`

Uso:

* elementos secundários
* gradientes
* hover states
* links secundários
* elementos interativos

### Azul Claro

HEX: `#00D0F0`
RGB: `0, 208, 240`

Uso:

* destaques
* detalhes visuais
* ícones
* bordas
* elementos tecnológicos
* efeitos sutis

### Ciano

HEX: `#00E8F0`
RGB: `0, 232, 240`

Uso:

* destaques de alta intensidade
* pequenos detalhes
* glow
* indicadores
* elementos tecnológicos

### Ciano Brilhante

HEX: `#00F0EC`
RGB: `0, 240, 236`

Uso:

* pontos de maior destaque
* final de gradientes
* efeitos luminosos
* pequenos accents

### Fundo Escuro da Identidade

HEX: `#000820`
RGB: `0, 8, 32`

Uso:

* elementos dark
* footer
* áreas de destaque
* componentes escuros
* fundos especiais quando já existirem no projeto

---

# 2. GRADIENTE OFICIAL

Substitua os gradientes atuais pela identidade visual oficial.

Gradiente principal:

```css
linear-gradient(
  135deg,
  #0050F8 0%,
  #0088F8 45%,
  #00D0F0 75%,
  #00F0EC 100%
)
```

O gradiente deve transmitir:

**Azul Elétrico → Azul Tecnológico → Ciano → Ciano Brilhante**

Utilizar o gradiente principalmente em:

* palavras de destaque dos títulos
* CTAs principais
* elementos gráficos
* ícones especiais
* badges
* pequenos efeitos visuais
* bordas ou highlights quando apropriado

Evitar aplicar o gradiente em excesso.

A identidade deve continuar sendo **clean, premium, tecnológica e profissional**.

---

# 3. FUNDO DA LANDING PAGE

A Landing Page atualmente utiliza Light Mode.

MANTER o Light Mode.

Utilizar:

### Fundo principal

`#FFFFFF`

### Fundo secundário

`#F8FAFC`

### Fundo alternativo

`#F3F4F6`

### Texto principal

`#000820`

### Texto secundário

Utilizar tons de azul/cinza neutros com excelente contraste, evitando cores excessivamente saturadas.

Priorizar:

`#334155`

ou

`#475569`

---

# 4. BOTÕES E CTAs

Todos os botões devem seguir a identidade OrionFlow.

## Botão Primário

Usar:

`#0050F8`

Hover:

`#0088F8`

Texto:

`#FFFFFF`

O botão deve ter aparência:

* moderna
* premium
* tecnológica
* limpa
* alta conversão

Pode utilizar gradiente oficial nos CTAs principais quando isso já fizer parte do design existente.

Gradiente:

`#0050F8 → #00F0EC`

Não exagerar nos efeitos.

---

# 5. LINKS

Links principais devem utilizar:

`#0050F8`

Hover:

`#0088F8`

Links de maior destaque podem utilizar o gradiente oficial, desde que mantenham excelente legibilidade.

---

# 6. TÍTULOS

Manter os títulos existentes exatamente como estão.

Não alterar:

* tamanho
* peso
* fonte
* alinhamento
* espaçamento
* hierarquia

Alterar somente a cor.

Textos principais:

`#000820`

Palavras estratégicas destacadas:

usar o gradiente oficial:

`#0050F8 → #00F0EC`

O efeito deve ser semelhante ao conceito atual de texto destacado, porém totalmente alinhado ao logo.

---

# 7. BADGES E SELos

Badges atualmente roxos devem ser convertidos para a identidade azul/ciano.

Prioridade:

* azul elétrico
* azul intermediário
* ciano
* gradiente oficial

Exemplo:

Background sutil:

`rgba(0, 80, 248, 0.08)`

Border:

`#0088F8`

Texto:

`#0050F8`

Não utilizar roxo.

---

# 8. ÍCONES

Ícones de destaque devem utilizar:

`#0050F8`

ou

`#0088F8`

Ícones tecnológicos podem utilizar:

`#00D0F0`

ou

`#00E8F0`

Manter todos os ícones visualmente consistentes.

Não alterar o conjunto de ícones existente.

---

# 9. CARDS

Preservar os cards existentes.

Não alterar:

* estrutura
* tamanho
* conteúdo
* layout
* espaçamento

Alterar somente os elementos relacionados à identidade visual.

Utilizar:

Background:

`#FFFFFF`

Border:

`#E2E8F0`

Hover border:

`#0088F8`

Destaques:

`#0050F8`

Pequenos accents:

`#00D0F0`

---

# 10. SOMBRAS E GLOW

Manter sombras discretas e profissionais.

Evitar sombras muito fortes.

Quando houver glow tecnológico, utilizar exclusivamente tons da identidade.

Exemplos:

```css
rgba(0, 80, 248, 0.20)
```

```css
rgba(0, 208, 240, 0.20)
```

```css
rgba(0, 232, 240, 0.15)
```

NUNCA utilizar glow roxo.

---

# 11. HEADER / NAVBAR

Aplicar a nova identidade visual mantendo exatamente o layout atual.

Logo:

preservar o logo existente.

Links:

`#000820`

Hover:

`#0050F8`

CTA:

`#0050F8`

Hover:

`#0088F8`

Manter aparência clean e premium.

---

# 12. FOOTER

Aplicar:

Fundo:

`#000820`

Texto principal:

`#FFFFFF`

Texto secundário:

`#CBD5E1`

Links:

`#00D0F0`

Hover:

`#00F0EC`

Elementos de destaque:

`#0050F8`

O footer deve ser visualmente conectado ao logo.

---

# 13. PÁGINA PRINCIPAL

Aplicar a identidade visual completa na página principal.

Garantir consistência em:

* Hero
* Navbar
* CTAs
* títulos
* subtítulos
* badges
* cards
* ícones
* seção de funcionalidades
* seção comparativa
* seção de conexão WhatsApp
* seção de preços
* FAQ
* CTA final
* Footer

REMOVER qualquer ocorrência de:

* roxo
* violeta
* magenta
* pink
* gradientes roxos

Substituir pelos tons oficiais do logo.

---

# 14. PÁGINA "CRIAR CONTA"

A página de criação de conta deve utilizar EXATAMENTE a mesma identidade visual da Landing Page.

Não criar uma identidade diferente.

Aplicar:

* mesmo azul primário
* mesmo azul secundário
* mesmo ciano
* mesmo gradiente
* mesmos estados de hover
* mesmos estilos de botões
* mesmos accents
* mesma linguagem visual

Botão principal:

`#0050F8`

Hover:

`#0088F8`

Elementos de destaque:

`#00D0F0`

Não utilizar roxo.

---

# 15. PÁGINA DE LOGIN

A página de Login deve seguir exatamente a mesma identidade visual.

Manter:

* layout atual
* estrutura atual
* campos atuais
* textos atuais
* funcionalidades atuais
* responsividade atual

Alterar somente a identidade visual necessária.

Utilizar:

Primary:

`#0050F8`

Secondary:

`#0088F8`

Accent:

`#00D0F0`

Cyan:

`#00E8F0`

Bright Cyan:

`#00F0EC`

Dark:

`#000820`

---

# 16. CONSISTÊNCIA ENTRE PÁGINAS

A Landing Page, Criar Conta e Login devem parecer partes do MESMO produto.

O usuário deve perceber imediatamente que está dentro do OrionFlow.

Criar uma linguagem visual consistente entre:

**Landing Page**
↓
**Criar Conta**
↓
**Login**
↓
**Sistema**

Não permitir que cada página tenha uma paleta diferente.

---

# 17. VARIÁVEIS DE CORES

Sempre que possível, centralizar as cores em variáveis/tokens de design.

Exemplo:

```css
:root {
  --color-primary: #0050F8;
  --color-primary-hover: #0088F8;

  --color-blue-light: #00D0F0;
  --color-cyan: #00E8F0;
  --color-cyan-bright: #00F0EC;

  --color-dark: #000820;

  --color-background: #FFFFFF;
  --color-background-secondary: #F8FAFC;
  --color-background-tertiary: #F3F4F6;

  --color-text-primary: #000820;
  --color-text-secondary: #475569;

  --color-border: #E2E8F0;
}
```

Gradiente:

```css
--gradient-primary: linear-gradient(
  135deg,
  #0050F8 0%,
  #0088F8 45%,
  #00D0F0 75%,
  #00F0EC 100%
);
```

Sempre que possível, utilizar esses tokens em vez de espalhar valores de cor pelo código.

---

# 18. REGRAS IMPORTANTES

### NÃO FAZER

* Não utilizar roxo.
* Não utilizar violeta.
* Não utilizar magenta.
* Não utilizar pink.
* Não criar novos gradientes roxos.
* Não modificar o layout.
* Não modificar textos.
* Não modificar funcionalidades.
* Não modificar a estrutura das páginas.
* Não alterar a identidade tipográfica.
* Não criar componentes desnecessários.

### FAZER

* Usar exclusivamente a paleta do logo.
* Manter Light Mode na Landing Page.
* Manter o design atual.
* Aplicar a identidade de forma consistente.
* Centralizar cores em tokens quando possível.
* Garantir excelente contraste.
* Manter aparência SaaS premium.
* Manter estética tecnológica.
* Utilizar azul elétrico como cor primária.
* Utilizar ciano como cor de destaque.
* Utilizar o gradiente oficial com moderação.
* Aplicar a mesma identidade na Landing Page, Criar Conta e Login.

---

# 19. RESULTADO ESPERADO

O resultado final deve parecer uma evolução natural do projeto atual, e não uma nova interface.

A única mudança visual relevante deve ser a substituição da identidade de cores atual pela identidade oficial do logo OrionFlow.

A sensação visual desejada é:

**Tecnologia + IA + Automação + Confiabilidade + Modernidade + Premium**

Paleta principal:

`#0050F8`
`#0088F8`
`#00D0F0`
`#00E8F0`
`#00F0EC`
`#000820`

Gradiente oficial:

`#0050F8 → #0088F8 → #00D0F0 → #00F0EC`

Antes de finalizar, faça uma verificação global no projeto para garantir que não existam mais referências visuais à antiga paleta roxa.

IMPORTANTE: faça a alteração de forma GLOBAL e CONSISTENTE em todas as páginas, componentes e estados visuais relevantes.

