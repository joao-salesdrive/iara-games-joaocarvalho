# Iara Games

Plataforma de distribuição de jogos indie brasileiros, com foco exclusivo em desenvolvedores nacionais. O projeto tem como missão dar visibilidade a criadores independentes de todo o Brasil, oferecendo uma experiência em português, com preços em reais e curadoria honesta da comunidade.

---

## Vídeo Pitch

[Assistir no Loom](https://www.loom.com/share/a236b5e155d54672abfa2869a88fc874)

---

## Sprint 02 — Evolução e UX

### O que evoluiu da Sprint 01 para a Sprint 02

| Aspecto | Sprint 01 | Sprint 02 |
|---|---|---|
| HTML | Estrutura básica com `<div>` | HTML semântico com `<main>`, `<section>`, `<nav>`, `<footer>`, `aria-label` |
| CSS | Apenas Flexbox | Flexbox + CSS Grid no footer |
| Páginas | Somente `index.html` | `index.html`, `login.html`, `cadastro.html`, `em-construcao.html` |
| Formulários | Nenhum | Login e cadastro com validação HTML nativa |
| Footer | Ausente | Footer completo com navegação em grid de 3 colunas |
| Acessibilidade | Básica | `aria-label`, `aria-required`, `role`, `alt` descritivos em todas as imagens |
| ESG | Não abordado | Seção "Jogos Conscientes" com selo Eco, conectando à proposta ambiental |
| Idioma | `lang="en"` | Corrigido para `lang="pt-BR"` |

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

## Justificativas de UX e UI

### HTML semântico
O uso de elementos como `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>` e atributos `aria-label` melhora a acessibilidade para leitores de tela e facilita a indexação por mecanismos de busca. Cada seção da home possui um `<h2>` identificado por `aria-labelledby`, criando uma hierarquia clara de conteúdo.

### CSS Grid no footer
O footer utiliza `display: grid` com `grid-template-columns: 280px 1fr` para separar a área da marca das colunas de navegação, e `grid-template-columns: repeat(3, 1fr)` nas colunas internas. Isso garante alinhamento consistente e facilita a manutenção do layout.

### Paleta de cores e contraste
A combinação de fundo `#242424` com texto branco `#ffffff` foi validada com nível de contraste AAA (15.5:1), garantindo legibilidade em qualquer cenário, incluindo usuários com baixa visão.

### Tipografia
Geist para textos corridos (boa legibilidade em tamanhos menores) e Geist Mono para títulos, labels e elementos de interface (reforça o caráter técnico e gamer da plataforma).

### Formulários acessíveis
Todos os campos possuem `<label>` associado via `for/id`, `aria-required="true"` nos campos obrigatórios, `autocomplete` para facilitar o preenchimento e `placeholder` descritivos. O botão de submit é um `<button type="submit">` semântico.

### Selo Eco
O selo posicionado entre a imagem e o nome do jogo foi escolhido para ser visível sem interromper a hierarquia visual do card. As cores verde escuro `#1a3d1a` com texto `#6efab4` mantêm o padrão da paleta da plataforma e comunicam claramente o significado ambiental.

### Decisão de navegação
O botão de login no header leva para `login.html`, que por sua vez conecta com `cadastro.html`. Esse fluxo reduz a fricção — o usuário nunca fica em beco sem saída e sempre tem um caminho de volta para a home.

---

## Estrutura de arquivos

```
iara-games/
├── index.html          # Home — página principal
├── login.html          # Página de login
├── cadastro.html       # Página de cadastro
├── em-construcao.html  # Placeholder para páginas futuras
├── style.css           # Estilos da home
├── auth.css            # Estilos compartilhados de login e cadastro
├── em-construcao.css   # Estilos da página placeholder
└── images/
    ├── logo-iara-v1.png
    ├── image50.png
    ├── image25-1.png
    ├── fobia.png
    ├── aila.png
    ├── ruff-ghannor.png
    ├── chroma-squad.png
    ├── lenda-heroi.png
    ├── bagdex.png
    └── icons/
        ├── icon-user.png
        ├── icon-user.svg
        ├── arrow_left.png
        └── arrow_right.png
```

---

## Tecnologias utilizadas

- HTML5 semântico
- CSS3 (Flexbox + Grid)
- Google Fonts — Geist e Geist Mono

---

## Autor

**João Pedro Carvalho**
FIAP — Sprint 02 · 2025
