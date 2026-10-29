# Chapter 2 — Bed Leveling, Decoded

"Level your bed" is the first advice every beginner receives, and it is followed by the least clarity of anything in the hobby. This chapter untangles it for good.

## Why the bed matters so much

Think of the first layer as painting a straight line on a wall (Chapter 3's slicer sends a perfectly calibrated hot-glue pen — the nozzle — to do the painting).

- If the bed is too **far** from the nozzle, the line is laid down soft and round, and it does not stick. The print peels up or comes loose partway through.
- If the bed is too **close**, the nozzle bulls into the bed, the plastic has nowhere to flow, and you get thin, scratched, uneven lines that refuse to grip anything.

Only a small band of "just right" — a squished, translucent-looking line that grabs the bed — actually works. The job of "bed leveling" is getting the whole bed into that band.

## The phrase that confuses everyone

Here is the secret: **"bed leveling" is really two different jobs wearing one name.**

### Job 1: Tramming (getting the bed physically even)

The bed plate must sit parallel to the printer's X-axis (the rail the nozzle car rides on). If one corner is low, prints lean, and one area of the bed always works while another always fails. This is adjusted with the four screws (or knobs) under the bed, and it is a mechanical job — same procedure whether your printer has a self-leveling probe or not.

### Job 2: Setting the distance (getting the nozzle the right distance away)

Once the bed is even, the nozzle still needs to be the right height above it — like holding a pen close enough that its tip touches, but not so hard the paper dents. On printers with **automatic bed leveling (ABL)**, a probe measures the bed and software handles this. On fully manual printers, you do it with the paper test.

Both jobs matter, they use different controls, and mixing them up is the number-one cause of beginner frustration. When advice online says "I re-leveled and it's still bad," it almost always means only one of the two jobs was done.

## The paper test (the classic manual method)

For the nozzle-to-bed distance. A sheet of plain printer paper is about 0.1 mm thick — remarkably close to the first layer height we want.

1. Preheat the bed (and nozzle, if your printer likes it) to printing temperature for the material — for PLA around 60 °C bed, and hot nozzle around 200 °C. Metal expands when warm; always do this at operating temperature.
2. Home the printer (usually "Home All" on the menu). The nozzle drops to its zero point.
3. Slide a sheet of paper under the nozzle, right at the contact point.
4. Adjust the height so the paper has a slight, even drag: you can pull it out, and it slightly resists — like pulling a bank card through a tight wallet slot, not a piece of sandpaper.
5. Do this at each of the four corners, then repeat all four a second time (adjusting one corner slightly affects its neighbors, so a second pass settles everything).
6. Finish by checking the center point the same way.

On printers with a bed that moves forward-backward and screws at the front corners, this whole routine takes ten minutes the first time and two minutes once your hands learn the feel.

## Tramming with the knobs underneath

When one corner of the bed is genuinely too low or too high (usually most obvious as one corner of the paper test that always feels the same no matter what, or a first layer that only works in one region):

1. Run the paper test at all four corners first and **notice the pattern**. Note which corner felt loose (nozzle too far — the corner needs to come up) and which felt trench-tight or grinding (needs to come down).
2. Turn the corresponding **knob or screw under the bed**. Righty-tighty raises, lefty-loosey lowers, but treat this as slow tuning: an eighth-turn at a time is plenty at the start.
3. Run the paper test again. Adjust the pattern again. It converges in two or three rounds; do not chase perfection beyond that.

Once you trust the routine, you will realize: tramming is not delicate surgery. It is stubborn, repeatable, and slightly boring, which is exactly why it works.

## Automatic bed leveling (ABL) — what it does and doesn't

Printers with a probe (a small sensor that taps the bed at several points) handle the *distance* job: they map the bed and adjust the software's model of the surface so the first layer has even clearance across it. On a flat-bed machine, this is genuinely a huge convenience — especially in a household with vibrations, occasional bumps, or prints you start and then carry on with your day.

Two things ABL does **not** do:

- **It does not replace clean and dry.** Fingerprints, dust, and old plastic residue affect adhesion way beyond what software can fix. A wash with dish soap and warm water every handful of prints, dried with a lint-free towel, beats any probe.
- **It does not tram the bed physically.** If the bed is badly warped — some very cheap machines ship with warped plates — a probe can only partially compensate. If a corner is a mile out, its knob or screw still wants adjusting. The paper test remains useful even on automatic machines, because it tells you the *mechanical* shape of the bed.

## The Z offset, when your printer mentions it

Many machines with ABL expose a setting called **Z offset** — a number setting where zero height is relative to the probe's bed map. When your first layer is consistently too squished (grinding, thin lines), raise the Z offset a hair (typically +0.05 mm steps makes a real difference). When it is too far (round ropey lines that don't stick), lower it by the same amount.

You will rarely touch any other number. It is a trim knob, not a surgery.

## The first layer is a diagnostic, not a ritual

Treat the first ten minutes of every early print as your diagnostic window — this is how failures turn into cheap lessons instead of spaghetti messes (no pun ruined later by Chapter 6). You are looking for:

- All lines **touching each other**, no gaps showing bed between them.
- Corners of small shapes **staying put** — no peeling up.
- The nozzle **not plowing** the bed or leaving shiny, scraped, overly flat lines.

Small errors at this stage are correctable with a knob turn or an offset nudge, and you will re-level less than you think you will. A bed that holds its tram and gets touched politely stays level for weeks.

The number of printers whose owners blame "bad beds" that actually just needed one good, slow, temperature-warmed tramming is remarkable. Yours is probably fine.

Next: with the bed holding a first layer, software takes over — see [03-slicers-in-plain-english.md](03-slicers-in-plain-english.md).
