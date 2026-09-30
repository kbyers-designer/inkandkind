# Ink & Kind Studio website — GitHub Pages deploy

This folder is the complete website, ready to push to GitHub.

## What's in here

- `index.html` — the whole landing page
- `assets/` — all images
- `CNAME` — tells GitHub Pages this site lives at inkandkind.com

## Deploy steps

1. **Create a repo** on GitHub (any name, e.g. `inkandkind-website`). Upload everything in this folder, or push it from the command line.
2. **Turn on Pages:** in the repo, go to Settings → Pages. Under "Build and deployment", choose Deploy from a branch, then `main` and `/(root)`. Save.
3. **Set the custom domain:** in that same Pages settings page, enter `inkandkind.com` in the Custom domain box and save. (The CNAME file does the same job; doing it in settings is the reliable way.) Tick "Enforce HTTPS" once the certificate is issued.
4. **Point your DNS at GitHub.** Wherever inkandkind.com is registered, add these records:
   - Apex domain (`inkandkind.com`): four A records pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www.inkandkind.com`: a CNAME record pointing to `<your-github-username>.github.io`
5. **Wait.** DNS can take a few minutes to a few hours. GitHub provisions the HTTPS certificate automatically. Once "Enforce HTTPS" is on, you're live at https://inkandkind.com.

## Updating the site later

Edit `index.html`, commit, and push — GitHub Pages redeploys automatically in a minute or two.
