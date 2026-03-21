# Letterbox Drops — Website

Website for [Letterbox Drops](https://letterboxdrops.uk), a door-to-door leaflet distribution company based in Oxford, covering the whole of Oxfordshire.

---

## File Structure

```
/
├── index.html          # Main homepage
├── oxford.html         # Location page — Oxford
├── witney.html         # Location page — Witney
├── abingdon.html       # Location page — Abingdon
├── bicester.html       # Location page — Bicester
├── logo.png            # Logo (not included in repo)
├── og-image.png        # Open Graph image for social sharing (not included in repo)
├── sitemap.xml         # XML sitemap for search engines
├── robots.txt          # Crawler instructions
├── llms.txt            # AI crawler guidance (llmstxt.org standard)
└── README.md           # This file
```

---

## Tech Stack

- Plain HTML, CSS — no frameworks, no build tools, no dependencies
- Inline CSS per page for maximum performance
- Google Fonts (Ubuntu 400/700) loaded non-render-blocking via `media="print"` swap
- Forms handled by [Formspree](https://formspree.io)
- Analytics via Google Analytics 4 (`G-FNEEML2NBJ`)

---

## Pages

| Page | URL | Purpose |
|------|-----|---------|
| Homepage | `/` | Main marketing page covering all of Oxfordshire |
| Oxford | `/oxford` | Local landing page for Oxford |
| Witney | `/witney` | Local landing page for Witney |
| Abingdon | `/abingdon` | Local landing page for Abingdon |
| Bicester | `/bicester` | Local landing page for Bicester |

---

## SEO

Each page includes:
- Unique `<title>` and `<meta name="description">`
- `<link rel="canonical">`
- Open Graph tags (`og:title`, `og:description`, `og:image`, `og:locale`)
- Twitter Card tags
- `<meta name="robots" content="index, follow">`
- JSON-LD structured data using `@graph` format with `LocalBusiness`, `BreadcrumbList`, and `WebPage` schema
- Location pages include `OfferCatalog` with pricing schema (£60/thousand)

---

## Forms

Both forms (main site contact form and "Work for us" application) post to Formspree endpoints:
- Contact/quote form: `https://formspree.io/f/xreybgja`
- Hidden email capture: `https://formspree.io/f/myknzyor`

Each location page form includes a hidden `location` field so enquiries are tagged by town.

---

## Deployment

The site is static HTML — deploy to any host that serves static files. Recommended: [Cloudflare Pages](https://pages.cloudflare.com/) or [Netlify](https://netlify.com).

Both handle gzip/Brotli compression and cache headers automatically, which completes the PageSpeed optimisations applied in the code.

### Cloudflare Pages
1. Push this repo to GitHub
2. Connect repo to Cloudflare Pages
3. No build command needed — set output directory to `/`

### Netlify
1. Push this repo to GitHub
2. Connect repo in Netlify dashboard
3. Build command: leave blank. Publish directory: `/`

---

## Assets Needed

Two image files are referenced but not included in the repo:

- **`logo.png`** — company logo, displayed at 56px height in the nav
- **`og-image.png`** — Open Graph image for social sharing, should be 1200×630px

Add these to the root of the repo before deploying.

---

## Contact

**Letterbox Drops**
Email: hello@letterboxdrops.uk
Phone: 01865 965193
Based in Oxford, Oxfordshire
