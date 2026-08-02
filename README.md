# MMW8 Brand Repo

Source of truth for MMW8's brand system, structured so it can be read
directly by AI tools (Claude) as well as humans.

## Structure

- `brand-core.md` — logo, color, type, voice, grid (canonical values)
- `deck-guidelines.md` — slide deck specifics, references brand-core.md
- `web-guidelines.md` — landing page / case study specifics
- `social-guidelines.md` — social post / poster specifics
- `assets/` — images referenced by the .md files (logo, grid diagrams, color swatches, type scale)
- `reference/approved-examples/` — past artifacts that nailed the brand, for pattern reference
- `reference/rejected-examples/` — things that missed, with a one-line note on why

## How to edit

- Small text edits: open the file on github.com, click the pencil icon, edit, commit.
- Adding images or bigger changes: use GitHub Desktop — pull the repo locally, edit files
  in any text editor, drop new images into the right `assets/` subfolder, then commit + push
  from the app.
- Filenames: lowercase, hyphenated, no spaces (e.g. `mmw8-lockup.svg`, not `Logo Final v2.svg`).

## Working with Claude / Canva

- For most artifacts, only the relevant guideline file + brand-core.md is needed —
  no need to load the whole repo each time.
- Canva Brand Templates hold the enforced visual layout; these .md files hold voice,
  content limits, and which template to use. Template names/links go in each
  guideline file's header.
- For web artifacts, no Canva step — built directly from web-guidelines.md.

## Status
Currently a skeleton — real values from the Canva brand kit, deck template, and poster
still need to be filled into brand-core.md, deck-guidelines.md, and social-guidelines.md.
