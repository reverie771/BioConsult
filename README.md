# Oprea-Barac — V2 (Velican structure)

Static site for Oprea-Barac. **V2 mirrors the structure of velican-expertaudit.ro** while keeping the V1 typography (Fraunces + Hanken Grotesk), color palette, and components that worked.

## Stack

Plain HTML + CSS, no build step. Type loaded from Google Fonts.

## File layout

```
index.html         — Pagina principală
despre.html        — Despre Noi
audit.html         — Audit Financiar
expertiza.html     — Expertiză Contabilă
insolventa.html    — Insolvență
evaluari.html      — Evaluări
contact.html       — Contact
interior.css       — Stiluri partajate (toate paginile interioare)
```

## What's new vs V1

1. **Nav**: added a "Home" link first, plus a hover/focus dropdown under "Audit Financiar" listing the yearly Transparency Reports (currently placeholder `#` links — see "TODO" below).
2. **Home page restructured** to mirror Velican:
   - **Hero**: 4 photographic service cards (Audit · Expertiză · Insolvență · Evaluări) instead of the V1 editorial hero.
   - **Contact info trio** (Email · Telefon · Adresă) under the about block.
   - **3 info blocks** with photos: "Dorești un audit?", "Informații financiare" (links to mfinante.gov.ro), "Portofoliu clienți".
3. **Kept from V1**: about section, stats strip (22+ ani, 4 profesii, 160+ clienți, 540+ misiuni), Parteneri grid, Contact CTA section, footer.

## TODO before going live

### Placeholder photographs
All photos on the home page currently load from `picsum.photos` (random placeholder service). Search the file `index.html` for the string `picsum.photos` — there are 7 occurrences:

- 4 in the hero service cards (vertical 3:4 aspect)
- 3 in the info blocks (horizontal 4:3 aspect)

Replace each URL with your own image, either a relative path (`images/audit.jpg`) or a CDN URL. Cards keep their layout regardless of image dimensions, but matching the suggested aspect ratio looks best.

### Transparency Report PDFs
The dropdown under "Audit Financiar" lists six reports (2020–2025) with `href="#"` and a "PDF" flag. Once the PDFs exist:

1. Drop the files into a folder (e.g., `pdfs/`).
2. In each HTML file, replace `href="#"` for each year with the real path, e.g. `href="pdfs/raport-transparenta-2024.pdf"`.
3. Optionally remove `<span class="pdf-flag">PDF</span>` from rows whose PDF is now real — it's just a visual reminder that it's missing.

Seven files need this update: `index.html` plus all six interior pages.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy

Static — works on Vercel, Netlify, GitHub Pages, Cloudflare Pages with no configuration.
