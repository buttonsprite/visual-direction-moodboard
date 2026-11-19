# From Reference Research to Shared Visual Direction (Playbook)

Stages 1–5 form the default co-creative loop, with Stages 2–4 repeating as taste sharpens. When a concrete execution question arises and the user wants to test treatments, jump directly from Stage 4 to Stage 6 for small controlled trials, then return to search or synthesis. Always carry forward known context, preferences, and delegation without re-asking.

---

## Stage 1: Align Starting Point & Clues

1. **Read context first**: Extract the design subject, audience, context of use, and hard constraints from existing conversation and project files. Separate verified facts from agent assumptions.
2. **Ask minimally**: Only ask **1–3 short questions** if you genuinely do not know *what* is being designed, *where* it lives, or *what problem* this round solves. Wait for answers before searching. If the user explicitly wants open-ended inspiration, treat open exploration as the goal.
3. **Never demand a style label upfront**: "I don't know what style I like yet" is the exact problem this workflow solves. Do not ask the user to pick fonts, colors, or style names before showing real work.
4. **Preserve raw cues**:
   - Starting from scratch: propose 2–4 contrasting keyword clusters (drawn from eras, music, materials, places, or sensory scenes).
   - Keywords given: search the user's exact terms directly while adding related expansions for comparison.
   - References given: inspect the full project, studio, and series applications first, then branch outward.
   - Specific design problem given: organize search directly around the problem (e.g., photo cropping, dark-background typography, series consistency) without forcing a full brand brief first.

> Once clues are enough to search, start searching immediately — do not add a redundant "Shall I begin?" gate.

---

## Stage 2: Curated Search & Asset Reliability

### 1. Multi-Lingual & Cross-Medium Query Expansion
- **Translate mood into craft terms**: Expand intuitive mood words (e.g., "warm, rough, handmade") into professional design queries across English and relevant design cultures (e.g., `risograph editorial poster`, `tactile packaging typography`, `swiss grid zine`, `装丁 デザイン`). Always keep **user words** distinct from **agent expansions**.
- **Search across mediums**: Look beyond direct product competitors into posters, book design, album sleeves, exhibition identity, packaging, architectural photography, and editorial web to avoid category clichés.
- **Multiple interpretations per keyword**: Surface at least **2 visually distinct interpretations** per core keyword, plus 1–2 boundary cases that help the user draw a clear "yes / not this" line.

### 2. High-Signal Sources & Anti-Slop Filtering
- **Prioritize**: Studio portfolios, full Behance case studies, Are.na channels, Fonts In Use, It's Nice That, Brand New, Awwwards, Cosmos, ArchDaily, Read.cv, design annuals, and independent publishing archives.
- **Filter out**: AI-generated image dumps, generic template marketplaces, and low-res re-pinned collages. Never pass AI-generated images off as real design references.
- **Follow strong leads to full projects**: When a promising reference appears, inspect the complete project to see how the system handles layouts, typography, details, and series variations rather than stopping at an isolated thumbnail.

### 3. First-Round Volume & Local Image Caching
- **Volume target**: Collect **15–30 distinct, valid works** in Round 1 (10–15 for a tightly scoped single problem). Paginate or group by keyword when exceeding 24 items. Document actual coverage and known search gaps honestly.
- **Stable IDs**: Assign sequential IDs (`I001`, `I002`…) that never change across rounds, tabs, or exports. One work may carry multiple keyword tags.
- **Local caching to prevent broken images**: Many design sites block hotlinking. **Download verified previews into `assets/` and link them via relative paths in HTML.** Collapse unreachable or broken sources with reasons rather than leaving broken thumbnails in the gallery.
- **Clean status separation**: Track four non-overlapping states: `Candidate`, `Agent Pick`, `User Selected`, and `Collapsed (with reason)`. Recommendations never overwrite candidate records; mark unverified items honestly.

---

## Stage 3: Deliver a Zero-Dependency Interactive Gallery

### 1. Default Format: Self-Contained Single-File HTML
Generate `image-selection.html` referencing local `assets/` images so the user can double-click and open it immediately — no local server required, portable, and easy to share:
- **Image-first layout**: Large, sharp thumbnails with restrained spacing. Show only `ID + short title + keyword tags + original project link` on cards; put longer notes in the detail modal or `notes.md`.
- **Full-frame lightbox**: Clicking an image opens its full uncropped composition (never force destructive square crops). Allow cycling through series or detail shots when available.
- **Clear views & counts**: Provide view tabs (`All Candidates` / `New This Round` / `Agent Picks` / `Selected`) + keyword filter pills + `Clear Filters`. Display live counts with explicit units (e.g., `24 references · 14 projects`). Keep a collapsible section at the bottom for duplicates or broken links.
- **Low-friction marking & one-click export**: Let users tag items as `Like`, `Maybe`, or `No` with an optional one-line note (saved in `localStorage`). Pin a prominent **Copy Selection Feedback** button that copies a clean `ID + keyword + rating + note` summary ready to paste straight back into chat.

> Only spin up a local server if the environment strictly requires it; if used, verify the page stays reachable *after* startup returns, verify selections survive restart, and never hand out a temporary `localhost` URL as a shareable link.

### 2. Pre-Delivery Check & Guided Opening
- **Verify before handing off**: Confirm images load cleanly, lightbox works, IDs and keywords match, original links open, and one-click copy outputs valid text. Note anything that could not be verified.
- **Lead with 2–3 contrast pairs**: Never just drop a file path and ask "Which do you like?" Highlight 2–3 contrasting pairs to spark immediate judgment (e.g., *"For 'rough handmade', compare `I004` (coarse single-ink halftone) vs. `I011` (warm thick paper & generous whitespace) — which direction feels closer?"*).
- **Wait for actual feedback**: Do not synthesize or declare a direction before reading the user's reply or pasted export.

---

## Stage 4: Art-Director Critique & Next Round

Start from the specific IDs or reactions the user calls out. **Record user quotes verbatim** and keep them separate from agent analysis.

### 1. Five-Dimension Craft Breakdown
When a user gives an intuitive reaction (*"I love `I012`"* or *"`I007` feels cheesy"*), translate it into concrete craft decisions across five lenses:
1. **Type-to-Image Hierarchy**: Overlay vs. framed photo window vs. full bleed; hairline serif vs. heavy display contrast.
2. **Color & Contrast**: Low-saturation paper tones vs. bold chromatic tension vs. monochrome + single accent.
3. **Material & Print Craft**: Coarse halftone, paper fiber, film grain, glass/metal speculars, crisp digital flat.
4. **Composition & Cropping**: Breathing whitespace, extreme close-up crop, symmetrical formality, collage tension.
5. **Series Scalability**: Does this system still hold up when swapped from a hero photo to ordinary real-world user content?

### 2. Route the Next Round by Feedback
- **Strong anchor**: Dig deeper into the full project, creator, studio, or craft technique; bring back validating references.
- **Multiple appealing directions**: Keep the divergence alive as 2 parallel tracks instead of prematurely blending them.
- **Partial appreciation**: Isolate the single loved element (e.g., *"keep the headline scale, drop the dark brown palette"*) and search across other styles so you don't copy the whole piece wholesale.
- **Concrete execution question**: Narrow search to that problem, or — with user buy-in — jump to **Stage 6** for a small controlled trial.
- **Nothing fits**: Diagnose with user quotes whether the mismatch is semantic, medium-based, or tonal (too vintage / too corporate), then revise keywords and pivot.
- **Consensus is clear**: Move straight to **Stage 5** synthesis without unnecessary confirmation ceremony.

Continue sequential numbering for new candidates, tag them as `New This Round` with the rationale for adding them, and keep prior rounds intact.

---

## Stage 5: Synthesize the Moodboard

Once selections and critique clearly support one or more directions (or explicit delegation was granted):

1. **Frame the directions**: Build one board if choices align, or 2–3 clearly distinct boards if genuine aesthetic forks remain. Name each direction here.
2. **Lead with fidelity**: Anchor each board around hero works, detail crops, and series applications. Do not cram every selected image onto one canvas — record curation trade-offs in notes. If a collage weakens the artwork, present it as a clean reference page instead.
3. **Three-part rationale**: For each direction, connect **Key craft decisions in the references → How they translate to this project → What still needs validation**.
4. **Preserve attribution & traceability**: Clearly label any bridging references added by the agent, and keep direct links back to the full candidate gallery and critique notes.

> If the user only asked for a moodboard, deliver and stop here. Distinguish clearly between *visual direction aligned* and *original brand/UI finalized*.

---

## Stage 6: Controlled Trials with Real Content (On Demand)

Enter only when the user asks for drafts, photo treatments, or interface explorations. Trials are discussion probes, never automatic finals.

1. **Be honest about craft provenance**: Separate *documented original process*, *agent approximation*, and *material boundaries*. Mark unknown processes as unknown — never describe a digital filter as reproducing an analog print process.
2. **Two comparison axes** (start small; do not exhaustively permute everything):
   - **Same input, multiple methods**: Apply 2–3 treatments/layouts to one real asset to compare tone.
   - **Same method, multiple inputs**: Apply a promising method across 3–5 diverse real assets (varying lighting, composition, subject) to test robustness.
3. **Control variables & show layers**: Keep product goal, real copy pool, aspect ratio, and core functionality constant across directions while varying layout, crop, and treatment. When helpful, show `Original Reference → Project Raw Asset → Treatment → Final Layout` so issues are easy to diagnose.
4. **Separate trial IDs & feedback**: Number trials independently (`T001`+, referencing `from I012`). **Liking a reference ≠ approving a trial's crop, occlusion, or typography** — log them separately.
5. **Diagnose & hand off**: When a trial misses the mark, isolate which variable failed (color, texture, scale, hierarchy, or source asset) and adjust only that variable next round. After user confirmation, distill verified rules (color roles, typography, image treatment, layout, motion) into `visual-language.md`, linking each rule to its supporting references and approved trials.
