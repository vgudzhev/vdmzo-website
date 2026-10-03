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
CNAME             custom domain for GitHub Pages
```

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

**GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root. The `CNAME` file points the site at `vdmzo.com`. At your DNS provider, add the GitHub Pages A records for the apex domain and a `CNAME` record for `www` pointing to `<user>.github.io`.

Netlify, Cloudflare Pages or S3 also work: upload the repository root as-is.

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
