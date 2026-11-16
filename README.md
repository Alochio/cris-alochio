# Cris Alochio — Treino personalizado

Sistema estático para montar, conferir e baixar fichas de treino em PDF. Os dados e a geração do PDF ficam no navegador.

O arquivo `modelo.pdf` é o modelo padrão incluído: a capa e a página final são preservadas, e o cabeçalho original é usado nas fichas. Não é necessário enviar o modelo a cada uso. As tabelas compartilham a mesma folha quando há espaço; treinos extensos continuam na folha seguinte com os títulos repetidos.

## Publicar no GitHub Pages

1. Envie os arquivos do projeto para a raiz do repositório, incluindo `index.html`, `modelo.pdf`, a pasta `assets/` e `.nojekyll`.
2. No repositório, abra **Settings → Pages**.
3. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
4. Selecione a branch que contém os arquivos (por exemplo, `main`), a pasta **/(root)** e clique em **Save**.
5. Abra o endereço informado pelo GitHub Pages após a publicação.

O projeto usa caminhos relativos e funciona também em `https://usuario.github.io/repositorio/`. Não há etapa de build, servidor de aplicação ou dependência de CDN. A biblioteca PDF-LIB 1.17.1 e sua licença estão em `assets/`.

Referências: [configuração da publicação](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) e [arquivos estáticos e .nojekyll](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site).

## Abrir localmente

Na pasta do projeto, execute:

```sh
python -m http.server 8000
```

Acesse `http://localhost:8000/`. Use o endereço HTTP para que o navegador consiga carregar o modelo PDF.

A pasta `.tools/` contém apenas ferramentas e arquivos de verificação local e está excluída pelo `.gitignore`.
