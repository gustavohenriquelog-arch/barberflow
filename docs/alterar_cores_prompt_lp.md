# PROMPT: Atualização de Paleta — OLYON (Landing Page, Login, Cadastro)

Atue como Engenheiro Front-end. Faça uma mudança de **cores apenas** — não é redesign. Aplique de forma global e consistente em Landing Page, `/login` e `/register`.

## REGRA DE OURO
NÃO alterar: layout, estrutura, textos, funcionalidades, componentes, fluxos, tipografia, espaçamento ou responsividade — exceto ajuste mínimo de contraste quando a nova cor exigir. NÃO manter nenhum roxo/violeta/magenta/pink no projeto — remova todas as ocorrências, incluindo gradientes.

## PALETA OFICIAL (substitui o roxo/azul-ciano anterior)

| Nome | Hex | Uso |
|---|---|---|
| Azul Elétrico | `#0050F8` | Primário: CTAs, botões, links importantes, estados ativos |
| Azul Intermediário | `#0088F8` | Hover, secundário, gradientes |
| Azul Claro | `#00D0F0` | Destaques, ícones, bordas, accents tecnológicos |
| Ciano | `#00E8F0` | Destaques de alta intensidade, glow, indicadores |
| Ciano Brilhante | `#00F0EC` | Fim de gradientes, efeitos luminosos |
| Fundo Escuro | `#000820` | Footer, texto principal, componentes dark |

**Gradiente oficial** (usar com moderação — títulos-destaque, CTAs, badges, não em excesso):
```css
linear-gradient(135deg, #0050F8 0%, #0088F8 45%, #00D0F0 75%, #00F0EC 100%)
```

## LANDING PAGE — Light Mode mantido
- Fundos: `#FFFFFF` (principal) / `#F8FAFC` / `#F3F4F6` (alternância de seções)
- Texto principal: `#000820` · Texto secundário: `#334155` ou `#475569`
- Botão primário: fundo `#0050F8`, hover `#0088F8`, texto branco (gradiente oficial permitido nos CTAs principais)
- Links: `#0050F8`, hover `#0088F8`
- Títulos: cor `#000820`; palavras-chave de destaque usam o gradiente oficial
- Badges: fundo `rgba(0,80,248,0.08)`, borda `#0088F8`, texto `#0050F8`
- Ícones de destaque: `#0050F8`/`#0088F8`; ícones tecnológicos: `#00D0F0`/`#00E8F0`
- Cards: fundo `#FFFFFF`, borda `#E2E8F0`, hover border `#0088F8`
- Glow/sombra (quando já existir): `rgba(0,80,248,0.20)` ou `rgba(0,208,240,0.20)` — nunca roxo
- Header/navbar: manter o logo; links `#000820`, hover `#0050F8`; CTA `#0050F8`→hover `#0088F8`
- Footer: fundo `#000820`, texto `#FFFFFF`, texto secundário `#CBD5E1`, links `#00D0F0`→hover `#00F0EC`

Aplicar em TODAS as seções existentes (Hero, comparativo, funcionalidades, conexão WhatsApp, preço, FAQ, CTA final, footer) — verificação global ao final para garantir zero resquício de roxo.

## `/register` E `/login`
Mesma identidade visual da Landing Page, sem exceção — usuário deve perceber que é o mesmo produto em todas as telas. Primário `#0050F8`, hover `#0088F8`, accent `#00D0F0`. Manter layout, campos e textos atuais de cada tela — só a cor muda.

## TOKENS (usar em vez de cor solta no código, quando possível)
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
  --gradient-primary: linear-gradient(135deg, #0050F8 0%, #0088F8 45%, #00D0F0 75%, #00F0EC 100%);
}
```

## RESULTADO ESPERADO
O produto deve parecer uma evolução natural do design atual — mesma estrutura, mesma sensação premium/tecnológica, só que na identidade oficial azul/ciano do logo, sem nenhum roxo remanescente.

