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

**Additional reference:** a separate "MMW 27 Slide Deck Template" Figma file
(12 real 1920×1080 frames) exists alongside the Canva template above. 5 of
its 12 frames — title, founder quote, section statement, pull-quote close,
and a dense-list/audience-grid layout — are recreated as real HTML in the
MMW8 Design System's `slides/` directory and are safe to use as ground truth
alongside the Canva template. The remaining 4 frames (metrics/stat-heavy
layouts) render their headline/body text as hand-outlined vector paths
rather than live text in the Figma source, so their exact copy/layout isn't
reconstructable from that file — treat those as an open gap, not yet backed
by a recreated reference.

## 2. Grid (see brand-core.md §4 for the canonical formula)
Decks use the **12-square grid**, same system as web — not the 5-square
social/poster formula. Square size = canvas width ÷ 12. Decks are
**landscape-only at 1920×1080** (per the source Figma deck template — there
is no confirmed portrait deck format), so square = 160px, tiling to 6.75
squares tall (expected — only the width needs to divide evenly). Do not use
a fixed column/gutter grid — the visible yellow square grid IS the layout
system. All slide elements (headline blocks, image panels, quote blocks,
logo lockup) snap to this grid — never placed off-grid. See brand-core.md
§4 for the fill-square, dot-marker, and heading-sizing rules that govern how
content sits within it: headline sizes use the same square ÷ 2 (primary) /
square ÷ 3 (secondary) formula as every other artifact, computed off the
deck's own 160px square — 80px primary / 53px secondary.

## 3. Output contract
| Slide type | Headline limit    | Body limit                 | Notes                               |
| ---------- | ------------------ | ---------------------------- | -------------------------------------- |
| Title      | ≤8 words          | —                             | logo top-left, per brand-core §1       |
| Content    | ≤8 words headline | 3 bullets, ≤14 words each   | 1 idea per slide                        |
| Quote      | —                  | ≤25 words                    | attribute below, small caption size    |
| Closing    | ≤6 words          | CTA ≤3 words                 | logo centered                           |

