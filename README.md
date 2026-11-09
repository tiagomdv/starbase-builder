# starbase-builder

This game follows the SpaceX story. You learn how the rockets, the tanks, and the pads work by running them. The detail stays close to real hardware. The first chapter is small on purpose. You develop Starship at Starbase in Texas and fly it to orbit before anything else opens. Starbase is where Starship was really developed. After that you choose a branch: Starlink, the Moon and Mars, or the Falcon story at the real Falcon sites.

Open `index.html` in a browser. There is no build step. Open `index.html?test` for the same start with a day of half a second. That start is not saved.

**Live release:** `0.11.0-screen`. The next row is `0.12.0-raptor`. Today's rocket is a Falcon 1 stand-in. From `0.12.0-raptor` it becomes a Starship development article.

Owned ground is one red dashed line. The water side follows the coast. The back side sits about 8 km inland on the solid beach, and it follows the bay where the water cuts in. The word on that line is limit.

Starfactory, Mega Bay, and the Orbital Pad are separate buys. Each one sits on its own plot. The building is about one tenth of that plot. The Land column counts the plots. Buy 10 and Buy 50 sit above those plots. Each one costs 1 money per steel. Buy 50 is off when money is under 50.

The header is the range console. A lamp reads Range open or Range closed. The wind sits under that line. Money, steel, RP-1, liquid oxygen, fleet, and day are numerals in the center. The version label sits under those counts.

Pause sits beside the day count. The line above the count reads Paused. Pause stops the day clock, and a static fire or a flight stops with it. Builds, refurbs, and upgrades wait while paused. Days keep moving while a rocket loads propellant, burns, or flies. The day adds no money, no steel, and no fluid. Investors pay when a goal is finished. A roll, a raise, and a lower leave the day running. More than one rocket can roll at the same time, and the factory can build during that roll, a fire, or a flight. The pad still holds one. Weather only gates a launch at liftoff. A closed range during a flight that already left does not stop the climb.

Goals, Wiki, and Fleet have an outline. Wiki opens over the game. The articles read the live settings. A note says In real life when the game and the Falcon 1 sources differ.

The game has no sound until `8.3.0-sound`. Falcon 1 is the only rocket you can build. A static fire holds when the Merlin thrust, the pad, the RP-1, the liquid oxygen, and the wind all clear. The sky repeats from the day number, so you can wait for a calm day.

Specific impulse and engine mass are on the rocket sheet. They do not decide this test yet. The same sheet shows stage dry mass, liftoff mass, and a one-stage payload. A fresh Merlin is a Merlin 1A at 318 kN. Raise Merlin thrust fits a Merlin 1C at 343 kN. That sum is not a flown orbit. Lighten the stage still cuts dry mass on that rocket. The rocket sheet is one drawing. The tank, the fuel fitting, and the engine each carry that part's percent, and the big number is the lowest part. The line under the name matches that number. Thrust stays at the fresh figure.

A build takes 8 to 12 days. A clean fire stays on the mount for 1 day of inspection. Then the rocket can fly. RP-1 and liquid oxygen sit in separate tanks. One press fills a tank for 6 money. A short tank stops the fire and the launch. The launch farm raises the tanks to a flight load.

The guide below is the rest of the story. The build map is `design-docs/program-roadmap-design.html`.

## Today's rocket: a Falcon 1 stand-in

Falcon 1 is a small orbital rocket with one Merlin engine on the first stage. That engine burns two fluids. RP-1 is refined kerosene. Liquid oxygen is the oxidizer. The engine needs both. A tank of one fluid cannot stand in for the other.

Each fluid sits in its own tank on the Orbital Pad card. One press fills that tank. The launch farm buys raise those tanks to a flight load. They still cost steel. A static fire loads a printed amount of RP-1 and a printed amount of liquid oxygen. A launch loads the full first-stage load. If either tank is short, the rocket stays on the ground.

The Starfactory builds the rocket from steel and holds the finished article until the Mega Bay takes it. The bay houses the fleet. You refurb one part from the rocket sheet. The Merlin costs 24 steel and takes 2 days. Pad level 2 cuts that job by 1 day. Inspect the fuel fitting takes 1 day and no steel. Refurb the stage takes 4 or 5 days and no steel. Return to Mega Bay parks the rocket. The pad is where the rocket lights and flies. After a clean fire, the rocket stays on the mount for inspection. Then it can launch. The first stage is lost at sea.

The engine lab shows thrust, specific impulse, engine mass, and how many times the Merlin can restart. Specific impulse is how much push you get from each kilogram of propellant. A purchase moves one of those numbers. The structure lab shows stage dry mass and liftoff mass. Payload capacity is what those numbers leave for a named orbit. It is not the sum of the masses.

A firing follows those numbers. The log names the short part. That part can be the Merlin, the fuel fitting, the stage, the pad, or a tank. The Merlin shows the seconds it has left. A lit static fire spends 5. A static fire does not spend the fuel fitting. The screen counts fires and launches in the last 30 days.

The yard, the map, Land, the Inspector, the purse, the tanks, the motion, and the part sheet all carry over to Starship. Merlin becomes Raptor. RP-1 becomes methane. The oxygen tanks stay.

## What comes later

The build map is `design-docs/program-roadmap-design.html`. It was restructured on 2026-11-09.

**Phase 0, Starship to orbit.** Raptor and methane replace Merlin and RP-1. A cryo proof and a tanking run come before the static fire. A prototype can leave the factory with a defect that the tests find. Then a hop, a high hop with a flip and a landing, a booster and a ship stacked at the tower, and a suborbital flight test where staging can fail. The first paying contract arrives with that test. Orbit closes the chapter.

**Recovery and catch.** Bring the booster home, catch it with the tower, check it for defects, and refurbish it. Then the factory builds faster.

**Choose a branch.** After that you pick where to go next, in any order.

**Starlink.** You may keep a launch for your own satellites. Each bird has mass, power, radio, and a design life. Building them uses the same steel, tanks, and pads as a customer flight.

**The Moon and Mars.** A depot in orbit holds propellant. A Moon site comes first, then a Mars site. Texas still builds the rockets.

**The Falcon story.** It starts where SpaceX really started. The rockets are built in California. Falcon 1 flies from Kwajalein. Falcon 9 opens at Cape Canaveral SLC-40, then Vandenberg, then 39A, with Falcon Heavy and crew. RP-1 comes back here.

**xAI.** When the pads are busy, a data center can compete with the rockets for steel and power. The panel shows the power used and whether a new cluster delayed a booster.

## Where the rest of the notes live

`VERSION` is the live label. `AGENTS.md` is how we write and how we ship. `FUTURE_FEATURES.md` is open work. `IMPLEMENTATION_LOG.md` is what already shipped. The version map is `design-docs/program-roadmap-design.html`. The lessons are `design-docs/learning-guide.html`.
