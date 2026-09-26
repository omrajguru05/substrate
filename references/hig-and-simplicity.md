# Substrate Labs — Brutal Simplicity, Apple HIG & Universal Accessibility

A core mandate for all Substrate interfaces, system designs, product surfaces, and components.

> "When doing the UI, the UI should be brutally simple. There should not be technical language or clutter. The UI should be so easy that even a grandmother can use it. Very few buttons, no clutter, no complex UI. The app should be very simple, hiding complex things behind the scenes — even when doing system design, the model must be compliant to this."

Every user interface, component, and interaction in Substrate must be fully compliant with the Apple Human Interface Guidelines and auditable via `omrajguru/hig-compliance-auditor`.

---

## 1. The Grandma Standard (Brutal Simplicity)

1. **Zero Technical Jargon:**
   - Never expose database concepts, pipeline states, inference tokens, memory buffers, or server architecture to the user.
   - Speak in clear, human, direct terms: what does this document mean, what can you do with it, and what happens next.
2. **Minimal Buttons & Zero Clutter:**
   - Every screen should have one obvious primary action, not five competing actuators.
   - Remove auxiliary toggles, nested menus, and decorative badges.
   - If a screen feels busy, remove controls until only the essentials remain.
3. **Hide Complexity Behind the Scenes:**
   - Multi-step biological computations, model pipelines, file normalization, and OCR parsing must happen quietly in the background.
   - The user sees only a calm status ("Reading document…", "Preparing summary…") and the final clear result.
   - System design and data models must absorb complexity so the user never has to manage it.
4. **Forgiving by Default:**
   - Destructive actions must be clearly explained with instant, friction-free undo or confirmation.
   - Inputs must accept natural variations (e.g. flexible date formats, drag-and-drop or file pickers) without throwing cryptic errors.

---

## 2. Apple HIG Core Design Principles

Every interface must embody these eight foundational principles:

### 1. Purpose — Design with Intention
Identify what matters most to people and focus relentlessly on making those core tasks effortless. Resist feature bloat and secondary distractions.

### 2. Agency — Let People Act Their Own Way
Give people freedom, keep them continuously informed of system state, and make recovery from mistakes easy, painless, and obvious.

### 3. Responsibility — Act in People's Best Interest
Prioritize patient and user safety, data privacy, and complete transparency about what the product does. Disclose limitations where they matter.

### 4. Familiarity — Build on What People Know
Use established physical and digital patterns consistently. A search field looks like a search field; a back button takes you back; reading text flows naturally. Never invent unprompted, proprietary interaction paradigms for basic tasks.

### 5. Flexibility — Adapt to Diverse Contexts & Needs
Support diverse devices, screen sizes, input methods (touch, pointer, keyboard, assistive hardware), orientations, and human perspectives.

### 6. Simplicity — Be Clear and Direct
Remove the unnecessary; every element must earn its place. Whitespace is a first-class structural material. If an element does not help someone understand or act, delete it.

### 7. Craft — Care About Every Detail
Show dedication through thoughtful execution, smooth 60fps/120fps interactions, exact pixel alignments, consistent typography, and robust error resilience.

### 8. Delight — Make It Human
Design for the emotions you want to inspire: calm, trust, reassurance, and satisfaction. Delight in Substrate comes from quiet competence and clarity, never from theatrical animations or gimmicks.

---

## 3. Accessibility Foundations

An accessible interface is:
- **Intuitive:** Uses familiar, predictable, and consistent interactions that make tasks completely straightforward.
- **Perceivable:** Never relies on a single sensory method to convey information. Information is accessible through sight, hearing, and touch.
- **Adaptable:** Flexibly adapts to how people want to use their device, honoring Dynamic Type, system font scaling, reduced motion, and assistive personalization.

---

## 4. The Six Disability Categories & Implementation Standards

### 1. Vision
- **Text Sizing & Fluid Scale:** Typography must scale fluidly across viewports without clipping, truncating, or breaking containers. Support larger text sizes gracefully.
- **Strict Contrast Ratios:** Meet WCAG AAA contrast where feasible (minimum 4.5:1 for body copy; 7:1 for fine metadata). The pure black ground (`#000000`) paired with observed text (`#A3A3A3` and `#FFFFFF`) provides high, crisp readability without glare.
- **Dual-Channel Signaling (Never Color Alone):** Blood-red and bio-green must never be the sole conveyor of meaning. Pair colors with icons, labels, shapes, or structural positions.
- **Screen Reader Hierarchy:** Full semantic HTML (`header`, `main`, `footer`, `nav`, `article`, `figure`, `figcaption`). Provide descriptive `alt` text for images, captions for videos, and visually-hidden context (`.sr-only`) for screen readers when the visual surface is intentionally minimal.

### 2. Hearing
- **Text Alternatives:** Provide comprehensive text-based alternatives for all audio and video assets (transcripts, closed captions, written summaries).
- **Multi-Sensory Cues:** Pair all audio feedback with visual indicators (e.g. status changes, glowing dots, progress bars).

### 3. Mobility
- **44×44px Minimum Touch Targets:** Every interactive element (buttons, links, menu items, audio scrubbers, pagination pills) must have a touch target of at least 44×44 CSS pixels, regardless of its visual font size.
- **Adequate Spacing:** Separate interactive actuators by at least 8px to prevent accidental taps, especially on mobile.
- **Full Keyboard Navigation:** All interactive elements must be focusable via Tab and activatable via Enter/Space. Focus rings must be prominent and unambiguous:
  ```css
  :focus-visible {
    outline: 2px solid #b51f2e;
    outline-offset: 4px;
  }
  ```
- **Simple Gestures:** Never require complex multi-finger gestures, precision drags, or velocity-dependent actions for core navigation. Always provide standard tap/click alternatives.

### 4. Speech
- Allow 100% keyboard-only and pointer-only navigation.
- Ensure the interface functions flawlessly with Switch Control, Full Keyboard Access, and Voice Control accessibility features.

### 5. Cognitive
- **Streamlined Single-Path Tasks:** Present one decision at a time. Group related items logically; avoid fragmented choices.
- **No Time-Boxes:** Never impose artificial countdowns, expiring sessions, or timed interaction traps on normal reading or review tasks.
- **Avoid Excessive Animation:** Keep DOM elements still. The user must never have to chase moving buttons or read jumping text.
- **Full Media Control:** Never autoplay audio or unmuted video. Allow users to pause, scrub, and stop any playback at will.
- **Predictable Error Recovery:** When an error occurs, explain exactly what went wrong and provide a single, direct path to fix it (e.g. "We could not read this file. Try uploading the original PDF or a clearer scan.").

### 6. Motion
- **Respect `prefers-reduced-motion`:** All canvas specimens (`NeuralSpecimen`, `SpecimenField`, `SignalSpecimen`) and CSS transitions must listen to `window.matchMedia('(prefers-reduced-motion: reduce)')`. When active, freeze all loops immediately and render a calm, static frame.
- **Keep Elements in View:** Avoid abrupt camera shifts, disorienting parallax, or head-anchored content that strains visual comfort.

---

## 5. Architectural & System Design Compliance

The requirement for brutal simplicity applies not only to the UI, but to the **underlying system design and data models**:

1. **Absorb Complexity in the Architecture:**
   - If an operation requires 4 API calls, background file polling, and format conversion, wrap that in a single backend orchestration service.
   - The frontend should only observe a simple status enum: `idle | reading | ready | error`.
2. **Deterministic State Modeling:**
   - Eliminate race conditions, half-loaded states, and flicker. State transitions must be linear and predictable.
3. **Resilient Data Contracts:**
   - When external models or Sanity CMS return empty arrays or missing optional fields, fail gracefully with clean fallback copy rather than rendering broken layouts or error screens.
