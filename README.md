# SHINYA — Website

> Bar à sushi gastronomique · Saint-Sauveur, Québec

## Overview

Single-page website for **SHINYA (深夜)**, an upscale Japanese sushi bar in Saint-Sauveur, Quebec. Built as a zero-dependency static HTML file.

**Live features:**
- Bilingual (FR/EN) with instant toggle — no page reload
- French as default language
- Fully responsive (mobile, tablet, desktop)
- Smooth scroll navigation with active section tracking
- Animated hero with scroll indicator
- Full menu with Cuisine / Drinks tab toggle
- Chef profiles
- Reservation form
- Location section with map placeholder
- Contact form
- Fade-in scroll animations via Intersection Observer

---

## File Structure

```
/
├── index.html       ← Entire site (HTML + CSS + JS)
├── vercel.json      ← Vercel deployment config
└── README.md
```

---

## Deploy to Vercel

### Option 1 — Vercel CLI

```bash
npm i -g vercel
vercel --prod
```

### Option 2 — GitHub + Vercel Dashboard

1. Push this repo to GitHub
2. Go to [vercel.com](https://vercel.com) → **Add New Project**
3. Import your GitHub repository
4. Framework Preset: **Other** (static site)
5. Root Directory: `/` (leave as default)
6. Click **Deploy**

Vercel will auto-detect `vercel.json` and serve `index.html`.

---

## Customization

All bilingual content lives in the JavaScript `content` object near the bottom of `index.html`:

```js
const content = {
  fr: { ... },
  en: { ... }
}
```

To update any text, find the relevant key and edit the French and English values.

### Key sections to personalize:
- **Address** — Search for `147, rue Principale` to update the real address
- **Phone / Email** — Search for `450) 123-4567` and `bonsoir@shinyasushi.ca`
- **Social links** — The `href="#"` on Instagram and Google Maps links
- **Google Maps** — Replace the CSS map placeholder with a real `<iframe>` embed

---

## Fonts

Loaded via Google Fonts CDN:
- **Playfair Display** — Headlines
- **DM Sans** — Body & UI

---

## License

© SHINYA · All rights reserved
