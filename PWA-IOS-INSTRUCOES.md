# PWA do Dashboard Centro Oeste

Arquivos criados para transformar o painel em aplicativo:

- `manifest.webmanifest`: nome, cores, modo standalone e icones do app.
- `sw.js`: cache local para abrir mais rapido e manter o painel disponivel depois do primeiro acesso.
- `pwa-register.js`: registra o service worker no navegador.
- `icons/`: icones do app, incluindo `apple-touch-icon.png` para iPhone/iPad.

## Como testar no computador

1. Abra a pasta em um servidor local, por exemplo com Python:

   ```bash
   python -m http.server 8080
   ```

2. Acesse:

   ```text
   http://localhost:8080
   ```

3. No Chrome ou Edge, abra DevTools > Application > Manifest e Service Workers para conferir se o PWA foi reconhecido.

## Como instalar no iPhone/iPad

1. Publique a pasta em um endereco HTTPS.
2. Abra o link pelo Safari no iPhone ou iPad.
3. Toque em Compartilhar.
4. Toque em Adicionar a Tela de Inicio.
5. Confirme o nome do app e toque em Adicionar.

## Observacoes importantes para iOS

- O iOS instala PWAs somente pelo Safari.
- O site precisa estar em HTTPS quando publicado fora do `localhost`.
- O icone usado pelo iOS e `icons/apple-touch-icon.png`.
- O modo standalone usa as metas `apple-mobile-web-app-capable` e `apple-mobile-web-app-title` adicionadas no `index.html`.
