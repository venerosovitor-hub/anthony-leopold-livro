# A História de Anthony Leopold — página de download

Site simples e gratuito para hospedar no GitHub Pages, com download do livro em EPUB e PDF.

## Estrutura

```
index.html              → a página inteira (HTML + CSS, sem dependências externas além da fonte)
assets/
  background.jpg         → imagem de fundo do topo (janela com vela e mansão)
  capa-livro.jpg          → capa final do livro
  logo-transparente.png   → logotipo "A História de Anthony Leopold" (fundo transparente, usado no topo)
  logo-selo.jpg           → versão do logo com fundo dourado (usada como ícone da aba do navegador)
downloads/
  A-Historia-de-Anthony-Leopold.pdf
  A-Historia-de-Anthony-Leopold.epub
```

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (por exemplo `anthony-leopold-livro`).
2. Faça upload de todos os arquivos e pastas acima mantendo essa mesma estrutura (o `index.html` precisa ficar na raiz do repositório).
3. No repositório, vá em **Settings → Pages**.
4. Em "Build and deployment", escolha **Deploy from a branch**, selecione a branch `main` e a pasta `/root`, depois clique em **Save**.
5. Em alguns minutos o site fica no ar em `https://SEU-USUARIO.github.io/anthony-leopold-livro/`.

## Como atualizar toda semana

O arquivo do livro (PDF e EPUB) é cumulativo — cada semana ele já sai com o capítulo novo incluído. Por isso, a forma mais simples de atualizar é:

1. Substitua os dois arquivos dentro de `downloads/` pelas versões mais novas, **mantendo exatamente os mesmos nomes** (`A-Historia-de-Anthony-Leopold.pdf` e `A-Historia-de-Anthony-Leopold.epub`). Assim os botões de download continuam funcionando sem precisar tocar no HTML.
2. Abra o `index.html`, procure a seção `<ul class="chapters">` e adicione uma nova linha com o título do capítulo novo, no mesmo formato das existentes:

   ```html
   <li><span class="ch-num">Capítulo 4</span><span class="ch-title">&nbsp; Título do Capítulo</span></li>
   ```

3. Salve, suba (commit) o `index.html` e os dois arquivos atualizados. O GitHub Pages publica a nova versão automaticamente.

## Outros ajustes rápidos

- **Instagram:** o link já aponta para `@ahistoriadeanthonyleopold`. Para trocar, edite o `href` da seção `#contato` no `index.html`.
- **Texto de "Sobre a História":** fica na seção `id="sobre"`, é só editar os parágrafos.
- **Cores:** estão centralizadas no início do `<style>`, nas variáveis `--gold`, `--ink`, `--parchment` etc.
