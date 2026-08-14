---
brand: MMW8 (Medellín Music Week, Edition 8)
version: 0.5
last_updated: 2026-08-14
applies_to: [decks, landing-pages, case-studies, social-posts]
---

# MMW8 Brand Core
> Source of truth for all AI-generated artifacts. Artifact-specific files
> (deck-guidelines.md, web-guidelines.md, social-guidelines.md) reference
> this file and should never override values here without updating this
> file first.

---

## 1. Logo

**Files:** `/assets/logo/MMW Logo 1.svg`

| Property                | Value                                                                  |
| ----------------------- | ---------------------------------------------------------------------- |
| Clearspace              | logo height ÷ 2, on all sides                                          |
| Minimum width (digital) | 120px                                                                  |
| Minimum width (print)   | 25mm                                                                   |
| Approved backgrounds    | #0A0A0A (black), #FFFFFF (white), or a full-bleed background image/video from `assets/backgrounds/` |
| Never                   | stretch, rotate, recolor outside approved backgrounds, add drop shadow |

**Note:** clearspace and minimum-width values above are reasonable defaults, not yet verified against a real Canva file. Confirm against an actual logo placement if precision matters for a specific artifact.

**Primary Purple (#6B2FD6):** listed as an approved logo background in an earlier version of this file. It does not appear anywhere else in the confirmed palette or in the mounted Figma files — treat as legacy/unconfirmed rather than an active brand color unless it turns up in the Canva brand kit.

**No single canonical lockup is specified** — three alternate lockup versions exist (`mmw-logo-1/2/3`, each with a white variant for dark backgrounds) plus a symbol-only mark (`mmw-logosimbolo`). Pick per artifact based on available space; none is designated "the" default.

---

## 2. Color
> Confirmed against MMW's Canva brand kit palette (Aug 2026).

| Name          | Hex     | Use case                                                      |
| ------------- | ------- | ------------------------------------------------------------- |
| Signal Green  | #07F328 | Standard flat background                                      |
| Cyan          | #0BCBFF | Secondary / alt background                                    |
| Magenta       | #FF00FF | Secondary / alt background                                    |
| Signal Blue   | #005DF5 | Secondary / alt background                                    |
| Accent Yellow | #F8FC07 | Grid squares, dots, small highlight blocks — capped at ~10% of a composition |
| Ink Black     | #000000 | Text, dark neutral                                            |
| Paper White   | #FFFFFF | Light neutral, light-background artifacts (web, case studies) |

**Rule:** no more than 3 colors per artifact (1 background + 1 accent + black or white text, whichever contrasts). Accent Yellow is an accent, not a primary — it never carries body text or fills a whole background.

**Backgrounds:** #07F328 is the standard flat background color. Cyan, Magenta and Signal Blue are secondary/alt backgrounds for variety. In practice, full-bleed photographic backgrounds from `assets/backgrounds/` are just as common as flat color fills — reference the specific one by filename in each artifact's guideline file when it matters (e.g. "use `assets/backgrounds/topographic-blue.png` style for this social post").

---

## 3. Typography

| Role              | Font   | Weight     | Case                                   |
| ----------------- | ------ | ---------- | -------------------------------------- |
| Primary heading   | Syne   | Extra Bold | ALL CAPS                               |
| Secondary heading | Syne   | Extra Bold | ALL CAPS                               |
| Body / Label      | Roboto | Regular    | Mixed / ALL CAPS for dates & locations |

**Sizing:** headings are sized as a ratio of the grid square, not a fixed pixel value — see Section 4 for the formula and confirmed ratios. This keeps sizing correct across any canvas or viewport size instead of breaking on formats other than the one it was designed on.

**Confirmed usage:** Syne Extra Bold used for event name + edition ("OCTAVA EDICIÓN 2027") and taglines like "UNA ESTACIÓN DE ENCUENTRO," all-caps. Roboto Regular used for location/date labels ("Medellín," "Colombia," "Febrero 15 - 21").

**Confirmed body/label reference sizes** (non-grid-tied, e.g. content-grid components on web):

| Token          | Size |
| -------------- | ---- |
| `body-lg`      | 34px |
| `body-md`      | 20px |
| `body-sm`      | 16px |
| `label`        | 14px |

Only Syne 800 (Extra Bold) is loaded — no other Syne weight is part of this system. Roboto loads at 400 (Regular) and 500 (Medium, for labels/buttons).

---

## 4. Grid — the compositional system
> Confirmed against MMW's Canva poster/deck template and the mounted Figma
> files (Aug 2026). This grid is visible in the final artifact (not a
> hidden alignment guide) and scales to any canvas size via the formulas
> below — this is what makes it portable across web, decks, and social.

**Two square-grid systems — don't cross them.** Which one applies depends on whether the canvas has a fixed/near-fixed reference width (web, decks) or can be any orientation (social, posters):

| Artifact class | Squares across | Formula | Confirmed example |
| --------------- | ---------------- | -------- | ------------------- |
| Web & decks | 12 | square = reference width ÷ 12 | Web: 100px at a 1200px container width (`GridOverlay square="100px"` on the home-page hero). Deck: 160px on the 1920×1080 landscape canvas (1920 ÷ 12) — decks are landscape-only per the source Figma deck template, there is no confirmed portrait deck format. |
| Social & posters | 5 | square = shorter canvas side ÷ 5 | 216px on a 1080×1920 canvas |

Both formulas tile the *other* dimension imperfectly (a 1920×1080 deck lands at 6.75 squares tall; a 1080×1920 story lands at ~8.9 squares tall) — that's expected, not an error. Only the divided dimension needs to land on a whole number. **Never apply the 5-square formula to a web or deck canvas, or the 12-square formula to a social canvas** — mixing them produces a square size that doesn't match either format's built grid.

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

**Headings — sized as a fraction of the grid square, not a fixed pixel value.**
Primary heading = square ÷ 2. Secondary heading = square ÷ 3. This is the
same formula everywhere (web, decks, social) — only the square itself
differs per artifact class (see the table earlier in this section):

| Tier              | Font   | Weight     | Case     | Formula    | Web (square=100) | Deck (square=160) | Social/poster (square=216) |
| ----------------- | ------ | ---------- | -------- | ---------- | ------------------ | -------------------- | ----------------------------- |
| Primary heading   | Syne   | Extra Bold | ALL CAPS | square ÷ 2 | 50px                | 80px                  | 108px                          |
| Secondary heading | Syne   | Extra Bold | ALL CAPS | square ÷ 3 | 33px                | 53px                  | 72px                           |
| Tagline / body    | Roboto | Regular    | Mixed    | — flexible | —                   | —                      | —                               |

**Implemented in `HeadingBlock`:** the component takes a `square` prop and computes `fontSize` directly from it (`square / 2` or `square / 3`) — always pass the square for the canvas you're actually on. It defaults to 216 (the social/story/poster square, matching `GridOverlay`'s default) if you omit `square` — web and deck callers must pass their own `square` explicitly or they'll render at the social size.

**Heading fill color — assigned per line, in order, based on total line count.**
Applies to both heading tiers. Color sequence is always Signal Green → Accent
Yellow → Paper White, assigned to lines top to bottom:

| Line count | Line 1                 | Line 2                   | Line 3                 |
| ---------- | ----------------------- | ------------------------- | ------------------------ |
| 1 line     | Signal Green (#07F328) | —                          | —                         |
| 2 lines    | Signal Green            | Accent Yellow (#F8FC07)   | —                         |
| 3 lines    | Signal Green            | Accent Yellow             | Paper White (#FFFFFF)    |

Line breaks should still land on natural phrase/word boundaries for
readability, but don't hesitate to break a long headline into more lines to
fit the canvas — headlines can be big, and there's no hard line-count cap.
`HeadingBlock` renders every line it's given; the fill-color sequence
cycles green → yellow → white every 3 lines rather than stopping there.

**Lines have zero vertical gap.** Heading lines stack directly against each
other — no margin or gap between them, ever, regardless of how many lines
a heading breaks into.

**Applying this on the web:** the same formula becomes a CSS calc tied to
viewport width instead of a fixed canvas (web's square is 12-based, not
5-based — see the grid table earlier in this section):
```css
--square-web: calc(100vw / 12);
--heading-primary: calc(var(--square-web) / 2);
--heading-secondary: calc(var(--square-web) / 3);
```
This keeps headings scaling correctly across breakpoints the same way they
scale across canvas sizes — one formula, many formats.

**Spacing scale** (confirmed via the Figma web recreation, used for content-grid components — cards, footers, forms):

| Token     | Value |
| --------- | ----- |
| `space-1` | 8px   |
| `space-2` | 16px  |
| `space-3` | 24px  |
| `space-4` | 32px  |
| `space-5` | 48px  |
| `space-6` | 64px  |

**Signature shape — buttons, cards, tags:** flat fill, `inset 0 0 0 2px black` border, plus a hard `0px 4px 0px black` offset shadow (no blur, no soft elevation). Image cards use a thin 1px Accent Yellow inset border instead of a shadow. **Corner radii: none** — 0px on every button, card, tag, and input; the dot marker and play-button circles are true circles (`border-radius: 50%`), not rounded rectangles. Hover/press states are not defined anywhere in the source material — treat as an open question rather than inventing an easing/hover system.

---

## 5. Voice — examples, not adjectives

Persona: *the friend backstage who knows every act personally and isn't afraid to say what's actually good.*

| Don't                                             | Do                                                                                                           |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| "Join us for an unforgettable musical experience" | "8 years, one week, zero filler lineup."                                                                     |
| "We are excited to announce our speaker lineup"   | "The lineup's up. Some of these names you'll recognize. One of them you'll be telling people you saw first." |

**Banned words:** "unforgettable," "elevate," "journey," "synergy," "game-changing"
**Formatting rule:** no em-dashes, no bold section headers in body copy (per Julian's standing preference)
**Language:** Spanish is the working language for real web/social copy (e.g. "Octava edición," "Notifícame cuando salgan los tickets"). Dates and locations are set ALL CAPS ("Medellín," "Febrero 15 – 21") even inside otherwise mixed-case body text. English examples in this file illustrate voice/tone only — don't ship English copy for MMW8 artifacts unless the brief specifically calls for it.

---

## 6. Output contracts — by artifact
> Reasonable defaults, not yet tested against a real generated artifact — expect to refine these once you've reviewed output from Claude Design or Canva against them.

| Artifact                  | Headline limit               | Body limit                | Notes            |
| -------------------------- | ------------------------------ | -------------------------- | ------------------ |
| Deck slide                | ≤8 words                     | 6 bullets, ≤14 words each | 1 idea per slide |
| Landing hero               | ≤10 words                     | subhead ≤20 words          | CTA ≤3 words      |
| Social caption             | ≤12 words hook (first line)   | ≤280 chars total           | 1 emoji max        |
| Case study section header | ≤6 words                     | —                          | sentence case     |

---

## 7. Known AI failure modes (anti-patterns to watch for)

- Defaults to centered layouts — MMW8 grid is left-aligned unless spec says otherwise
- Over-explains in captions — trim to the punch line
- Adds hype adjectives despite banned-words list — re-check output against Section 5
- Picks a 4th color when composing — enforce the 3-color max explicitly in the prompt