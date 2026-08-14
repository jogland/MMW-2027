---
applies_to: landing pages, case studies (web)
references: brand-core.md
---

# MMW8 — Web Guidelines
> Voice, color, and type rules live in brand-core.md. This file holds
> layout, component, and responsive rules specific to web artifacts.
> Not built in Canva — built directly as HTML/React from this spec.

## 1. Grid — two systems, don't conflate them

### 1a. Content grid (see brand-core.md §4 for canonical values)
Applies to: conventional content components — card grids, footer columns,
forms, news cards.

| Property | Value |
|---|---|
| Columns | 12 |
| Gutter | 24px |
| Margin | 80px desktop / 16px mobile |
| Max content width | 1200px |

### 1b. Full-bleed section grid (desktop)
Applies to: hero and all full-bleed background sections. This is a
**structural** grid, not decorative — it governs horizontal alignment of
text blocks, images, and highlight-boxes across the entire section.

| Property | Value |
|---|---|
| Columns | 12 |
| Gutter | 0 (no gutter — column edges are flush) |
| Margin | edge-to-edge (full viewport width, no side margin) |
| Alignment | elements snap to column edges, both left/right start-points
  and, in most cases, to the same horizontal row-lines as neighboring
  elements (text blocks and images sharing a "row" align their tops) |
| Visual overlay | the yellow grid lines are this grid made visible — the
  underlying structure is real, not an applied texture |

**Mobile:** the 12-column grid collapses to a single stacked column (see
mobile mockup) — full-bleed sections lose the multi-column alignment and
elements stack top-to-bottom at full width. Treat 1a's mobile margin (16px)
as the baseline for mobile full-bleed sections too.

**Do not merge these two systems.** Both use 12 columns, but the content grid
has a 24px gutter and an 80px/16px margin while the full-bleed grid has zero
gutter and zero margin — they operate at different z-index layers with
different jobs. Treat their column edges as coincidentally sharing a count,
not as the same grid; forcing a full-bleed element to align against the
content grid's gutter math will produce alignment bugs.

**Confirmed square unit:** the full-bleed grid is rendered as a literal
square overlay (`GridOverlay`), not just abstract columns — 100px squares at
a 1200px reference width (`square = reference width ÷ 12`). Recompute per
actual viewport width for other sizes. This is the same 12-square system
decks use (see deck-guidelines.md §2) — web and decks are the two 12-square
formats; social/posters use a separate 5-square formula (brand-core.md §4).
All full-bleed elements snap to this grid — never placed off-grid.

## 2. Components

Real, reusable patterns extracted from the actual home page (not invented) — pull from this set rather than designing new primitives:

| Component | Props | Notes |
|---|---|---|
| `Button` | `variant` (yellow/white/dark/green/outline), `icon`, `fullWidth`, `onClick`, `type` | trailing black circle + arrow badge by default (`icon`); full-width under 480px |
| `Tag` | `color`, `textColor`, `size` | section label pattern (CONEXIÓN, CREACIÓN, etc.), defaults to accent yellow |
| `HeadingBlock` | `lines`, `tier` (primary/secondary), `align`, `maxWidth`, `square` | renders the green→yellow→white highlighted-line heading motif, cycling every 3 lines, zero gap between lines — always pass `square={100}` on web (defaults to 216, the social square, if omitted) — see brand-core.md §4 |
| `ImageCard` | `src`, `alt`, `width`, `height` | 1px Accent Yellow inset border |
| `GridOverlay` | `square`, `lineColor`, `opacity` | the visible structural yellow square grid |
| `DotMarker` | `size`, `color` | grid-intersection accent dot, 3-4 max per composition |
| `PlayButton` | `onClick`, `size` | video-thumbnail play control |
| `EmailSignupForm` | `placeholder`, `buttonLabel`, `onSubmit`, `stacked` | bordered input + CTA button row |
| `NavBar` | `logoSrc`, `onMenuClick` | collapses to hamburger under 768px |
| `Footer` | `email`, `phone` | dark footer with contact + newsletter |

**Signature shape** (Button, Tag, ImageCard, form inputs): flat fill, 2px inset black border, hard 4px black offset shadow (no blur), zero corner radius. See brand-core.md §4 for the full spec. Hover/press states are not yet defined for any component — don't invent an easing/hover system.

## 3. Output contract
| Section | Headline limit | Body limit | Notes |
|---|---|---|---|
| Hero | ≤10 words | subhead ≤20 words | CTA ≤3 words |
| Case study section header | ≤6 words | — | sentence case |

## 4. Known failure modes
- Defaults to centered layouts — MMW8 is left-aligned unless spec says otherwise
- Over-explains in body copy — trim to the point
