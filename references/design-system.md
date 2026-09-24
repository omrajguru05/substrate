# Substrate Labs — Design System

Dark-field laboratory identity and publishing design system for Substrate Labs (`substrates.in`). Every page is a specimen slide on a black microscope field — grey is structure, red is stimulus, green is response. There is no light mode.

---

## 1. System Tokens

```yaml
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
```

---

## 2. Core Metaphor: The Dark Field

Substrate Labs is not browsed. It is **observed**. The screen is the dark-field of a microscope, every page is a specimen slide laid on the stage, and the visitor is the instrument. The interface never explains this metaphor — it simply behaves like it.

1. **The void.** Pure black (`#000000`), edge to edge. It is not a dark theme; it is the absence of a lamp. Light mode does not exist, is not hidden behind a toggle, and will never be planned. Content floats in the field the way tissue floats in the viewing circle — anchored by hairlines, never by boxes.
2. **The drawing.** Grey structure: mono labels, reticle coordinates, metadata, subtle separation rules, and the dim linework of the specimen itself. Grey is how the lab takes notes.
3. **The signal.** Exactly two colors that carry meaning. **Blood red is stimulus** — selection, focus, alarm, active states, the action potential firing. **Bio green is response** — a synapse received, life confirmed, the organism answering back. Nothing in this lab is red or green for decoration.

Motion doctrine: **the DOM is still; life happens in the canvas.** The specimen carries all animation — wandering, firing, glowing. Chrome never twinkles, never pulses, never decorates itself with CSS keyframes.

---

## 3. Color Discipline

Every functional color exists in two states: its **vial value** (hex on stockroom bottle) and its **observed value** (`-display` tokens under the microscope on black):

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

- **Red acts. Green answers.** Red marks visitor stimulation: text selection, active states, focus rings, alerts, the single underline on a primary link. Green appears only when something is alive or has succeeded. One element never carries both.
- **Tissue is drawn in translucent grey**, never in arbitrary colors: `rgba(163, 163, 163, 0.16)` for distant structure, `rgba(163, 163, 163, 0.38)` for connective paths, and `rgba(163, 163, 163, 0.72)` for near detail.
- **No fifth hue will ever be admitted.** No blue, no purple, no amber.

---

## 4. Typography Hierarchy

- **Relative Sans (variable, 100–900)** is the voice of the lab — neutral, precise, unhurried. Set at `14px` (`body-md`) for brief interfaces and `clamp(1.02rem, 1.2vw, 1.12rem)` (`body-article`, line-height `1.8`) for long-form reading.
- **Relative Mono (variable, 100–900)** is the instrument's handwriting. Everything the machine says — coordinates, statuses, timestamps, nav meta, table headers, citations, code — is `10px`–`11px`, weight `500`, uppercase, tracked out to `0.14em`–`0.22em`.
- **Geist Pixel Square** is the shout. Giant uppercase display type for the footer headline (`SUBSTRATE LABS`, `NOT FOUND`) and newsroom banner. Exactly one shout per surface. Render at `clamp(2.8rem, 9.6vw, 9.4rem)` with line-height `0.88` and tracking `-0.02em`.

---

## 5. Layout Architecture

### Home Slide

Full-bleed slide (`min-h-screen supports-[height:100dvh]:min-h-dvh`):
1. **Instrument header**: Brand mark (`24px`–`32px`, LCP preload) at left; mono nav links at right (`Newsroom`, email, handle).
2. **Observation field**: Centered specimen canvas (`NeuralSpecimen`, max-width `64rem`) with `HomePillBanner` floating at the bottom threshold.
3. **Editorial footer**: Pixel shout (`SUBSTRATE LABS`), tagline at left, tracked mono label at right (`COMING SOON`).

### 4-Tier Publishing Shell

Articles and newsroom index use a responsive 4-tier container scale:
- `article-frame` (`680px`): Prose, quotes, audio controls, footnotes.
- `article-frame-wide` (`1140px`): Standard figures, tables, code blocks, stats.
- `article-frame-full` (`1280px`): Complex charts, diagrams, split media groups.
- `publishing-nav` / `publishing-footer` (`1440px`): Global page shell.

---

## 6. Canvas Specimen Doctrine

The DOM is motionless. Life happens in HTML5 Canvas specimens:

1. **`NeuralSpecimen`**: Multi-soma interactive neural preparation with wandering somatic bodies, dendritic trees, axonal pathways, and synaptic boutons. Action potentials fire with a dual-stroke glow (thick blood-red sheath with intense pale white core). Responds to mouse velocity and click stimuli.
2. **`SpecimenField` (Journey Canvas)**: Microscopic organism preparation used on newsroom index surfaces. Multi-lobed membranes, undulating cilia, nucleus displacement, and interactive radar pings.
3. **`SignalSpecimen`**: Linear biological signal wave monitor.

All canvases honor `window.matchMedia('(prefers-reduced-motion: reduce)')` by halting animation and rendering a dormant static frame.

---

## 7. The 18 Rich Block Components

1. `articleImage`: Picture frame with caption, credit, source link, and responsive sizing.
2. `articleVideo`: HTML5 video with poster, loop, muted, playsinline.
3. `vimeo`: 16:9 embedded Vimeo host.
4. `diagram`: Mermaid.js diagram with dark styling and full-screen modal expansion.
5. `chart`: Apache ECharts visualization with dark field, blood-red and bio-green series accents.
6. `svgGraphic`: Sanitized vector graphic with dark-field inversion support.
7. `editorialQuote`: Pull quote with 2px blood-red left border and uppercase mono attribution.
8. `codeSample`: Shiki syntax highlighter (`github-dark`), Relative Mono, uppercase header bar, copy button.
9. `callout`: Top/bottom hairline container with uppercase mono tag (`NOTE`, `WARNING`, `METHOD`).
10. `dataTable` & `sortableTable`: Table with sticky first column, uppercase mono headers, optional column sorting.
11. `stats`: Metric cards featuring large Relative Sans numerals, unit identifiers, and mono labels.
12. `gallery`: 2-column grid or touch-friendly scroll-snap carousel.
13. `timeline`: Chronological milestone list with mono timestamps.
14. `accordion`: Minimal disclosure widget for technical appendixes.
15. `download`: Asset download card with file metadata and download link.
16. `math`: KaTeX mathematical typesetting with scrollable display equations.
17. `citationReference`: Academic bibliography entries with DOI, arXiv, and PubMed links.
18. `mediaGroup`: Compound container supporting tabbed rails, carousels, and responsive split columns (`50/50`, `60/40`, `67/33`).
19. `divider`: Hairline line, dots (`· · ·`), or negative space.

---

## 8. Do's and Don'ts

- **Do** start every page from pure black (`#000000`).
- **Do** let the canvas carry all motion, and respect `prefers-reduced-motion`.
- **Do** use mono caps with `0.14em`–`0.22em` tracking for machine metadata.
- **Do** separate content with hairlines (`rgba(255, 255, 255, 0.14)`) and void.
- **Do** reserve red for stimulus and green for response.
- **Do** use HugeIcons free stroke set exclusively with `currentColor`.
- **Don't** build a light mode, a theme toggle, or a dim variant.
- **Don't** animate DOM elements (no pulsing badges, no blinking dots).
- **Don't** add gradients, blur glass, or drop shadows.
- **Don't** introduce colors outside the eight tokens (no blue, no purple).
- **Don't** round chrome past `2px` (circles only for biology or author avatars).
