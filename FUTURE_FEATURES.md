# Future features — starbase-builder

The ordered draft is the version table in `design-docs/program-roadmap-design.html`.

Phases 0 through 5 are the earlier draft, through `5.0.0-compute`. Phases 6 through 10 are the notes that used to live only in this file. A new idea is a new row at the bottom of that table.

When a row ships or is dropped, remove it from the table and note the ship in `IMPLEMENTATION_LOG.md`.

**Last shipped:** `0.7.0-tanks`. The header shows RP-1 and liquid oxygen. A short tank stops the fire, and the Orbital Pad card shows fires in the last 30 days and days since the last fire. See `IMPLEMENTATION_LOG.md`.

## UI and UX

The screen pass is not a pile of names on the map. Detail belongs to objects.

A main building is one thing you buy. Its parts are created with it. Each part is its own object, with its own place on that building and its own job. Zoomed out, you see the main. Zoomed in, you see the parts. A name shows for the part under the pointer, and for the one you selected. The buy column lists mains only. It does not list every part.

Not in the panel slice. The first time parts exist in the game, they are stats on the building you already bought. Starfactory, Mega Bay, and Orbital Pad keep those names. A weak stat can fail on its own. Placeable parts, roads, and pipes stay the later rule below. A tank farm is still the tanks patch, not a new name for the pad.

The three mains for the first pass:

- **Starfactory.** Hall, roof crane, stack stand.
- **Mega Bay.** Hall, one berth, service crane. A second bay, the high bay, and the Sanchez yard are later mains, not rooms inside this one.
- **Orbital pad.** As bought: mount, flame trench, deluge plate, deluge pumps, one water tank. Two upgrades, bought separately. The tank farm adds an oxygen tank, a kerosene tank, and a methane tank. The Starship tower adds the tower, the chopsticks, and the ship arm. A Falcon 1 does not use the methane tank or the arms. Pad 2 is a later main and gets the same choices.

A quiet part can be selected. It does not change the fire until the version that needs it.

Massey's is its own site inland, later. Its parts are the ship cryo stand, the booster cryo stand, the static-fire stand, and the methane farm.

The object rule and the part pictures are in `design-docs/site-objects-design.html`.

Leave the map free of a caption for every part. Leave the launch track off until a rocket actually flies.

The owned line shipped in `0.4.0-borderline`. It follows the coast, about 8 km inland on the solid beach, and it follows the bay where the water cuts in. Each building is a separate buy on a fixed plot, and the building is about one tenth of that plot. The Land column counts plots. The picture is `design-docs/0.4.0-borderline-design.html`.

## Motion, then pictures

`0.6.0-motion` plays the loop you already have, on the map. The static-fire modal closes. A build shows in the Starfactory. The finished Falcon 1 rolls from the Starfactory along the yard road to Mega Bay. It rolls from the bay to the Orbital Pad on that same road. At the pad it rises onto the mount. The static fire burns on the mount, and the flame stays on the map. This version only animates steps that already exist. Later versions add their own animations on top of the same system.

`0.12.0-picture` replaces the plain halls. Starfactory, Mega Bay, and the Orbital Pad each get a picture you can read on the map. The seats stay. The buys stay. No new rule.

`0.13.0-motion-final` is a final pass on every animation once the buildings are drawn. Speeds, timing, and look all match. It covers the roll, the raise, the fire, refueling, flight, and landing.

This chapter builds one Falcon 1. The factory finishes that rocket. The bay holds it and refurbishes it. The bay does not stack sections yet. Sections come from the factory and get mounted in the bay when Starship arrives. The tower that lifts a stack is the later pad upgrade, not this raise.

No new fire rule. The numbers that pass or fail the fire stay the ones you already have.

Later rows on `design-docs/program-roadmap-design.html` add rules on that same coast line. `6.0.0-yard` adds pad buffer, the first houses, and the highway closure. `6.2.0-stand` is an inland test stand on a parcel of about 930 acres. `6.3.0-farm` lets tank-pad acres set propellant and deluge capacity. `6.4.0-mitigation` is wetland you cannot build on, required before the second pad. `6.5.0-town` adds a clinic and a school after the beds exist. None of those rules ship with the line.

## Sound

The live game is quiet. The mute button and the Web Audio tones are out of `index.html`. They come back at `10.3.0-sound` on `design-docs/program-roadmap-design.html`: a build, a countdown, a fire, a landing, and a mute that stays in the browser.
