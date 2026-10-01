---
version: 1.0.0
name: Substrate
description: Dark-field laboratory identity and publishing design system for Substrate Labs. Every page is a specimen slide on a black microscope field — grey is structure, red is stimulus, green is response. There is no light mode.
colors:
  primary: "#000000"
  white: "#FFFFFF"
  grey: "#8A8A8A"
  blood-red: "#8B0000"
  bio-green: "#39FF88"
  grey-display: "#A3A3A3"
  blood-red-display: "#B51F2E"
  bio-green-display: "#39D353"
  rule: "rgba(255, 255, 255, 0.14)"
  hairline-subtle: "rgba(255, 255, 255, 0.08)"
  hairline-hover: "rgba(255, 255, 255, 0.18)"
  tissue-far: "rgba(163, 163, 163, 0.16)"
  tissue-mid: "rgba(163, 163, 163, 0.38)"
  tissue-56: "rgba(163, 163, 163, 0.56)"
  tissue-near: "rgba(163, 163, 163, 0.72)"
  soma-membrane: "#161616"
  soma-nucleus-rest: "#5E5E5E"
  soma-label-ground: "#0A0A0A"
typography:
  display-specimen:
    fontFamily: Geist Pixel Square
    fontSize: clamp(2.8rem, 9.6vw, 9.4rem)
    fontWeight: 400
    lineHeight: 0.88
    letterSpacing: -0.02em
  body-md:
    fontFamily: Relative Sans
    fontSize: 0.875rem
    fontWeight: 400
    lineHeight: 1.5
    letterSpacing: -0.015em
  body-article:
    fontFamily: Relative Sans
    fontSize: clamp(1.02rem, 1.2vw, 1.12rem)
    fontWeight: 400
    lineHeight: 1.8
    letterSpacing: -0.01em
  label-caps:
    fontFamily: Relative Mono
    fontSize: 0.6875rem
    fontWeight: 500
    lineHeight: 1.45
    letterSpacing: 0.22em
containers:
  text: 680px
  media: 1140px
  wide: 1280px
  page: 1440px
stipple:
  pitch-field: 8px
  pitch-panel: 7px
  dot-radius-steps: [0.20, 0.27, 0.33, 0.39, 0.44]
  dot-colors:
    - "{colors.tissue-far}"
    - "{colors.tissue-mid}"
    - "{colors.tissue-56}"
    - "{colors.tissue-near}"
    - "rgba(255, 255, 255, 0.86)"
  dither-cell: 2px
  meter-step: 4px
  meter-height: 16px
  meter-max-width: 240px
  tree-glyph: "└"
  tree-indent: 2ch
assets:
  logo:
    src: "/soma/soma-mark-outline.svg"
    repo: "assets/soma/soma-mark-outline.svg"
    cdn: "https://assets.substrates.in/brand-assets/identity/soma-mark-outline.svg"
    viewBox: "-120 -120 240 240"
    format: "svg"
  logo-filled:
    src: "/soma/soma-idle.svg"
    repo: "assets/soma/soma-idle.svg"
    cdn: "https://assets.substrates.in/brand-assets/identity/soma-idle.svg"
    viewBox: "-120 -120 240 240"
  logo-legacy:
    src: "/substrate-logo.png"
    url: "https://substrates.in/substrate-logo.png"
    width: 960
    height: 880
    status: "retired from new work"
  mascot:
    name: Soma
    repo: "assets/soma/"
    cdn: "https://assets.substrates.in/brand-assets/identity/"
    file-pattern: "soma-{state}.svg | soma-{state}-compact.svg"
    states: [idle, hello, happy, listening, reading, thinking, unsure, surprised, sorry, recording, carrying, done, sleeping]
    full-viewBox: "-120 -120 240 240"
    compact-viewBox: "-80 -80 160 160"
  og-image:
    src: "/substrate-og-image.png"
    url: "https://substrates.in/substrate-og-image.png"
    width: 4800
    height: 2520
  favicon:
    src: "/icon.png"
    apple: "/apple-icon.png"
fonts:
  relative-sans:
    local: "/fonts/The-Relative-Sans-Variable.ttf"
    cdn: "https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf"
    format: "truetype"
    weights: "100 900"
  relative-mono:
    local: "/fonts/The-Relative-Mono-Variable.ttf"
    cdn: "https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf"
    format: "truetype"
    weights: "100 900"
  geist-pixel-square:
    local: "/fonts/GeistPixel-Square.woff2"
    cdn: "https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2"
    format: "woff2"
    weights: "400 900"
rounded:
  sm: 0px
  md: 2px
  pill: 9999px
spacing:
  xs: 8px
  sm: 16px
  md: 24px
  lg: 40px
  xl: 56px
  xxl: 80px
components:
  slide:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.grey-display}"
  specimen-panel:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.grey-display}"
    rounded: "{rounded.sm}"
    padding: 24px
  brand-mark:
    src: "{assets.logo.src}"
    height: 32px
  soma:
    membrane: "{colors.soma-membrane}"
    membraneStroke: "rgba(255, 255, 255, 0.85)"
    dendrites: "rgba(255, 255, 255, 0.45)"
    eyes: "{colors.white}"
    pupils: "{colors.primary}"
    nucleus: "{colors.soma-nucleus-rest}"
    nucleus-done: "{colors.bio-green-display}"
    signal-recording: "{colors.blood-red-display}"
  stipple-meter:
    track: "{colors.tissue-mid}"
    fill: "{colors.white}"
    typography: "{typography.label-caps}"
    rounded: "{rounded.sm}"
  tree-index:
    glyphColor: "{colors.tissue-mid}"
    textColor: "{colors.grey-display}"
    textColorCurrent: "{colors.white}"
    fontFamily: Relative Mono
    fontSize: 14px
  key-hint:
    fontFamily: Relative Mono
    fontSize: 11px
    letterSpacing: 0.18em
    textColor: "{colors.tissue-near}"
  display-headline:
    typography: "{typography.display-specimen}"
    textColor: "{colors.white}"
  body-copy:
    typography: "{typography.body-md}"
    textColor: "{colors.grey-display}"
  meta-label:
    typography: "{typography.label-caps}"
    textColor: "{colors.grey-display}"
  meta-label-live:
    typography: "{typography.label-caps}"
    textColor: "{colors.white}"
  link-quiet:
    typography: "{typography.label-caps}"
    textColor: "{colors.grey-display}"
  link-quiet-hover:
    typography: "{typography.label-caps}"
    textColor: "{colors.white}"
  signal-action:
    typography: "{typography.label-caps}"
    backgroundColor: "{colors.blood-red}"
    textColor: "{colors.white}"
    rounded: "{rounded.sm}"
  signal-action-hover:
    typography: "{typography.label-caps}"
    backgroundColor: "{colors.blood-red-display}"
    textColor: "{colors.white}"
    rounded: "{rounded.sm}"
  home-pill:
    backgroundColor: "rgba(0, 0, 0, 0.76)"
    borderColor: "{colors.blood-red-display}"
    textColor: "#d4d4d4"
    textColorHover: "{colors.white}"
    rounded: "{rounded.pill}"
    backdropBlur: "12px"
  synapse-indicator:
    backgroundColor: "{colors.bio-green}"
    textColor: "{colors.primary}"
    rounded: "{rounded.pill}"
    size: 6px
  synapse-indicator-active:
    backgroundColor: "{colors.bio-green-display}"
    textColor: "{colors.primary}"
    rounded: "{rounded.pill}"
    size: 6px
  selection:
    backgroundColor: "{colors.blood-red-display}"
    textColor: "{colors.white}"
  editorial-quote:
    borderLeftColor: "{colors.blood-red-display}"
    borderLeftWidth: 2px
    textColor: "{colors.white}"
  code-figure:
    backgroundColor: "{colors.primary}"
    borderColor: "{colors.rule}"
    rounded: "{rounded.md}"
---

## Overview

Substrate Labs is not browsed. It is **observed**. The screen is the dark-field
of a microscope, every page is a specimen slide laid on the stage, and the
visitor is the instrument. The interface never explains this metaphor — it
simply behaves like it.

The system is built from three materials only:

- **The void.** Pure black (`#000000`), edge to edge. It is not a dark theme;
  it is the absence of a lamp. Light mode does not exist, is not hidden behind a
  toggle, and will never be planned. Content floats in the field the way tissue
  floats in the viewing circle — anchored by hairlines, never by boxes.
- **The drawing.** Grey structure: mono labels, reticle coordinates, metadata,
  subtle separation rules, and the dim linework of the specimen itself. Grey is
  how the lab takes notes.
- **The signal.** Exactly two colors that carry meaning. **Blood red is
  stimulus** — selection, focus, alarm, active states, the action potential
  firing. **Bio green is response** — a synapse received, life confirmed, the
  organism answering back. Nothing in this lab is red or green for decoration.

Motion follows one doctrine: **the DOM is still; life happens in the canvas.**
The specimen (interactive neural network, journey preparation, or signal wave)
carries all animation — wandering, firing, glowing. Chrome never twinkles, never
pulses, never decorates itself with CSS keyframes. Quiet pages are dormant, not
dead.

---

## Colors

Every functional color exists in two states: its **vial value** — the hex on
the label of the bottle in the stock room — and its **observed value**
(`-display` tokens) — what the compound actually looks like under the
instrument, on black. UI rendered on the black field uses the observed twins;
artwork printed on white (paper, physical stationery, packaging) uses the vial
values directly.

| Token | Hex | State | Role |
| --- | --- | --- | --- |
| `primary` | `#000000` | — | The ground. Background of everything, forever. |
| `white` | `#FFFFFF` | — | Full-strength signal. Display headlines, live labels, nuclei, active links. |
| `grey` | `#8A8A8A` | vial | Brand grey. Stock formulation; structural marks on white media. |
| `blood-red` | `#8B0000` | vial | Stimulus at rest. Solid fills on white; pressed states. |
| `bio-green` | `#39FF88` | vial | Response at full fluorescence. |
| `grey-display` | `#A3A3A3` | observed | Grey as rendered on black — body copy, metadata, quiet links. |
| `blood-red-display` | `#B51F2E` | observed | Red as rendered on black — selection, focus rings, underlines, alerts. |
| `bio-green-display` | `#39D353` | observed | Green as rendered on black — glows, live states, success indicators. |

### Soma Neutrals

Three greys exist only inside the Soma mascot artwork. They are not new hues and
they are never used for chrome, text, or backgrounds.

| Token | Hex | Role |
| --- | --- | --- |
| `soma-membrane` | `#161616` | Soma's body fill, so the cell reads as a solid object on the black field. |
| `soma-nucleus-rest` | `#5E5E5E` | Soma's nucleus when nothing is happening. |
| `soma-label-ground` | `#0A0A0A` | The ground of a tag or page Soma is holding. |

### Hairlines and Rules

Separation is achieved by optical density, hairlines, and void:

- `var(--article-rule)`: `rgba(255, 255, 255, 0.14)` — Primary structural rule
  for section headings, article breaks, table rows, and footer borders.
- `rgba(255, 255, 255, 0.08)` — Subtle resting hairline for canvases, panels,
  and secondary controls.
- `rgba(255, 255, 255, 0.18)` — Interactive hairline on hover or focused states.

### Discipline

- **Red acts. Green answers.** Red marks anything the visitor stimulates: text
  selection, active states, focus rings, alerts, the single underline on a
  primary link. Green appears only when something is alive or has succeeded. One
  element never carries both.
- **Tissue is drawn in translucent grey**, never in arbitrary colors:
  `rgba(163, 163, 163, 0.16)` for distant structure, `rgba(163, 163, 163, 0.38)`
  for connective paths, and `rgba(163, 163, 163, 0.72)` for near detail.
- **No fifth hue will ever be admitted.** There is no blue, purple, or amber in
  this building.

---

## Typography

Three distinct voices, one volume knob:

- **Relative Sans (variable, 100–900)** is the voice of the lab — neutral,
  precise, unhurried.
  - Set at `body-md` (`14px`, line-height `1.5`, tracking `-0.015em`) for
    landing pages and short descriptions.
  - Set at `body-article` (`clamp(1.02rem, 1.2vw, 1.12rem)`, line-height
    `1.8`, tracking `-0.01em`) for long-form publishing.
- **Relative Mono (variable, 100–900)** is the instrument's handwriting.
  Everything the machine says — coordinates, statuses, timestamps, nav meta,
  table headers, citations, code — is `label-caps`: `10px`–`11px`, weight `500`,
  uppercase, tracked out to `0.14em`–`0.22em` so each glyph stands alone like a
  marking on a reticle.
- **Geist Pixel Square** is the shout. Giant uppercase display type for the
  footer headline (`SUBSTRATE LABS`, `NOT FOUND`) and newsroom index banner.
  One shout per surface. Render at `clamp(2.8rem, 9.6vw, 9.4rem)` with
  line-height `0.88` and tracking `-0.02em`.

### Font Links & CDN Distribution

All three primary laboratory typefaces are self-hosted in `/public/fonts/` and mirrored on global CDN origins with `@font-face` configured for `font-display: swap`:

| Typeface | Format | Weights | Local File Path | Direct CDN URL |
| --- | --- | --- | --- | --- |
| **Relative Sans Variable** | TrueType (`.ttf`) | 100–900 | [`/fonts/The-Relative-Sans-Variable.ttf`](/fonts/The-Relative-Sans-Variable.ttf) | [https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf](https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf) |
| **Relative Mono Variable** | TrueType (`.ttf`) | 100–900 | [`/fonts/The-Relative-Mono-Variable.ttf`](/fonts/The-Relative-Mono-Variable.ttf) | [https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf](https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf) |
| **Geist Pixel Square** | WOFF2 (`.woff2`) | 400–900 | [`/fonts/GeistPixel-Square.woff2`](/fonts/GeistPixel-Square.woff2) | [https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2](https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2) |

```css
/* Primary Typography: Relative Sans Variable */
@font-face {
  font-family: "Relative Sans";
  src: url("/fonts/The-Relative-Sans-Variable.ttf") format("truetype"),
       url("https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf") format("truetype");
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

/* Technical & Metadata Typography: Relative Mono Variable */
@font-face {
  font-family: "Relative Mono";
  src: url("/fonts/The-Relative-Mono-Variable.ttf") format("truetype"),
       url("https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf") format("truetype");
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}

/* Display Typography: Geist Pixel Square */
@font-face {
  font-family: "Geist Pixel Square";
  src: url("/fonts/GeistPixel-Square.woff2") format("woff2"),
       url("https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2") format("woff2");
  font-weight: 400 900;
  font-style: normal;
  font-display: swap;
}
```

Fallback stacks: Inter / -apple-system / BlinkMacSystemFont / sans-serif for Relative Sans; Geist Mono / ui-monospace / monospace for Relative Mono; Relative Mono / monospace for Geist Pixel Square.

---

## Brand Assets & Logos

**Soma is the default Substrate logo.** The source SVGs live in this repo at
[`assets/soma/`](../assets/soma/), are served from the brand CDN at
[`https://assets.substrates.in/brand-assets/identity/`](https://assets.substrates.in/brand-assets/identity/), and ship to the site under `/public/soma/`. Every identity
graphic sits on pure black ground (`#000000`).

| Asset | Size | Site Path | CDN URL |
| --- | --- | --- | --- |
| **Primary Logo (Soma mark, outline)** | 240 × 240 viewBox | `/soma/soma-mark-outline.svg` | [https://assets.substrates.in/brand-assets/identity/soma-mark-outline.svg](https://assets.substrates.in/brand-assets/identity/soma-mark-outline.svg) |
| **Filled Logo (Soma, idle)** | 240 × 240 viewBox | `/soma/soma-idle.svg` | [https://assets.substrates.in/brand-assets/identity/soma-idle.svg](https://assets.substrates.in/brand-assets/identity/soma-idle.svg) |
| **Small Logo (Soma, idle, compact)** | 160 × 160 viewBox | `/soma/soma-idle-compact.svg` | [https://assets.substrates.in/brand-assets/identity/soma-idle-compact.svg](https://assets.substrates.in/brand-assets/identity/soma-idle-compact.svg) |
| **Open Graph Visual Asset** | 4800 × 2520 | [`/substrate-og-image.png`](/substrate-og-image.png) | [https://substrates.in/substrate-og-image.png](https://substrates.in/substrate-og-image.png) |
| **Favicon** | 32 × 32 | [`/icon.png`](/icon.png) | [https://substrates.in/icon.png](https://substrates.in/icon.png) |
| **Apple Touch Icon** | 180 × 180 | [`/apple-icon.png`](/apple-icon.png) | [https://substrates.in/apple-icon.png](https://substrates.in/apple-icon.png) |
| *Legacy strata logo (retired)* | 960 × 880 | [`/substrate-logo.png`](/substrate-logo.png) | [https://substrates.in/substrate-logo.png](https://substrates.in/substrate-logo.png) |

### Logo Specifications & Usage
- **Geometry**: Soma, a neuron's cell body. An irregular round membrane, 14
  short dendrites, two eyes, a mouth, and one nucleus at the lower right.
- **Which file**: Below `48px` (site header, favicon) use the **compact idle
  Soma**, because dendrites turn to noise at that size. From `48px` up, use the
  **outline mark** where the logo sits beside text (footers, documents, print)
  and the **filled idle Soma** where it stands alone (splash, about page, social
  avatar).
- **Rendering**: Inline SVG or `<img>` on `#000000`, `object-contain`. The mark
  is white only. Never recolour it, never put it on a light ground.
- **Scaling**: Height is strictly `24px` on mobile (`<=600px`), `28px` on tablet
  (`601px`–`960px`), and `32px` on desktop (`>960px`). At these sizes use the
  compact file.
- **Interaction**: Opacity `0.9` at rest, `1.0` on hover over `200ms`. The logo
  never changes expression on hover. Expressions belong to the mascot, not the
  mark.
- **LCP Preload**: The header logo is the primary Largest Contentful Paint
  element and must be preloaded:
  ```html
  <link rel="preload" as="image" href="/soma/soma-idle-compact.svg" fetchPriority="high" />
  ```
- **Favicon & app icons**: Regenerate `/icon.png` and `/apple-icon.png` from
  `soma-idle-compact.svg` on black. Until that is done they still show the
  strata mark.
- **Legacy strata logo**: The strata-and-rising-circle mark is retired from new
  work. Replace it wherever you touch a surface that still uses it.

---

## Soma — Mascot & Logo

Soma is a neuron's cell body, the part of the cell that receives signals and
decides whether to fire. That is what the product does for a person's records,
so Soma is both the logo and the one character in the lab.

### Anatomy

| Part | Drawing | Colour |
| --- | --- | --- |
| Membrane | Irregular closed path, `scale(60)` | Fill `#161616`, stroke `rgba(255,255,255,0.85)` |
| Dendrites | 14 short curved strokes, full files only | `rgba(255,255,255,0.45)`, `2px`, round caps |
| Eyes | Two `r=14` circles at `(±20, −10)` | White, pupils black |
| Mouth | One short stroke | White, `3px`, round caps |
| Nucleus | `r=8` circle at `(26, 32)` | `#5E5E5E` at rest. Bio green only in `done` |
| Props | Tag, page, sound marks, signal dot | Greys and white. Red only for `recording` |

### The Thirteen States

Each state has a full file (`-120 -120 240 240`, with dendrites and props) and a
compact file (`-80 -80 160 160`, body only). Every file is at
`https://assets.substrates.in/brand-assets/identity/soma-<state>.svg` and `https://assets.substrates.in/brand-assets/identity/soma-<state>-compact.svg`, for example
[`soma-done.svg`](https://assets.substrates.in/brand-assets/identity/soma-done.svg). Pick the state that describes what
the system is actually doing. The status text beside Soma must still be literal.

| State | Show it when | Pair it with copy like |
| --- | --- | --- |
| `idle` | Nothing is happening; default and logo | — |
| `hello` | First visit, empty state, sign-in | "Upload a report to begin." |
| `happy` | A person finishes something by themselves | "Changes saved." |
| `listening` | The microphone is open and waiting | "Listening…" |
| `recording` | Audio is being captured (red dot = stimulus) | "Recording · 00:42" |
| `reading` | A document is being read | "Reading document…" |
| `thinking` | A step with no better literal name is running | "Comparing reports…" (never "Thinking…") |
| `carrying` | Something is being moved or saved; the tag names it | "Saving to Fever notes…" |
| `done` | A task finished (green nucleus = response) | "Summary ready." |
| `unsure` | The model could not read a value reliably | "We could not read this value. Check page 4." |
| `surprised` | Something unexpected but harmless | "This file is larger than usual. It may take 3 minutes." |
| `sorry` | Something failed | "We could not read this file. Try the original PDF." |
| `sleeping` | Paused, offline, or after hours | "Processing resumes at 9:00." |

### Rules

- **One Soma per surface.** Never two, never a crowd, never as a bullet or icon.
- **Red and green keep their meaning on Soma.** The nucleus turns green only in
  `done`. Red appears only as the `recording` signal dot. The glow on these two
  is a signal, not decoration; no other state may glow.
- **Soma never replaces words.** Every state sits beside literal text that
  explains the situation without the drawing. Soma is `aria-hidden="true"` (or
  `alt=""`) unless it is the logo, which gets `alt="Substrate"`.
- **`sorry` is shown, not said.** The face carries the apology so the copy does
  not have to: no "Oops", no "Sorry!", just what happened and what to do.
- **Motion lives in the canvas.** In the DOM, Soma is a still SVG. Blinking,
  breathing, or waving is drawn in a canvas specimen and freezes on the still
  pose under `prefers-reduced-motion`.
- **Text on props uses Relative Sans.** The `carrying` tag ships with a Geist
  fallback; set it in Relative Sans when you rebuild it, and keep the label to
  one or two lower-case words.
- **Inlining several SVGs on one page**: every file defines `id="glow"` and
  `id="redglow"`. Rename the ids or load the files with `<img>` so they do not
  collide.
- **Don't** redraw, recolour, rotate past the `hello` tilt (−8°), add limbs, or give Soma clothes, hats, or props outside
  the set.

---

## The Stipple Layer

Stipple is the dot-matrix way of drawing in Substrate, after the way scientific
illustrators shade by hand and the way an instrument prints its readout. It adds
five things and changes nothing else: the black ground, the two signal colours,
square chrome, hairlines, and the still DOM all stay as they are.

### 1. Dot-matrix tone (canvas only)

- Tone is **dot size on a fixed grid**. No gradients, no blur.
- Grid pitch: `8px` for full-bleed fields, `7px` for panels.
- Five steps, as a share of the pitch (radius) and colour:

  | Step | Radius | Colour | Use |
  | --- | --- | --- | --- |
  | 1 | `0.20` | `rgba(163,163,163,0.16)` | Distant structure, grain |
  | 2 | `0.27` | `rgba(163,163,163,0.38)` | Connective tissue |
  | 3 | `0.33` | `rgba(163,163,163,0.56)` | Body |
  | 4 | `0.39` | `rgba(163,163,163,0.72)` | Near detail, membranes |
  | 5 | `0.44` | `rgba(255,255,255,0.86)` | Nuclei, highlights |

- A visitor's click sends a **red ring of dots** outward through the grid. When
  the ring reaches Soma or another living thing, it answers with a **green
  ring**. Red acts, green answers.
- A specimen that represents work in progress **develops dot by dot**: each grid
  cell has a fixed random threshold and appears when progress passes it.
- Throttle to about 30fps, stop when off-screen or the tab is hidden, and draw a
  single still frame under `prefers-reduced-motion`.

### 2. Dither meter

- Track: a `2px` checker in `rgba(163,163,163,0.38)`, `16px` tall, up to
  `240px` wide, square corners.
- Fill: solid white. It snaps to `4px` steps and jumps; it never animates.
- Number: Relative Mono, tabular figures, padded to two digits (`04%`, `48%`,
  `100%`).
- Always `role="progressbar"` with `aria-valuenow`, `aria-valuemin`,
  `aria-valuemax`, and an `aria-label`.

### 3. Tree index

- Glyph `└` (U+2514) in `rgba(163,163,163,0.38)`, then one space, in Relative
  Mono `14px`.
- Indent `2ch` per level. Two levels at most.
- The current item turns white at weight `600`. No arrows, no highlight bars,
  no red.
- Use it for article contents and for multi-step progress. A finished step
  shows the 6px green synapse dot **and** the word "Done".
- The glyph is decoration to a screen reader: wrap it in `aria-hidden="true"`
  and keep the list a real `<ol>` inside a labelled `<nav>`.

### 4. Key hints

- Mono caps, `11px`, `0.18em` tracking, `rgba(163,163,163,0.72)`:
  `PRESS ↑ / ↓ TO SCROLL`, `PRESS ESC TO CLOSE`.
- Show only under `(hover: hover) and (pointer: fine)`. Hide on touch.
- Name a key that already works. A hint is never the only way to do something.

### 5. Soma in stipple

- Soma is the only character drawn in a Stipple field, one per surface.
- In a stipple field, keep a clear ring of void around Soma (about `10px`
  beyond the dendrites) so the drawing stays readable.
- Draw Soma from the SVG paths (`Path2D` accepts them directly) at whole-pixel
  positions. Do not re-draw Soma as pixel art or in dots.

### Stipple don'ts

- Don't use a grey ground like `#141414`. The field is `#000000`.
- Don't animate dots, meters, or tree items with CSS.
- Don't use dither as a background texture or a card fill.
- Don't use the tree glyph for lists that have no hierarchy.

---

## Layout & Container Hierarchy

Substrate operates on two architectural layouts: **The Specimen Slide** (home)
and **The 4-Tier Publishing Shell** (newsroom & articles).

### 1. The Home Slide

A single, full-bleed slide (`min-h-screen supports-[height:100dvh]:min-h-dvh`)
divided into three bands:

1. **Instrument header** — Soma mark at left (`24px` mobile, `28px` tablet,
   `32px` desktop; preloaded with high priority as LCP asset), mono nav links
   at right (`Newsroom`, email, handle).
2. **Observation field** — central specimen canvas (`NeuralSpecimen`), centered,
   max-width `64rem` (`1024px`), flexible height with `HomePillBanner` anchored
   over the specimen base.
3. **Editorial footer** — the pixel display shout (`SUBSTRATE LABS`), followed
   by the quiet metadata row: tagline at left, tracked mono label at right
   (`COMING SOON`).

### 2. The 4-Tier Publishing Shell

Articles and newsroom index pages use a responsive 4-tier container scale
defined in CSS custom properties:

```css
:root {
  --article-text-width: 680px;   /* Pure prose, quotes, footnotes, audio controls */
  --article-media-width: 1140px; /* Standard figures, tables, code blocks, stats */
  --article-wide-width: 1280px;  /* Dense charts, interactive diagrams, galleries */
  --article-page-width: 1440px;  /* Header nav, footer bar, full bleed canvas */
  --article-rule: rgba(255, 255, 255, 0.14);
}
```

- **`article-frame`**: Standard prose column (`max-width: 680px`). Gives
  typographic density and ideal measure (60–75 characters per line).
- **`article-frame-wide`**: Media column (`max-width: 1140px`). Houses figures,
  code blocks with copy buttons, interactive ECharts, and data tables.
- **`article-frame-full`**: Panoramic column (`max-width: 1280px`). Reserved for
  dense biological network diagrams, multi-column media groups, and galleries.
- **Gutters & Padding**: Mobile screens default to `16px` (`calc(100% - 32px)`),
  scaling to `24px` (`calc(100% - 48px)`) on desktop.

---

## Elevation & Depth

There is no elevation. Nothing casts a drop shadow and nothing floats above
anything; the lab is flat, and depth is **biological, not optical**:

- **Translucency is distance.** The grey tissue alphas (`0.16` / `0.38` / `0.72`)
  replace shadow stacks.
- **A firing signal is drawn twice:** a thick blood-red body
  (`rgba(181, 31, 46, 0.85)`) with a thin pale core (`rgba(255, 220, 225, 0.95)`)
  riding inside it — the exact way a biological axon illuminates under
  stimulus.
- **Layering order:** dust motes drift behind, tissue structure next, signals
  above structure, and cells / nuclei on top.

---

## Shapes & Controls

Square is the frame; the circle is the life.

- **All chrome is square (`0px`)**, with `2px` as the only concession on small
  interactive elements (code boxes, tags, inputs, media frames).
- **Circles are reserved for biology:** cells, nuclei, Soma, Stipple dots, the
  6px synapse indicator dot, author avatar portraits.
- **Pills (`9999px`)** are used only for navigational back actuators and the
  floating `HomePillBanner`.
- **Icons are HugeIcons (free stroke set exclusively).** 24px grid, ~1.5px
  stroke, inheriting `currentColor`, no fills, no duotone, no animated icons.
  An icon is a technical annotation in the margin of a lab notebook.

---

## Canvas Specimen Doctrine

The DOM is motionless. Life in Substrate occurs strictly within HTML5 Canvas
specimens. The codebase maintains three distinct preparations:

1. **`NeuralSpecimen`** (`components/neural-specimen.tsx`):
   - Multi-soma interactive neural preparation with wandering somatic bodies,
     dendritic trees, axonal pathways, and synaptic boutons.
   - Action potentials propagate across branches with a dual-stroke glow: thick
     blood-red sheath with an intense pale pinkish-white core.
   - Microscopic dust motes drift continuously in the background void.
   - Responds dynamically to mouse velocity and click stimuli.
2. **`SpecimenField` / Journey Canvas** (`components/specimen-field.tsx`):
   - Microscopic organism preparation used on newsroom index surfaces.
   - Features multi-lobed membranes, undulating cilia, nucleus displacement, and
     interactive radar ping waves on crosshair pointer movements.
3. **`SignalSpecimen`** (`components/signal-specimen.tsx`):
   - Linear biological signal wave monitor for stimulus/response diagnostics.

### Motion Safety

All canvas animation loops must check `window.matchMedia('(prefers-reduced-motion: reduce)')`.
When reduced motion is preferred, render a single still, dormant frame. Never
run requestAnimationFrame loops when motion is disabled or when the tab is
inactive.

---

## The Component System

### 1. Slide & Nav Components

- **`slide`**: The base container of every page (`#000000`, text `#A3A3A3`).
- **`brand-mark`**: The Soma mark (outline, or compact idle below `48px`).
  Clean heights (`24px` to `32px`), preloaded as LCP asset.
- **`Soma`**: The mascot, one per surface, in one of thirteen states. See
  *Soma — Mascot & Logo*.
- **`display-headline`**: Giant Geist Pixel Square shout. White, leading `0.88`,
  `select-none`. Exactly one per page.
- **`HomePillBanner`** (`components/home-pill.tsx`): Floating announcement pill
  anchored over the specimen stage. Features subtle border glow (`#B51F2E`),
  `backdrop-blur-md`, truncated label, and directional arrow. Supports internal
  Next.js routing and external new-tab targets.
- **`PublishingShell`** (`components/article/shell.tsx`): Master layout for
  editorial pages. Houses the top sticky grid navigation, pill back button,
  and bottom metadata rule.

### 2. The 18 Rich Block Components (`components/article/renderer.tsx`)

Every long-form article is rendered via Sanity Portable Text and an extensible
rich block pipeline:

1. **`articleImage`**: Responsive picture frame with Next.js Image, caption,
   photographic credit, and external source link.
2. **`articleVideo`**: Native HTML5 video player with poster image, looping,
   playsinline, and custom aspect-ratio container.
3. **`vimeo`**: Responsive `16:9` embedded Vimeo video with lazy host
   isolation.
4. **`diagram`**: Interactive Mermaid.js diagram with dark lab styling and
   full-screen modal expansion (`.diagram-expanded`).
5. **`chart`**: Apache ECharts data visualization. Rendered with black ground,
   blood-red and bio-green series accents, CSV parser, and responsive resize.
6. **`svgGraphic`**: Sanitized vector graphic. Strips scripts and harmful
   attributes; supports dark-field inversion via `.invert-svg`.
7. **`editorialQuote`**: Pull quote formatted with a `2px` blood-red left
   border, large Relative Sans type, and uppercase mono attribution.
8. **`codeSample`**: Shiki syntax highlighter (`github-dark`), Relative Mono
   typeface, uppercase filename/language bar, and one-click copy button.
9. **`callout`**: Structural note bounded by top and bottom hairline rules with
   an uppercase mono tag (`NOTE`, `WARNING`, `METHOD`).
10. **`dataTable` & `sortableTable`**: Responsive table with sticky first
    column, uppercase mono column headers, and optional column sorting.
11. **`stats`**: Grid of numerical metrics featuring large Relative Sans
    numerals, small unit identifiers, mono labels, and descriptions.
12. **`gallery`**: Multi-image presentation supporting either a 2-column grid or
    a touch-friendly scroll-snap carousel.
13. **`timeline`**: Chronological milestone list with mono timestamps and
    nested image assets.
14. **`accordion`**: Minimal disclosure widget for technical appendixes and
    supplemental data.
15. **`download`**: File asset card showing filename, file type, file size, and
    download link.
16. **`math`**: Mathematical typesetting via KaTeX. Renders inline and
    scrollable display equations safely.
17. **`citationReference`**: Academic bibliography entries with DOI, arXiv,
    and PubMed linking, paired with superscript numbered markers (`[^1]`).
18. **`mediaGroup`**: Flexible compound container supporting tabbed rails,
    carousels, and responsive split columns (`50/50`, `60/40`, `67/33`).
19. **`divider`**: Section separation in three styles: hairline `line`, centered
    `dots` (`· · ·`), or pure negative `space`.

---

## Responsive Breakpoints & Fluidity

The system scales across five responsive viewports:

- **Ultra-compact (`<= 350px`)**: Single-column layouts, stats stacks
  vertically, brand font scales down to `11px`.
- **Mobile (`<= 600px`)**: Nav compresses to 2 columns; article padding reduces
  to `16px`; tables scroll horizontally via `.table-scroll`; giant display
  shout renders at `clamp(2.8rem, 6.5vw, 5.8rem)`.
- **Tablet (`601px`–`800px`)**: Featured article switches to 2-column; media
  groups collapse into single columns; specimen journey canvas maintains
  `160px` height.
- **Laptop (`801px`–`960px`)**: Full 3-column navigation grid; specimen canvas
  expands to `480px` width; charts render full legend and tooltips.
- **Desktop (`> 960px`)**: Full measure across all four container tiers (`680px`,
  `1140px`, `1280px`, `1440px`).

---

---

## Brutal Simplicity & Apple HIG Accessibility

Substrate interfaces must pass the **Grandma Test**: they must be brutally simple, completely free of engineering jargon, uncluttered, and so intuitive that anyone can use them effortlessly.

### 1. The Grandma Standard
- **Zero Technical Jargon:** Never expose engineering or pipeline terminology to users. Use plain, direct, human words.
- **Minimal Buttons & Zero Visual Noise:** Provide one clear primary action per screen. Remove extraneous pills, nested options, and secondary clutter. If a screen feels full, subtract until only the essentials remain.
- **Complexity Hidden Behind the Scenes:** System design and data models must absorb pipeline orchestration, data normalization, and parsing. The user experiences only a calm status ("Reading document…", "Preparing summary…") and the final result.
- **Forgiving Interactions:** Support easy undo, clear error recovery, and flexible input types.

### 2. Apple HIG Eight Core Principles
Every screen and component must satisfy these principles:
- **Purpose:** Design with intention. Identify what matters most to users and focus relentlessly on making those core tasks effortless.
- **Agency:** Let people act their own way. Give them freedom, keep them informed of state changes, and make recovery from mistakes easy.
- **Responsibility:** Act in people's best interest. Prioritize safety, privacy, and full transparency about what the product does.
- **Familiarity:** Build on what people know. Use established physical and digital patterns consistently.
- **Flexibility:** Adapt to diverse contexts and needs. Support multiple devices, interaction types, and perspectives.
- **Simplicity:** Be clear and direct. Remove the unnecessary; every element must earn its place.
- **Craft:** Care about every detail. Show dedication through thoughtful execution, smooth 60fps/120fps interactions, and exact alignment.
- **Delight:** Make it human. Design for calm, satisfaction, and trust.

### 3. Universal Accessibility (Six Disability Categories)
- **Vision:** Dynamic Type scaling, strict contrast standards (minimum 4.5:1 body, 7:1 metadata), dual-channel signaling (never color alone; red/green paired with shapes, icons, or text), comprehensive screen-reader semantics (`sr-only` context, descriptive `alt` text).
- **Hearing:** Full text alternatives for all audio and video (transcripts, captions), visual indicators paired with audio states.
- **Mobility:** Minimum 44×44px interactive touch targets, adequate spacing (>=8px), prominent keyboard focus rings (`:focus-visible` with `2px solid #b51f2e; outline-offset: 4px`), simple gestures with click/tap alternatives.
- **Speech:** Full keyboard and pointer navigation; zero speech-only barriers; compatibility with Switch Control.
- **Cognitive:** Streamlined single-action tasks, no artificial time-boxes or countdowns, zero flashing animations, full media playback control, and clear error recovery.
- **Motion:** Honor `prefers-reduced-motion: reduce` by freezing canvas loops into a dormant static frame; gentle transitions; comfortable view boundaries.

---

## Do's and Don'ts

**Do**

- Do start every page from the black slide (`#000000`) and justify what you
  place on it.
- Do make the interface brutally simple — so easy a grandmother can use it
  without hesitation.
- Do hide complex computational pipelines and data transformations behind
  the scenes.
- Do let the canvas carry all motion, and always honor `prefers-reduced-motion`
  with a still, dormant frame.
- Do use mono caps with `0.14em`–`0.22em` tracking for anything the machine says.
- Do separate content with hairlines (`rgba(255, 255, 255, 0.14)`) and void;
  density is admitted only through the grey tissue alphas.
- Do reserve red for visitor-stimulated states and green for living or
  successful ones — and check both vial and observed values against where they
  render.
- Do pick icons from the HugeIcons free stroke set and inherit `currentColor`.
- Do use the 4-tier container scale (`680px` / `1140px` / `1280px` / `1440px`)
  for publishing surfaces.
- Do ensure every interactive element meets the 44×44px minimum touch target.
- Do use the Soma mark as the logo, and pick the Soma state that matches what
  the system is actually doing.
- Do draw tone in canvas specimens with Stipple dots on a fixed grid.

**Don't**

- Don't expose technical jargon, pipeline mechanics, or database terms in the UI.
- Don't clutter the screen with competing buttons, nested menus, or auxiliary
  toggles.
- Don't build a light mode, a theme toggle, or a "dim" variant. The lamp is off
  permanently.
- Don't pulse badges, blink status dots, or animate anything in the DOM to "feel
  alive". If it must be alive, it belongs in the specimen canvas.
- Don't add gradients, glass, glow-as-decoration, or drop shadows — depth is
  translucency, not blur.
- Don't introduce a color outside the eight tokens; there is no blue, no purple,
  and there never will be.
- Don't fill icons, mix icon packs, or use emoji as UI glyphs.
- Don't round chrome past `2px`, and don't put circles anywhere except on
  living things or author avatars.
- Don't set a second display headline on a page, and don't shrink the shout — it
  is either enormous or it is body copy.
- Don't use the retired strata logo on new work, and don't show more than one
  Soma on a surface.
- Don't let Soma's face replace literal status text.
- Don't use pseudo labels or filler labels: no eyebrow labels that restate the
  heading, no mono "readouts" without real data (`SIGNAL 07`, `SPECIMEN #042`,
  decorative coordinates), no decorative `01 / 02 / 03`, no filler chips. Mono
  `label-caps` exists for real values only. If deleting a label loses nothing,
  delete it.

