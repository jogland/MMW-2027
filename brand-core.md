---
brand: MMW8 (Medellín Music Week, Edition 8)
version: 0.1-sample
last_updated: 2026-07-13
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

| Name | Hex | Use case |
|---|---|---|
| Primary Purple | #6B2FD6 | Primary CTA, headlines on dark bg |
| Signal Yellow | #F5D90A | Accent only — max 10% of any composition |
| Ink Black | #0A0A0A | Body text, dark backgrounds |
| Paper White | #FAFAFA | Light backgrounds |

**Rule:** no more than 3 colors per artifact (1 primary + 1 accent + 1 neutral). Never place Signal Yellow behind body text — contrast fails accessibility.

---

## 3. Typography

| Role | Font | Weight | Size (web/deck) |
|---|---|---|---|
| Display / Headline | [Font Name] | Bold (700) | 48–64px |
| Subhead | [Font Name] | Medium (500) | 24–32px |
| Body | [Font Name] | Regular (400) | 16–18px |
| Caption / Meta | [Font Name] | Regular (400) | 12–14px |

**Rule:** headlines are sentence case, never all-caps except single-word event tags (e.g. "MMW8").

---

## 4. Grid — by artifact

| Artifact | Columns | Gutter | Margin | Notes |
|---|---|---|---|---|
| Slide deck (16:9) | 12 | 24px | 5% of canvas width | content safe zone = inner 90% |
| Landing page | 12 | 24px | 80px desktop / 16px mobile | max content width 1200px |
| Social post (1:1) | 4 | 16px | 8% | logo always bottom-right, 24px inset |
| Social post (9:16) | 4 | 16px | 6% top/bottom, 8% sides | keep top 15% clear for platform UI |

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
