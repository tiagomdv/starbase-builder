# Future features — starbase-builder

The ordered draft is the version table in `design-docs/program-roadmap-design.html`. That page is the source of truth. This file holds the detail behind its rows.

Phase 0 is Starship development at Starbase in Texas, up to orbit. Phase 1 is recovery and the catch. Phases 2, 3, and 4 are a branch the player chooses: Starlink, the Moon and Mars, or the Falcon story at the real Falcon sites. Phases 5 through 9 are compute, the yard, longer flights, picture and record, and the fleet desk. A new idea is a new row at the bottom of that table.

When a row ships or is dropped, remove it from the table and note the ship in `IMPLEMENTATION_LOG.md`.

**Last shipped:** `0.20.0-tank`. The hall you already bought is Mid Bay. A hopper hops 25 m, then 50 m and 150 m. A soft 150 m landing opens the tank rocket, and that rocket hops 150 m only. See `IMPLEMENTATION_LOG.md`. The next play row is `0.21.0-nose`.

## Roadmap restructure (2026-11-09)

Tiago approved a new order on 2026-11-09. The goal is to set the story straight. Starbase in Texas is the real Starship site. Falcon never started there. So phase 0 is now Starship development at Starbase, up to orbit. The Falcon story moves to its real sites, as a branch after phase 1.

The shipped slices, `0.1.0-foundation` through `0.11.0-screen`, were built on a Falcon 1 stand-in on the Texas site. The yard, the map, Land, the Inspector, the purse, the tanks, the motion, and the part sheet all carry over. From `0.12.0-raptor` the vehicle becomes a Starship development article.

The real test chain after a vehicle is built is tank proof, tanking, static fire, data review, then the range. Tanking means the crew fills the tanks and drains them again. `0.13.0-proof` shipped that order. `0.16.0-bay` is live, and the pad still runs it. A new article can leave with a real short part. Falcon 1 ran a thinner chain. It went more often from build to a pad static fire to flight, and a flight carried more risk. `4.0.0-falcon1` keeps that.

The real Falcon order comes from SpaceX Brief. The rockets were built in California, at El Segundo and then Hawthorne. Falcon 1 flew from Omelek Island in the Kwajalein Atoll, from 2006 to 2009. It made orbit on 28 September 2008. Falcon 9 started at Cape Canaveral SLC-40, with its first flight in June 2010. Vandenberg SLC-4E came next. SpaceX leased LC-39A in 2014 and first launched from there in February 2017. Falcon Heavy and crew flights fly from 39A.

The invented Louisiana and Florida Starbases are dropped. The real Falcon sites replace them.

After phase 1 the player chooses a branch. Phases 2, 3, and 4 can be played in any order. The Moon and Mars branch needs the catch from `1.1.0-catch`.

One design check stays open. The staging row, `0.24.0-suborbital`, must stay decided by the hardware. A staging failure names the short part. It is not a hidden chance. The mix is 3.6 kg of liquid oxygen for each kg of methane, and methane has its own tank. The kerosene tank waits for the Falcon story.

The game parallels came from Starbase Research. Buzz Aldrin's Race Into Space and the KSP TestFlight mod show tests that earn reliability part by part. KSP RP-1 splits research time from factory time. Anno 1800 opens a second site while the first keeps earning.

## UI and UX

`0.11.0-screen` shipped the layout pass on Land, the Inspector, and the rocket sheet. No fire, purse, or part rule moved. A staging failure now sits in `0.24.0-suborbital`, when a booster and a ship exist.

The notes below are not that row. Detail belongs to objects.

A main building is one thing you buy. Its parts are created with it. Each part is its own object, with its own place on that building and its own job. Zoomed out, you see the main. Zoomed in, you see the parts. A name shows for the part under the pointer, and for the one you selected. The buy column lists mains only. It does not list every part.

The first time parts exist in the game, they are stats on the building you already bought. Starfactory, Mid Bay, and Orbital Pad keep those names. High Bay and Mega Bay are later buys. A weak stat can fail on its own. Placeable parts, roads, and pipes stay the later rule below. A tank farm is still the tanks patch, not a new name for the pad.

The three mains:

- **Starfactory.** Hall, roof crane, stack stand.
- **Mid Bay.** Hall, one berth, service crane. The High Bay, Mega Bay, and the Sanchez yard are later mains, not rooms inside this one.
- **Orbital pad.** As bought: mount, flame trench, deluge plate, deluge pumps, one water tank. Two upgrades, bought separately. The tank farm adds an oxygen tank, a kerosene tank, and a methane tank. The methane tank goes to work at `0.12.0-raptor`. The kerosene tank waits for the Falcon story. The Starship tower adds the tower, the chopsticks, and the ship arm. The tower goes up at `0.23.0-stack`, and the catch arrives at `1.1.0-catch`. The hop at `0.18.0-hop` lands on a nearby pad. Pad 2 is a later main and gets the same choices.

A quiet part can be selected. It does not change the fire until the version that needs it.

Massey's is its own site inland, later. Its parts are the ship cryo stand, the booster cryo stand, the static-fire stand, and the methane farm. Until it exists, the cryo proof from `0.13.0-proof` runs on the Orbital Pad. `6.2.0-stand` is the row that moves those tests inland.

The object rule and the part pictures are in `design-docs/site-objects-design.html`.

Leave the map free of a caption for every part. Leave the launch track off until a rocket actually flies.

The owned line shipped in `0.4.0-borderline`. It follows the coast, about 8 km inland on the solid beach, and it follows the bay where the water cuts in. Each building is a separate buy on a fixed plot, and the building is about one tenth of that plot. The Land column counts plots. The picture is `design-docs/0.4.0-borderline-design.html`.

One backlog item stays open. Cancel placing, `#btn-x`, and Skip the fire watch, `#event-skip`, were dead before `0.17.0-tidy`, and no player can reach them. A later row removes them, or brings them back with a path that shows them.

## Motion, then pictures

`0.6.0-motion` plays the loop you already have, on the map. The static-fire modal closes. A build shows in the Starfactory. The finished rocket rolls from the Starfactory along the yard road to Mega Bay. It rolls from the bay to the Orbital Pad on that same road. At the pad it rises onto the mount. The static fire burns on the mount, and the flame stays on the map. Later versions add their own animations on top of the same system.

`0.8.0-flight` shipped the first launch. `0.9.0-economy` shipped the purse. `0.10.0-parts` shipped the Merlin, the fuel fitting, and the stage. `0.11.0-screen` shipped the screen layout. `0.12.0-raptor` shipped. `0.13.0-proof` shipped. `0.13.1-fixes` shipped. `0.16.0-bay` shipped. `0.17.0-tidy` shipped. `0.20.0-tank` is live. The next play row is `0.21.0-nose`, then `0.22.0-stages`. After those come `0.23.0-stack`, `0.24.0-suborbital`, and `0.25.0-orbit`. `0.26.0-tracking`, `0.27.0-picture`, and `0.28.0-motion-final` come after orbit, still in phase 0.

Phase 0 should take about 90 real minutes at 1x, from an empty yard to orbit. At 3x it is shorter. Each row should add about 10 minutes of play, not of waiting. Tiago locked that target on 2026-11-11. On 2026-11-12 he added `0.15.0-sheet`, `0.16.0-bay`, and `0.17.0-roll` before the hop. On 2026-11-17 he merged `0.17.0-roll` into `0.16.0-bay` and left the hop at `0.18.0-hop`. On 2026-11-18 he added `0.17.0-tidy` before the hop. Those rows sit inside the same target. On 2026-11-27 he added `0.20.0-tank`, `0.21.0-nose`, and `0.22.0-stages` before the tower. The 90 minute target grows by those three rows.

`0.26.0-tracking` lets you follow flights on the map. When you zoom out, each rocket shows its path and a box that grows and shrinks around it, with live numbers like altitude, speed and flight phase. Later, with many launches and some automation, you can watch them all fly at once.

`0.27.0-picture` replaces the plain halls. Starfactory, the Mid Bay, and the Orbital Pad each get a picture you can read on the map. The High Bay and Mega Bay get one when those buys exist. The seats stay. The buys stay. No new rule.

`0.28.0-motion-final` is a final pass on every animation once the buildings are drawn. Speeds, timing, and look all match. It covers the roll, the raise, the tests, the fire, refueling, the hops, flight, and landing.

The Starfactory hold stays one finished article. From this row the next build starts once that article has left the hold. The bay holds the article and refurbishes it. The bay does not stack sections yet. The tower stacks the ship on the booster at `0.23.0-stack`. The hop is `0.18.0-hop`. From `0.17.0-tidy` a stored build kept the name Starhopper and a number: Starhopper 1, Starhopper 2, and so on. There is no short serial. SH stays free for Super Heavy at `0.22.0-stages`. A new build is named SN. A stored Starhopper keeps its name. One Raptor lifts, hovers, and lands on a nearby pad, like Starhopper at Boca Chica in 2019. A vehicle that survives can take the next selected height, while its remaining life, its propellant, and the required inspection allow it. A stored Starhopper keeps the three low hops, 25 m, 50 m, and 150 m. An SN also hops 10 km. The 25 m and 50 m targets are game choices, not historical flights. 150 m is the height Starhopper, SN5, and SN6 flew. The pad shows the height. The parts table shows the methane, the oxygen, the thrust, and the floor. This row includes the vehicle shape and the flight-relevant mass. The steel price of 28 and the build of 8 to 12 days are the initial balance, and a later sitting can move them. The camera moves to the pad. A countdown runs from T-10 on the screen, with no sound. The flame grows with thrust. Landing reads the engine and the fuel lines. A short names the part. A scrub damages nothing. Every 30 days a program review pays 12 money for each clean test on the pad record. A clean test is a cryo proof that held, a tanking run that held, a static fire that held, or a hop that landed soft. That pay sits beside the seven goal pays. The first soft landing also pays a goal, Land a hop, once, for 60 money. `6.1.0-rounds` rebalances them later. Initial balance is a dry mass of 102000 kg and burns of 8, 14, and 22 seconds. The loads and the floors are on the design page. `0.17.0-tidy` sets the Starhopper name and the parts table. This row uses them. The design page is `design-docs/0.18.0-hop-design.html`. `0.19.0-high-hop` is the high hop and the old pipeline row together. A new build is named SN 1, SN 2, and so on. It adds a 10 km hop: climb, belly, flip, and landing burn. The factory may start the next article once the first has left the hold. The header shows the same fire count the pad already has. The design page is `design-docs/0.19.0-high-hop-design.html`. `0.20.0-tank` takes the 10 km hop off the pad until `0.21.0-nose`. The catch is `1.1.0-catch`.

On 2026-11-27 Tiago asked the hops to leave a reading you keep. A clean hop moves the factory card. The rocket sheet stays on the rocket that flew. The next height stays off until the reading from the hop before it is there. The rocket that flew stays as it is. A bay fix repairs that rocket only. The factory moves only after a clean hop. Each landing closes half the gap to that hop's cap, so the same hop helps less every time. A 25 m landing moves thrust toward 1600 kN. A 50 m landing moves fuel lines toward 20 seconds. A 150 m landing moves thrust toward 1814 kN, fuel lines toward 40 seconds, and the Structure floor toward 60. These caps are game numbers. A new shape starts again at 1400 kN, 0 seconds, and a Structure floor of 20. A miss does not move the numbers. A 25 m landing writes that the engine landed, and that is what lets you try 50 m and 150 m. A 150 m hopper landing opens the tank SN at `0.20.0-tank`. A 150 m tank landing opens the nose article at `0.21.0-nose`. A 10 km landing opens the booster and the ship at `0.22.0-stages`. Pass a booster and Pass a ship both write a reading, and `0.23.0-stack` waits until both are there. The 50 m hop stays off until the 25 m reading is there. It does not open a vehicle. A line can say In real life. That is what SpaceX flew. Your serial is the rocket you built. `0.24.0-suborbital` flies the stack. `0.25.0-orbit` closes the phase 0 rules. `0.20.0-tank` shipped. The hall is Mid Bay. The hopper and the tank rocket both use it. The structure check stays a window, about 30 wide and then about 10 wide, and the cryo proof writes the real number. Cryo, tanking, and the static fire still come before a hop. A bigger hall is a buy. The hopper and the tank SN fit the Mid Bay. `0.21.0-nose` lets you buy the High Bay, and the nose article will not start without it. The ship fits the High Bay. `0.22.0-stages` lets you buy Mega Bay, and the booster will not start without it. `1.4.0-halls` is another buy. A finished goal does not place the hall.

Today the fire passes or fails on thrust, the pad, the tanks, the wind, Structure, and the fuel lines. `0.12.0-raptor` changed the numbers. Raptor 1 is 1814 kN. Pad level 1 holds 2000 kN. The engine floor is 1500 kN. A fire loads 609 kg of methane and 2193 kg of liquid oxygen. The floors for Structure and the fuel lines stay 70 and 5 seconds. A skipped short lights and misses. The debrief names the part. A lit miss takes up to 40 off Structure and leaves it at 20 at worst. Short Fuel lines still light, and thrust ends early. A closed range or a short tank still scrubs. A scrub does not damage the rocket.

## Test campaign

A launch before the first contract spends the purse and pays nothing. That flight is the test. Fire the Orbital Pad until the card shows a run of clean results. Then fly.

The pad card already shows fires in the last 30 days, and days since the last fire. A static fire that lights joins that record. The hidden launch joins it. A cryo proof, a tanking run, a hop, and a scrub stay off it. The header Fires number reads that same count. The hop is `0.18.0-hop`. The 10 km hop is `0.19.0-high-hop`.

Reliability is that record. It is not a meter you buy. A cryo proof shows the tanks hold. A tanking run shows the fuel lines hold. A clean static fire proves the mount and the engine. A flight proves the vehicle. A fail names the part. If every test logs the same line, the tests teach nothing.

`0.14.0-defects` shipped. A prototype can leave the Starfactory with one short part. The short is a real number: Structure 60, Fuel lines 0 seconds, or thrust 1400 kN. Those are game numbers. Structure 60 is the cliff for a null seed. From `0.16.0-bay`, Structure is a number you measure. That paragraph is below. The cryo proof finds Structure. The tanking run finds the fuel lines. The static fire finds a short engine. The live fire also reads Structure and the fuel lines. You can skip a test, and the part stays as it is until a pad check. Through phase 0, bay jobs keep their current steel and time costs: the engine takes 24 steel and 2 days, or 1 day at pad level 2, the fuel lines take 1 day and no steel, and Structure takes 4 to 5 days and no steel, the button shows that span before the press, there is no extra money price, no new currency, and no fail roll, and the one-time refurb goal pay of 40 stays. `1.2.0-refurb` runs the same check on a flown stage. `1.3.0-rate` keeps factory speed and the process upgrade. It may add to the Structure floor from `0.16.0-bay`.

`0.14.2-seed` shipped. One seed in the save picks the defect order and the 10-day sky. A null seed keeps the old order and the old sky. Restart rolls a new seed. A test start uses seed 11. The header has 1x, 2x, 4x, and Skip. The design page is `design-docs/0.14.2-seed-design.html`. `0.17.0-tidy` replaces the moving-day rule. From that row the day holds while a fill, a fire, or a flight runs.

`0.15.0-sheet` shipped. The rocket window names the short part. It shows the number the rocket has and the number the test needed. In Mega Bay the fix button is on that row. On the pad the window does not start the job. This row adds no new test. The design page is `design-docs/0.15.0-sheet-design.html`.

`0.16.0-bay` shipped. It lets you check Structure while the rocket is in Mega Bay. Structure is a fixed number you have to measure. The real number is rolled at build end from the seed, salted by article count and part, and stored on the vehicle. A check costs one bay day and no money. The first reading is about 30 wide. The second is about 10 wide. Only the pad test writes the exact number. Hidden Structure rolls between the scrap floor and 100. Each found and fixed Structure fault raises that part's build floor by 8. It rises once per article, and only when the number stored at build was under 70. `0.20.0-tank` stops that floor step. A bay fix repairs that rocket only. Fuel lines and thrust keep today's fixed shorts. A lit miss takes up to 40 off Structure and leaves it at 20 at worst. Check Structure switches off once the pad has measured the number. The design page is `design-docs/0.16.0-bay-design.html`. `6.2.0-stand` still moves the pad checks inland later. `0.17.0-roll` is merged into this row. Do not revive it.

`0.17.0-tidy` shipped. Tiago added it on 2026-11-18 and decided its open questions the same day. It tidies the Inspector, the Land plot cards, and the rocket window. Numbers drop to 14 and 16 px. The page uses at most four sizes outside the locked top bar, and most uppercase labels go. The rocket window becomes one parts table with small buttons and a Has against Needs margin bar, and it fits at 1280 by 800 without a scroll. Long sentences move to the wiki. Every action and every number stays on screen or one click away. Four rule changes ride in this row and nothing else. The road and the lift are measured in game days. A road takes half a day to 1 day, and each lift takes half a day, at every speed and in `?test`. Skip during a road finishes the road and any running lift, then jumps. The day holds while a fill, a fire, or a flight runs. `0.17.0-tidy` replaces the moving-day rule that `0.14.2-seed` kept. The speeds are 1x and 3x, and an old 2x or 4x save loads at 3x. Every build is named Starhopper and a number: Starhopper 1, Starhopper 2, and so on. There is no short serial, so SH stays free for Super Heavy at `0.22.0-stages`. An old TA-1 loads as Starhopper 1. The save stays version 1. The design page is `design-docs/0.17.0-tidy-design.html`.

The first paying contract arrives at `0.24.0-suborbital`. It reads the test and flight record before it offers the sale. The sale names how many flights and how many clean results it wants. Pay arrives when a flight meets the sale. `0.25.0-orbit` lets a contract ask for an orbit card.

Staging can fail at `0.24.0-suborbital`. The booster and the ship separate in flight. If the part that does that is short, the debrief names it.

`1.0.0-recovery` is the first way to spend less. A stage that comes home loses life on a hard flight. A customer who asks you to bring the stage home waits for `7.0.0-ladder`.

A flight load is a large spend. Until the contract, the day adds no money. Investors pay when a goal is finished. A run of unpaid flights can stall the yard. `0.18.0-hop` adds a program review every 30 days. It pays 12 money for each clean test in that window. A clean test is a cryo proof that held, a tanking run that held, a static fire that held, or a hop that landed soft. The seven goal pays stay. The first soft landing pays the goal Land a hop once, for 60 money. `6.1.0-rounds` pays once for the first hop, the first orbit, and the first catch. It rebalances the goals, the reviews, and those one-time payments. When the contract is planned, that first paid flight should cover the next vehicle.

The minimal save shipped in `0.14.1-teeth`. Autosave runs at the end of each day. A reload continues that yard. Restart still wipes it. `8.4.0-saves` keeps slots, the flight history, and a harder or easier start.

Later rows on `design-docs/program-roadmap-design.html` add rules on that same coast line. `6.0.0-yard` adds pad buffer, the first houses, and the highway closure. `6.2.0-stand` is an inland test stand on a parcel of about 930 acres. `6.3.0-farm` lets tank-pad acres set propellant and deluge capacity. `6.4.0-mitigation` is wetland you cannot build on, required before a second Orbital Pad. `6.5.0-town` adds a clinic and a school after the beds exist. None of those rules ship with the line.

## Sound

The live game is quiet. The mute button and the Web Audio tones are out of `index.html`. They come back at `8.3.0-sound` on `design-docs/program-roadmap-design.html`: a build, a countdown, a fire, a landing, and a mute that stays in the browser. Sound stays on this row. The countdown in `0.18.0-hop` is visual only. It does not pull a tone forward.
