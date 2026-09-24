---
name: substrate
description: "The complete dark-field laboratory design system, component architecture, interactive specimen doctrine, and brand language guidelines for Substrate Labs (substrates.in). Apply whenever designing, building, or writing interfaces, specimen canvases, articles, product copy, or scientific publications for Substrate."
---

# Substrate Labs — Design System & Brand Language

A unified dark-field laboratory identity, component engineering system, and brand language for Substrate Labs (`substrates.in`).

> Every page is a specimen slide on a black microscope field — grey is structure, red is stimulus, green is response. The writing is clear, calm, capable, and human. The work comes first.

This master skill consolidates two core disciplines into a single operating standard:
1. **[Design System](#part-1--the-dark-field-laboratory-design-system)** ([references/design-system.md](./references/design-system.md)): Dark-field laboratory identity, 8-color vial/observed token system, typography, 4-tier container scale, canvas specimens, and the 18 rich article components.
2. **[Brand Language & Writing Voice](#part-2--substrate-voice--core-qualities)** ([references/brand-language.md](./references/brand-language.md)): Product copy, interface microcopy, research updates, technical papers, clinical/medical safety, release headlines, and the 14-question pre-publication test.

---

## Core Non-Negotiables

1. **The Ground is Void:** Pure black (`#000000`), edge to edge. It is not a dark theme; it is the absence of a lamp. Light mode does not exist, is not hidden behind a toggle, and will never be planned.
2. **The Signal is Strict:** Exactly two colors mean things. **Blood red (`#B51F2E` observed / `#8B0000` vial) is stimulus** — user activation, selection, focus rings, alerts, action potentials. **Bio green (`#39D353` observed / `#39FF88` vial) is response** — synapse confirmed, living organism, success. Never use red or green for decoration. Never admit a fifth hue (no blue, no purple).
3. **The DOM is Still; Life Happens in the Canvas:** Chrome never twinkles, blinks, or decorates itself with CSS keyframes. All motion lives inside HTML5 Canvas preparations (`NeuralSpecimen`, `SpecimenField`, `SignalSpecimen`). All canvases must honor `prefers-reduced-motion` with a dormant static frame.
4. **4-Tier Container Architecture:** All publishing surfaces follow strict container bounds: Prose text (`680px`), Media figures/tables/code (`1140px`), Wide/Dense charts and diagrams (`1280px`), and Page shell (`1440px`).
5. **Hairlines Over Boxes:** Density and structure are achieved via hairlines (`rgba(255,255,255,0.14)` and `0.08`–`0.18`) and negative void space, never via drop shadows, blurred glass, or floating cards.
6. **Confidence Without Theatre:** State things plainly. Never manufacture excitement around ordinary progress. Never make ambitious work vague to sound impressive.
7. **Literal Interface Language:** Interfaces describe what is actually happening. Use "Reading document…" never "Thinking…"; use "Report deleted" never "Success! Your report has been successfully deleted".
8. **Evidence Before Adjectives:** Never rely on empty praise ("revolutionary", "powerful", "seamless", "next-generation"). If something improved, state the evidence and replace the adjective with a human-scale number.
9. **Human-Scale Numbers First:** Translate raw infrastructure metrics into human terms before giving technical specifications (e.g. "A 300-page record takes about 2½ minutes to process" before stating "120 pages per minute").
10. **Unapologetic Honesty About Limitations:** State uncertainty and limitations with the same clarity and confidence as capabilities. A limitation that materially affects use belongs near the relevant capability, not buried in legal disclaimers.

---

## Mandatory Reference Inspection

> [!IMPORTANT]
> **Agents and developers must inspect the corresponding reference documentation when executing deep tasks:**
> - **[`references/design-system.md`](./references/design-system.md)**: Inspect before modifying UI tokens, layout containers, specimen canvases, or article components.
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

rounded:
  sm: 0px           # Default for chrome, containers, buttons, inputs
  md: 2px           # Concession for code boxes, tags, media frames
  pill: 9999px      # Concession for HomePillBanner and navigation back button
```

## 1.2 Typography Hierarchy

- **Relative Sans (variable, 100–900)**: The calm, neutral, precise voice of the lab. Used for all reading prose, body descriptions, and section subtitles.
- **Relative Mono (variable, 100–900)**: The instrument's handwriting. Used for reticle coordinates, dates, status tags, table headers, math/code, and navigation metadata. Tracked out (`0.14em`–`0.22em`), uppercase, weight `500`.
- **Geist Pixel Square**: The shout. Monolithic uppercase pixel headline (`SUBSTRATE LABS`, `NOT FOUND`). Exactly one shout per surface. Fluidly rendered at `clamp(2.8rem, 9.6vw, 9.4rem)`.

## 1.3 Layout & 4-Tier Container System

1. **The Single-Slide Ground (Homepage)**:
   - Header with LCP brand mark (`24px`–`32px`, priority preloaded) and mono links (`Newsroom`, email, handle).
   - Central observation field with `NeuralSpecimen` and anchored `HomePillBanner`.
   - Bottom editorial footer with pixel display shout and quiet metadata row (`COMING SOON`).
2. **The 4-Tier Editorial Architecture**:
   - `article-frame` (`680px`): Reading column for prose, pull quotes, audio player, and footnotes.
   - `article-frame-wide` (`1140px`): Media figures, code blocks, data tables, and metrics.
   - `article-frame-full` (`1280px`): High-density ECharts, Mermaid diagrams, and multi-column media groups.
   - `publishing-nav` / `publishing-footer` (`1440px`): Global header grid and bottom colophon.

## 1.4 Canvas Specimen Preparations

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

# Part 2 — Substrate Voice & Core Qualities

Substrate sounds **clear, calm, capable, and human**.

The writing never needs to prove that the company is intelligent, serious, transparent, humane, technically capable, or ambitious. Those qualities must be apparent from the work, the evidence, the decisions we explain, and the way we speak to people.

## 2.1 Calm
Sound composed. Never use urgency, exaggerated excitement, dramatic framing, or inflated language to make ordinary work feel consequential.

- *Avoid:* "This changes everything." / "A new era begins today." / "The future of medicine starts here."
- *Prefer:* "Clinical 1 is available today." / "We have started testing the model on longer patient records." / "Document processing is currently delayed."

## 2.2 Confident
State what is known without unnecessary hedging. Confidence should come from knowing what the evidence supports.

- *Avoid:* "We believe Clinical 1 may potentially offer improvements when working with longer records."
- *Prefer:* "Clinical 1 handles longer records than the previous model."

## 2.3 Straightforward
Get to the point early. Do not introduce a simple idea with multiple lines of setup. Do not hide an inconvenient fact behind formal corporate language.

- *Avoid:* "We are currently experiencing a temporary degradation in certain parts of the document processing experience."
- *Prefer:* "Document processing is delayed. Uploads are working normally, but results may take longer than usual."

## 2.4 Humane
Write for the person using the product. Put the useful human meaning before the engineering specification.

- *Avoid leading with:* "200K context window."
- *Prefer leading with:* "You can give it an entire patient history and ask questions across it."
- *Avoid leading with:* "40% lower inference cost."
- *Prefer leading with:* "A workload that previously cost about ₹100 now costs about ₹60."

## 2.5 Kind
Do not blame people for errors. Do not make someone feel uninformed because they do not understand a technical term. Do not hide bad news behind cheerful language.

- *Avoid:* "Invalid user configuration."
- *Prefer:* "This device is using a setting the system does not currently support."
- *Avoid:* "Invalid file uploaded."
- *Prefer:* "We could not read this file. Try uploading the original PDF or a clearer scan."

---

# Part 3 — Product & Interface Writing Language

## 3.1 Literal Interface States
Interfaces must describe what is actually happening.

| State | Avoid | Prefer |
| --- | --- | --- |
| **Loading** | "Thinking…" / "Working its magic…" / "Understanding your health…" | "Reading document…" / "Extracting clinical information…" / "Comparing reports…" |
| **Errors** | "Something went wrong." | "We could not read this file. Try uploading the original PDF or a clearer scan." |
| **Empty States** | "Nothing here yet. Your journey starts when you upload your first report." | "No reports yet. Upload a document to begin." |
| **Confirmations**| "Success! Your report has been successfully deleted." | "Report deleted." / "Changes saved." |
| **Buttons / CTAs**| "Get started" / "Explore" / "Continue" | "Upload report" / "Compare reports" / "Review fields" / "Download PDF" |

## 3.2 Banned Filler & Pseudo Labels
Every word must explain what something is, help someone decide, or communicate a limitation.
- *Avoid:* "Your clinical intelligence workspace" → *Prefer:* "Recent reports"
- *Avoid:* "Begin your document analysis journey" → *Prefer:* "Upload report"
- *Rule:* If a label or heading can disappear without making the interface harder to understand, remove it. Whitespace is always better than filler.

## 3.3 Uncertainty & Limitations
Uncertainty is an inherent part of scientific systems. State it directly and locally.
- *Avoid:* "AI can make mistakes."
- *Prefer:* "The model could not determine this value reliably." / "The model found two possible readings for this value. Check the original report."
- *Rule:* Explain limitations with the same confidence as capabilities: "Poor scans and uncommon abbreviations remain the largest sources of error."

---

# Part 4 — Research, Technical & Clinical Communication

## 4.1 Research Writing
Distinguish clearly between what was observed, what is inferred, and what remains uncertain:
- "The model extracted 91% of medications correctly on this evaluation set."
- "This suggests the additional pre-training data improved abbreviation recognition, though we have not verified the mechanism."
- "We do not know whether this improvement will transfer to handwriting from other hospital systems."

## 4.2 Model Cards & Releases
Every model release must lead with tangible capability and evidence:
- *Avoid:* "Clinical 2 represents an unprecedented leap in healthcare intelligence."
- *Prefer:* "Clinical 2 reads handwritten prescriptions more reliably and handles longer records than Clinical 1. It makes fewer extraction errors on structured discharge summaries but remains limited on low-resolution scans."

## 4.3 Medical & Safety Language
Medical writing must be rigorous without becoming sterile:
- Distinguish between: extracted information, model interpretation, clinical finding, suggestion, uncertainty, diagnosis, and recommendation.
- Never imply that a system has made a diagnosis when it has only summarized or classified information.
- Safety copy must reduce ambiguity, not merely reduce legal exposure: "This result should be reviewed before it is used for a clinical decision."

---

# Part 5 — Editorial, Brand & Operational Voice

## 5.1 Headlines
Headlines should be interesting without becoming theatrical.
- *Avoid:* "The dawn of biological intelligence."
- *Prefer:* "Understanding whole patient histories in one pass."
- *Avoid:* "Transforming healthcare through AI."
- *Prefer:* "Extracting clinical records with fewer errors."

## 5.2 Changelogs & Incident Reports
- State what changed or what failed directly.
- *Avoid:* "We squashed some nasty bugs and sprinkled performance magic."
- *Prefer:* "Fixed an issue where PDF uploads larger than 50MB failed without an error message."
- *Incident communication:* State the issue, the impact, what is working, and when the next update will occur.

## 5.3 Careers & About
- Describe the actual daily work, the team, and the physical location (Mumbai, India).
- Never use startup clichés: "rockstars", "ninjas", "change the world", "fast-paced environment".

---

# Part 6 — Common Rewrites & The 14-Question Final Test

## 6.1 Common Rewrites Table

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

## 6.2 The 14-Question Pre-Publication Test

Before publishing any interface, component, article, or release note, ask:
1. Does this tell the person what they actually need to know?
2. Could a useful number replace an adjective?
3. Are we describing the product, or advertising the idea of the product?
4. Are we saying something because it matters, or because the page felt empty?
5. Could this be shorter without losing meaning?
6. Are we making an uncertain claim sound certain?
7. Are we hiding a relevant limitation?
8. Are we exposing technical detail that the reader does not need yet?
9. Would a human-scale example explain this better?
10. Does the interface describe what is actually happening?
11. Does the call to action say what happens next?
12. Could this sentence belong to almost any technology company?
13. Is there any drama that the facts themselves do not justify?
14. If this sentence or component disappears and nothing is lost, have we removed it?
