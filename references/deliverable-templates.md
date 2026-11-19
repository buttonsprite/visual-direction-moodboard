# Deliverable & Record Templates

Use only what the current round needs — never force every file in Round 1. Rule of thumb: **the gallery handles visual inspection and low-friction feedback; Markdown handles lightweight traceability.**

---

## 1. Light Exploration Log: `notes.md` (Round 1 Default)

Combine brief, keyword routes, and round-by-round critique into one clean file for fast iteration.

```markdown
# <Project Name> · Visual Direction Notes

## 1. Starting Point
- **Subject & Context**:
- **Known Constraints**:
- **User Quotes & Initial Instincts**:
- **What This Round Should Clarify**:

## 2. Keyword Routes
| ID | User Term | Agent Expansions (EN / Cross-Medium) | Sources Covered | Known Gaps |
| --- | --- | --- | --- | --- |
| W01 | warm, rough, handmade | risograph editorial, tactile paper print | Behance, Are.na, Fonts In Use | Few mobile UI examples |

## 3. Critique & Revisions (append per round)
### Round 1
- **User Picks & Verbatim Quotes**:
  - `I004` (Like): "Great type-to-image breathing room"
  - `I011` (No): "Too dark and heavy"
- **Five-Dimension Craft Read (Agent)**:
  - Type-to-image: generous margins + light serif headline
  - Color: drop heavy browns; shift to warm paper white + fresh single accent
- **Next Move**: Inspect full project behind `I004`; add 8 lighter-palette layout references (`I025`–`I032`)
```

---

## 2. Single-File Candidate Gallery: `image-selection.html` Spec

Default to a zero-dependency single HTML file referencing local `assets/` images (instant double-click open, no broken hotlinks, portable):

### Required UI & Interactions
1. **Top bar**: Project title, view tabs (`All Candidates` / `New This Round` / `Agent Picks` / `Selected`), keyword filter pills, `Clear Filters`, and live counter with explicit units (e.g., `Showing 18 / 24 references · 14 projects`).
2. **Card grid**: Large crisp previews, stable ID (`I001`), short title, keyword tags, original project link icon, 3 quick-tag buttons (`Like` / `Maybe` / `No`), and an optional one-line note input.
3. **Full-frame lightbox**: Click any image to inspect full uncropped composition, metadata, original source link, 1-line agent craft note, and series/detail shots if available.
4. **Collapsed section**: Expandable footer listing duplicates, broken links, or filtered items with reasons.
5. **Sticky export bar (essential)**: Persist ratings in `localStorage` and provide a prominent **Copy Selection Feedback** button that copies this exact chat-ready format:

```text
[Visual Reference Feedback · Round 1]
- Like:
  - I004 [W01 warm-rough]: Love the type-to-image ratio and whitespace
  - I012 [W02 paper-print]: Like the paper grain, not the dark palette
- Maybe:
  - I018 [W01 warm-rough]:
- No:
  - I007 [W01 warm-rough]: Feels like a generic template
```

### Standard Handoff Message
```text
This round started from "<user terms>" and expanded into <routes>, curating <N> real design references (from <M> projects), cached locally.

👉 Open gallery: <path to image-selection.html>

A few high-contrast pairs to start with:
1. <I00X> vs. <I00Y>: <one-line craft difference>
2. <I00A> vs. <I00B>: <one-line craft difference>

Mark Like / Maybe / No directly in the gallery and hit "Copy Selection Feedback" to paste it back here — or just reply with IDs and gut reactions.
```

---

## 3. Candidate Ledger: `source-manifest.md` (Multi-Round / Project Mode)

Keep in sync with the gallery's embedded JSON when formal traceability is needed:

```markdown
### I001 · <Project or Work Title>
- **Local Preview / Source URL**: `assets/I001.jpg` | <URL>
- **Creator / Year / Archive**: <mark unknown if unavailable>
- **Keyword & Query**: `W01` · `risograph editorial poster`
- **Craft Note (Agent Initial Read)**: Coarse single-ink halftone + edge-hugging display type
- **Status**: `Candidate` / `Agent Pick` / `User Selected` / `Collapsed (reason)`
- **User Quote**: <leave blank until feedback>
- **Series / Details**: <if any>
```

---

## 4. Moodboard Synthesis: `moodboard.html` / Direction Structure

Repeat per distinct direction (let large images and series relationships carry the story):

```markdown
# Direction A: <Direction Name>

- **One-Line Tone**:
- **Basis**: Built from user picks `I004`, `I012` and Round 1–2 critique (if agent-delegated, state explicitly)

## Key Works & Craft Decisions
- **Anchor Reference** (`I004`): <1–2 decisive visual moves, e.g., type-to-image ratio & margins>
- **Supporting & Detail References** (`I012`, `I019`): <texture, color, or series extensions>
- **Agent Bridging References** (if any, state purpose):

## Translation to This Project
- **Keep & adapt**:
- **Explicitly avoid**:
- **Open for trial validation**:

## Back-Links
- Candidate gallery: `image-selection.html` · Notes: `notes.md`
```

---

## 5. Living Decision Log: `decision.md` (Multi-Round Projects)

Pin current truth at the top; log round history below:

```markdown
# <Project Name> · Visual Decision Log

## Current Status (Latest)
- **Confirmed**: <scope, user basis, artifact>
- **Comparing**: <open directions & links>
- **Dropped**: <direction & reason>
- **Next Question**:

## Round History
- **Round 2 (date)**: ...
- **Round 1 (date)**: ...
```

---

## 6. Controlled Trials & Visual Handoff: `ui-drafts/` & `visual-language.md`

Use when entering Stage 6:

```markdown
# <Project Name> · Trial Validation

## Trial Question
- **Key screen / interaction**:
- **Controlled variables (fixed)**: real copy pool, aspect ratio, core actions
- **Tested variables (changed)**: layout / crop / image treatment / color
- **Comparison axis**: Same input, multiple methods (`T001`–`T003`) / Same method, multiple inputs (`T004`–`T008`)

## Process & Boundaries
- **Documented original craft**: <unknown if unpublished>
- **Agent approximation**: <method & known differences>
- **Material boundaries**: <which inputs work well vs. break>

## Separate Feedback Record
- **Reference preference**: <what the user liked in the original work>
- **Trial reaction**: <accepted / rejected crop, occlusion, or type-to-image hierarchy>
- **Next round**: keep X / change Y

## Visual Language Handoff (verified rules only)
- **Color roles / Type-to-image / Image treatment / Composition & motion**:
- **Supporting trials & reference IDs**:
- **Still unverified / open**:
```
