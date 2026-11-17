---
name: enemy-ai
description: Create low-cost state-machine enemy behaviors. Use when working on this part of the ADEYEMI Three.js browser game.
---

# Enemy Ai

## Purpose
Use finite state machine with patrol/investigate/chase/windup/attack/recover/dead and bounded update schedules. Include sensing radius, line-of-sight approximation, leash, obstacle handling. Avoid expensive global pathfinding in first release.

## Procedure
1. Read `AGENTS.md`, `docs/ROADMAP.md`, and relevant design/architecture docs. Inspect actual repository state.
2. Describe smallest safe change and explicit acceptance criteria. Refuse unrelated feature creep.
3. Implement only the assigned subsystem or deliver a comparative plan if review-only.
4. Write focused tests for pure logic; run existing checks/build when available.
5. Call out manual gameplay/visual tests that cannot be automated or were not run.
6. Summarize changed files, test evidence, measured impact (if any), known issues, and next one task.

## Constraints
- Web-first vanilla JS + Three.js, low-end hardware, inexpensive tools; no hidden paid services.
- Distinguish measurement from estimates, and actual assets from placeholders.
- Preserve existing public interfaces and other working gameplay.
- Keep historical-fantasy representation and rights documentation respectful and accurate.

## Deliverable
Implementation or bounded design, tests/results, acceptance checklist, and concise handoff notes.
