# iGreen Club — Design System

> **Escopo:** documentação visual e tokens CSS  
> **Direção:** fiel à identidade do site original  
> **Referência:** https://igreenclub.com/  
> **Status:** especificação inicial — requer validação visual

---

## Nota de precisão

Este documento organiza uma proposta de Design System para o iGreen Club com base na estrutura e no conteúdo público identificados. O CSS computado, os arquivos de fonte e todas as telas renderizadas do site não foram inspecionados diretamente nesta análise.

Por isso, os valores de cores, tipografia, espaçamentos, raios e sombras apresentados abaixo são **estimativas de partida**, não medições certificadas do site. Antes de utilizá-los como referência oficial de marca, valide-os contra capturas de tela, estilos carregados e ativos oficiais.

A documentação considera a experiência pública do iGreen Club e elementos relacionados à proposta iGreen Energy. Áreas autenticadas do portal ou aplicativo podem conter padrões adicionais que não estão cobertos aqui.

---

## 1. Visão geral

O sistema deve comunicar:

- Sustentabilidade e responsabilidade ambiental.
- Economia e benefícios tangíveis.
- Tecnologia acessível e experiência digital simples.
- Confiança, clareza e proximidade.

A arquitetura proposta divide o sistema em cinco camadas:

1. **Foundations:** cores, tipografia, espaçamento, bordas e elevações.
2. **Components:** botões, cards, campos, badges e navegação.
3. **Patterns:** hero, benefícios, cashback, simulador, etapas e FAQ.
4. **Templates:** landing page, página de benefícios, parceiros e experiência mobile.
5. **Guidelines:** responsividade, acessibilidade e regras de aplicação.

## 2. Foundations

### 2.1 Paleta de cores

Os valores abaixo formam uma paleta inicial estimada. Confirme os HEX com a interface oficial antes da implementação final.

| Token | HEX | Uso sugerido |
|---|---|---|
| `color-primary` | `#168A45` | Ações principais e identidade |
| `color-primary-hover` | `#106638` | Hover e estados ativos |
| `color-primary-dark` | `#123B2B` | Títulos e fundos institucionais |
| `color-primary-light` | `#EAF6EE` | Cards e seções suaves |
| `color-accent` | `#B7E36A` | Destaques e indicadores |
| `color-white` | `#FFFFFF` | Superfícies e textos invertidos |
| `color-background` | `#FFFFFF` | Fundo principal |
| `color-surface` | `#F5F8F5` | Superfícies secundárias |
| `color-text` | `#202A24` | Texto principal |
| `color-text-secondary` | `#6B756E` | Texto auxiliar |
| `color-border` | `#E3EAE5` | Bordas e divisórias |

#### Intenção de uso

- **Verde principal:** reservar para ações primárias e elementos de marca.
- **Verde escuro:** utilizar em títulos, áreas institucionais e elementos de maior peso.
- **Verde claro:** aplicar em superfícies suaves, agrupamentos e cards.
- **Cor de destaque:** usar com moderação para indicadores e chamadas visuais.
- **Neutros:** garantir legibilidade, respiro e hierarquia.

### 2.2 Tipografia

Família sugerida para implementação inicial: `Inter`, com fallback para `system-ui` e `sans-serif`. A fonte efetivamente utilizada pelo site precisa ser confirmada.

| Estilo | Tamanho | Peso | Uso |
|---|---:|---:|---|
| Display | 56 px | 700 | Headline principal |
| H1 | 48 px | 700 | Título principal |
| H2 | 36 px | 700 | Título de seção |
| H3 | 28 px | 700 | Subtítulo |
| H4 | 20 px | 600 | Título de card |
| Body | 16 px | 400 | Texto corrido |
| Small | 14 px | 400 | Texto auxiliar |
| Caption | 12 px | 400 | Legendas e metadados |

**Regras tipográficas sugeridas**

- Headings: line-height entre `1.15` e `1.25`.
- Texto corrido: line-height entre `1.5` e `1.7`.
- Headings grandes podem usar letter-spacing negativo discreto.
- Evitar muitos pesos diferentes na mesma página.
- Validar a família e os pesos contra os arquivos reais do site.

### 2.3 Espaçamento

| Token | Valor | Aplicação |
|---|---:|---|
| `spacing-1` | 4 px | Microespaçamentos |
| `spacing-2` | 8 px | Ícone e texto |
| `spacing-3` | 12 px | Elementos compactos |
| `spacing-4` | 16 px | Padding padrão |
| `spacing-6` | 24 px | Cards e agrupamentos |
| `spacing-8` | 32 px | Separação interna |
| `spacing-12` | 48 px | Blocos e componentes |
| `spacing-16` | 64 px | Seções |
| `spacing-24` | 96 px | Grandes intervalos |

### 2.4 Bordas, raios e sombras

| Token | Valor sugerido |
|---|---|
| `radius-sm` | 8 px |
| `radius-md` | 12 px |
| `radius-lg` | 20 px |
| `radius-xl` | 28 px |
| `radius-full` | 999 px |
| `border-default` | `1px solid #E3EAE5` |
| `shadow-sm` | `0 2px 8px rgba(18, 59, 43, .06)` |
| `shadow-md` | `0 8px 24px rgba(18, 59, 43, .09)` |
| `shadow-lg` | `0 16px 48px rgba(18, 59, 43, .12)` |

---

## 3. Componentes

### 3.1 Botões

Variantes previstas:

- **Primary:** ação principal, fundo verde e texto branco.
- **Secondary:** ação complementar, fundo verde claro e texto verde escuro.
- **Outline:** ação de menor ênfase, contorno verde.
- **Dark:** ação em áreas de destaque, fundo verde profundo.

Estados necessários:

- Default
- Hover
- Focus-visible
- Active
- Disabled
- Loading

Diretrizes:

- Altura mínima recomendada de 48 px.
- Área clicável confortável em dispositivos móveis.
- Texto curto, orientado à ação.
- Foco visível por teclado.
- Não depender apenas de cor para comunicar estado.

### 3.2 Cards

Tipos sugeridos:

| Tipo | Conteúdo |
|---|---|
| Benefit Card | Ícone, título, descrição e ação |
| Cashback Card | Indicador, explicação e ação |
| Statistic Card | Número em destaque e legenda |
| Step Card | Número/ícone, título e explicação |
| Partner Card | Marca do parceiro, categoria e benefício |
| Testimonial Card | Depoimento e identificação |

Diretrizes:

- Padding inicial sugerido: 24 px.
- Raio inicial sugerido: 20 px.
- Borda neutra e sombra discreta.
- Hover com elevação sutil apenas quando o card for interativo.
- Manter consistência de alinhamento e altura em grids.

### 3.3 Navegação

A navegação pública pode contemplar:

- Logo.
- Links para seções ou páginas principais.
- Acesso à plataforma ou área do usuário.
- CTA principal.

Em telas menores, avaliar menu recolhido e manter o CTA principal acessível sem comprometer a área útil.

### 3.4 Formulários

Um campo deve prever:

- Label persistente.
- Input.
- Texto de ajuda opcional.
- Estado de erro com mensagem textual.
- Estado de sucesso quando aplicável.
- Foco visível.
- Indicação de campo obrigatório.

### 3.5 Outros componentes

- **Badge:** categorias, benefícios e status.
- **Accordion / FAQ:** pergunta expansível e resposta.
- **Statistic:** valor, unidade e legenda.
- **Testimonial:** texto, nome e contexto.
- **Footer:** navegação, contato, redes e informações legais.
- **Icon:** usar uma família consistente e tamanhos padronizados.

---

## 4. Patterns e estrutura de página

### 4.1 Hero

Estrutura sugerida:

1. Headline orientada ao principal benefício.
2. Texto de apoio curto.
3. CTA principal.
4. CTA secundário, se necessário.
5. Imagem ou elemento visual de apoio.

A composição deve deixar clara a proposta de valor sem competir com muitos elementos simultâneos.

### 4.2 Benefícios e cashback

- Apresentar benefícios em cards com hierarquia clara.
- Diferenciar categorias por texto e ícone, não apenas por cor.
- Explicar condições relevantes junto ao benefício.
- Usar CTA específico para cada ação.

### 4.3 Simulador de economia

- Agrupar entradas relacionadas.
- Exibir unidades e explicações junto aos campos.
- Destacar o resultado com hierarquia visual.
- Informar premissas e limitações do cálculo.
- Permitir correção fácil dos valores inseridos.

### 4.4 Etapas de adesão

- Apresentar passos em ordem.
- Usar numeração ou ícones consistentes.
- Manter descrições curtas.
- Em mobile, reorganizar em coluna.

### 4.5 FAQ

- Pergunta com área clicável ampla.
- Indicador visual de expansão.
- Resposta com boa legibilidade.
- Suporte a teclado e leitores de tela.

---

## 5. Layout e responsividade

Breakpoints propostos — validar contra o comportamento real do site:

| Faixa | Largura |
|---|---:|
| Mobile | Até 767 px |
| Tablet | 768–1199 px |
| Desktop | 1200 px ou mais |

| Propriedade | Desktop | Tablet | Mobile |
|---|---:|---:|---:|
| Margem lateral | 64 px | 32 px | 20 px |
| Grid | 12 colunas | 8 colunas | 4 colunas |
| H1 | 48–56 px | 40 px | 32–36 px |
| Espaço entre seções | 96 px | 72 px | 56 px |
| Cards | 3–4 colunas | 2 colunas | 1 coluna |

### Regras gerais

- Utilizar container centralizado com largura máxima.
- Reduzir margens e espaçamentos progressivamente em telas menores.
- Evitar textos longos em colunas estreitas.
- Empilhar cards no mobile quando necessário.
- Garantir que botões e campos tenham área de toque adequada.
- Não permitir rolagem horizontal involuntária.

---

## 6. Tokens CSS

O bloco a seguir reúne os tokens iniciais estimados e pode ser utilizado como ponto de partida no projeto.

```css
:root {
  /* BRAND COLORS */
  --color-primary: #168A45;
  --color-primary-hover: #106638;
  --color-primary-dark: #123B2B;
  --color-primary-light: #EAF6EE;
  --color-accent: #B7E36A;

  /* NEUTRALS */
  --color-white: #FFFFFF;
  --color-background: #FFFFFF;
  --color-surface: #F5F8F5;
  --color-text: #202A24;
  --color-text-secondary: #6B756E;
  --color-border: #E3EAE5;

  /* FEEDBACK */
  --color-success: #168A45;
  --color-warning: #E6A23C;
  --color-error: #D94848;
  --color-info: #3685C8;

  /* TYPOGRAPHY */
  --font-family-base: "Inter", system-ui, sans-serif;

  --font-size-xs: 12px;
  --font-size-sm: 14px;
  --font-size-md: 16px;
  --font-size-lg: 18px;
  --font-size-xl: 20px;
  --font-size-2xl: 28px;
  --font-size-3xl: 36px;
  --font-size-4xl: 48px;
  --font-size-display: 56px;

  --font-weight-regular: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 600;
  --font-weight-bold: 700;

  --line-height-tight: 1.15;
  --line-height-normal: 1.5;
  --line-height-relaxed: 1.7;

  /* SPACING */
  --spacing-1: 4px;
  --spacing-2: 8px;
  --spacing-3: 12px;
  --spacing-4: 16px;
  --spacing-6: 24px;
  --spacing-8: 32px;
  --spacing-12: 48px;
  --spacing-16: 64px;
  --spacing-24: 96px;

  /* BORDER RADIUS */
  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 20px;
  --radius-xl: 28px;
  --radius-full: 999px;

  /* BORDERS */
  --border-width: 1px;
  --border-default: 1px solid var(--color-border);

  /* SHADOWS */
  --shadow-sm: 0 2px 8px rgba(18, 59, 43, .06);
  --shadow-md: 0 8px 24px rgba(18, 59, 43, .09);
  --shadow-lg: 0 16px 48px rgba(18, 59, 43, .12);

  /* LAYOUT */
  --container-max-width: 1200px;
  --container-padding: 64px;
  --section-spacing: 96px;

  /* TRANSITIONS */
  --transition-fast: 150ms ease;
  --transition-normal: 250ms ease;
}

@media (max-width: 1199px) {
  :root {
    --container-padding: 32px;
    --section-spacing: 72px;
  }
}

@media (max-width: 767px) {
  :root {
    --container-padding: 20px;
    --section-spacing: 56px;
  }
}
```

## 7. CSS base dos componentes

```css
/* GLOBAL */
body {
  font-family: var(--font-family-base);
  color: var(--color-text);
  background: var(--color-background);
  font-size: var(--font-size-md);
  line-height: var(--line-height-normal);
  margin: 0;
}

.container {
  width: min(
    calc(100% - 2 * var(--container-padding)),
    var(--container-max-width)
  );
  margin-inline: auto;
}

.section {
  padding-block: var(--section-spacing);
}

/* BUTTONS */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--spacing-2);
  padding: 14px 24px;
  border: 1px solid transparent;
  border-radius: var(--radius-md);
  font: inherit;
  font-weight: var(--font-weight-semibold);
  text-decoration: none;
  cursor: pointer;
  transition: var(--transition-fast);
}

.btn-primary {
  color: var(--color-white);
  background: var(--color-primary);
}

.btn-primary:hover {
  background: var(--color-primary-hover);
}

.btn-secondary {
  color: var(--color-primary-dark);
  background: var(--color-primary-light);
}

.btn-outline {
  color: var(--color-primary);
  background: transparent;
  border-color: var(--color-primary);
}

.btn:focus-visible {
  outline: 3px solid var(--color-accent);
  outline-offset: 3px;
}

.btn:disabled {
  opacity: .5;
  cursor: not-allowed;
}

/* CARDS */
.card {
  background: var(--color-white);
  border: var(--border-default);
  border-radius: var(--radius-lg);
  padding: var(--spacing-6);
  box-shadow: var(--shadow-sm);
  transition: var(--transition-normal);
}

.card:hover {
  box-shadow: var(--shadow-md);
  transform: translateY(-2px);
}

.card-highlight {
  background: var(--color-primary-light);
  border-color: transparent;
}

/* BADGES */
.badge {
  display: inline-flex;
  align-items: center;
  padding: 6px 12px;
  border-radius: var(--radius-full);
  background: var(--color-primary-light);
  color: var(--color-primary-dark);
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-semibold);
}

/* INPUTS */
.input {
  width: 100%;
  min-height: 48px;
  padding: 12px 16px;
  border: var(--border-default);
  border-radius: var(--radius-md);
  font: inherit;
  box-sizing: border-box;
}

.input:focus {
  outline: 2px solid var(--color-primary);
  outline-offset: 2px;
}

/* HEADINGS */
.heading-display {
  font-size: clamp(36px, 5vw, 56px);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
  letter-spacing: -0.035em;
}

.heading-section {
  font-size: clamp(28px, 3vw, 36px);
  font-weight: var(--font-weight-bold);
  line-height: var(--line-height-tight);
}

/* GRID */
.grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: var(--spacing-6);
}

@media (max-width: 767px) {
  .grid {
    grid-template-columns: 1fr;
  }

  .btn {
    min-height: 48px;
  }
}
```

---

## 8. Acessibilidade e qualidade

Checklist recomendado antes de publicar:

- [ ] Contraste de texto e fundo verificado.
- [ ] Foco de teclado visível em elementos interativos.
- [ ] Inputs com labels associados.
- [ ] Mensagens de erro descritas em texto.
- [ ] Imagens informativas com texto alternativo.
- [ ] Ícones decorativos ocultos de leitores de tela quando apropriado.
- [ ] Componentes interativos operáveis por teclado.
- [ ] Layout validado em larguras mobile, tablet e desktop.
- [ ] Estados hover, focus, active e disabled documentados.
- [ ] Conteúdo não depende exclusivamente de cor para transmitir significado.

---

## 9. Estrutura sugerida de arquivos

```text
igreen-design-system/
├── README.md
├── tokens/
│   └── tokens.css
├── styles/
│   ├── base.css
│   ├── buttons.css
│   ├── cards.css
│   ├── forms.css
│   └── layout.css
├── components/
│   ├── buttons.md
│   ├── cards.md
│   ├── navigation.md
│   ├── forms.md
│   └── feedback.md
├── patterns/
│   ├── hero.md
│   ├── benefits.md
│   ├── simulator.md
│   └── faq.md
└── guidelines/
    ├── responsive.md
    └── accessibility.md
```

## 10. Próximas validações para fidelidade ao original

Para transformar esta especificação em uma reprodução fiel, validar:

1. **Logo e marca:** versões, proporções, área de proteção e cores oficiais.
2. **Cores:** extrair os valores reais dos estilos computados e dos ativos gráficos.
3. **Tipografia:** identificar fontes carregadas, pesos e tamanhos reais.
4. **Layout:** medir largura dos containers, grid, margens e espaçamentos.
5. **Componentes:** registrar dimensões e estados reais de botões, cards, campos e menus.
6. **Imagens e ícones:** identificar ativos originais e regras de uso.
7. **Mobile:** comparar a experiência em diferentes larguras e registrar mudanças de layout.
8. **Área autenticada:** analisar separadamente as telas do portal ou aplicativo, caso façam parte do escopo.

---

## 11. Resumo

Este documento fornece uma base organizada para iniciar a implementação do Design System do iGreen Club: foundations, componentes, padrões de página, responsividade, acessibilidade e tokens CSS.

**Importante:** os tokens visuais são estimativas iniciais e não devem ser tratados como valores oficiais da marca até serem comparados com a interface real e seus ativos. A fidelidade final depende dessa etapa de inspeção e validação.
