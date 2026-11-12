# Future features — starbase-builder

The ordered draft is the version table in `design-docs/program-roadmap-design.html`. That page is the source of truth. This file holds the detail behind its rows.

Phase 0 is Starship development at Starbase in Texas, up to orbit. Phase 1 is recovery and the catch. Phases 2, 3, and 4 are a branch the player chooses: Starlink, the Moon and Mars, or the Falcon story at the real Falcon sites. Phases 5 through 9 are compute, the yard, longer flights, picture and record, and the fleet desk. A new idea is a new row at the bottom of that table.

When a row ships or is dropped, remove it from the table and note the ship in `IMPLEMENTATION_LOG.md`.

**Last shipped:** `0.14.1-teeth`. The static fire reads Structure and the fuel lines. A reload continues the yard. The Mega Bay fix stays off until the pad has checked that part. See `IMPLEMENTATION_LOG.md`. The next row is `0.14.2-seed`.

## Roadmap restructure (2026-11-09)

Tiago approved a new order on 2026-11-09. The goal is to set the story straight. Starbase in Texas is the real Starship site. Falcon never started there. So phase 0 is now Starship development at Starbase, up to orbit. The Falcon story moves to its real sites, as a branch after phase 1.

The shipped slices, `0.1.0-foundation` through `0.11.0-screen`, were built on a Falcon 1 stand-in on the Texas site. The yard, the map, Land, the Inspector, the purse, the tanks, the motion, and the part sheet all carry over. From `0.12.0-raptor` the vehicle becomes a Starship development article.

The real test chain after a vehicle is built is tank proof, tanking, static fire, data review, then the range. Tanking means the crew fills the tanks and drains them again. `0.13.0-proof` shipped that order. `0.14.1-teeth` is live, and the pad still runs it. A new article can leave with a real short part. Falcon 1 ran a thinner chain. It went more often from build to a pad static fire to flight, and a flight carried more risk. `4.0.0-falcon1` keeps that.

The real Falcon order comes from SpaceX Brief. The rockets were built in California, at El Segundo and then Hawthorne. Falcon 1 flew from Omelek Island in the Kwajalein Atoll, from 2006 to 2009. It made orbit on 28 September 2008. Falcon 9 started at Cape Canaveral SLC-40, with its first flight in June 2010. Vandenberg SLC-4E came next. SpaceX leased LC-39A in 2014 and first launched from there in February 2017. Falcon Heavy and crew flights fly from 39A.

The invented Louisiana and Florida Starbases are dropped. The real Falcon sites replace them.

After phase 1 the player chooses a branch. Phases 2, 3, and 4 can be played in any order. The Moon and Mars branch needs the catch from `1.1.0-catch`.

One design check stays open. The staging row, `0.21.0-suborbital`, must stay decided by the hardware. A staging failure names the short part. It is not a hidden chance. The mix is 3.6 kg of liquid oxygen for each kg of methane, and methane has its own tank. The kerosene tank waits for the Falcon story.

The game parallels came from Starbase Research. Buzz Aldrin's Race Into Space and the KSP TestFlight mod show tests that earn reliability part by part. KSP RP-1 splits research time from factory time. Anno 1800 opens a second site while the first keeps earning.

## UI and UX

`0.11.0-screen` shipped the layout pass on Land, the Inspector, and the rocket sheet. No fire, purse, or part rule moved. A staging failure now sits in `0.21.0-suborbital`, when a booster and a ship exist.

The notes below are not that row. Detail belongs to objects.

A main building is one thing you buy. Its parts are created with it. Each part is its own object, with its own place on that building and its own job. Zoomed out, you see the main. Zoomed in, you see the parts. A name shows for the part under the pointer, and for the one you selected. The buy column lists mains only. It does not list every part.

The first time parts exist in the game, they are stats on the building you already bought. Starfactory, Mega Bay, and Orbital Pad keep those names. A weak stat can fail on its own. Placeable parts, roads, and pipes stay the later rule below. A tank farm is still the tanks patch, not a new name for the pad.

The three mains:

- **Starfactory.** Hall, roof crane, stack stand.
- **Mega Bay.** Hall, one berth, service crane. A second bay, the high bay, and the Sanchez yard are later mains, not rooms inside this one.
- **Orbital pad.** As bought: mount, flame trench, deluge plate, deluge pumps, one water tank. Two upgrades, bought separately. The tank farm adds an oxygen tank, a kerosene tank, and a methane tank. The methane tank goes to work at `0.12.0-raptor`. The kerosene tank waits for the Falcon story. The Starship tower adds the tower, the chopsticks, and the ship arm. The tower goes up at `0.20.0-stack`, and the catch arrives at `1.1.0-catch`. The hop at `0.18.0-hop` lands on a nearby pad. Pad 2 is a later main and gets the same choices.

A quiet part can be selected. It does not change the fire until the version that needs it.

Massey's is its own site inland, later. Its parts are the ship cryo stand, the booster cryo stand, the static-fire stand, and the methane farm. Until it exists, the cryo proof from `0.13.0-proof` runs on the Orbital Pad. `6.2.0-stand` is the row that moves those tests inland.

The object rule and the part pictures are in `design-docs/site-objects-design.html`.

Leave the map free of a caption for every part. Leave the launch track off until a rocket actually flies.

The owned line shipped in `0.4.0-borderline`. It follows the coast, about 8 km inland on the solid beach, and it follows the bay where the water cuts in. Each building is a separate buy on a fixed plot, and the building is about one tenth of that plot. The Land column counts plots. The picture is `design-docs/0.4.0-borderline-design.html`.

## Motion, then pictures

`0.6.0-motion` plays the loop you already have, on the map. The static-fire modal closes. A build shows in the Starfactory. The finished rocket rolls from the Starfactory along the yard road to Mega Bay. It rolls from the bay to the Orbital Pad on that same road. At the pad it rises onto the mount. The static fire burns on the mount, and the flame stays on the map. Later versions add their own animations on top of the same system.

`0.8.0-flight` shipped the first launch. `0.9.0-economy` shipped the purse. `0.10.0-parts` shipped the Merlin, the fuel fitting, and the stage. `0.11.0-screen` shipped the screen layout. `0.12.0-raptor` shipped. `0.13.0-proof` shipped. `0.13.1-fixes` shipped. `0.14.1-teeth` is live. The next row is `0.14.2-seed`. Then come `0.15.0-sheet`, `0.16.0-bay`, `0.17.0-roll`, `0.18.0-hop`, `0.18.1-pipeline`, `0.19.0-high-hop`, and `0.19.1-split`. After those come `0.20.0-stack`, `0.21.0-suborbital`, and `0.22.0-orbit`. `0.23.0-tracking`, `0.24.0-picture`, and `0.25.0-motion-final` come after orbit, still in phase 0.

Phase 0 should take about 90 real minutes at 1x, from an empty yard to orbit. At 2x and 4x it is shorter. Each row should add about 10 minutes of play, not of waiting. Tiago locked that target on 2026-11-11. On 2026-11-12 he added `0.15.0-sheet`, `0.16.0-bay`, and `0.17.0-roll` before the hop, so those three rows sit inside the same target.

`0.23.0-tracking` lets you follow flights on the map. When you zoom out, each rocket shows its path and a box that grows and shrinks around it, with live numbers like altitude, speed and flight phase. Later, with many launches and some automation, you can watch them all fly at once.

`0.24.0-picture` replaces the plain halls. Starfactory, Mega Bay, and the Orbital Pad each get a picture you can read on the map. The seats stay. The buys stay. No new rule.

`0.25.0-motion-final` is a final pass on every animation once the buildings are drawn. Speeds, timing, and look all match. It covers the roll, the raise, the tests, the fire, refueling, the hops, flight, and landing.

The Starfactory builds one development article at a time. The bay holds it and refurbishes it. The bay does not stack sections yet. The tower stacks the ship on the booster at `0.20.0-stack`. The hop is `0.18.0-hop`. New builds are named Starhopper. Game serials are SH-1, SH-2, and so on. A loaded save keeps existing TA serials. One Raptor lifts, hovers, and lands on a nearby pad, like Starhopper at Boca Chica in 2019. A vehicle that survives can take the next selected height, while its remaining life, its propellant, and the required inspection allow it. The player picks 25 m, 50 m, or 150 m. The 25 m and 50 m targets are game choices, not historical flights. 150 m is the height Starhopper, SN5, and SN6 flew. The card shows the height, the methane, the oxygen, the thrust, and the floor. This row includes the vehicle shape and the flight-relevant mass. The steel price of 28 and the build of 8 to 12 days are the initial balance, and a later sitting can move them. The camera moves to the pad. A countdown runs from T-10 on the screen, with no sound. The flame grows with thrust. Landing reads the engine and the fuel lines. A short names the part. A scrub damages nothing. Every 30 days a program review pays for the clean tests on the pad record. That pay sits beside the seven goal pays. `6.1.0-rounds` rebalances them later. `0.18.1-pipeline` lets the factory build the next article during the test, and it puts the cadence count in the header. The bay slot is still the gate for the rocket that has to come home. `0.19.0-high-hop` stays the high hop only. It adds a flip and a landing, like the SN flights. `0.19.1-split` copies the compiled CSS into `index.html`. After that row the page loads nothing from a CDN. `geo-land.js` and `design-docs/countries.js` stay, because they are local files. A split into more files still needs approval. The catch is `1.1.0-catch`.

Today the fire passes or fails on thrust, the pad, the tanks, the wind, Structure, and the fuel lines. `0.12.0-raptor` changed the numbers. Raptor 1 is 1814 kN. Pad level 1 holds 2000 kN. The engine floor is 1500 kN. A fire loads 609 kg of methane and 2193 kg of liquid oxygen. The floors for Structure and the fuel lines stay 70 and 5 seconds. A skipped short lights and misses. The debrief names the part. Structure falls by 40. Short Fuel lines still light, and thrust ends early. A closed range or a short tank still scrubs. A scrub does not damage the rocket.

## Test campaign

A launch before the first contract spends the purse and pays nothing. That flight is the test. Fire the Orbital Pad until the card shows a run of clean results. Then fly.

The pad card already shows fires in the last 30 days, and days since the last fire. The cryo proof and the tanking run are live now, and each one joins that record. Each flight joins it later. The hop is `0.18.0-hop`. The header cadence number waits for `0.18.1-pipeline`. That number reads the same fire count.

Reliability is that record. It is not a meter you buy. A cryo proof shows the tanks hold. A tanking run shows the fuel lines hold. A clean static fire proves the mount and the engine. A flight proves the vehicle. A fail names the part. If every test logs the same line, the tests teach nothing.

`0.14.0-defects` shipped. A prototype can leave the Starfactory with one short part. The short is a real number: Structure 60, Fuel lines 0 seconds, or thrust 1400 kN. Those are game numbers. The cryo proof finds Structure. The tanking run finds the fuel lines. The static fire finds a short engine. The live fire also reads Structure and the fuel lines. You can skip a test, and the part stays as it is until a pad check. Through phase 0, bay jobs keep their current steel and time costs: the engine takes 24 steel and 2 days, or 1 day at pad level 2, the fuel lines take 1 day and no steel, and Structure takes 4 to 5 days and no steel, the button shows that span before the press, there is no extra money price, no new currency, and no fail roll, and the one-time refurb goal pay of 40 stays. `1.2.0-refurb` runs the same check on a flown stage. `1.3.0-rate` lets a better process send fewer defects out of the factory.

`0.14.2-seed` is the next row. It stores one seed in the save. Defect order and the weather table come from the seed. The player still sees every number. Restart rolls a new seed. A test start keeps a fixed seed. The same row adds speed 1x, 2x, and 4x, and a skip to the next named event. Waiting is the drag in the current build, so speed ships in this row. The design page for the row that just shipped is `design-docs/0.14.1-teeth-design.html`.

`0.15.0-sheet` shows that weak part in the rocket window. The window names the part, the number the rocket has, and the number the test needed. The fix in Mega Bay is easy to see. This row adds no new test.

`0.16.0-bay` lets you check a part while the rocket is in Mega Bay. That check reads the part, then the fix can start. The cryo proof, the tanking run, and the static fire stay on the pad. `6.2.0-stand` still moves those pad checks inland later.

`0.17.0-roll` lets a new rocket leave with a weak number you can see. It is not always Structure 60, fuel lines at 0 seconds, or thrust at 1400 kN. Those three stay the examples from `0.14.0-defects`. The exact range is decided in that row's design. It is not a hidden coin flip. `0.14.2-seed` still only chooses which part comes first. `1.3.0-rate` still only sends fewer weak parts out of the factory.

The first paying contract arrives at `0.21.0-suborbital`. It reads the test and flight record before it offers the sale. The sale names how many flights and how many clean results it wants. Pay arrives when a flight meets the sale. `0.22.0-orbit` lets a contract ask for an orbit card.

Staging can fail at `0.21.0-suborbital`. The booster and the ship separate in flight. If the part that does that is short, the debrief names it.

`1.0.0-recovery` is the first way to spend less. A stage that comes home loses life on a hard flight. A customer who asks you to bring the stage home waits for `7.0.0-ladder`.

A flight load is a large spend. Until the contract, the day adds no money. Investors pay when a goal is finished. A run of unpaid flights can stall the yard. `0.18.0-hop` adds a program review every 30 days. It pays for the clean tests in that window. The seven goal pays stay. `6.1.0-rounds` pays once for the first hop, the first orbit, and the first catch. It rebalances the goals, the reviews, and those one-time payments. When the contract is planned, that first paid flight should cover the next vehicle.

The minimal save shipped in `0.14.1-teeth`. Autosave runs at the end of each day. A reload continues that yard. Restart still wipes it. `8.4.0-saves` keeps slots, the flight history, and a harder or easier start.

Later rows on `design-docs/program-roadmap-design.html` add rules on that same coast line. `6.0.0-yard` adds pad buffer, the first houses, and the highway closure. `6.2.0-stand` is an inland test stand on a parcel of about 930 acres. `6.3.0-farm` lets tank-pad acres set propellant and deluge capacity. `6.4.0-mitigation` is wetland you cannot build on, required before a second Orbital Pad. `6.5.0-town` adds a clinic and a school after the beds exist. None of those rules ship with the line.

## Sound

The live game is quiet. The mute button and the Web Audio tones are out of `index.html`. They come back at `8.3.0-sound` on `design-docs/program-roadmap-design.html`: a build, a countdown, a fire, a landing, and a mute that stays in the browser. Sound stays on this row. The countdown in `0.18.0-hop` is visual only. It does not pull a tone forward.
