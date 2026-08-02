---
applies_to: landing pages, case studies (web)
references: brand-core.md
---

# MMW8 — Web Guidelines
> Voice, color, and type rules live in brand-core.md. This file holds
> layout, component, and responsive rules specific to web artifacts.
> Not built in Canva — built directly as HTML/React from this spec.

## 1. Grid (see brand-core.md §4 for canonical values)
| Property | Value |
|---|---|
| Columns | 12 |
| Gutter | 24px |
| Margin | 80px desktop / 16px mobile |
| Max content width | 1200px |

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
