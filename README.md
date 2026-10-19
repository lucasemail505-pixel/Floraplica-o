# Herbarium PWA

A aplicação foi isolada nesta pasta para não misturar os ficheiros de outros trabalhos do workspace.

## Estrutura

```text
herbarium-pwa/
  flora.html                 Entrada da aplicação
  manifest.webmanifest       Nome, ícones e comportamento de instalação
  service-worker.js          Cache do shell e suporte offline
  assets/
    css/app.css              Estilos da aplicação
    js/app.js                Navegação e interações
    icons/icon.svg           Ícone da aplicação
    icons/icon-maskable.svg  Ícone adaptativo para instalação
```

## Abrir

Sirva esta pasta através de `localhost` ou HTTPS. Abrir `flora.html` diretamente com `file://` não permite registar o service worker. No VS Code, pode usar a extensão Live Server no `flora.html`.

A PWA foi testada em `http://localhost:4173`; o manifesto e o shell são guardados em cache para a aplicação voltar a abrir sem rede depois da primeira visita.
