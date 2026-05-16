# Iara Games

Plataforma de distribuição de jogos indie brasileiros, com foco exclusivo em desenvolvedores nacionais. O projeto tem como missão dar visibilidade a criadores independentes de todo o Brasil, oferecendo uma experiência em português, com preços em reais e curadoria honesta da comunidade.

---

## Vídeo Pitch

[Assistir no Loom](https://www.loom.com/share/a236b5e155d54672abfa2869a88fc874)

---

## Sprint 03 — Bootstrap, Responsividade e Página de Jogo

### O que evoluiu da Sprint 02 para a Sprint 03

| Aspecto | Sprint 02 | Sprint 03 |
|---|---|---|
| Framework CSS | Sem framework | Bootstrap 5 via CDN |
| Tipografia | Geist + Geist Mono | Michroma (títulos) + Outfit (textos) — identidade visual da Atividade 01 |
| Paleta | `#3EA8DA`, `#E2FD4A` | `#009AFF`, `#FEA116`, `#E2FD4A` — paleta oficial da identidade visual |
| Páginas | `index.html`, `login.html`, `cadastro.html`, `em-construcao.html` | Adição de `jogo.html` — página de detalhes de jogo |
| Logo | PNG provisório | SVG vetorial final (`logo_iara.svg`) |
| CSS | `style.css` único | `variables.css` + `style.css` + `jogo.css` |
| Navbar | Flexbox manual | Componente Bootstrap com colapso automático e menu lateral mobile |
| Banner | Grid Flexbox estático | Grid 60/40 Bootstrap no desktop + Carousel Bootstrap no mobile |
| Cards de jogos | Flexbox manual | `row-cols-*` Bootstrap com breakpoints responsivos |
| Galeria | Ausente | Carousel Bootstrap com 5 screenshots e thumbnails sincronizadas |
| Avaliações | Ausente | Cards de review com nota, estrelas, barras de distribuição e `<time>` semântico |
| Acessibilidade | `aria-label`, `role`, `alt` | Expansão com `aria-labelledby`, `aria-current`, `aria-expanded`, `<figure>`, `<figcaption>`, `<time>`, `visually-hidden` |

---

## Persona principal

**Lucas Silveira** · 22 anos · Ensino Superior Incompleto · Renda Baixa-média

> "Quero jogar games que reflitam a minha realidade, minha cultura, não só coisas importadas. Mas é difícil achar isso numa plataforma só."

### Perfil e contexto
Lucas mora em São Paulo, cursa Design e usa o celular como principal dispositivo de entretenimento. Joga de forma casual (entre aulas e o trampo de freela) e tem orgulho da cultura brasileira. Está sempre no TikTok, YouTube e Discord.

### Objetivos
- Descobrir jogos brasileiros de qualidade com facilidade
- Apoiar desenvolvedores independentes nacionais
- Compartilhar descobertas com amigos e comunidade
- Jogar sem precisar de PC gamer caro
- Sentir que a plataforma foi feita para ele

### Necessidades
- Interface simples e responsiva no celular
- Descrições e avaliações em português
- Filtros por gênero, preço e plataforma
- Curadoria confiável de jogos indie
- Preços acessíveis ou opções gratuitas

### Dores e frustrações
- Dificuldade de encontrar jogos indie brasileiros: ficam enterrados em plataformas internacionais como Steam e itch.io
- A maioria das plataformas de indie games tem interface e avaliações só em inglês
- Não sabe se um jogo desconhecido vale a pena, falta de sistema de avaliações confiável em PT-BR

---

## Relação do projeto com valores ESG

**E — Games como educação ambiental**

A plataforma destaca jogos com temáticas ecológicas (biodiversidade, biomas brasileiros, meio ambiente) usando curadoria e selos para transformar o entretenimento em ferramenta de conscientização ambiental.

**S — Valorização da cultura e diversidade brasileira**

A Iara Games dá visibilidade a devs indie de todas as regiões do Brasil, promovendo diversidade cultural e regional na indústria de games.

**G — Transparência e comunidade**

A plataforma garante avaliações honestas da comunidade, sem pay-to-win ou conteúdo patrocinado oculto, criando um ambiente de confiança em PT-BR.

---

## Recursos de Acessibilidade

**Semântica HTML**
O projeto utiliza tags semânticas em toda a estrutura: `<header>`, `<nav>`, `<main>`, `<section>`, `<aside>`, `<footer>`, `<article>` e `<figure>` com `<figcaption>`. As seções possuem títulos associados via `aria-labelledby`, e datas são marcadas com `<time datetime="...">` para leitura correta por tecnologias assistivas.

**Textos alternativos**
Todas as imagens possuem atributo `alt` com descrição do conteúdo visual — capas de jogos, logotipo e screenshots. Imagens puramente decorativas utilizam `alt=""` combinado com `aria-hidden="true"`, sinalizando aos leitores de tela que devem ser ignoradas.

**ARIA**
Elementos interativos possuem `aria-label` descritivos: botões de navegação do banner, controles do carrossel, toggler do menu mobile e botões de compra. O carrossel de banner utiliza `role="tab"` e `aria-selected` nas barras de paginação. O breadcrumb é marcado com `aria-current="page"` na página atual.

**Navegação por teclado**
A estrutura de links e botões segue a ordem lógica do documento, permitindo navegação sequencial por teclado. O menu mobile é acessível via botão com `aria-expanded` e `aria-controls`, refletindo o estado aberto/fechado.

**Contraste e legibilidade**
A paleta utiliza texto branco `#FFFFFF` sobre fundo escuro `#242424`, e o azul principal `#009AFF` sobre fundo preto nos botões — ambos atendem aos critérios de contraste da WCAG 2.1 AA. O verde `#E2FD4A` é utilizado apenas para destaques e preços, sempre sobre fundo escuro.

**Responsividade**
O layout se adapta a diferentes tamanhos de tela com o sistema de grid do Bootstrap. No mobile, o banner principal é substituído por um carrossel de toque, e o menu de navegação colapsa em um menu lateral acessível pelo botão hambúrguer.

---

## Recursos do Bootstrap Utilizados

**Sistema de Grid**
Uso do sistema de colunas responsivo em todas as páginas. O banner usa `col-lg-8` e `col-lg-4` para o layout 60/40. As seções de jogos usam `row-cols-2 row-cols-sm-3 row-cols-md-4 row-cols-lg-5` para adaptar a quantidade de cards por linha conforme o tamanho da tela. A página de jogo usa `col-12 col-lg-8` e `col-12 col-lg-4` para separar conteúdo principal e coluna lateral.

**Navbar**
Componente `navbar` com `navbar-expand-lg` para colapso automático em telas menores, `navbar-toggler` para o botão hambúrguer mobile e `collapse navbar-collapse` para o menu retrátil. Uso de `ms-auto` para alinhamento dos links à direita.

**Carousel**
Dois carrosséis distintos: o banner da home em mobile com `carousel slide` e controle via `data-bs-slide`, e a galeria de screenshots na página de jogo com thumbnails clicáveis via `data-bs-slide-to`. Ambos controlados pela API JavaScript do Bootstrap (`bootstrap.Carousel`).

**Utilitários de Espaçamento e Display**
Uso extensivo de classes utilitárias como `mt-*`, `mb-*`, `py-*`, `gap-*`, `d-flex`, `d-block`, `ms-auto`, `w-100` e `h-100` para espaçamento e controle de layout sem CSS adicional.

**Utilitários Responsivos**
Classes `flex-column`, `flex-lg-row`, `align-items-center`, `justify-content-between` e `offset-md-*` para comportamentos diferentes por breakpoint.

**Visually Hidden**
Classe `visually-hidden` para esconder títulos e legendas visualmente mantendo-os acessíveis para leitores de tela.

**Containers**
Uso de `.container` em todas as seções para limitar a largura do conteúdo e centralizar automaticamente com margens laterais responsivas.

---

## Justificativas de UX e UI

### Identidade visual aplicada
O logotipo SVG, a paleta de cores e a tipografia Michroma foram extraídos diretamente da Atividade 01 e aplicados de forma consistente nas duas páginas. O azul arara `#009AFF` é usado nos CTAs principais, o amarelo `#FEA116` nos links de "Ver todos" e o verde `#E2FD4A` em preços gratuitos e badges de destaque.

### HTML semântico
O uso de elementos como `<header>`, `<nav>`, `<main>`, `<section>`, `<aside>`, `<footer>`, `<article>` e `<figure>` melhora a acessibilidade para leitores de tela e facilita a indexação por mecanismos de busca. Cada seção possui um `<h2>` identificado por `aria-labelledby`, criando hierarquia clara de conteúdo.

### variables.css separado
As custom properties de cor foram isoladas em `variables.css` e importadas tanto no `style.css` quanto no `jogo.css`. Isso garante consistência da paleta em todo o projeto e facilita ajustes futuros em um único ponto.

### Paleta de cores e contraste
A combinação de fundo `#242424` com texto branco `#FFFFFF` atende ao nível de contraste AA da WCAG 2.1. O azul `#009AFF` sobre preto nos botões também passa nos critérios de contraste para texto grande.

### Tipografia
Michroma para títulos e elementos de interface (reforça o caráter gamer e a identidade da marca) e Outfit para textos corridos (boa legibilidade em tamanhos menores e peso variável de 300 a 700).

### Página de jogo
A página `jogo.html` foi estruturada em layout de duas colunas no desktop — conteúdo principal com galeria, descrição e avaliações à esquerda, e card de compra sticky à direita. No mobile as colunas empilham verticalmente e o card deixa de ser sticky para não ocupar espaço fixo em telas pequenas.

### Decisão de navegação
Todos os cards de jogos da home e as imagens do banner linkam para `jogo.html`. O breadcrumb na página de jogo permite retorno à home e à categoria, sem beco sem saída.

---

## Estrutura de arquivos

```
iara-games/
├── index.html              # Home — página principal
├── jogo.html               # Página de detalhes de jogo
├── login.html              # Página de login
├── cadastro.html           # Página de cadastro
├── em-construcao.html      # Placeholder para páginas futuras
├── variables.css           # Custom properties da paleta
├── style.css               # Estilos globais (home + componentes compartilhados)
├── jogo.css                # Estilos exclusivos da página de jogo
├── auth.css                # Estilos de login e cadastro
├── em-construcao.css       # Estilos da página placeholder
└── images/
    ├── logo_iara.svg
    ├── image50.png
    ├── image25-1.png
    ├── fobia.png
    ├── aila.png
    ├── ruff-ghannor.png
    ├── chroma-squad.png
    ├── lenda-heroi.png
    ├── bagdex.png
    ├── enigma do medo/
    │   ├── enigma_1.png
    │   ├── enigma_2.png
    │   ├── enigma_3.png
    │   ├── enigma_4.png
    │   └── enigma_5.png
    └── icons/
        ├── arrow_left.png
        └── arrow_right.png
```

---

## Tecnologias utilizadas

- HTML5 semântico
- CSS3 (Custom Properties + Flexbox + Grid)
- Bootstrap 5.3 (Grid, Navbar, Carousel, Utilitários)
- Google Fonts — Michroma e Outfit

---

## Autor

**João Pedro Carvalho**
FIAP — Sprint 03 · 2025
