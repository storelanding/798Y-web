# Ai Translator — website

A static landing site for the **Ai Translator** Android app on Google Play. Plain HTML + CSS; there is no build step.

| File | Purpose |
|---|---|
| `index.html` | App landing page |
| `policies.html` | Privacy Policy |
| `terms.html` | Terms of Use |
| `app-ads.txt` | Ad-network authorization file |
| `404.html` | Not-found page |
| `assets/` | `style.css`, `icon.svg`, `img/` (app screenshots) |
| `site.json` | Site metadata (used for future updates) |

## Deploy

**Cloudflare Pages:** Workers & Pages → Create → Pages → Connect to Git → pick this repo. Framework preset **None**, leave the build command empty, set the output directory to `/`. Add your domain under Custom domains.

**Vercel:** Add New → Project → import this repo. Framework **Other**, no build command, output directory `.`. Add your domain under Settings → Domains.

## After deploying

- **app-ads.txt** must be reachable at `https://<your-domain>/app-ads.txt`, and that domain must match the developer website listed on Google Play.
- **Privacy Policy URL** to enter on Google Play: `https://<your-domain>/policies.html`.
- Once the domain is known, add `siteUrl` to `site.json`, add a `Sitemap:` line to `robots.txt`, and create `sitemap.xml`.
