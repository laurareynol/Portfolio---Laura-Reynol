# Portfólio — Laura Reynol

Site estático de página única (`index.html`), sem build/dependências. Basta abrir o arquivo ou publicar via GitHub Pages.

## Estilo

Fundo escuro, painéis de "papel" (`.folha`) para texto e títulos grandes entre colchetes (`.carimbo`, ex. `[ Work . ]`) na fonte script "Aston Script", sempre em vinho escuro sólido (`--vinho`) — sem sombra ou segunda cor. Vinho é a única cor de destaque do site.

## Estrutura

- `index.html` — portfólio atual.
- `fonts/aston-script.woff2` e `fonts/aston-script.ttf` — a fonte dos títulos, hospedada localmente (não depende do Google Fonts).
- `arquivo/index-antigo.htm` — versão bem anterior do site (estilo azul/laranja), mantida só como referência. Não está em uso.

Para trocar a fonte dos títulos no futuro, basta substituir os dois arquivos em `fonts/` (mesmo nome) ou ajustar o bloco `@font-face` e a variável `--display` no início do `<style>`.

## Como adicionar um projeto novo

No `index.html`, cada projeto é um par de blocos: uma `<section class="faixa">` (título-carimbo + categorias, fundo escuro) seguida de um `<article class="folha">` (texto + grade de imagens, fundo papel). Duplique os dois blocos de "Projeto A" e ajuste:

1. O conteúdo do `<h2 class="carimbo">` — nome do projeto, formato `[ Nome . ]`.
2. `.proj-meta` — categorias/tags curtas (ex.: identidade visual, 2026, papelaria).
3. Remova o `.proj-status` ("aguardando conteúdo") quando o projeto tiver conteúdo real.
4. `.proj-corpo` — texto sobre o desafio/ideia/solução.
5. `.grade-img` — cada `<div class="slot">` é um espaço de imagem. Troque o conteúdo por uma tag `<img>` real. As classes `s-g2`/`s-g3`/`s-g4`/`s-g6` controlam quantas colunas (de 6) a imagem ocupa; `destaque` dá um leve tom vinho a um slot.
6. Dê um `id` único ao `<article class="folha">` (ex. `id="projeto-c"`) e adicione a entrada correspondente na lista `.indice-lista`.

## Como adicionar imagens

Duas formas:

1. **Mandar direto no chat** — a forma mais simples. As imagens são salvas numa pasta do repositório (ex. `imagens/nome-do-projeto/`) e os placeholders viram `<img>` reais.
2. **Subir você mesma no GitHub** — crie uma pasta `imagens/`, suba os arquivos por lá (github.com → o repositório → "Add file") e avise quais arquivos correspondem a qual projeto.
