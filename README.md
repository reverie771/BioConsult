# Bio Consult

Static website for Bio Consult — audit financiar, expertiză contabilă, insolvență, evaluări.

## Stack

Plain HTML + CSS. No build step. Type loaded from Google Fonts (Fraunces + Hanken Grotesk).

## Structure

```
index.html        — Pagina principală (Home)
despre.html       — Despre Noi
audit.html        — Audit Financiar
expertiza.html    — Expertiză Contabilă
insolventa.html   — Insolvență
evaluari.html     — Evaluări
contact.html      — Contact
interior.css      — Stiluri partajate pentru paginile interioare
```

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy

Static — works on Vercel, Netlify, GitHub Pages, Cloudflare Pages with no configuration.
