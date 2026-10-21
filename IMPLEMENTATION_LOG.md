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
- The rocket sheet says one burn, and it calls the sum a one-stage payload. The user's guide says the Merlin does not restart. The data sheet lists 420 kg from two burns and a liftoff mass of 27670 kg.
- No game number changed. The previous live file is `archive/index-0.5.2-realism.html`.
