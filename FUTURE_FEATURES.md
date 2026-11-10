# Future features — starbase-builder

The ordered draft is the version table in `design-docs/program-roadmap-design.html`. That page is the source of truth. This file holds the detail behind its rows.

Phase 0 is Starship development at Starbase in Texas, up to orbit. Phase 1 is recovery and the catch. Phases 2, 3, and 4 are a branch the player chooses: Starlink, the Moon and Mars, or the Falcon story at the real Falcon sites. Phases 5 through 9 are compute, the yard, longer flights, picture and record, and the fleet desk. A new idea is a new row at the bottom of that table.

When a row ships or is dropped, remove it from the table and note the ship in `IMPLEMENTATION_LOG.md`.

**Last shipped:** `0.14.0-defects`. A new article can leave with one real short part the tests can find. See `IMPLEMENTATION_LOG.md`. The next row is `0.15.0-hop`.

## Roadmap restructure (2026-11-09)

Tiago approved a new order on 2026-11-09. The goal is to set the story straight. Starbase in Texas is the real Starship site. Falcon never started there. So phase 0 is now Starship development at Starbase, up to orbit. The Falcon story moves to its real sites, as a branch after phase 1.

The shipped slices, `0.1.0-foundation` through `0.11.0-screen`, were built on a Falcon 1 stand-in on the Texas site. The yard, the map, Land, the Inspector, the purse, the tanks, the motion, and the part sheet all carry over. From `0.12.0-raptor` the vehicle becomes a Starship development article.

The real test chain after a vehicle is built is tank proof, tanking, static fire, data review, then the range. Tanking means the crew fills the tanks and drains them again. `0.13.0-proof` shipped that order. `0.14.0-defects` is live, and the pad still runs it. A new article can leave with a real short part. Falcon 1 ran a thinner chain. It went more often from build to a pad static fire to flight, and a flight carried more risk. `4.0.0-falcon1` keeps that.

The real Falcon order comes from SpaceX Brief. The rockets were built in California, at El Segundo and then Hawthorne. Falcon 1 flew from Omelek Island in the Kwajalein Atoll, from 2006 to 2009. It made orbit on 28 September 2008. Falcon 9 started at Cape Canaveral SLC-40, with its first flight in June 2010. Vandenberg SLC-4E came next. SpaceX leased LC-39A in 2014 and first launched from there in February 2017. Falcon Heavy and crew flights fly from 39A.

The invented Louisiana and Florida Starbases are dropped. The real Falcon sites replace them.

After phase 1 the player chooses a branch. Phases 2, 3, and 4 can be played in any order. The Moon and Mars branch needs the catch from `1.1.0-catch`.

One design check stays open. The staging row, `0.18.0-suborbital`, must stay decided by the hardware. A staging failure names the short part. It is not a hidden chance. The mix is 3.6 kg of liquid oxygen for each kg of methane, and methane has its own tank. The kerosene tank waits for the Falcon story.

The game parallels came from Starbase Research. Buzz Aldrin's Race Into Space and the KSP TestFlight mod show tests that earn reliability part by part. KSP RP-1 splits research time from factory time. Anno 1800 opens a second site while the first keeps earning.

## UI and UX

`0.11.0-screen` shipped the layout pass on Land, the Inspector, and the rocket sheet. No fire, purse, or part rule moved. A staging failure now sits in `0.18.0-suborbital`, when a booster and a ship exist.

The notes below are not that row. Detail belongs to objects.

A main building is one thing you buy. Its parts are created with it. Each part is its own object, with its own place on that building and its own job. Zoomed out, you see the main. Zoomed in, you see the parts. A name shows for the part under the pointer, and for the one you selected. The buy column lists mains only. It does not list every part.

The first time parts exist in the game, they are stats on the building you already bought. Starfactory, Mega Bay, and Orbital Pad keep those names. A weak stat can fail on its own. Placeable parts, roads, and pipes stay the later rule below. A tank farm is still the tanks patch, not a new name for the pad.

The three mains:

- **Starfactory.** Hall, roof crane, stack stand.
- **Mega Bay.** Hall, one berth, service crane. A second bay, the high bay, and the Sanchez yard are later mains, not rooms inside this one.
- **Orbital pad.** As bought: mount, flame trench, deluge plate, deluge pumps, one water tank. Two upgrades, bought separately. The tank farm adds an oxygen tank, a kerosene tank, and a methane tank. The methane tank goes to work at `0.12.0-raptor`. The kerosene tank waits for the Falcon story. The Starship tower adds the tower, the chopsticks, and the ship arm. The tower goes up at `0.17.0-stack`, and the catch arrives at `1.1.0-catch`. The hop at `0.15.0-hop` lands on a nearby pad. Pad 2 is a later main and gets the same choices.

A quiet part can be selected. It does not change the fire until the version that needs it.

Massey's is its own site inland, later. Its parts are the ship cryo stand, the booster cryo stand, the static-fire stand, and the methane farm. Until it exists, the cryo proof from `0.13.0-proof` runs on the Orbital Pad. `6.2.0-stand` is the row that moves those tests inland.

The object rule and the part pictures are in `design-docs/site-objects-design.html`.

Leave the map free of a caption for every part. Leave the launch track off until a rocket actually flies.

The owned line shipped in `0.4.0-borderline`. It follows the coast, about 8 km inland on the solid beach, and it follows the bay where the water cuts in. Each building is a separate buy on a fixed plot, and the building is about one tenth of that plot. The Land column counts plots. The picture is `design-docs/0.4.0-borderline-design.html`.

## Motion, then pictures

`0.6.0-motion` plays the loop you already have, on the map. The static-fire modal closes. A build shows in the Starfactory. The finished rocket rolls from the Starfactory along the yard road to Mega Bay. It rolls from the bay to the Orbital Pad on that same road. At the pad it rises onto the mount. The static fire burns on the mount, and the flame stays on the map. Later versions add their own animations on top of the same system.

`0.8.0-flight` shipped the first launch. `0.9.0-economy` shipped the purse. `0.10.0-parts` shipped the Merlin, the fuel fitting, and the stage. `0.11.0-screen` shipped the screen layout. `0.12.0-raptor` shipped. `0.13.0-proof` shipped. `0.13.1-fixes` shipped. `0.14.0-defects` is live. The next row is `0.15.0-hop`. Then come `0.16.0-high-hop`, `0.17.0-stack`, `0.18.0-suborbital`, and `0.19.0-orbit`. `0.20.0-tracking`, `0.21.0-picture`, and `0.22.0-motion-final` come after orbit, still in phase 0.

`0.20.0-tracking` lets you follow flights on the map. When you zoom out, each rocket shows its path and a box that grows and shrinks around it, with live numbers like altitude, speed and flight phase. Later, with many launches and some automation, you can watch them all fly at once.

`0.21.0-picture` replaces the plain halls. Starfactory, Mega Bay, and the Orbital Pad each get a picture you can read on the map. The seats stay. The buys stay. No new rule.

`0.22.0-motion-final` is a final pass on every animation once the buildings are drawn. Speeds, timing, and look all match. It covers the roll, the raise, the tests, the fire, refueling, the hops, flight, and landing.

The Starfactory builds one development article at a time. The bay holds it and refurbishes it. The bay does not stack sections yet. The tower stacks the ship on the booster at `0.17.0-stack`. The hop is `0.15.0-hop`. One Raptor on a short test vehicle lifts off, hovers, and lands on a nearby pad. This is like Starhopper at Boca Chica in 2019. That vehicle flew 150 meters in August of that year. The high hop at `0.16.0-high-hop` adds a flip and a landing, like the SN flights. The catch is `1.1.0-catch`.

The fire still passes or fails on thrust, the pad, the tanks, and the wind. `0.12.0-raptor` changed the numbers. Raptor 1 is 1814 kN. Pad level 1 holds 2000 kN. The engine floor is 1500 kN. A fire loads 609 kg of methane and 2193 kg of liquid oxygen.

## Test campaign

A launch before the first contract spends the purse and pays nothing. That flight is the test. Fire the Orbital Pad until the card shows a run of clean results. Then fly.

The pad card already shows fires in the last 30 days, and days since the last fire. The cryo proof and the tanking run are live now, and each one joins that record. Each flight joins it later. The hop is `0.15.0-hop`.

Reliability is that record. It is not a meter you buy. A cryo proof shows the tanks hold. A tanking run shows the fuel lines hold. A clean static fire proves the mount and the engine. A flight proves the vehicle. A fail names the part. If every test logs the same line, the tests teach nothing.

`0.14.0-defects` is live. A prototype can leave the Starfactory with one short part. The short is a real number: Structure 60, Fuel lines 0 seconds, or thrust 1400 kN. Those are game numbers. The tests can find it. The fix is the days and the steel prices that already exist. You can skip a test, and the part stays as it is. `1.2.0-refurb` runs the same check on a flown stage. `1.3.0-rate` lets a better process send fewer defects out of the factory.

The first paying contract arrives at `0.18.0-suborbital`. It reads the test and flight record before it offers the sale. The sale names how many flights and how many clean results it wants. Pay arrives when a flight meets the sale. `0.19.0-orbit` lets a contract ask for an orbit card.

Staging can fail at `0.18.0-suborbital`. The booster and the ship separate in flight. If the part that does that is short, the debrief names it.

`1.0.0-recovery` is the first way to spend less. A stage that comes home loses life on a hard flight. A customer who asks you to bring the stage home waits for `7.0.0-ladder`.

A flight load is a large spend. Until the contract, the day adds no money. Investors pay when a goal is finished. A run of unpaid flights can stall the yard. `6.1.0-rounds` pays once for the first hop, the first orbit, and the first catch. When the contract is planned, that first paid flight should cover the next vehicle.

Later rows on `design-docs/program-roadmap-design.html` add rules on that same coast line. `6.0.0-yard` adds pad buffer, the first houses, and the highway closure. `6.2.0-stand` is an inland test stand on a parcel of about 930 acres. `6.3.0-farm` lets tank-pad acres set propellant and deluge capacity. `6.4.0-mitigation` is wetland you cannot build on, required before a second Orbital Pad. `6.5.0-town` adds a clinic and a school after the beds exist. None of those rules ship with the line.

## Sound

The live game is quiet. The mute button and the Web Audio tones are out of `index.html`. They come back at `8.3.0-sound` on `design-docs/program-roadmap-design.html`: a build, a countdown, a fire, a landing, and a mute that stays in the browser.
