# Chapter 3 — Slicers, in Plain English

The model is the recipe; the printer is the oven. Between them sits the **slicer** — the software that reads a 3D model, divides it into hundreds of thin layers, and writes the numbered instruction list (G-code) the printer follows. This chapter teaches just enough of it to be dangerous, then shows you the handful of settings that truly matter.

## What a slicer actually does

Open a slicer (examples later in this chapter) and drop in a model file — usually a `.STL` or `.3MF`. The program will show you the simulated object on a print bed. Click "slice" and it lays bare the plan: outlines per layer, infill patterns, travel moves, and an estimated print time. Save the result onto an SD card, USB stick, or over your Wi-Fi, and the printer runs it like a music playlist.

The word *slice* is literal. The software looks at your object as a stack of paper-thin layers — 0.2 mm is the common default — and turns each layer into the sideways movements that draw it.

## Which slicer?

Every community has its favorite; the differences mostly matter to experts. For a beginner, the rule is short:

- **The slicer your printer's maker recommends** is almost always fine and pre-configured with your exact printer's profile. Use it first.
- Popular names you will encounter: **Cura**, **PrusaSlicer**, **OrcaSlicer**, **Bambu Studio** (for the popular brands). Any of them can print every object in this book.
- Do **not** compare slicer feature lists on forums at midnight. Pick your brand's recommendation, learn six settings (below), and move on.

Most slicers are free and offline-capable — a good fit for a local-first hobby.

## The six settings that matter

Open any slicer and you will face dozens of knobs. Relax. For useful home printing in PLA, only these six meaningfully change outcomes:

### 1. Layer height

How tall each printed layer is. **0.2 mm** is the perfect default: strong enough for functional parts, visible-but-fine layer lines, reasonable time. Drop to 0.12–0.16 for showy smooth surfaces; rise to 0.28 for chunky functional items you will hide in a drawer. Layer height is the biggest single driver of print time.

### 2. Infill

The pattern inside the object. Defaults (around 15%, grid pattern) suit almost everything. Functional clips and brackets that take real force deserve 30–40%; signs or display items are fine at 10% (hollow-ish walls with a sparse interior). More infill increases time and material roughly proportionally.

### 3. Walls (also called perimeters)

The number of solid outline loops per layer, typically 2–3. This is where functional strength largely comes from — for parts that get stressed (hinge pieces, hooks, brackets), leave this at 3 rather than 2. Do not worry about it further until something breaks.

### 4. Supports

Removable scaffolding for overhangs — parts of your model that hang in the air unsupported. As a rule of thumb: slopes steeper than about 45 degrees from vertical need support; vertical or tapered surfaces do not. Good slicer defaults plus the checkbox "generate supports" will carry you. The art of *not* needing supports — by re-orienting the model on the bed — is learned fastest by printing the useful objects in Chapter 5, whose models are usually designed to print support-free or support-light.

### 5. First-layer extras: skirt, brim, raft

Three ways to help the first layer:

- **Skirt** — a loose practice ring drawn around the print that never touches it. Purges the nozzle and previews flow. Free insurance, on by default; fine.
- **Brim** — extra flat flaps of the first layer reaching outward from the print, peeled away afterward. Useful for tall skinny parts whose small footprint might peel. It is the common upgrade when a first layer "mostly" sticks.
- **Raft** — a thick sacrificial base layer for the whole model. Almost never needed in PLA; try a brim first, and only reach for a raft for very odd geometries.

### 6. Temperatures

Your filament specifies a nozzle range (see [04-pla-basics.md](04-pla-basics.md)) — the slicer profile for generic PLA usually starts correctly (around 200 °C nozzle, 60 °C bed). Leave them alone unless a print misbehaves in a way Chapters 6 names specifically. Like the oven dial, temperatures are a trim control, not a starting debate.

## The one habit worth keeping from day one

**Name your profile and version your changes.** When the default profile works, save a copy called "PLA — house profile" and only customize that copy. When you change something that helps, update the profile and note it. After a month you will have one calm, reliable, *yours* configuration instead of a scroll of unsaved experiments — and a bad print will be traceable ("what changed since the last good one?") instead of mysterious.

## The three phases of a slice (worth understanding once)

1. **Slice:** read the model, build the layer plans, generate toolpaths. Seconds. Click it.
2. **Preview:** the slicer shows you the plan layer by layer. Ten seconds of scrolling here is the cheapest insurance in 3D printing: you can see supports hanging into odd places, a model printed in midair, or a floating island of plastic that would print into a bird's nest (see Chapter 6).
3. **Save and send:** write the file and move it to the printer. Time estimates are estimates — assume twenty percent longer than promised for the whole first week.

## Small things beginners worry about that mostly take care of themselves

- **Print speed** — defaults are fine; faster settings on the same machine mostly change texture and failure modes, not your household usefulness.
- **Cooling fan** — profiles set sensible PLA values (fan on from layer 2 or so). Leave it.
- **Retraction** (string-mitigation travel tricks) — modern profiles default well; only tune when stringing appears (Chapter 6 has the fix list).
- **Fixing every warning the slicer prompts about.** Orange warnings are worth a look; yellow ones are often safe to ignore. Read the hint, use judgment.

## Where models come from (a one-line forward)

The slicer needs a model, and the best free models live in a few big shared libraries. What you download, what their licenses actually let you do, and how to stay comfortably within the rules — that is the next two chapters' work, or jump ahead to [07-free-models-and-licenses.md](07-free-models-and-licenses.md).

Next, though, is the material itself: the humble plastic that does nearly all of it — see [04-pla-basics.md](04-pla-basics.md).
