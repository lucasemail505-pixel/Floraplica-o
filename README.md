# Herbarium PWA

A aplicação foi isolada nesta pasta para não misturar os ficheiros de outros trabalhos do workspace.

## Estrutura

```text
herbarium-pwa/
  index.html                 Entrada do GitHub Pages
  flora.html                 Entrada da aplicação
  manifest.webmanifest       Nome, ícones e comportamento de instalação
  service-worker.js          Cache do shell e suporte offline
  assets/
    css/app.css              Estilos da aplicação
    js/app.js                Navegação e interações
    icons/icon.svg           Ícone da aplicação
    icons/icon-maskable.svg  Ícone adaptativo para instalação
    icons/icon-192.png       Ícone de instalação 192 × 192
    icons/icon-512.png       Ícone de instalação 512 × 512
    icons/icon-maskable-512.png Ícone adaptativo 512 × 512
```

## Abrir localmente

Sirva esta pasta através de `localhost` ou HTTPS. Abrir `flora.html` diretamente com `file://` não permite registar o service worker. No VS Code, pode usar a extensão Live Server no `index.html`.

## Publicar no GitHub Pages

1. Crie um repositório GitHub só para esta aplicação e carregue **o conteúdo desta pasta** para a raiz do repositório (`index.html`, `flora.html`, `manifest.webmanifest`, `service-worker.js`, `assets/` e `.github/`). Não carregue a pasta de trabalho que contém os outros projetos.
   **Importante:** `assets/` tem de ficar na raiz do repositório, ao lado de `flora.html`. Sem essa pasta, as fotografias devolvem 404 e não aparecem no site.
2. Na página do repositório, abra **Settings → Pages** e escolha **GitHub Actions** em *Build and deployment*.
3. Envie as alterações para o ramo `main`. O workflow em `.github/workflows/pages.yml` publica automaticamente o site.
4. Quando a ação terminar, abra **Settings → Pages** para obter o endereço. Para um repositório de projeto, será semelhante a `https://<utilizador>.github.io/<repositorio>/`.

Os caminhos do site, manifesto e service worker são relativos, por isso funcionam tanto na raiz de um domínio GitHub Pages como no subdiretório de um repositório. O service worker atualiza a cache da PWA quando é publicada uma nova versão.

As fotografias das plantas são carregadas do Unsplash, por isso não é necessário enviar a pasta `assets/` para que apareçam. É necessária uma ligação à internet para as carregar.
