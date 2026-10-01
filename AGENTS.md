# AGENTS.md — starbase-builder

**Repository**: https://github.com/tiagomdv/starbase-builder  
**Your Role**: Coding collaborator. The human (tiagomdv) is the strict Project Manager.

Read this file at the start of any session that implements, versions, or opens a pull request.

## How we write

This applies to the whole project. Chat, the game, design docs, the log, commit messages, and pull requests all use the same voice. Write sentences a person can read out loud.

Write short sentences, about twenty-five words or fewer. Use everyday words and the active voice. Say who does what. "The pad holds the rocket" is clearer than "The rocket is held by the pad." Stay in the present tense. Use numerals for counts, days, and costs.

Name buttons, buildings, and files as they appear on screen: Starfactory, Mega Bay, Orbital Pad, `index.html`. If a technical word is required, explain it once in plain words the first time it appears. Thrust, specific impulse, and pad level are fine after that explanation. A stack of undefined abbreviations is not.

In the game, a label says what the player can do or what just happened. "Static fire" and "Falcon 9 needs pad level 2" are enough. Do not write "simply," "just," "easily," or "obviously." Do not use slogans, exclamation marks, or a joke in place of the fact. A failure names the part that was short.

In chat and in docs, explain a change by what the player sees: the number on the panel, the rocket on the pad, the days the bay is busy. Comments in code are one sentence about why, in the same English.

Do not write dash-label fragments, tables of definitions, or consulting language when a few sentences will do. A table is for a real comparison, such as two rockets side by side. Design docs stay HTML and stay readable in the same voice.

## Core Rules (Non-Negotiable)

1. **One feature at a time** — Never work on multiple unrelated features in the same session unless the human explicitly scopes a small bundle.
2. **Human ships** — Only the human commits and pushes. Do not push code or open PRs unless the human explicitly asks in that session.
3. **Human tests** — Browser verification is the human’s job before something is considered shipped.
4. **AI implements (hybrid)** — Like `personal-expense-app`, the AI **may** write full feature slices into `index.html` (and approved files). The human reviews, tests, and decides ship.
5. Always respect the **current phase scope**.

**Standing PR Directive**: Every pull request description must state that changes were reviewed/tested by the human (for code PRs) and that the human requested the PR after verification.

## Start Simple, Accumulate

The project begins with the simplest possible visuals and systems.  
Rendering fidelity, animations, 2.5D improvements, and later Grok Imagine assets are **accumulated over time** in focused passes.  
Do not over-engineer early visuals.

## File Discipline (Non-Negotiable)

- **Do not create new files** unless the human has approved them for the current phase (or this bootstrap structure already lists them).
- The game should remain a single runnable `index.html` for as long as practical. Do not introduce separate `.js`, `.css`, build tools, or frameworks without explicit approval.
- **Approved structure** (bootstrap):
  - `VERSION` — one-line live release label
  - `README.md`, `AGENTS.md`, `FUTURE_FEATURES.md`, `IMPLEMENTATION_LOG.md`
  - `archive/` + `archive/MANIFEST.md` — frozen snapshots (never edit archive contents in place)
  - `design-docs/` — design artifacts (**always `.html`**, never `.md`)
  - `index.html` — live game (single-file)
- Keep any future real financial or personal data out of the repo.

## Versioning Ritual

**Scheme:** `N.x.y-codename` where **major N = phase number** (`0.x` = Phase 0 · Foundations, `1.x` = Phase 1 · Flight, …).

**Before any PR that meaningfully changes the live app (`index.html`):**

1. Copy current `index.html` → `archive/index-<version>.html` (once it exists)
2. Update `VERSION`
3. Update version display in the app UI (when present)
4. Update README live-release line
5. Add a row to `archive/MANIFEST.md`
6. After merge: git tag `v<version>` when the human wants tags

**Docs-only / design-only PRs:** bump `VERSION` if it marks a project milestone; otherwise a docs commit is enough for small edits.

**Never edit files inside `archive/`** (except appending to `MANIFEST.md` when archiving).

### Design Artifact Nomenclature

Design documents in `design-docs/` are **HTML only** (browser-readable, same spirit as the game):
- `<version>-<codename>-design.html`
- Implementation guides: `<version>-<codename>-implementation-guide.html`

**Do not create `.md` design docs.** Project process docs (`README.md`, `AGENTS.md`, `FUTURE_FEATURES.md`, `IMPLEMENTATION_LOG.md`) stay markdown.

Examples:
- `0.0.1-layout-aoe-3d.html`
- `0.1.0-foundation-design.html`

## Capturing Deferred Ideas

Out-of-scope ideas → offer to append to `FUTURE_FEATURES.md`. Keep the current session focused.

## Project Focus

**Product vision (locked):** A **simple, quick-to-finish** game that is **realistic and fun** — players enjoy the **processes and dynamics** of the space industry (build → house/stage → pad ops → fire/fail/refurb → cadence). Not a sprawling empire sim; depth from honest mechanics and visual cues.

**Thematic arc:** Foundations → Flight → Scale → Power → Cis-lunar → Mars  
(Each phase stays compact; the arc expands *where* you operate, not into endless grind.)

| Phase | Name | Focus |
|-------|------|-------|
| 0 | Foundations | Starbase ground, basic buildings, resources, vehicle design, first launches |
| 1 | Flight | Higher flight rate, recovery, Orbit view, light contracts |
| 2 | Scale | Land, workforce, housing, light city growth |
| 3 | Power | Contracts, world-economy links |
| 4 | Cis-lunar | Moon base + Earth↔Moon logistics |
| 5 | Mars | Mars base + interplanetary logistics |

**Core principle:** Sites accumulate. Earth Starbase remains critical even after outer bases unlock.

## Documentation Responsibilities

After the human approves work, help update:
- `VERSION` + README live-release line (when applicable)
- `FUTURE_FEATURES.md` (remove shipped items; append new open ideas)
- `IMPLEMENTATION_LOG.md` (**one section per `VERSION`** — see Log Files Philosophy)
- `README.md` when understanding of the project changes
- `archive/MANIFEST.md` when archiving

## Log Files Philosophy

| File | Role | Edit rule |
|------|------|-----------|
| **`IMPLEMENTATION_LOG.md`** | History of what shipped | **One section per `VERSION` label.** While that version is open, **update that section** (do not add another header for the same version). When a **new** version ships, **append one new section**. Do not rewrite older versions’ sections except for factual typos. |
| **`FUTURE_FEATURES.md`** | **Active backlog** only | **Remove** items when shipped or dismissed. **Append** new open ideas. |

## Session & Process Discipline

- Prefer **one fresh session per feature**.
- Use a design doc for layout, data model, animation approach, or anything non-trivial.
- Flow: scope → design (when needed) → implement → human tests → docs.

## Anti-Patterns

- Starting complex rendering or Grok Imagine assets before a playable foundation exists.
- Adding Moon/Mars systems before Earth Starbase feels good.
- Creating new source files or splitting the single-file game without approval.
- Pushing or opening PRs without human request.
- Multiple log sections for the same `VERSION` in `IMPLEMENTATION_LOG.md`.
- Rewriting past versions’ log sections (except typos).
- Writing chat, UI, or docs in fragments, jargon stacks, or a voice the human would not read aloud.

---

This file is the single source of truth for how any AI should behave while working on this repository.
