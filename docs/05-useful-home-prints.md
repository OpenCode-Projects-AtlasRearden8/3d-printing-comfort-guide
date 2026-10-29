# Chapter 5 — Genuinely Useful Home Prints

The 3D printing hobby is full of novelties — dragons, planets, articulated octopuses — and they are fine in moderation. But the deep satisfaction of owning a printer is different: **it becomes a part-replacement machine for your actual life.** A broken hinge no longer requires junking the whole thing. A drawer chaos gets a divider fitted to the drawer itself. A scrum of cables stops slithering behind the desk.

This chapter is the field guide to that feeling: the categories of home prints that earn their shelf space, and the practical technique for each.

## The four-part method (works for every category)

Whatever you print, this loop makes it successful on the second try, not the sixth:

1. **Measure with something true.** A ruler or calipers (a cheap set is worth keeping, but a ruler works for most things). Write the numbers down. Guessing is why fittings double-print.
2. **Decide where forces go.** Will it snap? bear weight? slide in and out? This decides print orientation (parts break along layer lines, so a clip's bend axis should run *along* the layers, not across them) — think of layers like wood grain.
3. **Grab the smallest sensible infill.** 15% default covers most; 30%+ only for load-bearing brackets (Chapter 3).
4. **Accept the first copy might be a prototype.** Print, test in place, measure the mismatch, edit the numbers (in a parametric model — see below — or by grabbing a different size), reprint. Two or three iterations is normal and cheap; each is minutes, not days.

That's it. The technique is **a bit of measuring plus the willingness to reprint a ten-minute part twice.**

## Cable clips and cable management

**The problem:** desk cables migrate; chargers slide behind nightstands; guitar cables and hose pipes wander.

**The prints that win here:**

- **Adhesive clips for charging cables** — small angled loops that stick on a desk edge and promise the cable "this is where you sleep."
- **Clamp-style clips** — slip over the desk edge; no adhesive needed for heavy leads.
- **Cable spools** — winder posts for long USB leads, headphone loops, fishing line, and lights-out in-law extension cords.
- **Under-desk trays and hooks** — for power strip, laptop charger, and the wire bundle nerve.

**Getting them right:** orientation matters more than size. Clip arms fail along layer lines, so the *loop's opening axis should run along the layers*. Also print two sizes on the same bed — the ten-minute "too tight" test tells you which the house actually needs. Adhesive clips live at print temperatures (desk-side) happily, but their sticky pad quality is what you buy separately — thin double-sided foam tape beats the printer's own glue tricks.

## Drawer dividers and organizers

**The problem:** kitchen junk drawers, tool drawers, desk drawers, craft bins — everything is a shoe shuffle.

**The prints that win:**

- **Modular grid systems** — adjustable-width dividers cut-to-length per drawer, printed in a few pieces that snap or slot together.
- **Custom trays** — for batteries, dice, screws, first-aid bits, hobby paints, and small medicine bottles that get lost in bulk bins.
- **Cutlery and stationery inserts** — shaped to a drawer's exact dimensions, which store-bought never quite match.

**Getting them right:** measure the inside length, width, and depth of the drawer (not the outside — walls eat millimeters); dividers print flat and hollow-ish (10–15% infill is plenty; they spend their whole life being pressed sideways, not bent). Custom-fit is the whole point — that's why parametric models (later in this chapter) shine here.

## The hinge fix (the hobby's flagship feel-good moment)

**The problem:** a plastic hinge snaps — a laptop stand, vacuum lid, toy chest, bread bin, pet-food tub — and the whole object becomes trash because the one hinge is gone and nobody sells it separately.

**The prints that win:**

- **Replacement hinge** — you measure the pivot width and hole spacing, grab a generic replacement that is roughly the same size (hinges are forgiving if you add padding: a rubber grommet fills slack), and print. Small, quick, saves the original object from the landfill.
- **Screwed-on brackets** — for weak joints, a printed bracket with holes you drill through and screw (a shoebox-size drill beat all-metal on most plastic repairs). The bracket carries the load so the original crack never teases again.
- **Snap-in repair plates** — for plain broken tabs on toy lids: print a plate that covers a crack and extends under a screw or slot.

**Getting them right:** the broken part teaches you where the old design was weak — print the replacement with a bit of extra thickness around the cracked area (you can make one in Tinkercad in twenty minutes even as a beginner; see the tools section below). If the replacement will bend in use, put its layer lines *along* the bend instead of across it — print it lying down, the way layers behave like wood grain.

## The other reliable winners (quick field notes)

- **Mounting pads and bumpers** — rubber-like feet (TPU) or plain PLA feet that stop furniture scratches; for doors that swing too far, a tiny stop that velcro-heads to the wall.
- **Bathroom and kitchen helpers** — toothpaste tube wringers, soap-bar lifter, a trivet sized to your pans (mind Chapter 4's heat warning: not for pans straight off the stove; pot saucers for a table, not burners).
- **Bike and garden odds** — pedal grips if you're handy, hose guides, plant stakes sized to pots (water-plants caveat in Chapter 4: keep PLA out of the watering dish).
- **Workshop and office** — bit holders in drawer-style, invaluable pen stands for a specific clipboard, toolkit cubbies.
- **Fun is allowed** — a phone stand shaped like a cat or a chess set for camping. The test is the same as always: will you be glad you printed it in six months? Fun that stays fun counts as useful.

## Where the models come from

All of these exist as free, printable files — you do not have to model them from scratch. The main libraries, how neighborhoods like search work ("drawer divider parametric"), plus what the licenses attached to those files actually permit, are covered next in [07-free-models-and-licenses.md](07-free-models-and-licenses.md). Reading the license when you save the file (not when someone asks) is a two-second habit that keeps you calm.

## If you eventually want to make your own (the one-tool suggestion)

For years the beginner path to making small edits — resist the urge to install professional CAD. **Tinkercad** (free, browser-based by Autodesk) is the friend-sized version: drag boxes and cylinders, subtract a hole to make a slot, adjust sizes by typed numbers, then export an STL to your slicer. Sixty minutes of quiet clicking turns "I wish this existed" into a file. It pairs perfectly with Chapter 7's parametric libraries — often you take someone's bracket and change one hole size.

That is the whole skill. Measure, orient, print, adjust once, put to work. Repeat.

One honest warning before you get too comfortable: prints *will* unravel sometimes. It happens to everyone, every month, forever — and it is far less frightening than it looks. That is next: see [06-fixing-spaghetti-prints.md](06-fixing-spaghetti-prints.md).
