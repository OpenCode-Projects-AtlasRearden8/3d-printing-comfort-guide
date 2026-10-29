# The 3D Printing Comfort Guide

A calm, plain-English manual for a first 3D printer — choosing modestly instead of collecting, understanding bed leveling for what it really is, speaking slicer in six settings, living happily in PLA, printing genuinely useful home things (cable clips, drawer dividers, hinge fixes), fixing spaghetti prints without panic, and staying safe and license-legal. Written the way a friend would explain it: step by step, honest trade-offs, never condescending.

Published as a free resource by [Asdale Dynamics, LLC](https://dylanasdale.github.io), the beginner-friendly education project of author Dylan Asdale.

## The one-sentence version

**Buy enough printer — not too much, level the bed for what it really means, keep your slicing simple, print things your home actually needs, and treat every failure as a note the machine left you.**

## Who this is for

- You are choosing a first 3D printer and want to avoid the shelf-of-regret outcome.
- You own a printer that has not yet survived its first successful, useful print.
- You would rather print a drawer divider that fits than fifty dragons that do not.
- You want a troubleshooting card that reads like a calm friend, not a forum flamewar.

## What is inside

- **docs/** — the guide itself, one Markdown file per chapter. `00-read-this-first.md` is front matter; the numbered chapters run 1–10:
  1. Choosing Modestly (the starter checklist, what you do not need yet, the regret-predicting questions)
  2. Bed Leveling, Decoded (tramming vs. distance, the paper test, ABL and the Z offset)
  3. Slicers, in Plain English (the six settings that matter, profiles, preview habits)
  4. PLA Basics (settings, moisture and storage, when the other plastics win)
  5. Genuinely Useful Home Prints (cable clips, drawer dividers, hinge fixes, the four-part method)
  6. Fixing Spaghetti Prints, Calmly (the two-minute rule, the causes named, rescue sequence)
  7. Free Model Sites and License Sanity (Printables, MakerWorld, Thingiverse, Thangs; CC0/CC BY/CC BY-NC in plain English)
  8. Fumes and Safety Basics (PLA and ventilation, the honest heat list, unattended-print calm)
  9. The First-Print Checklist and Troubleshooting Card (a printable pre-print ritual and one-page rescue table)
  10. Glossary (every term in the book, plain-English A–Z)
- **scripts/build.py** — a standard-library-only static site builder. Converts the chapters into a polished, offline-friendly HTML site: a landing page, one page per chapter with sidebar navigation and prev/next links, and a single "whole book" page for printing or Ctrl+F. Requires nothing but Python 3.9+, needs no network, and makes zero external requests.
- **scripts/style.css** — the site stylesheet (light/dark aware, print-friendly), copied into `site/` at build time.
- **tests/test_build.py** — tests for the converter, the builder, the CLI, docs linting, and repo hygiene.
- **site/** — the generated site (built locally; gitignored, not committed).

## Quick start

Read it as plain text:

```bash
less docs/00-read-this-first.md
```

Build the static site (Python 3.9+, nothing else):

```bash
python3 scripts/build.py
```

Then open `site/index.html` in any browser — no server needed, no JavaScript, no network. Prefer the whole book on one page?

```bash
xdg-open site/book.html      # Linux (or: open site/book.html on macOS)
```

Lint the documentation (links, anchors, chapter structure):

```bash
python3 scripts/build.py --check
```

Convert one chapter to HTML on stdout:

```bash
python3 scripts/build.py --from-md docs/09-first-print-checklist.md
```

Run the tests:

```bash
python3 -m unittest discover -s tests
```

## How this complements The Old Laptop Revival Guide

The two books share a voice but not a corner of the workshop:

| Question | Where to go |
| --- | --- |
| What do I make first, and how do I fit it? | This guide, ch. 5 & 9 |
| Why does my first layer fail, and what is a Z offset? | This guide, ch. 2, 3, 6 |
| Which file licenses let me do what? | This guide, ch. 7 |
| What can a revived old laptop itself do? | The Old Laptop Revival Guide, ch. 1–6 |
| Where does local AI fit in a home setup? | The Old Laptop Revival Guide, ch. 5 & 6 |

## License

MIT. See [LICENSE](LICENSE). Copyright (c) 2026 Asdale Dynamics, LLC.
