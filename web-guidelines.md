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
| Columns | 9 |
| Gutter | 0 (no gutter — column edges are flush) |
| Margin | edge-to-edge (full viewport width, no side margin) |
| Alignment | elements snap to column edges, both left/right start-points
  and, in most cases, to the same horizontal row-lines as neighboring
  elements (text blocks and images sharing a "row" align their tops) |
| Visual overlay | the yellow grid lines are this grid made visible — the
  underlying structure is real, not an applied texture |

**Mobile:** the 9-column grid collapses to a single stacked column (see
mobile mockup) — full-bleed sections lose the multi-column alignment and
elements stack top-to-bottom at full width. Treat 1a's mobile margin (16px)
as the baseline for mobile full-bleed sections too.

**Do not merge these two systems.** The 12-col content grid should never be
asked to align to the 9-col background grid or vice versa — they operate at
different z-index layers with different jobs, and forcing one to match the
other's math (12 vs. 9 don't share clean fraction boundaries) will produce
alignment bugs.

## 2. Components
| Component | States | Breakpoint behavior |
|---|---|---|
| Primary button | default / hover / disabled | full-width under 480px |
| Nav bar | default / scrolled | collapses to hamburger under 768px |
| Hero | — | stacks image below text under 768px |

## 3. Output contract
| Section | Headline limit | Body limit | Notes |
|---|---|---|---|
| Hero | ≤10 words | subhead ≤20 words | CTA ≤3 words |
| Case study section header | ≤6 words | — | sentence case |

## 4. Known failure modes
- Defaults to centered layouts — MMW8 is left-aligned unless spec says otherwise
- Over-explains in body copy — trim to the point
