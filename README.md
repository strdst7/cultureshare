# Ntsika Shembe Holdings — Website

**A South African IP origination holding company, rebuilt with a complete brand identity.**

Ntsika Shembe Holdings (Pty) Ltd is an IP origination holding company based in Vereeniging, Gauteng, South Africa. This repository contains the company's redesigned one-page website — a fully self-contained experience built around the brand idea **Originate · Engineer · Hold**.

> The original site (ns-holdings.co.za) was taken as content input and rebuilt with a new identity system: custom logo, palette, typography, voice, and a set of signature "wow" interactions. All external product links and unverifiable production claims were removed in a later pass per client direction.

---

## ✨ Signature experience

| Feature | What it does |
|---|---|
| **Brand intro** | ~2s cinematic opener — the gold diamond draws itself, the pillar rises, the wordmark types in. Shown once per session, skippable, `<noscript>`-safe. |
| **Audio-reactive hero** | A field of gold diamonds that **dances to the music** — driven by a live Web Audio analyser reading the track's low/mid/high bands. Pauses when off-screen. |
| **South African groove** | Generative amapiano-style track (112 BPM, log drums, shaker, pentatonic keys) synthesized live in the browser via the Web Audio API — royalty-free, offline, autoplays on landing where permitted. |
| **Scroll-driven story** | Apple-style pinned scroll walkthrough of Culture Share's four features (moderation → discovery → AI agent → CST economy), each demoed on a phone mockup. |
| **AI agent + CST demo** | Ask the in-platform agent about South African culture; watch answers type out and CST points credit to a live ledger. |
| **Interactive SA map** | Accurate nine-province map (Natural Earth data) — hover/click/pick provinces to see their languages, heritage, and music. |

## 🚀 Quick start

The site is a **single self-contained HTML file** — no build step, no dependencies, no external requests (fonts are embedded as subset variable WOFF2s, all art is inline SVG/canvas).

```bash
# just open it
open index.html

# or serve it (recommended for the sandboxed preview + full behavior)
python3 -m http.server 8080
# → http://localhost:8080
```

## 📁 Structure

```
ns-holdings/
├── index.html          ← the entire website (fonts, art, music, logic all embedded)
├── brand-identity.md   ← full brand system: concept, logo, palette, typography, voice, features
└── assets/
    ├── logo-dark.svg   ← lockup for dark backgrounds
    └── logo-light.svg  ← lockup for light/cream backgrounds
```

## 🎨 Brand at a glance

- **Concept — "The Pillar of Origin":** a diamond (the idea) with a rising pillar (engineered IP, held). Doubles as a custom "N".
- **Palette:** ink `#0B0906` · bone `#F3ECDC` · gold `#C89B3C` · ember `#C2692C`
- **Type:** Fraunces (editorial serif) + Manrope (modern sans), variable axes preserved after glyph subsetting
- **Voice:** proof-over-promise, first-person, grounded in South Africa

## ⚙️ Technical notes

- **Zero-dependency static site.** The full page ships at ~264 KB.
- **Performance:** fonts glyph-subset to the exact character set used (33% smaller); the reactive canvas pauses when off-screen; rAF-throttled scroll handlers.
- **Accessibility:** `:focus-visible` outlines, `aria-live` regions, `role="group"` on the dot rail, `color-scheme: dark`, reduced-motion support.
- **Honesty guardrail:** no live-site URLs or unverifiable "in production" claims remain; product demos are clearly labelled as illustrative.

## 📄 License

All rights reserved © 2026 Ntsika Shembe Holdings (Pty) Ltd. The brand assets (logo, identity, copy) are proprietary. The map geometry is derived from [Natural Earth](https://www.naturalearthdata.com/) (public domain) data.
