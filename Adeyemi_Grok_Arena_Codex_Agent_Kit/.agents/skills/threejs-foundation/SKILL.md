---
name: threejs-foundation
description: Initialize and maintain a lean Three.js Vite game shell. Use when working on this part of the ADEYEMI Three.js browser game.
---

# Threejs Foundation

## Purpose
Audit current repo, ensure vanilla ESM, WebGL support fallback, scene/camera/renderer startup, resize and cleanup, fixed-step loop and Low default. Run build, inspect console manually when possible. No enemies or full levels.

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
