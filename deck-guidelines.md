---
applies_to: slide decks
references: brand-core.md
primary_path: Claude Design → export to Canva
reference_template: Slide Deck Template (EAHQEs7Ll2w)
---

# MMW8 — Deck Guidelines
> Voice, color, and type rules live in brand-core.md. This file only holds
> what's specific to decks: layout contracts and how to produce them.

## 1. Production path
**Primary:** Claude Design, building from brand-core.md §2-4 (color, type,
grid), then exported to Canva for final refinement.

**Reference / fallback:** an existing Canva Brand Template — "Slide Deck
Template" (ID: EAHQEs7Ll2w, https://www.canva.com/brand/brand-templates/EAHQEs7Ll2w)
— confirmed to have the real grid, background media, and heading treatment
correctly baked in. Useful as:
- Ground truth for what a correctly-applied grid actually looks like
- A manual fallback if Claude Design's output doesn't match the spec
- 15 slide layouts available (title/cover, content with 3-line headline,
  metrics grid, image + text, full-bleed photo, agenda, contact/closing,
  and more)

This template does not support autofill (empty dataset) — using it directly
means copying pages and editing text by hand, not automated population.

## 2. Grid (see brand-core.md §4 for the canonical formula)
Square size = shorter canvas side ÷ 5. For the standard 1080×1920 or
1920×1080 deck canvas, square = 216px. Do not use a fixed column/gutter
grid — the visible yellow square grid IS the layout system. See
brand-core.md §4 for the fill-square, dot-marker, and heading-ratio rules
that govern how content sits within it.

## 3. Output contract
| Slide type | Headline limit    | Body limit                 | Notes                               |
| ---------- | ------------------ | ---------------------------- | -------------------------------------- |
| Title      | ≤8 words          | —                             | logo top-left, per brand-core §1       |
| Content    | ≤8 words headline | 3 bullets, ≤14 words each   | 1 idea per slide                        |
| Quote      | —                  | ≤25 words                    | attribute below, small caption size    |
| Closing    | ≤6 words          | CTA ≤3 words                 | logo centered                           |

## 4. Known failure modes
- Overfilling bullet slides — enforce 3-bullet max even if content wants more (split into 2 slides instead)
- Centering headlines by default — MMW8 decks are left-aligned unless slide type says otherwise
- Using free-form AI generation instead of the actual Slide Deck Template — free-form generation does not read this repo and will not reproduce the grid, logo placement, or heading treatment