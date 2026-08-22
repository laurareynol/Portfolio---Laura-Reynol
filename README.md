# Portfólio — Laura Reynol

Site estático de página única (`index.html`), sem build/dependências. Basta abrir o arquivo ou publicar via GitHub Pages.

## Estilo

Fundo claro e minimalista, formas orgânicas (blobs, cantos arredondados assimétricos, colagens de imagem sobrepostas) e uma fonte script elegante ("Petit Formal Script") para os títulos grandes, combinada com serifada itálica ("Playfair Display") nos subtítulos e uma sans limpa ("Inter") no corpo do texto. Vinho (`--vinho`) é a única cor de destaque.

> As fontes vêm do Google Fonts — carregam normalmente em qualquer navegador com internet, sem configuração extra.

## Estrutura

- `index.html` — portfólio atual.
- `arquivo/index-antigo.htm` — versão bem anterior do site (estilo azul/laranja), mantida só como referência. Não está em uso.

## Como adicionar um projeto novo

No `index.html`, cada projeto é um `<article class="proj">`. Duplique o bloco de "Projeto A" (ou "Projeto B") e ajuste:

1. `.proj-cabeca .nome` — nome do projeto.
2. `.paleta` — 2 a 4 bolinhas de cor (`<i style="background:#...">`) com as cores principais do projeto.
3. `.proj-meta` — categoria, ano, serviços (separados por `·` automaticamente via CSS).
4. Remova o `.proj-status` ("aguardando conteúdo") quando o projeto tiver conteúdo real.
5. `.proj-corpo` — texto sobre o desafio/ideia/solução.
6. `.colagem` — cada `<div class="peca">` é um espaço de imagem. Troque o conteúdo por uma tag `<img>` real. As classes `p1`/`p2`/`p3`/`p4` controlam tamanho e forma (retângulo orgânico, círculo, cartão levemente rotacionado); `destaque` dá um tom vinho de fundo a uma peça.
7. Dê um `id` único ao `<article>` (ex. `id="projeto-c"`) e adicione a entrada correspondente na lista `.indice-lista` (seção "Índice").

Se os projetos forem de disciplinas diferentes (ex. identidade visual vs. ilustração), duplique a seção `<section class="categoria">` ("Design Gráfico") antes do grupo de projetos daquela categoria.

## Como adicionar imagens

Duas formas:

1. **Mandar direto no chat** — a forma mais simples. As imagens são salvas numa pasta do repositório (ex. `imagens/nome-do-projeto/`) e os placeholders viram `<img>` reais.
2. **Subir você mesma no GitHub** — crie uma pasta `imagens/`, suba os arquivos por lá (github.com → o repositório → "Add file") e avise quais arquivos correspondem a qual projeto.
