# Oxford Leaflet Delivery — Landing Page

A static, SEO-optimised landing page for Oxford Leaflet Delivery, a door drop leaflet printing and distribution service based in Oxford, UK. Built for deployment on Cloudflare Pages.

---

## Files

| File | Purpose |
|---|---|
| `index.html` | Main landing page — single self-contained file |
| `logo.png` | Your logo — place in the same directory as index.html |
| `sitemap.xml` | XML sitemap for search engine indexing |
| `robots.txt` | Crawler directives including AI bot blocking |
| `llms.txt` | Structured content summary for LLM discoverability |
| `README.md` | This file |

---

## Deploying to Cloudflare Pages

1. Log in to the [Cloudflare Dashboard](https://dash.cloudflare.com)
2. Go to **Workers & Pages → Create → Pages**
3. Choose **Upload assets** (direct upload — no Git required)
4. Upload all files in this folder
5. Set your custom domain under **Custom Domains** once deployed

That's it. No build step, no framework, no configuration needed.

---

## Before Going Live

Update the following placeholders in `index.html` and `sitemap.xml`:

- **Domain** — replace all instances of `oxfordleafletdelivery.co.uk` with your actual domain
- **Phone number** — add your number to the nav if desired (currently text-only CTA)
- **Form action** — the quote form uses `data-netlify="true"` by default. For Cloudflare Pages, replace with a [Cloudflare Worker](https://workers.cloudflare.com/) endpoint or a third-party service like [Formspree](https://formspree.io)
- **Logo** — place your `logo.png` in the root directory alongside `index.html`
- **Sitemap dates** — update `<lastmod>` in `sitemap.xml` whenever you make content changes

---

## Form Handling Options

The quote form needs a backend to process submissions. Recommended options:

**Formspree (easiest)**
1. Sign up at [formspree.io](https://formspree.io)
2. Create a new form and copy your endpoint URL
3. In `index.html`, replace `action="/thanks"` with your Formspree URL and remove `data-netlify="true"`

**Cloudflare Workers**
1. Write a Worker to handle POST requests and forward to email
2. Replace the form `action` with your Worker URL

---

## SEO Notes

- Title, meta description, and Open Graph tags are set for Oxford/Oxfordshire leaflet delivery keywords
- LocalBusiness schema.org structured data is included in the `<head>`
- Canonical URL is set — update to match your live domain
- Google Analytics (GA4) tag `G-FNEEML2NBJ` is included in the `<head>`
- `sitemap.xml` should be submitted to [Google Search Console](https://search.google.com/search-console) once live

---

## Colours

| Token | Hex | Usage |
|---|---|---|
| Orange accent | `#f99229` | Labels, icons, highlights, stats |
| Navy | `#384b70` | Buttons, hero card, dark sections |
| Navy dark | `#293859` | Footer, hover states |

## Typography

**Ubuntu** — used throughout (body, headings, UI). Loaded from Google Fonts.

---

## Built by

Designed and developed with ♥ by [Letterbox Drops](https://www.facebook.com/letterboxdropsuk/)
