---
applies_to: social posts, posters
references: brand-core.md
primary_path: Claude Design → export to Canva
---

# MMW8 — Social & Poster Guidelines
> Voice, color, and type rules live in brand-core.md. This file only holds
> what's specific to social/poster formats.

## 1. Production path
No dedicated Canva brand template exists yet for social or poster formats
(unlike decks, which has one — see deck-guidelines.md). Primary path:
Claude Design, building from brand-core.md §2-4, then exported to Canva for
refinement. If a manual brand template gets built later for these formats,
document it here the same way deck-guidelines.md does.

**Reference:** a "MMW 27 Social Media" Figma file has 6 real 1080×1920
frames — Activity, Artist, Event, Post (Long Text), Poster, Program — all
recreated as real HTML in the MMW8 Design System's `social/` directory.
These are confirmed ground truth for 1080×1920 (Story/portrait). Per the
file owner's note, the same grid and type rules translate directly to
square and landscape social sizes by re-flowing the same blocks — no
separate square/landscape frames exist yet, so treat that translation as
the working assumption until real square/landscape examples show otherwise.

**Partner co-brand:** the Activity template carries a small Music Tech
Summit partner lockup set in Lexend Zetta Medium — the only place that font
appears in the system. Use it only for that one partner mark, not for MMW's
own type.

## 2. Platform safe zones
> Vertical formats (Stories, Reels, TikTok) overlay app UI — profile info,
> captions, buttons — over the top and bottom of the canvas. Keep primary
> content (headline, logo, key visual) clear of these zones. Figures below
> are current as of mid-2026 and drift as platforms update their UI —
> re-verify periodically rather than treating as permanently fixed.

| Platform            | Canvas       | Keep clear (top) | Keep clear (bottom) | Keep clear (sides)   |
| ---------------------- | -------------- | ------------------- | ---------------------- | ------------------------ |
| Instagram Stories    | 1080×1920    | 250px              | 250px                  | —                        |
| Instagram Reels      | 1080×1920    | 250px              | 400px                  | —                        |
| TikTok                | 1080×1920    | 108px              | 320px                  | 60px left / 120px right |

**In terms of the grid system (brand-core.md §4):** on a 1080×1920 canvas,
one square = 216px. Roughly translated: avoid placing primary content in
the top grid row, and keep the bottom 1.5-2 grid rows clear on Reels/TikTok
specifically (Stories has a bit more room at the bottom). Dot markers and
decorative fill squares can still extend into these zones since they're
background texture, not content that needs to be read — but headline text,
logo, and CTAs should sit inside the safe area.

## 3. Grid (see brand-core.md §4 for the canonical formula)
Square size = shorter canvas side ÷ 5 — same formula for every social/poster
format (square post, story, poster). Compute per canvas dimensions rather
than using a fixed column count. Example: a 1080×1080 square post has square
= 216px, same unit size as the 1080×1920 story/poster. **Decks and web use a
different, 12-square formula (see deck-guidelines.md §2 / web-guidelines.md
§1b) — don't reuse this 216px unit for those formats.** All elements snap to
this 5-square grid — never placed off-grid (see brand-core.md §4).

## 4. Output contract
| Format      | Hook/headline | Body/caption            | Notes                                       |
| ------------- | --------------- | -------------------------- | ---------------------------------------------- |
| Square post | ≤12 words     | ≤280 chars total        | 1 emoji max                                 |
| Story       | ≤8 words      | minimal — visual-led    |                                              |
| Poster      | ≤10 words     | date/venue/lineup block | see approved-examples/ for layout reference |

## 5. Known failure modes
- Placing headline text or logo in the top/bottom safe-zone margins — always check against Section 2 for the specific platform/format
- Adds hype adjectives despite banned-words list in brand-core §5 — recheck output
- Picks a 4th color — enforce brand-core §2's 3-color max