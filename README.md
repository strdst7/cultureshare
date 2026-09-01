# Culture Share — Website

**A South African cultural technology platform — social connection, a peer-reviewed cultural knowledge base, and applied AI.**

Culture Share is the brand. This repository contains the platform's one-page website — a fully self-contained experience built on the **Connect · Archive · Share** idea, with a warm ink-and-gold identity.

---

## ✨ Signature experience

| Feature | What it does |
|---|---|
| **Brand intro** | ~2s cinematic opener — the logo draws in, "Culture Share" types out, the tagline fades in. Shown once per session, skippable, `<noscript>`-safe. |
| **3D hero gem** | A rotating gold diamond rendered in WebGL above the hero headline. |
| **Culture Share video** | A full-width film panel (autoplay, muted, loop) embedded under the Culture Share section. |
| **Scroll-driven story** | Pinned scroll walkthrough of Culture Share's four features (moderation → discovery → AI agent → CST economy), each demoed on a phone mockup. |
| **AI agent + CST demo** | Ask the in-platform agent about South African culture; watch answers type out and CST points credit to a live ledger. |
| **Interactive SA map** | Accurate nine-province map (Natural Earth data) — hover/click/pick provinces to see their languages, heritage, and music. |
| **Board mode** | A full-screen presentation overlay (6 slides) with keyboard navigation. |

## 📄 Pages

- `index.html` — main page
- `index-alt.html` — alternate version using the gold NS monogram logo (horizontal header lockup)

Both deploy together via GitHub Actions to GitHub Pages.

## 🚀 Quick start

The site is a **single self-contained HTML file** — no build step, no dependencies (fonts are embedded as subset variable WOFF2s, all art is inline SVG/canvas).

```bash
# just open it
open index.html

# or serve it (recommended for full behavior)
python3 -m http.server 8080
# → http://localhost:8080
```

## 📁 Structure

```
├── index.html              ← main site (fonts, art, logic all embedded)
├── index-alt.html          ← alternate logo version
├── brand-identity.md       ← brand system: concept, logo, palette, typography, voice
├── README.md               ← this file
├── robots.txt / sitemap.xml / site.webmanifest
├── .github/workflows/deploy.yml   ← auto-build, validate & deploy to Pages on push
└── assets/
    ├── brand/              ← logo assets (NS monogram lockups + mark)
    ├── video/culture-share.mp4   ← the Culture Share film
    └── favicon/            ← favicon.svg (+ dark variant) + PNG set
```

## 🎨 Brand at a glance

- **Logo:** gold NS monogram (derived from NS_LOGO_NO_BG.pdf) on the alt page; gold diamond mark on the main page — both in the warm gold `#C89B3C`.
- **Palette:** ink `#0B0906` · bone `#F3ECDC` · gold `#C89B3C` · ember `#C2692C`
- **Type:** Fraunces (editorial serif) + Manrope (modern sans), variable axes preserved after glyph subsetting
- **Voice:** proof-over-promise, first-person, grounded in South Africa

## ⚙️ Technical notes

- **Zero-dependency static site.**
- **Performance:** fonts glyph-subset to the exact character set used; rAF-throttled scroll handlers; `content-visibility` on major sections.
- **Accessibility:** `:focus-visible` outlines, `aria-live` regions, `color-scheme: dark`, reduced-motion support.
- **Security layer:** CSP meta tag (with `media-src 'self'` for the video), Permissions-Policy, frame-bust guard.

## 📄 License

All rights reserved © 2026 Culture Share. The brand assets (logo, identity, copy) are proprietary. The map geometry is derived from [Natural Earth](https://www.naturalearthdata.com/) (public domain) data.
