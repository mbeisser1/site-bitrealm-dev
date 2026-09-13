# bitrealm.dev

The one-page site for Bitrealm LLC. Plain HTML and CSS, no build step, no JavaScript, no forms.

## Files

- `index.html` – the page
- `404.html` – not-found page; Cloudflare Pages serves it with a real 404 status
- `style.css` – the styles (dark theme, IBM Plex Mono)
- `content.md` – the page copy as a working document; edit there, then paste into `index.html` by hand
- `fonts/` – IBM Plex Mono, self-hosted so the page loads nothing from third parties
- `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` – the bracket mark as tab and home-screen icons
- `og.png` – 1200×630 preview image for links shared on LinkedIn, Slack, and similar
- `_headers` – security headers Cloudflare Pages applies to every response
- `robots.txt`

## Deploy on Cloudflare Pages

1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Pick `mbeisser1/site-bitrealm-dev`, production branch `main`.
3. Build settings: framework preset **None**, build command **empty**, build output directory **/** (the repo root).
4. Save and deploy. You get a `*.pages.dev` URL immediately.
5. In the project, **Custom domains** → **Set up a custom domain** → `bitrealm.dev`. Cloudflare adds the DNS record for you when the zone is already on Cloudflare; add `www.bitrealm.dev` the same way if you want it.

Every push to `main` redeploys. Other branches get preview URLs.

## Edit

Open `index.html` in a browser to preview locally. There is nothing to install.
