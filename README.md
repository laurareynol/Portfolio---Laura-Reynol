# Portfólio — Laura Reynol

Site estático de página única (`index.html`), sem build/dependências. Basta abrir o arquivo ou publicar via GitHub Pages.

## Estrutura

- `index.html` — portfólio atual (visual em preto/branco, tipografia mono, títulos entre parênteses).
- `arquivo/index-antigo.htm` — versão anterior do site, mantida só como referência. Não está em uso.

## Como adicionar um projeto novo

Em `index.html`, dentro de `<div class="projetos">`, duplique um bloco `<article class="proj">...</article>` inteiro e ajuste:

1. `proj-num` — número do projeto, ex. `( 03 )`.
2. Remova ou troque a tag `proj-status` (`aguardando conteúdo`) quando o projeto tiver conteúdo real.
3. `proj-tit` — nome do projeto, formato `(NOME.)`.
4. `proj-cat` — categoria (ex.: identidade visual, editorial, UI).
5. `proj-desc` — texto curto sobre o desafio/solução.
6. `grade-img` — cada `<div class="slot">` é um espaço de imagem. Troque o conteúdo do `<span>` por uma tag `<img>` real, ou mantenha as classes `s-g2`/`s-g3`/`s-g4`/`s-g6` para controlar quantas colunas (de 6) a imagem ocupa. As classes `acc-a`/`acc-b`/`acc-c` dão um fundo colorido de destaque a um slot.
7. `tags` — palavras-chave do projeto.

O bloco `( MAIS EM BREVE. )` no final da lista de projetos pode ser removido quando não fizer mais sentido, ou movido para depois do último projeto adicionado.
