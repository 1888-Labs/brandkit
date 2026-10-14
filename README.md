# 1888 Labs — Brand Kit

**Building open infrastructure for verifiable, distributed, and intelligent systems.**
Sign-off: *Research. Build. Verify.*

---

## 1. The logo

**The Ring Monogram.** A square tile in a 2×2 grid: a `1` and three `8`s. Each `8` is two linked rings, so the mark reads as chains, nodes and links between machines. The last ring is in Signal orange. It stands for the one piece you check yourself: *verify, don't assume.*

| Asset | Use it for |
|---|---|
| `mark-primary` (Ink tile) | Default. Avatars, app icons, light backgrounds |
| `mark-reverse` (Paper tile) | Dark backgrounds |
| `mark-accent` (Signal tile) | Stickers, merch, special moments. Use it sparingly |
| `mark-black` / `mark-white` | One-colour print, embossing, fax-grade reproduction |
| `symbol-*` (no tile) | When the mark sits inside its own container, e.g. a circle avatar crop |
| `mark-small-16px` | Only for 16 px favicons. The full monogram doesn't hold up at that size |
| `logo-horizontal-*` | Default full logo: website header, README, docs |
| `logo-stacked-*` | Square or centred spaces: title slides, posters |
| `wordmark-*` | When the mark already appears nearby, or space is very wide and short |

Suffixes: `on-light` = Ink text with the Ink tile · `on-dark` = Paper text with the Paper tile · `black` / `white` = one-colour.

### Clear space

Keep empty space around the logo equal to **¼ of the tile's height** on every side. On a 120 px tile, that's 30 px.

### Minimum size

- Full monogram: **24 px** on screen, **8 mm** in print.
- Below 24 px, switch to `mark-small-16px` (a single 8).
- Horizontal logo: **120 px** wide minimum.

### Don't

- Recolour the rings, or move the orange ring to another position.
- Put Signal orange on more than one ring.
- Stretch, rotate, outline or add shadows or gradients to the logo.
- Retype the wordmark. Always use the supplied files, where the text is already converted to outlines.
- Put the Ink tile on a busy photo without a solid backing.

---

## 2. Colour

| Name | Hex | RGB | Role |
|---|---|---|---|
| **Ink** | `#0F1115` | 15 17 21 | Primary dark, text, tiles |
| **Paper** | `#F3F1EA` | 243 241 234 | Primary light, backgrounds |
| **Signal** | `#FF5B22` | 255 91 34 | Accent: the verified ring, highlights, links on dark |
| **Graphite** | `#4A4D55` | 74 77 85 | Secondary text on Paper |

Proportion: roughly 60% Paper or Ink, 35% the other one, and **under 5% Signal**.

Contrast (WCAG):

- Ink on Paper: **16.7 : 1**. Use it for all text.
- Graphite on Paper: **7.5 : 1**. Fine for body text.
- Signal on Ink: **6.1 : 1**. Fine for text and links on dark.
- Signal on Paper: **2.7 : 1**. Graphics, icons and large display (24 px+) only. **Never body text.**

Developers can use `colors/tokens.css` and `colors/palette.json`.

---

## 3. Typography

| Role | Typeface | Weights | Notes |
|---|---|---|---|
| Display / wordmark | **Space Grotesk** | 700, 500 | Headlines, the `1888` wordmark. Tracking −2% |
| Labels / code | **JetBrains Mono** | 500, 700 | `LABS`, eyebrow labels, code, metadata. Uppercase labels are tracked +12–40% |
| Body | Space Grotesk 400/500 or system UI | — | 16–18 px, line height 1.5 |

Both fonts are free and open source (SIL Open Font License) on Google Fonts:

```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@500;700&family=Space+Grotesk:wght@400;500;700&display=swap">
```

---

## 4. Voice

Plain, technical, precise. We write like an engineer's README: what it is, what it does, how to check it.

- Say *"verifiable"* and show the proof. Avoid hype words: *revolutionary, next-gen, Web3-native*.
- Short declarative sentences. Projects get one-line descriptions, like MerkleForge's: *"A Rust framework for authenticated data structures and cryptographic proof verification."*
- Sign-off: **Research. Build. Verify.**

---

## 5. Files in this kit

```
svg/        master vector files (text converted to outlines, no font needed)
png/        each mark at 64–1024 px; each logo at @1x, @2x, @4x (transparent background)
favicon/    favicon.ico (16/32/48), favicon.svg, apple-touch-icon, android icons,
            site.webmanifest, head-snippet.html
social/     og-image 1200×630, GitHub social preview 1280×640,
            X header 1500×500, LinkedIn banner 1584×396, avatar 800×800
colors/     palette.json, tokens.css
figma/      full kit sheet for Figma, tokens.json, sheet preview
```

### Website favicon setup

Copy everything in `favicon/` to your site's root. Then paste `favicon/head-snippet.html` into your `<head>`.

### GitHub org

- Avatar: `social/avatar-800.png`
- Repository social preview: `social/github-social-preview-1280x640.png`
- README header: `svg/logo-horizontal-on-light.svg`. For dark-mode READMEs, use a `<picture>` element with the `on-dark` version as the alternate.

---

## 6. Using the kit in Figma

`figma/` contains:

- **`1888-labs-brand-kit-figma.svg`**: the whole kit on one sheet. Drag it onto a Figma canvas, or use *File → Import*. You get editable vectors and named layers: `Mark/…`, `Logo/…`, `Color/…`, `Type/…`.
  1. Select everything and press **Frame selection** (⌥⌘G / Ctrl+Alt+G).
  2. Right-click each mark or logo → **Create component**. Then publish the file as a team library, so every designer pulls the same logos.
- **`tokens.json`**: colours, fonts and radii in the standard W3C design-token format. Load it with Figma's variables import, or with a plugin such as Tokens Studio, to create **Ink / Paper / Signal / Graphite** as colour variables.
- **Fonts:** install Space Grotesk and JetBrains Mono first (free on Google Fonts), so the type-specimen text layers stay editable.
- `brand-kit-sheet-preview.png`: a quick preview of the sheet.
