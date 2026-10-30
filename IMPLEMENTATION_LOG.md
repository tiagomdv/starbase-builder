# Implementation Log — starbase-builder

History of what **shipped**, keyed by **version**.  
**Rule: one log section per `VERSION` label.** While a version is in progress, **edit that section** (do not add a new dated header). When a new version ships, **append one new section**.

---

## `0.0.1-bootstrap` — 2026-08-06

**Version:** `0.0.1-bootstrap` · docs only

- Project skeleton and long-term vision locked.
- Thematic arc: Foundations → Flight → Scale → Power → Cis-lunar → Mars.
- Core principles: start super simple and accumulate; sites accumulate; Earth Starbase stays critical; outer bases depend on Earth cadence/production.
- Visual direction: earthy AoE-style (grass, dirt, warm stone), simple shapes first, 2.5D later; Grok Imagine pipeline as future capability.
- Process: hybrid AI implement / human ships (same lab style as personal-expense-app).
- Later in this version (still docs-only): local clone; harvest of mechanisms from `~/starship-dev` into `FUTURE_FEATURES.md` (fail-forward debrief, infra/caps, recovery modes, mission ladder, etc.); map-first non-goals documented.
- No game code. Layout mock: `design-docs/0.0.1-layout-aoe-3d.html`.

---

## `0.1.0-foundation` — 2026-08-07

**Version:** `0.1.0-foundation` · first playable

### Product
- **Vision (locked in README / AGENTS / FUTURE_FEATURES):** simple, **quick-to-finish**, **realistic and fun** — showcase and enjoy this industry’s **processes and dynamics**, not a sprawling empire sim.
- Compact, finishable loop; realism of mechanics / processes / visual cues over content volume.
- **Visual Upgrade Rule:** upgrades change silhouette/footprint/secondary geometry (Pad L1→L2 trench + OLM).
- Design: `design-docs/0.1.0-foundation-design.html` (HTML only for design-docs).
- Design docs rule locked in `AGENTS.md`.

### Site (final foundation cut)
- **Three placeables:** Starfactory · Mega Bay · Orbital Pad (tank farm **out** of foundation).
- **Steel + propellant** from the **environment** (daily supply), not a factory steel mill or tank farm.
- Starfactory **builds rockets** (Falcon 1 / Falcon 9); hold one finished article until staged.
- Mega Bay **houses** up to **4** vehicles (visual slots + capacity pips) and runs **post-fire refurb**.
- Pad is for **static fire only** — not a hangar; return to bay after fire.

### Vehicles & ops
- SpaceX roadmap live: **Falcon 1**, **Falcon 9**; stubs: Heavy, Starship.
- Distance-based **rollout** bay↔pad (farther = longer); dashed path + transporter cue.
- **Static fire** close-up per class (1 vs 9 engines); P(success) from class × condition × pad level.
- **Failure** anomaly/RUD animation + SFX; scrap chance or heavy bay refurb.
- **Success** → wear + return to bay for light refurb days.
- Fleet list UI; multi-vehicle bay; Web Audio + mute.

### Process note
- Interim WIP labels (`0.1.0-wip`) and multi-entry logs during development were collapsed into this single version section (rule: one log per version).

---

## `0.2.0-merlin` — 2026-10-01

**Version:** `0.2.0-merlin`

- Falcon 1 is the only rocket you can build. Falcon 9 is locked.
- The factory shows Merlin thrust, specific impulse, mass, and restarts. One upgrade raises fresh thrust from 340 kN to 381 kN.
- A static fire holds when thrust, the pad, propellant, and the wind all clear. The chance roll is gone.
- The header shows today’s sky and the next two days. The sky comes from the day number.
- The README is the SpaceX story guide. The program roadmap records Falcon 1 first, then patches.
- The previous live file is `archive/index-0.1.0-foundation.html`.

## `0.2.1-field` — 2026-10-02

**Version:** `0.2.1-field`

- The map draws the gulf shore in sand, with a scale bar. World and Region show country borders and names.
- The left column offers the Build site and the Pad site. Inland ground is gone. The plant list is gone.
- Owned ground is a copper line on the same grid as the buildings, outside each sprite.
- The previous live file is `archive/index-0.2.0-merlin.html`.

---

## `0.3.0-panel` — 2026-10-09

**Version:** `0.3.0-panel`

- The header is the range console. Range open or Range closed is the large line. The sky and the wind sit under it.
- Steel, propellant, fleet, and day are numerals in the center of the header, at 32px. The version label sits under those four counts. The control hint is gone. The sound button and the Web Audio tones are out. Sound returns at `10.3.0-sound`.
- The fire rules are unchanged. The previous live file is `archive/index-0.2.1-field.html`.
- Unsold parcels no longer draw a dashed rectangle on the field. The left column still lists them for sale.
- A buy card shows the site name, the steel price as the large number, and one sentence. Acres stay on the owned line only. Square feet are off that column.
- The right column uses the approved sentences for the inspector, the fleet, and the goals. The fire rules are the same.
- A building card shows the name, one sentence, and one large number. Actions are black cards. A fleet row opens the rocket sheet. Raise Merlin thrust is on that sheet and applies to that rocket. The rocket picture is a simple shape.
- A Goals word in the left column opens the goals sheet. Under the view buttons, a temporary line shows a factory job or a rollout, and it leaves when that job ends.
- Fleet is a word at the bottom of the right column and opens the fleet sheet. Mega Bay starts with one slot. Another slot costs 30 steel, up to 4. The pad card is split into Fire, Roll, and Upgrade.
- A Wiki word at the left of the log opens pages for the three buildings, Falcon 1, and the static fire.
- Build, Merlin thrust, and refurb each take 1 day. A rollout is still a few seconds.
- The rocket sheet says Isp and engine mass. The pad number is the thrust limit. The factory button says Roll to Mega Bay. A scrap line says first stage.

---

## `0.4.0-borderline` — 2026-10-15

**Version:** `0.4.0-borderline`

- Owned ground is one red dashed line. The water side follows the coast for the whole beach. The back side sits about 8 km inland where the land is continuous, and it follows the bay where the water cuts in. The word on the line is limit. The only dash is that red line.
- Each building is its own buy and its own plot. Starfactory sits inland. Mega Bay sits between the factory and the pad. The Orbital Pad sits nearest the coast. The hall is about one tenth of its plot.
- The Land column counts plots. The highway is off the map. A rollout from Mega Bay to the Orbital Pad follows the yard road drawn between those two doors. The return uses that same road.
- The copper boxes and the corner dots are gone. The previous live file is `archive/index-0.3.0-panel.html`.
- No new fire rule. No yard purchase. No houses. The picture is `design-docs/0.4.0-borderline-design.html`.

## `0.5.0-structure` — 2026-10-15

**Version:** `0.5.0-structure`

- The rocket sheet shows stage dry mass, the structural limit, and payload to low Earth orbit. Stage dry mass starts at 1080 kg. That is the first stage with no propellant and no payload. The structural limit is 27572 kg, the design liftoff load.
- Payload is the lesser of what the burn can lift and what that load still has room for. A fresh Falcon 1 shows 420 kg. It is not the sum of the masses. The rocket does not fly the orbit yet.
- Lighten the stage costs 32 steel and takes 1 day in the Starfactory. Dry mass on that rocket falls by 80 kg, and payload rises to 486 kg. The burn is what stops the second number. The design load stops the first.
- No tanks. No suborbital flight. No new fire rule. The previous live file is `archive/index-0.4.0-borderline.html`.

## `0.5.1-liftoff` — 2026-10-21

**Version:** `0.5.1-liftoff`

- The rocket sheet calls 27572 kg the liftoff mass, because that number is the whole Falcon 1 at liftoff. A short line under it says the number stays fixed because the tanks do not change yet. The Falcon 1 wiki page uses the same words.
- The static fire footer names the real result. A held fire says the rocket held and goes back to Mega Bay for refurb. A failed fire names the short part and says the rocket goes back for refurb or scrap.
- Every count of days reads "1 day" for one and "days" for more. This covers the log, the Starfactory card, the bay slots, the rocket sheet, the job line, and the wiki.
- The factory start and progress lines in the log use the same wording as the job line: Starfactory, building, the rocket, and the day count.
- The static fire caption names what decides the test: thrust, pad, propellant, and wind.
- The rocket sheet explains why payload rises by 66 kg when the stage loses 80 kg. Before the cut, the liftoff mass stops payload at 420 kg. After the cut, the liftoff mass has room for 500 kg, but the burn stops payload at 486 kg.
- Lighten the stage stays on the rocket sheet after use. It shows as a disabled card that reads "Stage lightened. One cut per rocket."
- A small Pause button sits next to the day count in the header. It stops the day clock and reads Resume while paused, and the label above the count reads "Day · paused". Pause changes no rule. Jobs, refurb, and supply wait with the clock. A rollout still finishes while paused.
- When a build finishes, the log line carries a button that rolls that rocket to Mega Bay. It uses the same roll as the Starfactory card, and it leaves once the rocket has moved.
- The Goals, Wiki, and Fleet words are larger and brighter.
- This version adds no new building or rocket and changes no rule. The previous live file is `archive/index-0.5.0-structure.html`.

## `0.5.2-realism` — 2026-10-21

**Version:** `0.5.2-realism`

- Open `index.html?test` and the day is about half a second. Steel starts at 2000. The version label reads `0.5.2-realism · Test start`. There is no test button, and the game still saves nothing. A normal open still starts at 150 steel, and a day is still 4 seconds.
- A fresh Merlin is a Merlin 1A at 318 kN. Raise Merlin thrust fits a Merlin 1C at 343 kN. The old 381 kN step is gone.
- Each fire lowers thrust. When the Mega Bay finishes the refurb, that thrust comes back.
- A build takes 8 to 12 days. A clean refurb takes 2 days. A refurb after a miss takes 4 or 5 days. Raise Merlin thrust and Lighten the stage each take 3 to 5 days. Pad level 2 still cuts one day off a clean refurb.
- Propellant rises by 3 a day. A static fire still draws 8, so the refill covers about one fire every 2 to 3 days.
- Payload to low Earth orbit comes from one stage. The sum uses thrust, specific impulse, dry mass, and propellant mass, and it spends the burn against gravity. It does not use the room under the 27572 kg liftoff mass. A fresh Merlin 1A shows 282 kg. Lighten the stage still cuts 80 kg of dry mass, and that cut adds 80 kg of payload. The rocket does not fly.
- Wiki gains a Numbers page. Each line reads the game value from the same figures the code uses, then names the real figure, a source, and the simplification. One line says real Falcon 1 flights launched from Omelek in the Kwajalein Atoll, and this game builds them at Starbase.
- No tanks, no RP-1 and oxygen split, and no flight. The previous live file is `archive/index-0.5.1-liftoff.html`.

## `0.5.3-polish` — 2026-10-21

**Version:** `0.5.3-polish`

- Pause sits beside the day count. The button keeps one width, so Resume does not move the counts. The line above the count reads Paused.
- Press Pause and the day clock stops. A static fire already on the screen stops with it, and a new fire waits until Resume. Builds, refurbs, upgrades, and the propellant refill wait with the clock. A rollout already on the road can finish.
- Goals, Wiki, and Fleet have an outline, padding, and a hover state.
- Wiki opens over the game from the Wiki button beside the log. The same button or Escape closes it. The articles sit on the left. The open article sits on the right.
- Each article is a title, a few short paragraphs, and at most one fact box. The numbers come from `TUNING` and `ROCKET_DEFS`. A word in the text opens another article.
- Where the game differs from the 2008 Falcon 1 sources, the article ends with a note headed In real life. Kestrel stays off those pages until the upper stage is on. The version label stays `0.5.3-polish`.
- The Thrust article separates liftoff mass, in kilograms, from weight at liftoff, which is gravity's pull in kilonewtons. Thrust has to beat the weight.
- The rocket sheet says one burn, and it calls the sum a one-stage payload. The user's guide says the Merlin does not restart. The data sheet lists 420 kg from two burns and a liftoff mass of 27670 kg.
- No game number changed. The previous live file is `archive/index-0.5.2-realism.html`.

## `0.6.0-motion` — 2026-10-21

**Version:** `0.6.0-motion`

- A Falcon 1 under construction lies in the Starfactory. Roll to Mega Bay drives it flat along the yard road. The bay keeps it flat. That trip needs a Mega Bay with a free slot.
- Roll to the pad follows the same road. The nose points along the road, so the drive back faces the bay. At the pad the transporter raises the rocket. Static fire appears after the raise.
- The burn plays on the map. The flame runs east. The rocket stays vertical, and the pitch readout stays at 90°. The static-fire stage stays closed.
- A hold prints Held when the burn starts. A miss names the engine or the pad. Pause holds the roll, the raise, the lower, and the burn.
- Refurb days start when the rocket is back in the bay. The fire rule is unchanged. The previous live file is `archive/index-0.5.3-polish.html`.

## `0.7.0-tanks` — 2026-10-21

**Version:** `0.7.0-tanks`

- The header shows RP-1 and liquid oxygen in kilograms. The old single propellant number is gone.
- A static fire loads 220 kg of RP-1 and 484 kg of liquid oxygen. That is 2.2 kg of liquid oxygen for each kg of RP-1. The rocket equation still uses 21092 kg for a full stage.
- Each tank starts at two fires. One buy on the Orbital Pad card doubles that tank for 24 steel. The buy does not speed the daily refill.
- Before the burn, two bars beside the rocket fill for 2 seconds. The header numbers fall as they fill. Pause stops the fill. A closed range or a short tank does not start it. The log names the short fluid.
- A pad miss or an engine miss still spends both fluids and still counts. The card shows fires in the last 30 days, and days since the last fire. With no fire yet, the second line says "No fire yet."
- The day clock stops while a rocket loads propellant or burns. A roll, a raise, and a lower leave the day running, so steel, the tanks, and a factory job keep their pace. A test day is half a second.
- The two fill bars are drawn in screen pixels, 14 pixels wide, beside the rocket.
- The Numbers page links the Merlin page, the SmallSat chart, and the user's guide on the 140 kg per second note.
- The factory can start a rocket while another rocket rolls or burns. The pad still holds one rocket.
- More than one rocket can roll at the same time. The pad still holds one. A rocket on the way into Mega Bay keeps its slot. A rocket that is out still has a slot waiting, so it can come home.
- `index.html?test` fills both tanks and starts steel at 2000. The Wiki Propellant page and the Numbers page read these settings. The previous live file is `archive/index-0.6.0-motion.html`.

## `0.8.0-flight` — 2026-10-22

**Version:** `0.8.0-flight`

- After a clean static fire the rocket stays on the mount for 1 day of inspection. Then it is ready. A ready rocket offers Launch and Return to Mega Bay. A miss still goes back to the bay for refurb.
- Each Merlin counts firing seconds. A static fire adds 5 seconds. A launch adds the full burn. Thrust stays at the fresh Merlin figure. A refurb is needed after a miss, or when the total passes 180 seconds.
- The tank buys are the launch farm. They raise the tanks to 6592 kg of RP-1 and 14502 kg of liquid oxygen. Each day adds 1100 kg of RP-1 and 2417 kg of liquid oxygen, so a launch fills in about 6 days.
- Launch needs a ready rocket, the launch farm, a calm day, and a full flight load. The same fill bars load 6591 kg of RP-1 and 14501 kg of liquid oxygen, then the engine lights.
- The flight uses thrust, falling mass, gravity, and air drag. Five live numbers on the map show altitude, speed, mass, thrust against weight, and dynamic pressure. The panel keeps max-Q and its time. The day clock stops during the flight. Pause stops the climb and the readouts.
- When the Merlin runs dry, the log names the top height, the top speed, and max-Q. The first stage is lost at sea. There is no landing.
- The climb tips only 5 degrees from vertical, and a ready rocket that returns to Mega Bay parks in a bay slot instead of a 0-day post-fire refurb.
- Wiki gains a Flight page. Launch, Engines, Time, Pad, and Numbers describe the inspection, the ready rocket, firing seconds, the frozen clock, and the launch farm.
- `index.html?test` places the three buildings, a ready Falcon 1 on the mount, both tank buys, tanks filled for one launch, and a calm day. The previous live file is `archive/index-0.7.0-tanks.html`.

## `0.8.1-fix` — 2026-10-22

**Version:** `0.8.1-fix`

- Days keep moving while a rocket loads propellant, burns, or flies. The factory, the bay, and rolls keep their pace during a fire or a launch.
- The farm skips the daily RP-1 and liquid oxygen refill while a rocket loads or burns. A flight can last several days, so the farm keeps refilling then.
- Weather only gates a launch at liftoff. A closed range during a flight that already left does not stop the climb. Pause still stops the day and the burn.
- The pad still holds one rocket. Tank buys still wait while fluids move.
- The previous live file is `archive/index-0.8.0-flight.html`.

## `0.9.0-economy` — 2026-10-29

**Version:** `0.9.0-economy`

- Money is the first count in the header. A normal open starts at 150 money, 0 steel, 0 kg of RP-1, and 0 kg of liquid oxygen. The day adds no money, no steel, and no fluid. Investors add money once, when a goal is finished. The Goals sheet shows the amount. The pays are 40, 20, 70, 60, 40, and 50, in goal order.
- Buy steel sits above the plot cards. It costs 10 money and adds 10 steel. The button is off when money is under 10. Starfactory, Mega Bay, the Orbital Pad, the Falcon 1, Raise Merlin thrust, Lighten the stage, Another slot, Pad level 2, and both tank-capacity buys still spend steel only.
- The Orbital Pad card has Buy RP-1 and Buy liquid oxygen above the tank-capacity buys. Each costs 6 money and fills that tank in one press. A full tank does not sell. A launch tank is two presses, one for each fluid.
- A short purse logs `Need N money.` A short steel stock logs `Need N steel.` A roll, a static fire, and a launch still spend no money.
- A closed range or a short tank aborts the static fire and the launch. The log names every short part. The rocket sheet then shows Empty the tanks. That button dumps the RP-1 and the liquid oxygen. The rocket keeps its condition and stays where it is. Another fire waits until the tanks are empty. An engine or a pad that is short can still miss, cut condition, and send the rocket to the bay.
- A clean flight reaches 89.2 km and 1932 m/s, and that pays the Launch a Falcon 1 goal, 80 money. The rocket still needs the launch farm and a clean static fire. The first stage is lost only after a flight that leaves the pad.
- `index.html?test` is the same open with a day of half a second. Money starts at 150. Steel, RP-1, and liquid oxygen start at 0. The yard is empty. The previous live file is `archive/index-0.8.1-fix.html`.

## `0.10.0-parts` — 2026-10-29

**Version:** `0.10.0-parts`

- The rocket sheet is one drawing of the Falcon 1. The tank, the collar, and the engine bell each fill with that part's percent. A fresh fuel fitting reads 24% on the collar. The big number is the lowest part. The line under the name in the fleet matches it, such as `24% · Fuel fitting`. The window scrolls. In the bay, the drawing and the line beside it start that part's refurb. The lowest part carries the red mark. The fill stays at that percent when the day redraws the sheet. The scroll stays with it. Raise Merlin thrust and Lighten the stage sit in two smaller boxes under the numbers.
- A new Merlin has 180 seconds. A lit static fire spends 5. Life stops at 0. At 0 the Merlin is worn. The rocket goes to needs return, and the refurb clock does not start. Refurb the Merlin costs 24 steel and takes 2 days, or 1 day when the pad is level 2. It restores 180 seconds.
- The fuel fitting starts at 40 seconds. That 40 is a game number. No user's guide page prints a life for this nut. A static fire does not spend it. Launch needs 169 seconds. The Launch card says Try launch and prints the seconds on the fitting and the 169 the burn needs. The burn still lights. Thrust ends at 34 seconds. The log says the fuel fitting is short, and the first stage is lost. Inspect the fuel fitting takes 1 day and no steel, and it sets the fitting to 169 seconds.
- The stage starts at 100. A lit miss takes 40 off that life. An engine miss also sets the Merlin to 0. A pad miss leaves the Merlin's 5 second spend. Under 20 the rocket is scrap, and the log names the short part. Refurb the stage takes 4 to 5 days and no steel. It restores 100. A flight does not change stage life.
- A closed range or a short tank is still a scrub. The attempt may run. The three lives do not move. The player still empties the tanks from the sheet.
- The Mega Bay runs one part. In the bay, each band on the rocket is that part's refurb. The lowest part has the red mark. A second press waits. Return to Mega Bay parks the rocket. The first finished part pays the refurb goal of 40 money once.
- Buy 10 and Buy 50 sit above the plot cards. The rate is 1 money per steel, so the packs cost 10 and 50. Buy 50 is off when money is under 50. Buy 10 is off when money is under 10. The plot cards stay the larger buy.
- The 34 second cutoff is the DARPA board line in Space Daily on 21 July 2006. The 169 seconds are the Flight 3 timeline already in the wiki. The 5 second hold is the 2008 user's guide. The previous live file is `archive/index-0.9.0-economy.html`.
