# Future Features & Roadmap — starbase-builder

**Active backlog only.** Open ideas, planned milestones, and deferred-but-still-wanted work.

When something **ships** or is **dismissed**, document it in `IMPLEMENTATION_LOG.md`, then **remove it from this file**.

**Current phase:** 0 · Foundations  
**Last shipped:** `0.0.1-bootstrap` (docs only)  
**Thematic arc:** Foundations → Flight → Scale → Power → Cis-lunar → Mars

---

## Guiding principles (locked)

- Start **super simple** and accumulate. First playable uses flat / simple 2.5D shapes.
- Rendering fidelity, animations, and visual quality improve in focused passes over time.
- Sites **accumulate**. Starbase on Earth stays critical forever.
- Outer bases (Moon, Mars) depend on Earth cadence, reliability, and production.
- Grok Imagine will later become a real asset-generation pipeline for the project.

---

## Phase 0 · Foundations — next (open)

| Item | Notes |
|------|-------|
| `0.1.0-foundation` | Green grass terrain + pan/zoom + place extremely simple buildings (Pad, Mega Bay, Tank Farm, Starfactory). No real simulation yet. |
| Basic resource model | Steel, CH₄, LOX, Power (and later workforce). |
| Simple vehicle design panel | Create / queue basic Ship & Booster variants. |
| First stack on pad | Place a vehicle on the OLM. |
| Crude launch animation | Even a simple trajectory + particles is enough for first dopamine. |
| Static fire / hop / early orbital progression | Core early loop. |

**Visual direction for Phase 0:** Earthy AoE-style (green grass, dirt, warm stone). Simple shapes first. 2.5D depth can be improved in small dedicated passes.

---

## Rendering & Visual Fidelity (ongoing, not a single phase)

These are first-class work items that can be scheduled whenever the current gameplay feels too crude:

- Better 2.5D / isometric building rendering
- Improved terrain (subtle variation, dirt paths, coastal feel)
- Launch plume, engine exhaust, and particle systems
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

- Higher flight rate and recovery (chopsticks catch)
- Production scaling and parallel workstations
- Unlock **Orbit view** — simple Starlink constellation visualization
- First light contracts / missions
- Better launch and recovery animations

---

## Phase 2 · Scale (open sketch)

- Buy extra land around Starbase
- Workforce count + basic housing demand
- Light city growth (residential zones, simple buildings)
- More advanced vehicle design options

---

## Phase 3 · Power (open sketch)

- Stronger government / commercial contracts
- Light world-economy feedback (demand, reputation, funding)
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

---

## Other open ideas (lower priority)

- Save / load slots and export
- Simple replay or history of launches
- Multiple difficulty / starting condition presets
- Sound design (later)
- Florida site as an optional parallel Earth location

---

## Project goal (one line)

Build a multi-scale space industry game that starts as pure Starbase base-building satisfaction and grows into a living system of interdependent sites from Earth to Mars — starting simple and accumulating depth, fidelity, and ambition over time.
