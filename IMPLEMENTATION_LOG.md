# Implementation Log — starbase-builder

Append-only history of what shipped, major process decisions, and important dismissals.

---

## 2026-08-06 — Project bootstrap

**Version:** `0.0.1-bootstrap`

- Created project skeleton and locked the long-term vision.
- Thematic arc defined: Foundations → Flight → Scale → Power → Cis-lunar → Mars.
- Core principles locked:
  - Start super simple, accumulate features and visual fidelity over time.
  - Sites accumulate; Earth Starbase remains critical forever.
  - Outer bases (Moon, Mars) depend on Earth cadence and production.
- Visual direction for early work: earthy AoE-style (green grass, dirt, warm stone colors) with simple shapes first, 2.5D improvements later.
- Grok Imagine asset pipeline explicitly added as a future capability (not day-one work).
- Process style: hybrid (same as personal-expense-app) — AI may implement full slices, human tests and owns shipping.
- No game code yet. Next milestone: `0.1.0-foundation`.

---

## 2026-08-07 — Local workspace + starship-dev harvest

**Version:** still `0.0.1-bootstrap` (docs only)

- Cloned GitHub repo to local working tree: `/home/tiagomdv0/starbase-builder` (`origin` → `https://github.com/tiagomdv/starbase-builder.git`).
- Reviewed local prototype **`~/starship-dev/index.html`** (STARSHIP DEV ops slice: infra levels, vehicle caps, ship classes, contract ladder, multi-pad flights, phase machine, debrief, milestone finance, procedural audio, canvas range).
- Expanded **`FUTURE_FEATURES.md`** with a full **“Harvest from starship-dev”** section:
  - Mechanisms to reuse (fail-forward debrief, dual infra/caps track, recovery modes, mission ladder, phase odds, fleet/pad cadence, finance rounds).
  - Explicit non-goals (dark dashboard chrome, abstract-only upgrades, flight-only game identity).
  - Absorption order into Foundations → Flight so map-first design stays primary.
- Updated README immediate next steps (repo exists; next is `0.1.0-foundation`).
- Still **no game code** in this repo. Prototype remains outside the git tree as a reference only.

---

## 2026-08-07 — Foundation design (`0.1.0-foundation`)

**Version:** still `0.0.1-bootstrap` (docs only)

- Wrote and design-reviewed `design-docs/0.1.0-foundation-design.html` (writer/reviewer loop to 0 open issues; later converted from interim `.md` — **design docs are always `.html`**).
- Product pillars locked: map-first living Starbase; systems coupling over launch-only; **Visual Upgrade Rule** (every upgrade changes the object visibly and makes physical sense); realistic north-star catalog + process chains; 0.1.0 stays small and playable.
- 0.1.0 scope: 4 placeables (max 1 each), resources + day tick, one stack bay→pad, Pad L1→L2 trench/OLM visual, static fire must-have, earthy chrome from layout mock.
- PR plan: 8 slices (shell → … → static fire → polish/docs). TUNING includes `START_STEEL=220` economy invariant.
- Updated `FUTURE_FEATURES.md` and README next steps to point at the design (supersedes “no simulation in 0.1”).
- AGENTS: design artifacts in `design-docs/` must be `.html` only (not `.md`).

---

## 2026-08-07 — Design rev 4 + first `index.html` draft

**Version:** `0.1.0-wip`

### Product guide (rev 4) locked into design HTML
- **Compact, finishable game** even at “done” — enjoy the industrial ride; realism of mechanics/processes/visual cues over sprawl.
- **Reality ladder:** resource components → ecosystem → stack/load → static fire/hop → harder flight → recovery → deeper Starbase later.
- **0.1 start order:** place generators → grow resources → basic launch-adjacent event → slight visible site/rocket path improvement.

### First draft `index.html`
- Earthy chrome + canvas map (pan/zoom, grass/dirt/water, soft zones).
- 4 placeables (max 1): Starfactory, Tank Farm, Mega Bay, Orbital Pad.
- Day tick production (steel / CH₄ / LOX); Power display-only.
- One stack: build at bay → send to pad.
- Static fire spends propellant + flame juice.
- Pad L1→L2 Visual Upgrade Rule proof (wider trench, taller OLM, cheaper SF).
- Session goals checklist + event log.
- Not final `0.1.0-foundation` polish; human playtest next.

---

## 2026-08-07 — Rollout distance + static-fire close-up

**Version:** `0.1.0-wip`

- **Rollout bay → pad:** road-ish path (via Highway corridor). Duration from path length (`ROLLOUT_PX_PER_SEC`, min/max clamp). Map shows dashed path, transporter under stack, ETA in inspector. Farther placement = longer roll.
- **Static fire close-up:** dedicated event stage with phased animation (approach → chill → ignition → burn → shutdown → debrief). Detailed stack + plume/particles; pad L2 wider trench/taller OLM reflected in close-up. Map still shows short flame. Skip/Esc.
- Pattern for later: each rocket op (hop, orbit, …) gets its own close-up sequence, not one generic flash.

---

## 2026-08-07 — Factory builds rockets (not steel) · F1/F9 · sound

**Version:** `0.1.0-wip`

### Production honesty
- **Starfactory no longer produces steel.** Copy + mechanics: vehicles only.
- **Steel** = inbound materials supply (`+5/day` site-wide), spent on buildings and rocket builds.
- **Mega Bay** stages/houses only — “Stage vehicle from factory,” no manufacture.

### SpaceX roadmap (live)
- **Falcon 1** — 28 steel, 3 days, 1 engine, lighter SF prop + shorter burn.
- **Falcon 9** — 52 steel, 5 days, 9 engines, heavier SF prop + longer denser plume.
- Stubs (not buildable): Falcon Heavy, Starship.

### Per-class static fire
- Close-up silhouette, engine count, phase timings, plume density differ by rocket.
- Map vehicle scale/label by class.

### Sound (Web Audio, no assets)
- UI, build, ready, rollout, upgrade, SF start/ignition, engine rumble (F9 heavier), success/error.
- Mute button (persists `localStorage` `starbase-mute`).

### Loop
Factory queue → stage bay → distance rollout → class-specific SF.

---

## 2026-08-07 — `0.1.0-foundation` closed

**Version:** `0.1.0-foundation`

### Scope cut (keep it real, keep it small)
- **Removed tank farm** from foundation. **Steel + propellant** tick from the **environment** (site supply).
- Three placeables only: **Starfactory** (build rockets), **Mega Bay** (house + refurb), **Orbital Pad** (static fire).

### Multi-vehicle bay
- Mega Bay capacity **4** articles; visual **slots** + capacity pips on building.
- Factory hold **1** finished vehicle until staged into bay.
- Fleet list UI; select vehicle on map or list.

### Static fire risk
- P(success) from rocket class × vehicle condition × pad level.
- **Success** close-up vs **failure** anomaly/RUD animation + SFX.
- Fail → scrap chance or heavy bay refurb; success → light wear + bay refurb days.

### Refurb (realistic location)
- After SF, vehicle **returns to Mega Bay** (not refurbished on pad).
- Pad copy: “pad is not a hangar.”
- Bay runs day-tick refurb until ready again.

### Labels
- Resources: Steel, Propellant, Fleet (no CH₄/LOX tank UI).
- Guide + inspectors rewritten for three-building loop.
