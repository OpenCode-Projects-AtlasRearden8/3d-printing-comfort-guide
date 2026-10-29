# STATUS

Project: The 3D Printing Comfort Guide
Owner: Asdale Dynamics, LLC
State: complete and verified (October 2026)

## What was built

A beginner-facing, plain-English manual for a first 3D printer — choosing modestly (with collector's-regret guardrails), understanding bed leveling as the two distinct jobs it hides, learning the six slicer settings that matter, living comfortably in PLA, printing genuinely useful home objects (cable clips, drawer dividers, hinge fixes), handling failed "spaghetti" prints with a calm diagnostic routine, staying safe (fumes/heat/unattended prints), and navigating free model sites and their licenses — plus a printable first-print checklist with a one-page troubleshooting card and a full glossary. It complements The Old Laptop Revival Guide (the sibling repo): that guide covers reviving a machine with Linux and local AI; this one covers what a machine that *makes* things looks like for a beginner household.

- **docs/** (11 Markdown files: front matter + 10 numbered chapters):
  - `00-read-this-first.md` — front matter: audience, promises, needs list, five-minute version, trip map, companion note.
  1. Choosing Modestly (the modest starter checklist, what you do not need on day one, honest costs, regret-predicting questions, when to stop upgrading)
  2. Bed Leveling, Decoded (tramming vs. nozzle-distance, the paper test at operating temperature, corner knobs, ABL and what it does not do, Z offset)
  3. Slicers, in Plain English (what slicing is, which slicer, the six settings that matter, profiles, slice-preview-save, discardable anxieties)
  4. PLA Basics (PLA's strengths and limits, settings table, moisture and storage, handling tips, the other-plastics table for later)
  5. Genuinely Useful Home Prints (the four-part method, cable clips, drawer dividers, hinge fixes, other winner categories, Tinkercad pointer)
  6. Fixing Spaghetti Prints, Calmly (the two-minute rule, rescue sequence, named causes with fixes and order-of-likelihood, morale resets, local-first help)
  7. Free Model Sites and License Sanity (Printables, MakerWorld, Thingiverse, Thangs, search skills; CC0, CC BY, CC BY-NC, SA/ND, unlicensed files, habits)
  8. Fumes and Safety Basics (honest PLA fume picture, ventilation, heat rules, unattended-print habits, housekeeping, respirator question answered)
  9. The First-Print Checklist and Troubleshooting Card (printable five-minute ritual, first-ten-minutes watch points, after-print habits, one-page rescue table)
  10. Glossary (plain-English A–Z of every term used, plus what was deliberately left out)
- **scripts/build.py**: standard-library-only static site builder. Zero dependencies, zero network. Produces a landing page, one polished page per chapter with sidebar navigation and prev/next pagers, a single-page "whole book" for printing/Ctrl+F, and a stylesheet (light/dark aware, print styles). `00-` stems are treated as front matter, so kickers read "Front matter" and "Chapter N of 10".
- **scripts/style.css**: the site stylesheet (teal theme to distinguish the sibling repos), copied into `site/` at build time.
- **CLI flags**: `--docs/--out` for custom paths, `--from-md FILE` to convert one chapter to HTML on stdout, `--check` to lint the docs (chapter numbering, headings, link targets, local anchors, closed code fences, non-Latin characters).
- **tests/test_build.py**: 38 tests covering the Markdown converter (headings, slugs, inline formatting, escaping, checkboxes, tables, fences, quotes, rules), the builder (numbering, file manifest, tag balance, no `<script>`, sidebar/book contents, reproducible builds, companion constants), the CLI (all flags, exit codes), and repo hygiene (exact MIT line, README credit, secret-pattern scan, allowed top-level files, companion mentions, required topic coverage).
- **README.md, LICENSE** (MIT, exact line "Copyright (c) 2026 Asdale Dynamics, LLC"), **.gitignore** (site/ ignored).

## How to run it

```bash
python3 scripts/build.py            # build site/ from docs/
python3 scripts/build.py --check    # lint docs (links, anchors, numbering)
python3 scripts/build.py --from-md docs/09-first-print-checklist.md   # one chapter to stdout
python3 -m unittest discover -s tests   # run the test suite (38 tests)
```

Then open `site/index.html` in a browser — no server needed; the site makes no external requests from its own assets, so it works offline and from file://. `site/book.html` is the whole book on one printable page (checklist and troubleshooting card included). Chapters link to external model/legal sites (printables.com, makerworld.com, thingiverse.com, thangs.com, tinkercad.com) as references only — the site itself loads nothing from them.

## Verification results (run in this folder)

- `python3 --version` → Python 3.13.5
- `python3 scripts/build.py --check` → "Checked 11 markdown files: clean" (after fixing all flagged non-Latin/garbled tokens)
- `python3 scripts/build.py` → "Built 14 files into site" (12 HTML pages + book + index + style.css; 13 HTML total, no scripts, no external asset URLs)
- HTML structural check (html.parser tag balance over all 13 generated HTML pages) → 0 problems
- `python3 -m unittest discover -s tests` → 38 tests, OK (0 failures, 0 errors)
- Reproducible-build test passes (two consecutive builds byte-identical)
- Secret-pattern scan across docs/scripts/tests/README/LICENSE → 0 matches
- Git initialized with the existing configured identity; committed; nothing pushed, no remote, no Co-authored-by trailers
- Manual content read-through for quality after the first build; several garbled tokens found and rewritten (see fix-ups)

## Fix-ups applied during this pass

- A handful of garbled or truncated tokens slipped into the first drafts of chapters 2, 4, 5, 6, 7, 8, and 9 (stray CJK/Cyrillic fragments, mangled helper-clause sentences in the ABL paragraph, the blob-cleaning paragraph, the safety chapter's housekeeping lines, and one checklist item). Each was rewritten to be clean, honest, and consistent with the guide's one-voice style. The docs lint (non-Latin-character check) now guards the character-level version of that mistake permanently, and the full 38-test suite locks in the rest.
- To avoid guessing at volatile specifics, the guide keeps brand-agnostic skill framing (which printer models are "in" shifts; printer support features do not) and points at the four stable, well-known free model sites rather than naming trendy model listings that would drift.
- The tests were extended beyond the sibling repo's set with two content guards: documentation must mention the companion guide, and the docs text must cover the eight required topics (cable clips, drawer dividers, hinge, spaghetti, PLA, bed leveling, slicer, license, ventilation) so future edits cannot silently drop the core promise.

## Known gaps / honest limits

- No printer-brand-specific setup chapters: the guide is deliberately skill-based (brands and firmware menus drift faster than a book), so first-run instructions defer to each printer's paper manual. Chapter 1 explains why.
- Resin/SLA printing is intentionally out of scope beyond a pointer (it needs its own safety-first manual).
- No images or diagrams: the build pipeline is text-first; the paper test and knob geometry are described in words and will be easiest with the reader's own printer manual beside them. Illustrations would be the natural next investment.
- The troubleshooting card covers PLA-home failures; exotic failure modes (thermistor faults, firmware crashes) are named but deferred to manufacturer support.
- The site links to external references (disabled-feature honesty: they are href-only, the pages load nothing from them) — link rot in those communities over years is possible; the local-first core of the book is unaffected.
