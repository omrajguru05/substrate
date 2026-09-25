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
assets:
  logo:
    src: "/substrate-logo.png"
    url: "https://substrates.in/substrate-logo.png"
    width: 960
    height: 880
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
    height: 32px
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

All identity graphics are stored in `/public/` on pure black ground (`#000000`) and served at high resolution:

| Asset | Dimensions | Local File Path | Production Canonical URL |
| --- | --- | --- | --- |
| **Primary Substrate Logo** | 960 × 880 | [`/substrate-logo.png`](/substrate-logo.png) | [https://substrates.in/substrate-logo.png](https://substrates.in/substrate-logo.png) |
| **Open Graph Visual Asset** | 4800 × 2520 | [`/substrate-og-image.png`](/substrate-og-image.png) | [https://substrates.in/substrate-og-image.png](https://substrates.in/substrate-og-image.png) |
| **Favicon** | 32 × 32 | [`/icon.png`](/icon.png) | [https://substrates.in/icon.png](https://substrates.in/icon.png) |
| **Apple Touch Icon** | 180 × 180 | [`/apple-icon.png`](/apple-icon.png) | [https://substrates.in/apple-icon.png](https://substrates.in/apple-icon.png) |

### Logo Specifications & Usage
- **Geometry**: Strata lines representing geological/cellular layers beneath a rising circular biological body.
- **Rendering**: Transparent PNG placed on `#000000`, `object-contain`.
- **Scaling**: Height is strictly `24px` on mobile (`<=600px`), `28px` on tablet (`601px`–`960px`), and `32px` on desktop (`>960px`).
- **Interaction**: Opacity `0.9` at rest, transitioning to `1.0` on hover over `200ms`.
- **LCP Preload**: The header logo is the primary Largest Contentful Paint element and must be preloaded:
  ```html
  <link rel="preload" as="image" href="/substrate-logo.png" fetchPriority="high" />
  ```

---

## Layout & Container Hierarchy

Substrate operates on two architectural layouts: **The Specimen Slide** (home)
and **The 4-Tier Publishing Shell** (newsroom & articles).

### 1. The Home Slide

A single, full-bleed slide (`min-h-screen supports-[height:100dvh]:min-h-dvh`)
divided into three bands:

1. **Instrument header** — brand mark at left (`24px` mobile, `28px` tablet,
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
- **Circles are reserved for biology:** cells, nuclei, the 6px synapse
  indicator dot, author avatar portraits.
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
- **`brand-mark`**: The rising circle and strata logo. Clean heights (`24px` to
  `32px`), preloaded as LCP asset.
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

