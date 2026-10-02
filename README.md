# starbase-builder

This game follows the SpaceX story. You learn how the rockets, the tanks, and the pads work by running them. The detail stays close to real hardware. The first chapter is small on purpose. You finish Falcon 1 in Texas before any later rocket arrives.

Open `index.html` in a browser. There is no build step.

**Live release:** `0.2.1-field`. The map is the Texas coast. You buy the Build site and the Pad site. Owned ground is a copper line around those parcels. Falcon 1 is the only rocket you can build. A static fire holds when the Merlin’s thrust, the pad, the propellant, and the day’s wind all clear. The sky repeats from the day number, so you can wait for a calm day. Specific impulse and mass are on the engine card and do not decide this test yet. Propellant is still one stock. The guide below is the rest of the story. The build map is `design-docs/program-roadmap-design.html`.

## Falcon 1 in Texas

Falcon 1 is a small orbital rocket with one Merlin engine on the first stage. That engine burns two fluids. RP-1 is refined kerosene. Liquid oxygen is the oxidizer. The engine needs both. A tank of one fluid cannot stand in for the other.

You buy each fluid at a price the panel shows before you pay. Each fluid sits in its own tank. You can build a larger tank when the small one runs dry. A static fire and a flight each draw a printed amount of RP-1 and a printed amount of liquid oxygen. If either tank is short, the rocket stays on the ground.

The Starfactory builds the rocket from steel and holds the finished article until the Mega Bay takes it. The bay houses the fleet and does the refurb after a firing. The pad is where the rocket lights. The pad is not a hangar. After the fire, the rocket goes back to the bay.

The engine lab shows thrust, specific impulse, mass, and how many times the Merlin can restart. Specific impulse is how much push you get from each kilogram of propellant. A purchase moves one of those numbers. The structure lab shows the dry mass of the stage and how much load it can take. The panel adds the engine and the structure and shows the payload this rocket can lift.

A firing follows those numbers. The result names the short part when something is short. That part can be the engine, the structure, the pad, or a tank. Wear climbs by a known amount and falls when the bay finishes the refurb. The screen counts fires in the last 30 days.

A hop is the same rocket leaving the stand. Altitude and speed come from the thrust, the mass, and the propellant you loaded. An orbit attempt adds the upper stage burn. A success leaves an orbit card with altitude, inclination, and the mass on board. One small commercial contract pays when that card matches the orbit you sold. You can throw the core away and lift more, or land it and spend days in the bay putting it back together.

Falcon 9, Falcon Heavy, and Starship stay locked until this chapter is fun to play through.

## What comes later

Each of these is a patch. It is not in the finished Falcon 1 game.

**Falcon 9.** Nine Merlins on one core. It drinks more RP-1 and more liquid oxygen. It needs a pad you have already strengthened. Hop, orbit, and contracts use the same path as Falcon 1.

**A second pad, then Falcon Heavy.** The second pad is the same kind of pad on a second footprint in Texas. Falcon Heavy is three Falcon cores stacked as one article. It needs the stronger pad, more of both fluids, and a longer wait before that pad can take the next rocket.

**Customers.** NASA cargo to the station, crew, flights for other countries, and military payloads each open after you have already flown that class of mission. A card names the orbit, the mass, the pad days, and the pay.

**Starlink.** You may keep a launch for your own satellites. Each bird has mass, power, radio, and a design life. Building them uses the same steel, tanks, and pads as a customer flight.

**Starship.** Raptor burns methalox. That is liquid methane plus the liquid oxygen you already store. This patch adds a methane tank and a methane price. It also adds the tower, the catch, and a depot in orbit. A Moon landing and a Mars window are contracts that draw propellant from that depot.

**Louisiana.** A second Starbase, empty at first, with the same buildings and the same fluids. Texas can send a rocket there. The trip takes a counted number of days. This is a site upgrade. It is not required to finish Falcon 1.

**xAI.** When Starlink is up and the pads are busy, a data center can compete with the rockets for steel and power. The panel shows the power used and whether a new cluster delayed a booster.

## Where the rest of the notes live

`VERSION` is the live label. `AGENTS.md` is how we write and how we ship. `FUTURE_FEATURES.md` is open work. `IMPLEMENTATION_LOG.md` is what already shipped. The version map is `design-docs/program-roadmap-design.html`. The lessons are `design-docs/learning-guide.html`.
