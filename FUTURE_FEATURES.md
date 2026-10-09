# Future features — starbase-builder

The ordered draft is the version table in `design-docs/program-roadmap-design.html`.

Phases 0 through 5 are the earlier draft, through `5.0.0-compute`. Phases 6 through 10 are the notes that used to live only in this file. A new idea is a new row at the bottom of that table.

When a row ships or is dropped, remove it from the table and note the ship in `IMPLEMENTATION_LOG.md`.

**Last shipped:** Falcon 1 only. Merlin card, a fire that follows the numbers, and a sky you can wait out. See `IMPLEMENTATION_LOG.md`.

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

Leave the map free of a caption for every part. Leave the launch track off until a rocket actually flies. Land you own is one soft shape, not a stack of white boxes. Area is shown in acres, with square feet beside it, and the number has to match the ground the building sits on.

## Sound

The live game is quiet. The mute button and the Web Audio tones are out of `index.html`. They come back at `10.3.0-sound` on `design-docs/program-roadmap-design.html`: a build, a countdown, a fire, a landing, and a mute that stays in the browser.
