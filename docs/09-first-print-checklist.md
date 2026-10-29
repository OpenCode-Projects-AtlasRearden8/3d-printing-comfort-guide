# Chapter 9 — The First-Print Checklist and Troubleshooting Card

This chapter is designed to live on the wall next to the printer. It takes the whole book and compresses it into a pre-print ritual you can run in five minutes, plus a one-page rescue card for the days things sour.

Print this page from the readable site (the static build includes a one-page "whole book" version that prints cleanly), or copy the lists below onto a card. Machines change; checklists stay.

## Before the print: the five-minute ritual

Check off each of these before pressing start. In a few weeks the ritual runs on its own in under two minutes.

- [ ] **Filament loaded and flowing** — feed it, snip a clean angled tip (Chapter 4), and watch a smooth dollop of melted plastic come out during preheat.
- [ ] **Filament is dry** (bag sealed, silica inside, no pop-and-fizz on test extrusion) — Chapter 4.
- [ ] **Spool free to turn** — no tangle under the last wrap; the loose end is clipped.
- [ ] **Bed washed recently** — dish soap and water within the last handful of prints, dried on a lint-free towel — Chapter 2.
- [ ] **First layer settings sane** — default PLA profile in the slicer, 0.2 mm layer height, skirt on — Chapter 3.
- [ ] **Model oriented well** — no steep overhangs that surprise supports; watch the slicer preview once through — Chapter 3.
- [ ] **Z offset or ABL map fresh** (if something was adjusted, knocked, or the paper test disagrees with the machine) — Chapter 2.
- [ ] **Give me ten minutes** — you will stay near the printer through the first layers, which are 100% of the risk window.
- [ ] **The room is ready** — door cracked or window open, nothing flammable within reach, pets and children elsewhere — Chapter 8.

That is the whole ritual. Note it has no "hope" step — every line is mechanical.

## The first ten minutes, layer by layer

Watch these like a lifeguard. All early failures announce themselves here, quietly.

- **The skirt ring** — draw around the print first: check it forms smooth, connected, evenly-squished lines. A rough or gappy skirt is diagnosis in action (Chapter 6, "first layer").
- **The first layer lines** — should touch their neighbors, no gaps of visible bed between them, no gouged ridges. Lifting corners in the first minute are easy to rescue with a brim plus a reset (cheap now, expensive in three hours).
- **Silence check** — a grinding or ticking sound means something is scraping; stop the print and look. Prints do not need you to fix sound problems; they just ask you to notice them early.
- **The object detaches** — every printer owner's rite of passage. Stop the print at the moment it peels: do not watch it become spaghetti (Chapter 6).

## After the print, the same two habits every time

- **Peel, don't chisel.** Flex the steel plate; a print that resists even a patient hand wants a gentle spatula tap or a brief cool-down of the bed — never a hard metal pry.
- **Snapshot a good print.** A photo of a successful setup (bed state, filament, choice of model) is the best "reference chapter" you can write for yourself — and the fastest way to notice what changed when prints drift.

## The troubleshooting card

The one-page rescue version of Chapter 6. Symptoms first, most-likely cause second, calm fix third.

| What you see | Most likely cause | The calm fix |
| --- | --- | --- |
| Full spaghetti nest mid-print | Filament ran out, snapped, or tangled | Check spool; re-feed; reprint |
| Nothing sticks in the first minute | Bed distance or dirty bed | Paper test warm; wash plate; reduce Z offset |
| First layer fine, later layers lift | Drafty room or bed too cool | Close drafts; +5 °C bed; add a brim |
| Print has a stair-step, whole face moved | Layer shift — belts loose or stepper snagged | Tighten belts; clear path; re-anchor clips |
| Hairy web threads between parts | Wet filament (most common), then retraction | Dry filament first; then raise retraction; then -5 °C nozzle |
| Gappy, thin walls | Partial clog or feed snag | Re-feed; check path; clear hot nozzle; spare nozzle if jam repeats |
| Blob of plastic riding the nozzle | Retraction leftovers on hot nozzle | Clean hot (forceps, gloves, careful); consider silicone sock |
| Print stops halfway, alone | Power or printer error message | Read the screen; reseat power; run the print again fresh |
| Corner of the object curls up early | Overhangs and no brim | Reorient model; add brim; slow down a notch |
| Steam/hissing during prints | Filament very wet | Proper drying now (dryer or sealed bags with silica) |

A note that Chapter 6 is the detailed version of this table: every row there has three minutes of context worth knowing once. This card is the **read-again-thousand-times** version for when you are not really in the mood to read.

## The three friendly reminders that end most bad afternoons

1. **One change at a time.** Two changes make causes unknowable.
2. **Print something easy and small next.** A successful ten-minute clip resets morale in a way a four-hour gamble cannot.
3. **Failures are teaching**, not verdicts. A month into the hobby you will have a printer that works and a list of causes you know by name. Six months in, spaghetti becomes interesting rather than upsetting — a puzzle with three possible answers.

Onward to the last chapter: the vocabulary, decoded in one place — [10-glossary.md](10-glossary.md).
