# Cabaña La Martina

Landing page estática (HTML + Tailwind via CDN), pronta para o GitHub Pages. Não precisa de build.

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex.: `cabana-la-martina`).
2. Envie todo o conteúdo desta pasta para a raiz do repositório (`index.html` precisa ficar na raiz):
   ```bash
   git init
   git add .
   git commit -m "Primeira versão"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/cabana-la-martina.git
   git push -u origin main
   ```
3. No GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** / pasta **/ (root)** → **Save**
4. Em 1 a 2 minutos o site fica em `https://SEU-USUARIO.github.io/cabana-la-martina/`.

## Arquivos

- `index.html`: a página.
- `.nojekyll`: faz o Pages servir os arquivos como estão, sem processar com Jekyll.
- `ASSETS.md`: origem de cada imagem, fonte e script.
- `tools/download-assets.py`: opcional, baixa imagens, fontes e scripts para uso local.

## Observações

- Imagens, fontes, Tailwind e ícones são carregados de CDNs (HTTPS), por isso funcionam no Pages sem arquivos extras.
- Para hospedar tudo no repositório: `python3 tools/download-assets.py`, depois `mv index.local.html index.html` e envie também a pasta `assets/`.
- As imagens do Webflow vêm do template original: confirme os direitos de uso antes de publicar.
