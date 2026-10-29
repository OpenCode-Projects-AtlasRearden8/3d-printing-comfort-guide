# Chapter 6 — Fixing Spaghetti Prints, Calmly

Sooner or later you walk into the room and find it: a bird's nest of plastic strands where an object was supposed to be. Everyone who owns a printer meets this. The difference between a comfortable printer owner and a frustrated one is not prints-per-turn — it is **a short, calm routine for diagnosis**. This chapter is that routine.

## The two-minute rule (always, everyone)

When you see a failed print:

1. **Leave it.** Don't peel, don't poke, don't rescue.
2. **Take a photo in place.** Where did the nest start? A clear starting layer tells you most of the diagnosis before you touch anything.
3. **Note the time.** When did it go wrong? Early layers point to bed problems; middle prints point to shift, fuel, or overhang problems.

Then — and this is the mindset — you are not fixing a *disaster*. You are a mechanic reading a note a machine left you. The print is just paper: the evidence is on the bed and in the photos.

## The calm rescue sequence

1. Lift the failed print and its nest off the bed (flex your steel plate; large nests come off with the pan).
2. Snip the strand ball away from any still-stuck first layer, and check whether part of the object survived glued to the bed — sometimes the bottom half is fine and only the layers above it unraveled.
3. Clean the bed (dish soap and warm water or, between washes, a quick isopropyl wipe) — Chapter 2's essentials.
4. Diagnose below, change **one** thing, reprint.

One change at a time is the whole discipline. Two changes make success un-traceable; three make it a hobby of superstition.

## The Causes, named

Each cause has a look you can recognize. Match your photo to one of these.

### Spaghetti everywhere (a full nest, print fully detached)

**What it means:** at some layer, the whole object stopped sticking and the nozzle kept drawing in mid-air.

**Order of likelihood:**
1. **Filament ran out or snapped or tangled** — check the spool first. A tangle or snapped end is the most common culprit and quickest to find.
2. **First layer was never well stuck** — it peeled later and everything unraveled from there.
3. **Layer shift** knocked the whole object off its position (see below).
4. **Blob on the nozzle** dragged the part loose.

**Fixes:** check and re-feed the filament; re-tram or re-clean the bed (Chapter 2); try a brim (Chapter 3); re-anchor the nozzle blob (below).

### Corners lifting, object curling up (warping)

**What it means:** the first layer is not gripping, or the material wants to shrink as it cools. For PLA, almost always adhesion.

**Fixes:** wash the bed with soap; raise bed temperature 5 °C; add a brim; on ABL printers nudge Z offset closer (Chapter 2). Keep the print away from a cold draftsill — a cooling corner lifts more readily than a warm one.

### Nothing sticks at all (first layer fails within a minute)

**What it means:** nozzle-to-bed distance is wrong — too high, or the bed is dirty or un-trammed. Prints (temporarily as always) forgiven for this one: it is Chapter 2's whole reason for existing.

**Fixes:** re-run the paper test at operating temperature; wash the plate; if lines look round and ropey, reduce Z offset distance; if lines are gouged, raise it.

### Layer shifts (the stair-step look)

**What it means:** the whole print slid sideways mid-run. The object's part above the shift point belongs elsewhere.

**Fixes:** check for the printer walking or snagging cables; tighten loose belts (per your printer manual — two minutes and a screwdriver); ensure the print is not blocked by a part of the printer; jerk gear/belt wear is the deeper cause, rare in the first months.

### Stringing (hairy web-threads between printed parts)

**What it means:** the nozzle leaks while traveling between two points. PLA with wet filament strings heavily.

**Fixes:** dry the filament (Chapter 4 storage; also the honest answer if the spool is old); raise retraction distance/speed a hair via the printer profile community defaults; drop nozzle temp 5 °C. Try these in that order — moisture first, because it is the most common and free.

### Under-extrusion (thin, gappy lines; gaps on walls)

**What it means:** not enough plastic reaching the nozzle. Usually a partial clog or a snagged filament feeding slowly.

**Fixes:** re-feed filament and check the path tangles; clear the nozzle by briefly pushing fresh filament through while hot (or use the needle your kit provided, if any); if the spool is damp, the fizzes also read as gaps. If a nozzle is truly jammed, they are cheap and unscrewable — a spare or two is among the few "day one purchases" that actually earn their box.

### Blob on nozzle (a lump of melted plastic in progress)

**What it means:** retraction and stringing leftovers build up on a hot nozzle until they touch the print, drag it, and start a nest.

**Fixes:** while the nozzle is hot, **carefully** clean the bump with forceps or a small bare-metal brush, if yours shipped with one — never a bare hand (the nozzle is ~200 °C). A silicone sock, if yours shipped without one, cuts blob buildup down noticeably; most owners get along fine without it, but the sock is the quieter life.

### Print stops halfway (or reboots and starts in a new spot)

**What it means:** usually power or an error stop — check the printer's screen messages.

**Fixes:** check the power cable; long prints deserve a whole night where nobody unplugs the router or vacuums the outlet area. If a print started failing consistently right after a firmware or slicer update, that is a manufacturer bug, not your fault — your printer's support pages and community threads will already have it.

## When the diagnosis fails anyway

Some night, two good changes will be applied and the print still fails. That is the moment for the one tool that always works: **print something else easy actually, right now.** A ten-minute, low-stakes successful print resets morale in a way nothing else can. Then return to the problem fresh. Most failures dissolve in the morning that seemed midnight-epic.

You keep a paper log? A note on the fridge — good print, bad print, one-word cause — beats a spreadsheet habit and reads like a mood tracker for a machine. Do it for the first month. It ends on its own as failures stop recurring.

## Getting help the local-first way

When a term from this chapter is beyond you — belts, firmware, extruder motors — the same calm loop applies: **photo, model name (printer and slicer), symptom, what you already tried.** A post with those four things gets useful answers in hours rather than a week of guessing. The friendly places from Chapter 7's world (Printables and the big maker forums) all have this culture.

And words you still need to decode will be waiting in [10-glossary.md](10-glossary.md).

That is the whole spaghetti story: leave it, photo it, match the look, change one thing, reprint. Failures are a printer's way of teaching — and with a calm routine, you learn faster than anyone who only ever succeeds.

Next up, the paperwork side of the hobby — free model sites and being allowed to actually use those files: [07-free-models-and-licenses.md](07-free-models-and-licenses.md).
