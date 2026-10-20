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

## Abrir

Sirva esta pasta através de `localhost` ou HTTPS. Abrir `flora.html` diretamente com `file://` não permite registar o service worker. No VS Code, pode usar a extensão Live Server no `index.html`.

Para publicar no GitHub Pages, publique o conteúdo desta pasta na raiz da origem escolhida para o Pages, incluindo `index.html`, `flora.html`, `manifest.webmanifest`, `service-worker.js` e toda a pasta `assets`. A entrada `index.html` encaminha o endereço do projeto para `flora.html`.
