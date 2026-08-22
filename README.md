# Portfólio — Laura Reynol

Site estático de página única (`index.html`), sem build/dependências. Basta abrir o arquivo ou publicar via GitHub Pages.

## Estilo

Seções alternam entre bege claro (`.clara`) e vinho bem escuro (`.escura`) conforme a página é rolada — como no site do Cisne Negro. Títulos grandes (`.carimbo`, ex. `Trabalhos.`) usam a fonte script "Aston Script" e sempre a cor de acento da seção em que estão (vinho escuro nas seções claras, bege nas seções escuras — variável `--acento`, definida por seção). A navegação fica fixa na lateral esquerda (desktop) e, no topo, em telas menores; um `IntersectionObserver` detecta qual seção está no centro da tela e ajusta a cor do menu (vinho ou bege) por CSS puro.

O site tem seletor de idioma (PT/EN/ES) no rodapé da navegação. A troca é feita em JavaScript puro: cada texto traduzível tem um atributo `data-i18n="chave"`, e o dicionário com as três versões fica no `<script>` no final do `index.html` (objeto `TR`). A escolha do visitante fica salva no navegador (`localStorage`) e é aplicada de novo na próxima visita.

## Estrutura

- `index.html` — portfólio atual.
- `fonts/aston-script.woff2` e `fonts/aston-script.ttf` — a fonte dos títulos, hospedada localmente (não depende do Google Fonts).
- `arquivo/index-antigo.htm` — versão bem anterior do site (estilo azul/laranja), mantida só como referência. Não está em uso.

Para trocar a fonte dos títulos no futuro, basta substituir os dois arquivos em `fonts/` (mesmo nome) ou ajustar o bloco `@font-face` e a variável `--display` no início do `<style>`.

## Como adicionar um projeto novo

No `index.html`, cada projeto é um único `<section class="pagina clara">` ou `<section class="pagina escura">` (alterne a cor em relação ao projeto anterior, pra manter o efeito de mudança de cor). Duplique a seção de "Projeto A" ou "Projeto B" e ajuste:

1. O conteúdo do `<h2 class="carimbo">` — nome do projeto, formato `Nome.`.
2. `.proj-meta` — categorias/tags curtas (ex.: identidade visual, 2026, papelaria).
3. Remova o `.proj-status` ("aguardando conteúdo") quando o projeto tiver conteúdo real.
4. `.proj-corpo` — texto sobre o desafio/ideia/solução.
5. `.grade-img` — cada `<div class="slot">` é um espaço de imagem. Troque o conteúdo por uma tag `<img>` real. As classes `s-g2`/`s-g3`/`s-g4`/`s-g6` controlam quantas colunas (de 6) a imagem ocupa; `destaque` dá um leve tom de acento a um slot.
6. Dê um `id` único à seção (ex. `id="projeto-c"`) e adicione a entrada correspondente na lista `.indice-lista`.

Se quiser que o texto do projeto novo também apareça em inglês e espanhol, adicione um `data-i18n="chave-nova"` no elemento e a tradução correspondente nas três línguas dentro do objeto `TR`, no `<script>` no final do arquivo (é só me pedir que eu faço isso pra você quando enviar os projetos).

## Como adicionar imagens (incluindo sua foto)

Duas formas:

1. **Anexar o arquivo aqui na conversa** — use o botão/ícone de anexar arquivo (não cole ou arraste a imagem solta na mensagem; ela precisa ser um anexo de verdade pra eu conseguir salvá-la no repositório).
2. **Subir você mesma no GitHub** — crie uma pasta `imagens/`, suba os arquivos por lá (github.com → o repositório → "Add file") e avise quais arquivos correspondem a qual projeto.
