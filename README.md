# starbase-builder

A browser game where you run SpaceX hardware for real. You develop Starship at Starbase in Texas, fly it to orbit, then choose where the story goes next.

![Starbase Builder, live map with Land and Inspector](design-docs/images/readme-hero.png)

## Play it

Open `index.html` in a browser. There is no build step. Open `index.html?test` for the same start with fast days. That start is not saved.

## How to play

Buy steel and plots on Land. Build a rocket at Starfactory. Roll it to Mega Bay, then roll it to the Orbital Pad. Run a cryo proof, load methane and LOX, run a tanking run, then a static fire, then send the rocket home. The hop comes later. Parts wear out: Structure, Fuel lines, and Engine (Raptor). Goals, Wiki, and Fleet sit on the screen. The Wiki reads the live numbers, and a note says In real life when the game and the sources differ.

## What's real

The sites, the engines, and the propellants follow real SpaceX hardware. The game simplifies some steps so a session stays short. Those shortcuts sit in the Wiki under In real life notes.

## Status

Live release: `0.15.0-sheet`. Next row: `0.16.0-bay`. The rocket window names the short part. Has and Needed sit on that line. In Mega Bay the fix button is on the same row. On the pad the window does not start the job. One seed still drives the defect order and the sky. The header has 1x, 2x, 4x, and Skip. The cryo proof, the tanking run, and the static fire stay on the pad. The hop comes later.

## Where it's headed

The full build map is [`design-docs/program-roadmap-design.html`](design-docs/program-roadmap-design.html).

1. **Phase 0 · Starbase.** Starship development in Texas up to orbit: Raptor and methane, prototype tests, defects, the rocket window, a bay check, a visible weak number, hop, high hop, stack and tower, suborbital test, then orbit.
2. **Phase 1 · Recovery and catch.** Bring the booster home, catch it with the tower, inspect and refurbish it, then raise the factory rate.
3. **A branch, in any order.** Starlink. The Moon and Mars, with a depot in orbit. Or the Falcon story at the real Falcon sites: California factory, Kwajalein, Cape Canaveral, Vandenberg, and 39A.
4. **Later chapters.** Compute, the yard, longer flights, picture and record, and a fleet desk.

## How it's built

One person, Tiago, ships the game. A small team of Grok Bot agents helps: Lead, Builder, Critic, Playtester, and Research. The game is one HTML file. Versions are named `N.x.y-codename`. Tiago tests in the browser and is the only one who commits, pushes, and merges.

## Repo map

- [`VERSION`](VERSION) holds the live release label.
- [`AGENTS.md`](AGENTS.md) covers the voice, the realism rules, and how we ship.
- [`FUTURE_FEATURES.md`](FUTURE_FEATURES.md) lists the open ideas.
- [`IMPLEMENTATION_LOG.md`](IMPLEMENTATION_LOG.md) records what already shipped.
- [`design-docs/program-roadmap-design.html`](design-docs/program-roadmap-design.html) is the version map.
- [`design-docs/learning-guide.html`](design-docs/learning-guide.html) holds the lessons.
- [`archive/`](archive/) keeps frozen snapshots of past releases.
