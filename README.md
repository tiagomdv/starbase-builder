# starbase-builder

A **multi-site base-building and operations game** that starts at SpaceX’s Starbase and grows outward — from the muddy Texas coast to orbit, the Moon, and eventually Mars.

**North star:** Watch a real industrial spaceport grow under your hands, launch rockets with increasing cadence, and unlock new layers of existence (orbit, Moon base, Mars base) that all depend on the strength of what you built on Earth.

**Right now:** Phase 0 · Foundations — **`0.1.0-foundation`** playable. Factory builds rockets · Mega Bay houses fleet & refurbs · Pad static-fires (can fail). Steel & propellant from environment.

This project is also a deliberate learning vehicle for:
- Structured AI-collaboration workflows (same lab discipline as `trait-evolution-sim` and `personal-expense-app`)
- Incremental development of a complex simulation
- Using Grok Imagine later as a real asset-generation pipeline inside the project

---

## Thematic arc

| Phase | Name | Focus |
|-------|------|-------|
| **0** | **Foundations** | Starbase ground view. Place buildings, basic resources, vehicle design, first static fires → hops → early orbital attempts. Simple launch animations. See the physical base grow. |
| **1** | **Flight** | Higher flight rate, recovery, production scaling. Unlock simple **Orbit view** (Starlink constellation). First light contracts. |
| **2** | **Scale** | Buy extra land, workforce + basic housing, light city growth around the site. More advanced vehicle variants. |
| **3** | **Power** | Stronger contracts, light world-economy links. Starbase becomes a real industrial node. |
| **4** | **Cis-lunar** | Unlock **Moon base**. Logistics from Earth → Moon. You now manage two interdependent sites. |
| **5** | **Mars** | Unlock **Mars base**. Longer logistics chains, higher stakes. Full multi-site management. |

**Core principle:** Sites accumulate. Starbase on Earth never becomes irrelevant — outer bases depend on its cadence, reliability, and production capacity.

Full backlog and open ideas: `FUTURE_FEATURES.md`.  
Ship history: `IMPLEMENTATION_LOG.md`.

---

## Current version

**`VERSION` file** is the single source of truth.

> **Live release:** `0.1.0-foundation` · Phase 0 · Foundations

**Visual direction (locked for now):**
- Earthy, classic RTS feel (green grass, dirt, warm stone colors)
- Start with extremely simple shapes
- Add 2.5D depth and better rendering over time
- Later: Grok Imagine asset pipeline for real sprites and variants

---

## Philosophy

- **Start super simple, accumulate.** First playable version uses flat colored shapes. Rendering, animations, and fidelity improve in focused passes.
- **One focused goal per session / PR.**
- **Human = Project Manager + final ship decision.**
- **Observability and clarity** matter more than premature beauty.
- **Starbase remains the heart** even after Moon and Mars unlock.

---

## Planned tech stack (not implemented yet)

- Single-file `index.html` for as long as practical
- Tailwind CSS (CDN)
- Vanilla JavaScript + HTML Canvas (map, buildings, rockets, particles)
- localStorage for saves
- Later: optional external assets generated via Grok Imagine

No frameworks, no build step, in the early phases.

---

## Project structure

```
starbase-builder/
├── VERSION
├── README.md
├── AGENTS.md
├── FUTURE_FEATURES.md
├── IMPLEMENTATION_LOG.md
├── archive/
│   └── MANIFEST.md
└── design-docs/
```

Open `index.html` in a browser (no build step).

---

## Development approach

**Human = Project Manager + final ship decision.**

- One focused goal per session / PR
- Design first for non-trivial product choices
- AI may implement full feature slices; human tests in the browser and owns commits/pushes
- Archive meaningful snapshots before large changes
- Rendering improvements are first-class work (not an afterthought)

See `AGENTS.md` for full rules.

---

## Immediate next steps

1. ~~Review & accept this bootstrap vision~~ · ~~GitHub repo~~ · **local clone:** `~/starbase-builder` → `origin` = `tiagomdv/starbase-builder`
2. Optional: play the local prototype `~/starship-dev` for feel; open ideas harvested into `FUTURE_FEATURES.md` (do not merge that file into this repo as code)
3. **Design ready:** `design-docs/0.1.0-foundation-design.html` (map-first site, Visual Upgrade Rule, light sim + static fire). Design docs are always `.html`.  
4. First code milestone: `0.1.0-foundation` — implement PR plan in that design (shell → map → place → resources → stack → pad L2 visual → static fire → polish)

---

Built as a hands-on experiment in multi-scale space industry simulation and AI-assisted software development.
