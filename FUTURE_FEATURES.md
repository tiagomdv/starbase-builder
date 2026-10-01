# Future Features & Roadmap — starbase-builder

**Active backlog only.** Open ideas, planned milestones, and deferred-but-still-wanted work.

When something **ships** or is **dismissed**, document it in `IMPLEMENTATION_LOG.md`, then **remove it from this file**.

**Current phase:** 0 · Foundations  
**Last shipped:** Falcon 1 only. Merlin card, a fire that follows the numbers, and a sky you can wait out. See `IMPLEMENTATION_LOG.md`.  
**Thematic arc:** Foundations → Flight → Scale → Power → Cis-lunar → Mars  
**Prototype reference (local only, not in this repo):** `~/starship-dev/index.html` — playable single-file ops game. Harvest mechanisms; do **not** copy UI layout or dark “range dashboard” look. Starbase-builder stays earthy AoE 2.5D map-first.

---

## Guiding principles (locked)

- **Product vision:** Simple, **quick-to-finish**, **realistic and fun** — showcase and let the player **enjoy industry processes and dynamics** (factory → bay → pad → fire/refurb → cadence). Not a sprawling grind-sim.
- Start **super simple** and accumulate. First playable uses flat / simple 2.5D shapes.
- Rendering fidelity, animations, and visual quality improve in focused passes over time.
- Sites **accumulate**. Starbase on Earth stays critical forever.
- Outer bases (Moon, Mars) depend on Earth cadence, reliability, and production.
- Grok Imagine will later become a real asset-generation pipeline for the project.
- **Reuse ideas from `starship-dev`, not its product shape.** That file is a vertical slice of flight/ops systems; this game is multi-site base-building first.

---

## Field guide (open)

The lesson bank is `design-docs/learning-guide.html`. Improve it after the current game work, not in the same pass.

- Add images where a picture teaches faster than a paragraph.
- Organize the cards so a part sits inside the thing it belongs to. Merlin belongs inside Falcon 1. Thrust and specific impulse belong inside Merlin. Do the same for later rockets and their engines, tanks, and sites.
- Keep each card short enough to open from a button in the game.

---

## Phase 0 · Foundations — next (open)

**Shipped foundation:** `0.1.0-foundation` — see `IMPLEMENTATION_LOG.md`. Design history: `design-docs/0.1.0-foundation-design.html`.

| Item | Notes |
|------|-------|
| ~~`0.1.0-foundation`~~ | **Shipped** — Factory / Mega Bay (multi-house + refurb) / Pad; env resources; F1/F9; SF fail odds + animations; distance rollout. |
| After foundation | Hop close-up; factory→bay road logistics; tank farm when propellant production is interesting; Falcon Heavy / Starship unlocks; deeper VUR ladders. |
| Visual Upgrade Rule (forever) | Every level changes silhouette/footprint/secondary geometry on the map. |

**Visual direction for Phase 0:** Earthy AoE-style (green grass, dirt, warm stone). Simple shapes first. 2.5D depth can be improved in small dedicated passes. Layout mock: `design-docs/0.0.1-layout-aoe-3d.html`. Design: `design-docs/0.1.0-foundation-design.html`.

---

## Harvest from `starship-dev` (local prototype)

**Source:** `/home/tiagomdv0/starship-dev/index.html` (~3.9k lines, monorepo-less prototype).  
**Purpose of this section:** Capture **mechanisms that worked** (or are worth porting) so Foundations → Flight design can pull from a proven loop instead of inventing cold.  
**Rule:** Each row is an **open idea** until designed and shipped in *this* repo. Prefer redesign to fit map-first Starbase play.

### What the prototype already proves

- **Fail-forward loop:** launch → phase odds → success/fail debrief with *what to upgrade next* is more fun than silent RNG.
- **Infra + vehicle R&D dual track:** factory buildings and vehicle caps both feed flight odds; pure number-clicking still needs a map body in this game.
- **Architecture as loadout:** Hopper / expendable / RTLS Falcon-class / Starship-catch are different *recovery paths*, not just skins.
- **Cadence pressure:** pad slots, build days, refurb, multi-launch — “airline vs lab” fantasy.
- **Milestone finance:** claimable capital after heritage events (first flight, first orbit, N recoveries) funds the next factory step without endless passive drip only.
- **Dopamine stack:** countdown beeps, static fire, plume particles, catch vs RTLS presentation, event log.

### A. Infrastructure ↔ stats (map these onto placeable buildings)

Prototype buildings and effects — re-skin as Starbase map entities in Phase 0–1:

| Prototype id | Concept | Stat / loop impact | Starbase-builder fit |
|--------------|---------|--------------------|----------------------|
| Gigabay / High Bay | Stack & integrate | Build speed, parallel build slots | Mega Bay / Gigabay placeable; upgrade levels = visual tiers |
| Raptor Factory | Engine line | Engine reliability, thrust margin | Starfactory / engine bay building |
| Heatshield Tile Plant | TPS production | Reentry survival | Tile plant; gate LAND/CATCH missions |
| Propellant Farm | CH₄/LOX load | Turnaround, payload bonus | Tank farm; ties to CH₄/LOX resources |
| Ship Production Line | Ring sections / tooling | Cost, steel use, mfg speed | Starfactory / production line |
| Avionics & GNC Lab | Flight software | Landing/catch precision | Small lab building; high leverage later |
| Orbital Pad A/B | Launch complex | Cadence, pad reliability, catch base | Placeable pads; Pad B unlock after A level |
| Mechazilla / Catch Tower Arms | Chopsticks | Catch chance, reuse, refurb cut | Tower + arms as pad add-on; Starship recovery gate |

**Design note:** Prototype uses abstract level-ups. This game should show **physical growth** on the map (footprint, height, dirt roads) while keeping similar effect curves under the hood.

### B. Vehicle capabilities (R&D bars)

Port as a **vehicle / program tech panel**, not only free-floating stats:

| Cap | Helps | When it matters |
|-----|--------|-----------------|
| Heatshield | Reentry survival | Any recover-from-orbit / belly-flop path |
| Reusability | Landing/catch odds, wear, refurb time | Recovery contracts |
| Manufacturability | Build cost/time/steel | Factory fantasy, not flight odds |
| Payload class | Contract gate (tonnes) | Heavy / customer missions |
| Flight reliability | Ascent survival (anti-RUD) | Early flights |
| Δv / Energy | Orbit insertion | Orbit and deep-space pathfinders |

**Learning from flights:** prototype bumps caps slightly after successes — good for “every flight teaches.” Keep mild; avoid grind.

### C. Vehicle families / recovery modes

| Class | Orbit? | Recovery | Prototype lesson |
|-------|--------|----------|------------------|
| Prototype hopper | No | None | Cheap learning flights |
| Expendable orbital | Yes | None | Payload / pure insertion |
| RTLS booster class | Yes | Legs land | Cheap refurb; upper stage cost after flight |
| Starship catch class | Yes | Tower catch | Needs Mechazilla; whole-stack reuse fantasy |

**Key idea to keep:** *Catch is a mode of landing*, not a separate mission type. Contracts ask “need recover?”; architecture decides RTLS vs catch.

### D. Mission / contract ladder (early progression)

Prototype ladder (difficulty + pay escalate):

1. Suborbital hop  
2. Suborbital + recovery  
3. Orbital insertion  
4. Orbit + recovery  
5. Heavy payload deploy  
6. Deep-space pathfinder  

Gates: `needOrbit`, `needRecover`, `payloadReq`, `difficulty`. Ship class must be allowed to fly contract (e.g. hopper cannot orbit; catch needs tower).

**Starbase-builder twist:** same ladder, but missions are **scheduled from the base** (stack on pad → range clear → fly), not only modal list. Later: customer contracts (Phase 1–3) reuse the same phase flags.

### E. Flight phase machine (animation + resolution)

Proven phase sequence:

`preflight → countdown → ignition → ascent → stage → orbit → reentry → recovery → done`

- Preflight includes static-fire moment and hold-down feel.  
- Countdown with audible T− beeps.  
- Outcomes **pre-rolled** from phase odds at liftoff (stable displayed odds = honest UI).  
- Failure keys map to upgrade advice: ascent / orbit / reentry / recover (and catch partial).

**Port strategy:**

- Phase 0: abbreviated phases (hop may stop at ascent).  
- Phase 1: full chain + recovery presentation on map/sky.  
- Particles: flame, contrail, heat, explosion — already validated as “enough dopamine” without 3D.

### F. Debrief & observability

- **Last flight debrief panel** + modal: success/fail title, reason, recommended upgrades.  
- Phase odds bars (green/yellow/red).  
- Event **log** (good/warn/bad/info).  
- **FAIL_GUIDE**-style mapping: failure phase → concrete “what to build/upgrade.”

This is high priority for teaching the game without a wall of tutorial text.

### G. Fleet ops & pads

- Fleet as list of named vehicles with status: `building | ready | flight | refurb`.  
- Build queue days scaled by mfg / gigabay.  
- **Pad slots** = concurrent flights; multi-pad parallel launches (“Launch all ready”).  
- Select vehicle on list **or** click on range/map.  
- Per-ship assigned mission (not only global contract).  
- Condition / wear after recovery; refurb timer; Falcon upper-stage recost pattern.

### H. Economy & finance

| Mechanism | Prototype behavior | Starbase-builder idea |
|-----------|--------------------|------------------------|
| Credits / steel / R&D | Three currencies | Map to Credits + Steel + CH₄/LOX + Power + later workforce; R&D may stay abstract |
| Day tick passive income | Small credits + steel from infra | Prefer **production buildings** over pure passive; keep tiny passive only if needed |
| Milestone finance rounds | Claim once when check() true (first flight, N orbits, pad expand, day 30/100, IPO-path, …) | Excellent fit for Phase 0–3 funding fantasy |
| Contract payout | Pay + rd + steel on success | Keep; partial success / soft divert optional |
| Prestige | Soft score unlocking brand rounds | Optional brand/reputation meter |

### I. Audio & juice (later, but catalogued)

Procedural Web Audio (no asset files): UI ticks, build, upgrade, countdown, static fire, liftoff, max-Q, stage, orbit, reentry, catch vs RTLS, success/fail. Mute + localStorage preference.

**Status:** Sound design already listed as lower priority; keep as Phase 0 polish or Phase 1 pass.

### J. Explicitly **do not** port as-is

- Dark dashboard three-column “STARSHIP DEV” chrome (left infra list / center range / right fleet).  
- Global abstract upgrade buttons without map buildings.  
- Winning only via prestige modal without multi-site vision.  
- Falcon vs Starship as the whole game — Starbase-builder is **base first**, flight is the pulse.  
- Monolithic “everything in one PR” — this repo stays one milestone at a time.

### Suggested absorption order (into existing phases)

| When | Pull from harvest |
|------|-------------------|
| `0.1.0-foundation` | Building roster names from §A (simple placeables only) |
| Soon after foundation | Resource triad; pad stack; hop animation (subset of §E) |
| Mid Phase 0 | Caps §B lite; mission ladder §D hop→orbit; debrief §F lite |
| Late Phase 0 / Phase 1 | Full phase odds; recovery modes §C; pad B + tower; multi-flight §G |
| Phase 1–3 | Contracts + finance rounds §H; cadence/production scaling |
| Polish any time | Particles, tower animation, audio §I |

---

## Rendering & Visual Fidelity (ongoing, not a single phase)

These are first-class work items that can be scheduled whenever the current gameplay feels too crude:

- Better 2.5D / isometric building rendering
- Improved terrain (subtle variation, dirt paths, coastal feel)
- Launch plume, engine exhaust, and particle systems *(prototype has flame/contrail/heat/explosion — reimplement in earthy palette)*
- Tower / chopsticks animation
- Day/night or simple lighting later
- Construction states (foundations → steel → cladding → complete)

**Do not block gameplay milestones on perfect visuals.**

---

## Grok Imagine Asset Pipeline (future capability)

**Status:** Planned · high interest · not started

Once the core loop is playable and fun, introduce Grok Imagine as an official way to generate game objects:

- Buildings (Mega Bay, Starfactory, Gigabay stages, pads, towers, tank farms, housing…)
- Vehicles (different Ship/Booster variants, construction states)
- Effects (launch plumes, static fire, catch, explosions)
- UI icons and status art
- Later: Moon and Mars specific assets with different palettes

**Why it belongs in this project:**
- Fits the AI-collaboration lab philosophy perfectly
- Allows rapid visual iteration without external artists
- Can generate consistent variants (under construction, upgraded, damaged, etc.)
- Becomes a distinctive technical feature of the game itself

**Suggested approach when we reach it:**
1. Lock a clear visual style guide (prompts + examples)
2. Generate one category at a time
3. Start with base64 embedding or simple loading so the game can stay single-file as long as practical
4. Make regeneration / preview part of the design workflow

This should be treated as a deliberate mid-to-late Phase 0 or Phase 1 capability, not day-one work.

---

## Phase 1 · Flight (open sketch)

- Higher flight rate and recovery (chopsticks catch) — harvest §C §E §G
- Production scaling and parallel workstations — harvest §A gigabay/slots
- Unlock **Orbit view** — simple Starlink constellation visualization
- First light contracts / missions — harvest §D
- Better launch and recovery animations
- Debrief + phase odds as standard post-flight UX — harvest §F

---

## Phase 2 · Scale (open sketch)

- Buy extra land around Starbase
- Workforce count + basic housing demand
- Light city growth (residential zones, simple buildings)
- More advanced vehicle design options (variants beyond prototype four-class set)

---

## Phase 3 · Power (open sketch)

- Stronger government / commercial contracts
- Light world-economy feedback (demand, reputation, funding)
- Milestone finance ladder mature (heritage rounds, gov pathfinder) — harvest §H
- Starbase as a recognizable industrial node

---

## Phase 4 · Cis-lunar (open sketch)

- Unlock **Moon base**
- Earth → Moon logistics (vehicles, cadence, reliability matter)
- Managing two interdependent sites at once
- Moon-specific buildings and challenges

---

## Phase 5 · Mars (open sketch)

- Unlock **Mars base**
- Longer logistics chains and higher stakes
- Full multi-site management (Earth + Moon + Mars)
- Interplanetary dependencies
- Deep-space pathfinder contracts as Earth-side training for this phase

---

## Other open ideas (lower priority)

- Save / load slots and export (localStorage; multi-slot)
- Simple replay or history of launches (flight log table)
- Multiple difficulty / starting condition presets
- Sound design (later) — harvest §I
- Florida site as an optional parallel Earth location
- Program milestone / “multi-planetary bet” endgame checks (prototype prestige + orbits)

---

## Project goal (one line)

Build a **simple, quick, realistic, fun** multi-scale space-industry game: enjoy Starbase’s processes and dynamics first, then grow into interdependent sites (Earth → Moon → Mars) without losing compactness — accumulate depth and fidelity, not grind.
