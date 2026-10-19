# Entrega Pedi Yapa

Site de entrega do material produzido pela Tape para o Pedi Yapa: um vídeo vertical e 72 fotos em resolução máxima.

## Estrutura

```
index.html            página do site (não precisa de build)
site-config.js        link do botão "Descargar todo" (Releases do GitHub)
assets/fotos/         fotos originais, sem compressão (download)
assets/grandes/       versão 2600 px, usada na visualização em tela cheia
assets/thumbs/        versão 1400 px, usada na grade
assets/video/         vídeo (original para download + versão leve para tocar)
assets/logo/          logos do Pedi Yapa e da Tape, e favicon
```

## Publicar no GitHub Pages

1. No repositório: **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`.
3. Em alguns minutos o site abre em `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

O GitHub Pages grátis exige repositório público. Qualquer pessoa com o endereço consegue ver e baixar as fotos.

## Como subir (primeira vez)

1. No GitHub, crie um repositório vazio (sem README, sem .gitignore).
2. Extraia todos os .zip da entrega na mesma pasta. Quando perguntar, mescle as pastas. No fim, a pasta deve ter `index.html` e `assets/` com `fotos/`, `grandes/`, `thumbs/`, `video/` e `logo/`.
3. Com o GitHub Desktop: **File → Add local repository…**, escolha a pasta, crie o repositório e clique em **Publish repository**.
   Pelo terminal: `git init`, `git add .`, `git commit -m "Entrega Pedi Yapa"`, `git branch -M main`, `git remote add origin URL-DO-REPOSITORIO`, `git push -u origin main`.
4. Ative o Pages como descrito acima.

O envio tem cerca de 650 MB e pode demorar alguns minutos.

## Botão "Descargar todo"

Os originais somam cerca de 490 MB, grande demais para gerar um .zip dentro do navegador do celular. Use as Releases:

1. No repositório: **Releases → Draft a new release**.
2. Anexe os .zip do Lightroom (e o vídeo, se quiser).
3. Publique e copie o endereço da página da release.
4. Abra `site-config.js`, cole o endereço em `allUrl` e salve. O botão aparece sozinho.

## Vídeo

O vídeo do evento era 4K vertical em HEVC de 10 bits (146 MB), acima do limite de 100 MB por arquivo do GitHub. Por isso há duas versões em `assets/video/`:

- `PediYapa-video-web.mp4`: 1080x1920, H.264, toca na página.
- `PediYapa-video.mp4`: 2160x3840 (4K), H.264, abaixo de 100 MB. É o arquivo do botão "Descargar video".
- `poster.jpg`: quadro de capa.

O original em HEVC (146 MB) fica com a Tape. Se quiser entregá-lo, anexe-o à Release junto com os .zip das fotos.
