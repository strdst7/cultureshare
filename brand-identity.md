# Ntsika Shembe Holdings — Brand Identity System

A redesign of the company's web presence and visual identity, built around the founding idea: **the company originates ideas, engineers them into working products, and holds the IP it builds.** Every element of the identity traces back to that one idea.

---

## 1. Concept — "The Pillar of Origin"

The identity is built on a single geometric device: **a rotated square (diamond) with a rising pillar inside it.**

- The **diamond** is the emblem of origin — the seed, the concept, the starting point.
- The **pillar** is what the company *holds*: engineered IP, a working product, a standing structure.
- Together they read as *idea → built → held*, which is the company's exact operating model: **Originate · Engineer · Hold**.

The mark doubles as a custom "N" for Ntsika — the pillar rising through the diamond.

---

## 2. Logo

Two lockups are provided as SVG in `assets/`:

| File | Use |
|---|---|
| `logo-dark.svg` | For light/cream backgrounds (primary) |
| `logo-light.svg` | For dark/ink backgrounds (inverted) |

The website uses the mark alone in the nav (`mark.svg`, inline) and the full lockup in the footer.

**Clearance:** keep at least one diamond-width of space on all sides. **Minimum size:** 32 px for the mark; never crop the diamond.

---

## 3. Colour System

A South African evening palette: deep ink, warm cream, and 24-karat gold with a burnt-orange ember accent.

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

- Gold is used sparingly: only for the mark, section labels, numerals, and primary CTAs. Never flood a screen with it.
- Cream (`--bone`) is used as an *inverted* section background (the Culture Share section) to create a dramatic "day/night" rhythm in the page.
- Text on cream uses a deep warm brown (`#1B140B`), not pure black, to keep the palette warm.

---

## 4. Typography

| Role | Font | Weights |
|---|---|---|
| Display / headlines | **Fraunces** (variable serif) | 400–700, incl. italic |
| Body / UI | **Manrope** (geometric sans) | 400–800 |

- Fraunces' "soft" old-style serifs carry heritage and authority; its optical sizing keeps headlines elegant at every scale.
- Manrope is a modern, neutral sans that keeps the engineering side of the business crisp and current.
- Headlines lean on italic accents (`<em>` in gold) for editorial personality — a nod to the cultural-literary character of the brand.
- Both fonts are **embedded in the HTML file** as subset variable WOFF2s, so the site renders identically offline and in the sandboxed viewer with zero external requests.

---

## 5. Layout & Motifs

- **Diamond grid:** a subtle repeating diamond pattern is used as a texture behind hero and light sections (SVG data-URI, masked radially).
- **Ticker ribbon:** a slow gold marquee ("Originate · Engineer · Hold · IP Origination · …") separates hero from content — motion as brand voice.
- **Section numbering:** every section carries an editorial kicker — `01 — About NSH`, `02 — Flagship platform`, `03 — Capability`, `04 — Contact`.
- **Roman numerals** in the "How we work" process strip (I / II / III) reinforce the *Originate · Engineer · Hold* model.
- **Large ghost numerals** on service cards (`01`–`06`) with gold outline strokes echo the "holding" structure.
- **Dark → light → dark rhythm:** ink hero → ink about → **cream Culture Share** (daylight; the product is "live") → ink capability → ink contact. The single light section makes the flagship platform pop and symbolises the product being "out in the world."
- **South African groove (audio identity):** a generative amapiano-style background track — interlocking "log drums", shaker, hi-hat, deep bass, and a pentatonic keys melody at 112 BPM — is synthesised live in the browser with the Web Audio API. It tries to autoplay on landing; if the browser blocks autoplay, it starts on the first user gesture. A gold music toggle (bottom-right) lets visitors play/pause at any time and shows animated equaliser bars while playing. Because it is generated, not a file, it is royalty-free, plays offline, and works in any preview context.

### Signature interactions (wow factor)

- **Brand intro (once per session):** on first visit, a ~2s cinematic opener — the gold diamond draws itself stroke by stroke, the pillar rises, "Ntsika Shembe" types in letter by letter, then HOLDINGS and the tagline fade in, before the overlay lifts to reveal the site. Click anywhere to skip; it never replays within the same session; disabled entirely for reduced-motion users.
- **Audio-reactive hero:** a canvas field of ~90 floating gold diamonds fills the hero. When the South African groove plays, the diamonds surge, spin faster, brighten, and pulse on the beat (driven by a live Web Audio analyser reading the track's low/mid/high bands). When the music is off or blocked, they drift gently in ambient mode. Pauses when the tab is hidden; respects reduced motion.
- **In-page AI agent + CST demo:** the flagship Culture Share section ends with a working-feeling product demo. Visitors ask the agent anything about South African culture (via suggested chips or free text) and watch the answer type out — grounded in a keyword-matched demo knowledge base covering Zulu weddings, ulwaluko, mbaqanga, amapiano, moderation, discovery, and the CST economy. Every exchange credits CST to a live-animated ledger (with a "+N CST" toast and ledger feed), demonstrating the closed-loop points economy in action. Clearly labelled as an illustrative demo.
- **Interactive South Africa culture map:** a gold-line SVG map of South Africa's nine provinces (simplified from Natural Earth data) sits between Culture Share and Capability. Hover a province to preview its profile; click to pin; use the quick-picker chips to jump. The profile card shows each province's languages, traditions & heritage, and music indexed on Culture Share (e.g. Gauteng → amapiano & kwaito, KZN → maskandi & gqom, WC → ghoema & Cape Minstrels). Fully responsive: the map stacks above the card, and picker chips work on touch.
- **Scroll-driven story (Culture Share):** the flagship section is now an Apple-style pinned scroll narrative. As the visitor scrolls, the phone mockup stays pinned while four scenes take the stage in order — (01) AI moderation, (02) personalised discovery, (03) the in-platform AI agent, (04) the CST points economy. Each scene swaps the text AND the phone screen to demonstrate the feature (a moderation card on a feed, a "For You" personalisation screen, an in-phone agent chat, a CST wallet with live ledger). A vertical dot rail tracks progress and jumps between scenes; fully responsive (stacks on mobile), respects reduced motion, and pauses naturally as the user scrolls past.

---

## 6. Voice & Messaging

| Tone | Example |
|---|---|
| Direct, first-person-plural | "We originate ideas. We engineer them into living products." |
| Proof over promise | Proof comes from the working product and the build itself — not unverifiable "live" claims. All external product links and production-status assertions were removed as misleading. |
| Financial discipline | CST described as "not a cryptocurrency — a closed-loop digital incentive system." |
| Grounded origin | Vereeniging, Gauteng, South Africa — stated plainly in the hero meta. |

The wordmark tagline **"IP Origination & Technology"** now appears under the logo, giving the company an instantly readable elevator line.

---

## 7. What changed vs. the original site

| Aspect | Original | Redesign |
|---|---|---|
| First impression | Plain headline + small text | Hero statement + meta bar (founded, HQ, flagship, focus) + ticker |
| Identity | Text-only | Custom diamond/pillar mark, gold-on-ink palette, serif+sans type system |
| Structure | Single long column | Numbered editorial sections with kickers; day/night rhythm |
| Flagship product | 4 bullet cards | Scroll-driven story: 4 feature scenes with a phone mockup demonstrating each (moderation, discovery, AI agent, CST) |
| Capability | 6 text blocks | 6 service cards with icons, ghost numerals, hover motion |
| Contact | Plain email link | Big gold mail CTA + chip list of inquiry types |
| Technical | External assets | Fully self-contained single file (embedded fonts, inline SVG) — works offline and in any preview |

---

## 8. Files

```
ns-holdings/
├── index.html              ← the redesigned one-page website (fully self-contained)
├── brand-identity.md       ← this document
└── assets/
    ├── logo-dark.svg       ← lockup for dark backgrounds
    └── logo-light.svg      ← lockup for light/cream backgrounds
```

## 9. Performance & polish (final pass)

- **Subset variable fonts:** both fonts are embedded as *glyph-subset* variable WOFF2s — cut from 174 KB to 117 KB of raw font data (~33% smaller) with the full weight axes intact. The single HTML file ships at ~264 KB with zero external requests.
- **Canvas pauses off-screen:** the audio-reactive hero field renders only while the hero is in view (IntersectionObserver + `rootMargin`), and pauses when the tab is hidden — near-zero background cost.
- **Accessibility:** `:focus-visible` gold outlines on all interactive elements; `-webkit-tap-highlight-color` disabled; `color-scheme: dark` matches native controls; the map is no longer `aria-hidden` (it's interactive); story dots use a proper `role="group"`; `aria-live` on the CST balance and chat log.
- **Robustness:** the brand intro is hidden by a `<noscript>` guard (no JS → no full-screen overlay trap); all sessionStorage access is try/catch-safe for sandboxed contexts.
- **Details:** `theme-color` and Open Graph tags for mobile chrome & sharing; `text-wrap: balance` on headings; themed native scrollbars; footer tagline refined to "Originate · Engineer · Hold".
- **Verified:** 6 script blocks pass syntax, HTML structure valid, and a jsdom smoke test exercises the intro, music engine, agent demo (typing + CST award), map hover/click/picker, and story scenes with zero runtime errors.
