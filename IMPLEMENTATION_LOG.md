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
