# vdmzo-website

Company website for [vdmzo.com](https://vdmzo.com): cloud integration, automation software and AI.

Static HTML, CSS and JavaScript with no build step and no dependencies.

## Structure

```
index.html        single-page site (hero, services, AI, why, process, engagement, contact)
styles.css        all styling; brand tokens are at the top in :root
script.js         nav, scroll reveal, contact form
404.html          not-found page
assets/           favicon and social share image
```

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy (GitHub Pages)

1. The repository must be public, unless the account has GitHub Pro.
2. Settings → Pages → Build and deployment → Source: **Deploy from a branch** → `main` / `(root)` → Save.
3. After a minute or so the site is live at `https://vgudzhev.github.io/vdmzo-website/`.

### Custom domain (vdmzo.com)

1. Settings → Pages → Custom domain: `vdmzo.com` → Save. GitHub adds a `CNAME` file to the branch.
2. At your DNS provider, add `A` records for `vdmzo.com` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153` and `185.199.111.153`, and a `CNAME` record for `www` pointing to `vgudzhev.github.io`.
3. Once DNS has propagated, tick **Enforce HTTPS**.

`.nojekyll` tells Pages to serve the files as-is, without running Jekyll.

## Contact form

By default the form opens the visitor's email client, addressed to `hello@vdmzo.com`. To store submissions instead, create a form endpoint (for example with Formspree) and set `FORM_ENDPOINT` in `script.js`.

## Brand

| Token | Value |
|-------|-------|
| Background | `#0b0c0b` |
| Accent (lime) | `#a6e35b` |
| Text | `#e9ece8` |
| Muted | `#9aa09a` |
| Display font | Montserrat |
| Body font | Inter |
