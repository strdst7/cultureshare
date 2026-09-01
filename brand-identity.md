# Culture Share — Brand Identity System

Culture Share is a South African cultural technology platform: **social connection, a peer-reviewed cultural knowledge base, and applied AI**, mapped across the country's nine provinces. The identity is warm, editorial, and grounded — deep ink, cream, and gold.

---

## 1. Concept — "Connect · Archive · Share"

The brand is built on three verbs that describe the platform's whole loop:

- **Connect** — people to culture, contributors to audiences.
- **Archive** — a peer-reviewed cultural knowledge base, indexed by decade and topic.
- **Share** — the in-platform AI agent, discovery feed, and the CST points economy that keep the loop alive.

The visual identity keeps the founding emblem language: a diamond (the seed idea) with a rising pillar inside it — *idea → built → shared*.

---

## 2. Logo

| Asset | Use |
|---|---|
| `assets/brand/logo.png` | The gold **NS monogram** (transparent, 800×917) — used on the alternate page header/footer, hero, governance, board, and intro. |
| `assets/brand/nsh-logo.svg` / `nsh-logo.png` | Full lockup (mark + wordmark) with Fraunces/Manrope type. |
| `assets/brand/nsh-logo-light.svg` / `.png` | Bone-colored wordmark for dark surfaces. |
| `assets/brand/nsh-logo-mark.svg` / `.png` | Mark-only icon. |

**Clearance:** keep at least one mark-width of space on all sides. **Minimum size:** 32 px for the mark.

---

## 3. Colour System

A South African evening palette: deep ink, warm cream, and gold with a burnt-orange ember accent.

| Token | Hex | Role |
|---|---|---|
| `--ink` | `#0B0906` | Primary background |
| `--ink2` | `#13100A` | Raised dark surface |
| `--card` | `#1B150E` | Card surface |
| `--bone` | `#F3ECDC` | Primary text on dark |
| `--bone2` | `#E9DFC8` | Secondary text |
| `--sand` | `#C5B493` | Muted text |
| `--gold` | `#C89B3C` | Brand accent, CTAs |
| `--gold2` | `#E5C276` | Highlighted accent |
| `--ember` | `#C2692C` | Secondary accent, gradients |

**Usage rules**

- Gold is used sparingly: mark, section labels, numerals, primary CTAs.
- Cream (`--bone`) is the inverted section background (the Culture Share section) for a "day/night" rhythm.
- Text on cream uses a deep warm brown, not pure black, to keep the palette warm.

---

## 4. Typography

| Role | Font | Weights |
|---|---|---|
| Display / headlines | **Fraunces** (variable serif) | 400–700, incl. italic |
| Body / UI | **Manrope** (geometric sans) | 400–800 |

- Fraunces' "soft" old-style serifs carry heritage and authority; optical sizing keeps headlines elegant at every scale.
- Manrope keeps the engineering side crisp and current.
- Headlines lean on italic gold accents for editorial personality.
- Both fonts are **embedded in the HTML file** as subset variable WOFF2s — zero external requests.

---

## 5. Layout & Motifs

- **Diamond grid:** a subtle repeating diamond pattern behind hero and light sections (SVG data-URI).
- **Ticker ribbon:** a slow gold marquee ("Connect · Archive · Share · Applied AI · Culture Share · …").
- **Section numbering:** editorial kickers — `01 — Flagship platform`, `02 — Capability`, `03 — Contact`.
- **Day/night rhythm:** ink hero → cream Culture Share (the product, "out in the world") → ink map/capability → ink contact.
- **Culture Share film:** a full-width autoplay/muted/loop video panel at the foot of the flagship section.

### Signature interactions

- **Brand intro (once per session):** logo draws in, "Culture Share" types out, tagline fades in, overlay lifts. Click to skip; disabled for reduced-motion users.
- **3D hero gem:** a WebGL gold diamond above the hero headline.
- **In-page AI agent + CST demo:** ask about South African culture, watch answers type out, CST credits the ledger. Clearly labelled as an illustrative demo.
- **Interactive South Africa map:** gold-line SVG of the nine provinces (Natural Earth data) — hover/click/pick to see languages, heritage, and music.
- **Scroll-driven story (Culture Share):** pinned phone mockup with four feature scenes (AI moderation → discovery → AI agent → CST economy), dot rail, responsive, reduced-motion-safe.
- **Board mode:** full-screen 6-slide presentation with keyboard nav.

---

## 6. Voice & Messaging

| Tone | Example |
|---|---|
| Direct, first-person-plural | "Social connection. A living archive, and applied AI." |
| Proof over promise | The working platform and the build itself — no unverifiable "live" claims. |
| Financial discipline | CST described as "not a cryptocurrency — a closed-loop digital incentive system." |
| Grounded origin | South Africa — stated plainly in the hero meta. |

Contact: **hello@cultureshare.co.za**

---

## 7. Files

```
├── index.html              ← main site (self-contained)
├── index-alt.html          ← alternate logo version
├── brand-identity.md       ← this document
├── README.md
├── robots.txt / sitemap.xml / site.webmanifest
├── .github/workflows/deploy.yml   ← auto-deploy to Pages on push
└── assets/
    ├── brand/              ← logo assets
    ├── video/culture-share.mp4
    └── favicon/            ← favicon.svg (+ dark variant) + PNG set
```

## 8. Technical notes

- **Zero-dependency static site** — fonts embedded, inline art, no external requests.
- **Accessibility:** `:focus-visible` outlines, `aria-live`, `color-scheme: dark`, reduced-motion support.
- **Security:** CSP meta (media-src 'self' for the video), Permissions-Policy, frame-bust guard.
- **CI/CD:** GitHub Actions stamps build version, validates the bundle (placeholders, fonts, no external product links), and deploys both pages to GitHub Pages.
