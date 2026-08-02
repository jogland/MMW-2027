---
brand: MMW8 (Medellín Music Week, Edition 8)
version: 0.2
last_updated: 2026-08-02
applies_to: [decks, landing-pages, case-studies, social-posts]
---

# MMW8 Brand Core
> Source of truth for all AI-generated artifacts. Artifact-specific files
> (deck-guidelines.md, web-guidelines.md, social-guidelines.md) reference
> this file and should never override values here without updating this
> file first.

---

## 1. Logo

**Files:** `/assets/logo/mmw8-lockup.svg`, `/assets/logo/mmw8-mark-only.svg`

| Property | Value |
|---|---|
| Clearspace | logo height ÷ 2, on all sides |
| Minimum width (digital) | 120px |
| Minimum width (print) | 25mm |
| Approved backgrounds | #0A0A0A (black), #FFFFFF (white), Primary Purple (#6B2FD6) |
| Never | stretch, rotate, recolor outside approved backgrounds, add drop shadow |

---

## 2. Color
> Confirmed against MMW's Canva brand kit palette (Aug 2026).

| Name | Hex | Use case |
|---|---|---|
| Signal Green | #07F328 | Standard flat background |
| Cyan | #0BCBFF | Secondary accent |
| Magenta | #FF00FF | Secondary accent |
| Signal Blue | #005DF5 | Secondary accent / alt background |
| Accent Yellow | #F8FC07 | Grid squares, dots, small accents — max 10% of composition |
| Ink Black | #000000 | Text, dark neutral |
| Paper White | #FFFFFF | Light neutral, light-background artifacts (web, case studies) |

**Rule:** no more than 3 colors per artifact (1 background + 1 accent + black or white text, whichever contrasts).

**Backgrounds:** #07F328 is the standard flat background color. In most real artifacts, though, the background is a full-bleed image pulled from Canva's "Backgrounds" section rather than a flat fill. See `assets/backgrounds/` — drop a handful of representative background images there (not the full library) so I can match style, texture, and color mood when composing new artifacts. Reference the specific one by filename in each artifact's guideline file when it matters (e.g. "use `assets/backgrounds/topographic-blue.png` style for this social post").

---

## 3. Typography

| Role | Font | Weight | Case |
|---|---|---|---|
| Primary heading | Syne | Extra Bold | ALL CAPS |
| Secondary heading | Syne | Extra Bold | ALL CAPS |
| Body / Label | Roboto | Regular | Mixed / ALL CAPS for dates & locations |

**Sizing:** headings are sized as a ratio of the grid square, not a fixed pixel value — see Section 4 for the formula and confirmed ratios. This keeps sizing correct across any canvas or viewport size instead of breaking on formats other than the one it was designed on.

**Confirmed usage:** Syne Extra Bold used for event name + edition ("OCTAVA EDICIÓN 2027") and taglines like "UNA ESTACIÓN DE ENCUENTRO," all-caps. Roboto Regular used for location/date labels ("Medellín," "Colombia," "Febrero 15 - 21").

---

## 4. Grid — the compositional system
> Confirmed against MMW's Canva poster and deck (Aug 2026). This grid is
> visible in the final artifact (not a hidden alignment guide) and scales
> to any canvas size via the formula below — this is what makes it portable
> to web and to any future artifact format.

**Core formula:** `square size = shorter canvas side ÷ 5`
Confirmed on a 1080×1920 canvas: square = 216px. The grid tiles outward
from there across the full canvas (may overshoot the longer edge slightly
if it doesn't divide evenly — that's expected, not an error).

**Visual rules:**
- Grid squares are outlined in Accent Yellow (#F8FC07) and are part of the
  visible design, not a hidden guide.
- All elements (photos, text blocks, logo, cards) snap to grid lines — never placed off-grid.
- Selected squares can be filled solid Accent Yellow as compositional accents.
  This is a free creative choice, not a fixed rule, but real usage shows a
  pattern: avoid repeating the same column alignment across elements in one
  composition (vary 1-2 squares left/right between elements). For headings,
  the text's own fill-length determines which squares get used — the squares
  don't dictate a fixed text box first.
- Dot markers (small filled Accent Yellow circles) sit only at grid line
  intersections. Use 3-4 per composition maximum — this is a ceiling, not a target.
- Logo occupies exactly 2 grid squares, arranged 2 columns × 1 row.

**Headings — sized as a ratio of the grid square, not a fixed pixel value.**
This is what makes heading size portable across canvas formats: compute the
square size for whatever canvas you're on, then apply the ratio below.

| Tier | Font | Weight | Case | Ratio (font-size ÷ square) | Confirmed example |
|---|---|---|---|---|---|
| Primary heading | Syne | Extra Bold | ALL CAPS | 0.315 | 68px on 1080×1920 (square=216), line-height 1.2 — 2 lines fill 1 square tall |
| Secondary heading | Syne | Extra Bold | ALL CAPS | 0.208 | 45px on 1080×1920 (square=216), line-height 1.2 — 3 lines fill 1 square tall |
| Tagline / body | Roboto | Regular | Mixed | — no grid-square constraint | Sizing is flexible |

**Heading fill color — assigned per line, in order, based on total line count.**
Applies to both heading tiers. Color sequence is always Signal Green → Accent
Yellow → Paper White, assigned to lines top to bottom:

| Line count | Line 1 | Line 2 | Line 3 |
|---|---|---|---|
| 1 line | Signal Green (#07F328) | — | — |
| 2 lines | Signal Green | Accent Yellow (#F8FC07) | — |
| 3 lines | Signal Green | Accent Yellow | Paper White (#FFFFFF) |

A heading only breaks to 2 lines when the break itself does creative work —
either a natural spacing point or to emphasize a specific word by isolating
it on its own line — not just whenever text happens to wrap.

**Open question:** the sequence is defined through 3 lines. If a primary
heading ever runs to 4+ lines, confirm whether the sequence repeats
(Green → Yellow → White → Green) or something else applies.

**Applying this on the web:** the same ratio becomes a CSS formula tied to
viewport instead of a fixed canvas:
```css
--square: min(100vw, 100vh) / 5;
--heading-primary: calc(var(--square) * 0.315);
--heading-secondary: calc(var(--square) * 0.208);
```
This keeps headings scaling correctly across breakpoints the same way they
scale across Canva canvas sizes — one ratio, many formats.

---

## 5. Voice — examples, not adjectives

Persona: *the friend backstage who knows every act personally and isn't afraid to say what's actually good.*

| Don't | Do |
|---|---|
| "Join us for an unforgettable musical experience" | "8 years, one week, zero filler lineup." |
| "We are excited to announce our speaker lineup" | "The lineup's up. Some of these names you'll recognize. One of them you'll be telling people you saw first." |

**Banned words:** "unforgettable," "elevate," "journey," "synergy," "game-changing"
**Formatting rule:** no em-dashes, no bold section headers in body copy (per Julian's standing preference)

---

## 6. Output contracts — by artifact

| Artifact | Headline limit | Body limit | Notes |
|---|---|---|---|
| Deck slide | ≤8 words | 3 bullets, ≤14 words each | 1 idea per slide |
| Landing hero | ≤10 words | subhead ≤20 words | CTA ≤3 words |
| Social caption | ≤12 words hook (first line) | ≤280 chars total | 1 emoji max |
| Case study section header | ≤6 words | — | sentence case |

---

## 7. Known AI failure modes (anti-patterns to watch for)

- Defaults to centered layouts — MMW8 grid is left-aligned unless spec says otherwise
- Over-explains in captions — trim to the punch line
- Adds hype adjectives despite banned-words list — re-check output against Section 5
- Picks a 4th color when composing — enforce the 3-color max explicitly in the prompt
