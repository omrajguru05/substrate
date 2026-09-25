---
name: substrate
description: "The complete dark-field laboratory design system, component architecture, interactive specimen doctrine, and brand language guidelines for Substrate Labs (substrates.in). Apply whenever designing, building, or writing interfaces, specimen canvases, articles, product copy, or scientific publications for Substrate."
---

# Substrate Labs — Design System & Brand Language

A unified dark-field laboratory identity, component engineering system, Apple HIG accessibility framework, and brand language for Substrate Labs (`substrates.in`).

> Every page is a specimen slide on a black microscope field — grey is structure, red is stimulus, green is response. The interface is brutally simple: zero technical clutter, effortless for anyone to use, hiding all computational complexity behind the scenes. The writing is clear, calm, capable, and human. The work comes first.

This master skill consolidates three core disciplines into a single operating standard:
1. **[Design System](#part-1--the-dark-field-laboratory-design-system)** ([references/design-system.md](./references/design-system.md)): Dark-field laboratory identity, 8-color vial/observed token system, typography, 4-tier container scale, canvas specimens, and the 18 rich article components.
2. **[Brutal Simplicity & Apple HIG Compliance](#part-2--brutal-simplicity--apple-hig-compliance-the-grandma-standard)** ([references/hig-and-simplicity.md](./references/hig-and-simplicity.md)): The Grandma Standard, minimal buttons, hidden complexity, 8 Apple HIG principles, accessibility foundations, and 6 disability category standards.
3. **[Brand Language & Writing Voice](#part-3--substrate-voice--core-qualities)** ([references/brand-language.md](./references/brand-language.md)): Product copy, interface microcopy, research updates, technical papers, clinical/medical safety, release headlines, and the 14-question pre-publication test.

---

## Core Non-Negotiables

1. **The Ground is Void:** Pure black (`#000000`), edge to edge. It is not a dark theme; it is the absence of a lamp. Light mode does not exist, is not hidden behind a toggle, and will never be planned.
2. **The Signal is Strict:** Exactly two colors mean things. **Blood red (`#B51F2E` observed / `#8B0000` vial) is stimulus** — user activation, selection, focus rings, alerts, action potentials. **Bio green (`#39D353` observed / `#39FF88` vial) is response** — synapse confirmed, living organism, success. Never use red or green for decoration. Never admit a fifth hue (no blue, no purple).
3. **Brutal Simplicity (The Grandma Standard):** The user interface must be so simple, clear, and effortless that even a grandmother can use it without confusion or guidance. Zero technical jargon, minimal buttons, no clutter, and no complex visual mazes.
4. **Complexity Hidden Behind the Scenes:** In both frontend interfaces and backend system designs / data models, the architecture must absorb all complexity. The user only ever experiences an obvious, calm, and direct path.
5. **Apple HIG & Universal Accessibility Compliance:** Every interface must be auditable via `omrajguru05/hig-compliance-auditor`. Uphold the 8 Apple HIG Design Principles (Purpose, Agency, Responsibility, Familiarity, Flexibility, Simplicity, Craft, Delight) and satisfy all 6 Disability Categories (Vision, Hearing, Mobility, Speech, Cognitive, Motion).
6. **The DOM is Still; Life Happens in the Canvas:** Chrome never twinkles, blinks, or decorates itself with CSS keyframes. All motion lives inside HTML5 Canvas preparations (`NeuralSpecimen`, `SpecimenField`, `SignalSpecimen`). All canvases must honor `prefers-reduced-motion` with a dormant static frame.
7. **4-Tier Container Architecture:** All publishing surfaces follow strict container bounds: Prose text (`680px`), Media figures/tables/code (`1140px`), Wide/Dense charts and diagrams (`1280px`), and Page shell (`1440px`).
8. **Hairlines Over Boxes:** Density and structure are achieved via hairlines (`rgba(255,255,255,0.14)` and `0.08`–`0.18`) and negative void space, never via drop shadows, blurred glass, or floating cards.
9. **Literal Interface Language:** Interfaces describe what is actually happening. Use "Reading document…" never "Thinking…"; use "Report deleted" never "Success! Your report has been successfully deleted".
10. **Evidence Before Adjectives:** Never rely on empty praise ("revolutionary", "powerful", "seamless", "next-generation"). If something improved, state the evidence and replace the adjective with a human-scale number.
11. **Human-Scale Numbers First:** Translate raw infrastructure metrics into human terms before giving technical specifications (e.g. "A 300-page record takes about 2½ minutes to process" before stating "120 pages per minute").
12. **Unapologetic Honesty About Limitations:** State uncertainty and limitations with the same clarity and confidence as capabilities. A limitation that materially affects use belongs near the relevant capability, not buried in legal disclaimers.

---

## Mandatory Reference Inspection

> [!IMPORTANT]
> **Agents and developers must inspect the corresponding reference documentation when executing deep tasks:**
> - **[`references/design-system.md`](./references/design-system.md)**: Inspect before modifying UI tokens, layout containers, specimen canvases, or article components.
> - **[`references/hig-and-simplicity.md`](./references/hig-and-simplicity.md)**: Inspect before building or auditing any user-facing screen, interactive control, touch target, accessibility tree, or system architecture.
> - **[`references/brand-language.md`](./references/brand-language.md)**: Inspect before drafting product microcopy, technical announcements, clinical/medical documentation, research releases, or changelogs (contains the full 54 chapters of Substrate Brand Language).

---

# Part 1 — The Dark-Field Laboratory Design System

## 1.1 Design Tokens

```yaml
colors:
  primary: "#000000"          # The ground. Background of everything, forever.
  white: "#FFFFFF"            # Full-strength signal. Display headlines, live labels, nuclei.
  grey: "#8A8A8A"             # Brand grey (vial). Structural marks on white media.
  blood-red: "#8B0000"        # Stimulus at rest (vial). Solid fills on white; pressed states.
  bio-green: "#39FF88"        # Response at full fluorescence (vial).
  grey-display: "#A3A3A3"     # Observed grey on black — body copy, metadata, quiet links.
  blood-red-display: "#B51F2E"# Observed red on black — selection, focus rings, underlines, alerts.
  bio-green-display: "#39D353"# Observed green on black — glows, live states, success indicators.
  rule: "rgba(255, 255, 255, 0.14)"     # Primary structural hairline rule.
  hairline-subtle: "rgba(255, 255, 255, 0.08)"
  hairline-hover: "rgba(255, 255, 255, 0.18)"

typography:
  display-specimen:
    fontFamily: Geist Pixel Square
    fontSize: clamp(2.8rem, 9.6vw, 9.4rem)
    lineHeight: 0.88
    letterSpacing: -0.02em
  body-md:
    fontFamily: Relative Sans
    fontSize: 0.875rem (14px)
    lineHeight: 1.5
    letterSpacing: -0.015em
  body-article:
    fontFamily: Relative Sans
    fontSize: clamp(1.02rem, 1.2vw, 1.12rem)
    lineHeight: 1.8
    letterSpacing: -0.01em
  label-caps:
    fontFamily: Relative Mono
    fontSize: 0.6875rem (11px)
    fontWeight: 500
    lineHeight: 1.45
    letterSpacing: 0.22em

containers:
  text: 680px       # var(--article-text-width)
  media: 1140px     # var(--article-media-width)
  wide: 1280px      # var(--article-wide-width)
  page: 1440px      # var(--article-page-width)

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
  relative-mono:
    local: "/fonts/The-Relative-Mono-Variable.ttf"
    cdn: "https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf"
  geist-pixel-square:
    local: "/fonts/GeistPixel-Square.woff2"
    cdn: "https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2"

rounded:
  sm: 0px           # Default for chrome, containers, buttons, inputs
  md: 2px           # Concession for code boxes, tags, media frames
  pill: 9999px      # Concession for HomePillBanner and navigation back button
```

## 1.2 Typography & Font Distribution

- **Relative Sans (variable, 100–900)**: The calm, neutral, precise voice of the lab. Used for all reading prose, body descriptions, and section subtitles.
- **Relative Mono (variable, 100–900)**: The instrument's handwriting. Used for reticle coordinates, dates, status tags, table headers, math/code, and navigation metadata. Tracked out (`0.14em`–`0.22em`), uppercase, weight `500`.
- **Geist Pixel Square**: The shout. Monolithic uppercase pixel headline (`SUBSTRATE LABS`, `NOT FOUND`). Exactly one shout per surface. Fluidly rendered at `clamp(2.8rem, 9.6vw, 9.4rem)`.

### Font Links & CDN Distribution

| Typeface | Format | Weights | Local File Path | Direct CDN URL |
| --- | --- | --- | --- | --- |
| **Relative Sans Variable** | TrueType (`.ttf`) | 100–900 | [`/fonts/The-Relative-Sans-Variable.ttf`](/fonts/The-Relative-Sans-Variable.ttf) | [https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf](https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Sans-Variable.ttf) |
| **Relative Mono Variable** | TrueType (`.ttf`) | 100–900 | [`/fonts/The-Relative-Mono-Variable.ttf`](/fonts/The-Relative-Mono-Variable.ttf) | [https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf](https://in1.omcdn.xyz/static/identity/fonts/The-Relative-Mono-Variable.ttf) |
| **Geist Pixel Square** | WOFF2 (`.woff2`) | 400–900 | [`/fonts/GeistPixel-Square.woff2`](/fonts/GeistPixel-Square.woff2) | [https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2](https://cdn.jsdelivr.net/npm/@zpress/ui@0.8.8/src/theme/fonts/GeistPixel-Square.woff2) |

## 1.3 Brand Assets & Logos

| Asset | Dimensions | Local Path | Production Canonical URL |
| --- | --- | --- | --- |
| **Primary Substrate Logo** | 960 × 880 | [`/substrate-logo.png`](/substrate-logo.png) | [https://substrates.in/substrate-logo.png](https://substrates.in/substrate-logo.png) |
| **Open Graph Visual Asset** | 4800 × 2520 | [`/substrate-og-image.png`](/substrate-og-image.png) | [https://substrates.in/substrate-og-image.png](https://substrates.in/substrate-og-image.png) |
| **Favicon** | 32 × 32 | [`/icon.png`](/icon.png) | [https://substrates.in/icon.png](https://substrates.in/icon.png) |
| **Apple Touch Icon** | 180 × 180 | [`/apple-icon.png`](/apple-icon.png) | [https://substrates.in/apple-icon.png](https://substrates.in/apple-icon.png) |

- **Logo Specifications**: Transparent PNG placed on pure black (`#000000`), `object-contain`. Height is strictly `24px` on mobile (`<=600px`), `28px` on tablet (`601px`–`960px`), and `32px` on desktop (`>960px`). Opacity `0.9` at rest, `1.0` on hover. Preloaded via `<link rel="preload" as="image" href="/substrate-logo.png" fetchPriority="high" />`.

## 1.4 Layout & 4-Tier Container System

1. **The Single-Slide Ground (Homepage)**:
   - Header with LCP brand mark (`24px`–`32px`, priority preloaded) and mono links (`Newsroom`, email, handle).
   - Central observation field with `NeuralSpecimen` and anchored `HomePillBanner`.
   - Bottom editorial footer with pixel display shout and quiet metadata row (`COMING SOON`).
2. **The 4-Tier Editorial Architecture**:
   - `article-frame` (`680px`): Reading column for prose, pull quotes, audio player, and footnotes.
   - `article-frame-wide` (`1140px`): Media figures, code blocks, data tables, and metrics.
   - `article-frame-full` (`1280px`): High-density ECharts, Mermaid diagrams, and multi-column media groups.
   - `publishing-nav` / `publishing-footer` (`1440px`): Global header grid and bottom colophon.

## 1.5 Canvas Specimen Preparations

1. **`NeuralSpecimen`**: Interactive multi-soma biological neural network. Action potentials travel across axonal branches rendered with a dual-stroke technique: thick blood-red sheath (`rgba(181,31,46,0.85)`) with an intense pale pink-white core (`rgba(255,220,225,0.95)`). Responds to cursor velocity and click stimulation.
2. **`SpecimenField`**: Microscopic organism journey canvas. Multi-lobed membranes, undulating cilia, nucleus displacement, and interactive radar pings.
3. **`SignalSpecimen`**: Linear biological signal wave monitor.

## 1.5 The 18 Rich Article Block Components

- **`articleImage` / `articleVideo` / `vimeo`**: Structured media with caption, photographic credit, and external source link.
- **`diagram`**: Mermaid.js diagram in dark-field palette with a one-click modal expansion for deep inspection.
- **`chart`**: Interactive Apache ECharts with dark canvas ground, blood-red and bio-green series accents, CSV parser, and responsive resizing.
- **`svgGraphic`**: Sanitized SVG vectors with dark-field auto-inversion (`.invert-svg`).
- **`editorialQuote`**: Editorial pull quote with `2px` blood-red left border and uppercase mono attribution.
- **`codeSample`**: Shiki syntax highlighter (`github-dark`), Relative Mono, uppercase language header, and one-click copy button.
- **`callout`**: Bounded by upper and lower hairline rules with an uppercase mono category tag (`NOTE`, `WARNING`, `METHOD`).
- **`dataTable` / `sortableTable`**: Data table with sticky first column, uppercase mono column headers, and optional numeric/alphabetical sorting.
- **`stats`**: Grid of numerical metrics featuring large Relative Sans numerals, unit identifiers, and mono labels.
- **`gallery`**: 2-column image grid or touch-friendly scroll-snap carousel.
- **`timeline`**: Chronological milestone list with mono timestamps.
- **`accordion`**: Minimal disclosure widget for technical appendixes.
- **`download`**: File asset card with file metadata and download link.
- **`math`**: KaTeX mathematical typesetting with scrollable display equations.
- **`citationReference`**: Academic bibliography entries with DOI, arXiv, and PubMed links, connected to superscript numbered citations.
- **`mediaGroup`**: Compound container supporting tabbed rails, carousels, and responsive split columns (`50/50`, `60/40`, `67/33`).
- **`divider`**: Section separation in three styles: hairline `line`, centered `dots` (`· · ·`), or negative `space`.

---

# Part 2 — Brutal Simplicity & Apple HIG Compliance (The Grandma Standard)

Every interface in Substrate must pass the **Grandma Test**: it must be brutally simple, completely free of engineering jargon, uncluttered, and so intuitive that anyone can use it effortlessly.

## 2.1 The Grandma Standard
1. **Zero Technical Jargon:** Never expose engineering or computational terminology (e.g. "embeddings", "vector space", "inference pipeline", "token buffers") in user-facing surfaces. Use plain, direct, human language.
2. **Minimal Buttons & Zero Visual Noise:** Provide one clear primary action per screen. Remove extraneous pills, nested options, and secondary clutter. If a screen feels full, subtract until only the essentials remain.
3. **Hide Complexity Behind the Scenes:** System design and data architecture must absorb multi-step pipelines, data conversions, and parsing routines. The user sees only a calm status ("Reading document…", "Preparing summary…") and the final result.
4. **Forgiving Interactions:** Support easy undo, clear error recovery, and flexible input types. Never blame the user.

## 2.2 Apple HIG Eight Core Principles
Every screen and component must satisfy these principles:
- **Purpose:** Design with intention. Identify what matters most to users and focus relentlessly on making those core tasks effortless.
- **Agency:** Let people act their own way. Give them freedom, keep them informed of state changes, and make recovery from mistakes easy.
- **Responsibility:** Act in people's best interest. Prioritize safety, privacy, and full transparency about what the product does.
- **Familiarity:** Build on what people know. Use established physical and digital patterns consistently.
- **Flexibility:** Adapt to diverse contexts and needs. Support multiple devices, interaction types, and perspectives.
- **Simplicity:** Be clear and direct. Remove the unnecessary; every element must earn its place.
- **Craft:** Care about every detail. Show dedication through thoughtful execution, smooth 60fps/120fps interactions, and exact alignment.
- **Delight:** Make it human. Design for calm, satisfaction, and trust.

## 2.3 Accessibility Foundations
- **Intuitive:** Interactions are familiar, straightforward, and consistent.
- **Perceivable:** Information is accessible through sight, hearing, and touch. Never rely on color alone.
- **Adaptable:** Supports Dynamic Type, system font scaling, and personalization.

## 2.4 Six Disability Categories & Implementation Standards
- **Vision:** Dynamic Type scaling, strict contrast standards (minimum 4.5:1 body, 7:1 metadata), dual-channel signaling (never color alone; red/green paired with shapes, icons, or text), comprehensive screen-reader semantics (`sr-only` context, descriptive `alt` text).
- **Hearing:** Full text alternatives for all audio and video (transcripts, captions), visual indicators paired with audio states.
- **Mobility:** Minimum 44×44px interactive touch targets, adequate spacing (>=8px), prominent keyboard focus rings (`:focus-visible` with `2px solid #b51f2e; outline-offset: 4px`), simple gestures with click/tap alternatives.
- **Speech:** Full keyboard and pointer navigation; zero speech-only barriers; compatibility with Switch Control.
- **Cognitive:** Streamlined single-action tasks, no artificial time-boxes or countdowns, zero flashing animations, full media playback control, and clear error recovery.
- **Motion:** Honor `prefers-reduced-motion: reduce` by freezing canvas loops into a dormant static frame; gentle transitions; comfortable view boundaries.

---

# Part 3 — Substrate Voice & Core Qualities

Substrate sounds **clear, calm, capable, and human**.

The writing never needs to prove that the company is intelligent, serious, transparent, humane, technically capable, or ambitious. Those qualities must be apparent from the work, the evidence, the decisions we explain, and the way we speak to people.

## 3.1 Calm
Sound composed. Never use urgency, exaggerated excitement, dramatic framing, or inflated language to make ordinary work feel consequential.
- *Avoid:* "This changes everything." / "A new era begins today." / "The future of medicine starts here."
- *Prefer:* "Clinical 1 is available today." / "We have started testing the model on longer patient records." / "Document processing is currently delayed."

## 3.2 Confident
State what is known without unnecessary hedging. Confidence should come from knowing what the evidence supports.
- *Avoid:* "We believe Clinical 1 may potentially offer improvements when working with longer records."
- *Prefer:* "Clinical 1 handles longer records than the previous model."

## 3.3 Straightforward
Get to the point early. Do not introduce a simple idea with multiple lines of setup. Do not hide an inconvenient fact behind formal corporate language.
- *Avoid:* "We are currently experiencing a temporary degradation in certain parts of the document processing experience."
- *Prefer:* "Document processing is delayed. Uploads are working normally, but results may take longer than usual."

## 3.4 Humane
Write for the person using the product. Put the useful human meaning before the engineering specification.
- *Avoid leading with:* "200K context window."
- *Prefer leading with:* "You can give it an entire patient history and ask questions across it."
- *Avoid leading with:* "40% lower inference cost."
- *Prefer leading with:* "A workload that previously cost about ₹100 now costs about ₹60."

## 3.5 Kind
Do not blame people for errors. Do not make someone feel uninformed because they do not understand a technical term. Do not hide bad news behind cheerful language.
- *Avoid:* "Invalid user configuration."
- *Prefer:* "This device is using a setting the system does not currently support."
- *Avoid:* "Invalid file uploaded."
- *Prefer:* "We could not read this file. Try uploading the original PDF or a clearer scan."

---

# Part 4 — Product & Interface Writing Language

## 4.1 Literal Interface States
Interfaces must describe what is actually happening.

| State | Avoid | Prefer |
| --- | --- | --- |
| **Loading** | "Thinking…" / "Working its magic…" / "Understanding your health…" | "Reading document…" / "Extracting clinical information…" / "Comparing reports…" |
| **Errors** | "Something went wrong." | "We could not read this file. Try uploading the original PDF or a clearer scan." |
| **Empty States** | "Nothing here yet. Your journey starts when you upload your first report." | "No reports yet. Upload a document to begin." |
| **Confirmations**| "Success! Your report has been successfully deleted." | "Report deleted." / "Changes saved." |
| **Buttons / CTAs**| "Get started" / "Explore" / "Continue" | "Upload report" / "Compare reports" / "Review fields" / "Download PDF" |

## 4.2 Banned Filler & Pseudo Labels
Every word must explain what something is, help someone decide, or communicate a limitation.
- *Avoid:* "Your clinical intelligence workspace" → *Prefer:* "Recent reports"
- *Avoid:* "Begin your document analysis journey" → *Prefer:* "Upload report"
- *Rule:* If a label or heading can disappear without making the interface harder to understand, remove it. Whitespace is always better than filler.

## 4.3 Uncertainty & Limitations
Uncertainty is an inherent part of scientific systems. State it directly and locally.
- *Avoid:* "AI can make mistakes."
- *Prefer:* "The model could not determine this value reliably." / "The model found two possible readings for this value. Check the original report."
- *Rule:* Explain limitations with the same confidence as capabilities: "Poor scans and uncommon abbreviations remain the largest sources of error."

---

# Part 5 — Research, Technical & Clinical Communication

## 5.1 Research Writing
Distinguish clearly between what was observed, what is inferred, and what remains uncertain:
- "The model extracted 91% of medications correctly on this evaluation set."
- "This suggests the additional pre-training data improved abbreviation recognition, though we have not verified the mechanism."
- "We do not know whether this improvement will transfer to handwriting from other hospital systems."

## 5.2 Model Cards & Releases
Every model release must lead with tangible capability and evidence:
- *Avoid:* "Clinical 2 represents an unprecedented leap in healthcare intelligence."
- *Prefer:* "Clinical 2 reads handwritten prescriptions more reliably and handles longer records than Clinical 1. It makes fewer extraction errors on structured discharge summaries but remains limited on low-resolution scans."

## 5.3 Medical & Safety Language
Medical writing must be rigorous without becoming sterile:
- Distinguish between: extracted information, model interpretation, clinical finding, suggestion, uncertainty, diagnosis, and recommendation.
- Never imply that a system has made a diagnosis when it has only summarized or classified information.
- Safety copy must reduce ambiguity, not merely reduce legal exposure: "This result should be reviewed before it is used for a clinical decision."

---

# Part 6 — Editorial, Brand & Operational Voice

## 6.1 Headlines
Headlines should be interesting without becoming theatrical.
- *Avoid:* "The dawn of biological intelligence."
- *Prefer:* "Understanding whole patient histories in one pass."
- *Avoid:* "Transforming healthcare through AI."
- *Prefer:* "Extracting clinical records with fewer errors."

## 6.2 Changelogs & Incident Reports
- State what changed or what failed directly.
- *Avoid:* "We squashed some nasty bugs and sprinkled performance magic."
- *Prefer:* "Fixed an issue where PDF uploads larger than 50MB failed without an error message."
- *Incident communication:* State the issue, the impact, what is working, and when the next update will occur.

## 6.3 Careers & About
- Describe the actual daily work, the team, and the physical location (Mumbai, India).
- Never use startup clichés: "rockstars", "ninjas", "change the world", "fast-paced environment".

---

# Part 7 — Common Rewrites & The 14-Question Final Test

## 7.1 Common Rewrites Table

| Category | Avoid | Prefer |
| --- | --- | --- |
| **Marketing → Useful** | "Experience the power of advanced clinical intelligence." | "Review reports, prescriptions, and patient histories in one place." |
| **Vague → Specific** | "Improved performance across complex medical tasks." | "The model reads prescriptions more reliably and makes fewer extraction errors on long reports." |
| **Technical → Human** | "40% lower inference cost." | "A typical workload that cost ₹100 before now costs about ₹60." |
| **Defensive → Honest** | "Results may occasionally vary in certain edge cases." | "Poor scans and uncommon abbreviations remain the largest sources of error." |
| **Corporate → Direct** | "We are currently experiencing degraded performance." | "Document processing is slower than usual. We are investigating the cause." |
| **Blaming → Helpful** | "Invalid file format provided." | "We could not read this file. Try uploading the original PDF or a clearer scan." |
| **Feature → Use Case** | "Long-context reasoning." | "Ask questions across an entire patient history." |
| **Praise → Evidence** | "Our most powerful model yet." | "Clinical 2 handles longer records and reads handwriting more reliably than Clinical 1." |

## 7.2 The 14-Question Pre-Publication Test

Before publishing any interface, component, article, or release note, ask:
1. Does this tell the person what they actually need to know?
2. Is the interface so simple that a grandmother could use it without hesitation?
3. Could a useful number replace an adjective?
4. Are we describing the product, or advertising the idea of the product?
5. Are we saying something because it matters, or because the page felt empty?
6. Could this be shorter without losing meaning?
7. Are we making an uncertain claim sound certain?
8. Are we hiding a relevant limitation?
9. Are we exposing technical detail that the reader does not need yet?
10. Would a human-scale example explain this better?
11. Does the interface describe what is actually happening?
12. Does the call to action say what happens next?
13. Could this sentence belong to almost any technology company?
14. If this sentence or component disappears and nothing is lost, have we removed it?
