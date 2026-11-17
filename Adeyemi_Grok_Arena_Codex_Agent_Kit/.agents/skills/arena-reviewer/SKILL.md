---
name: arena-reviewer
description: Compare Grok Arena proposals against Codex plans without merge conflicts. Use when working on this part of the ADEYEMI Three.js browser game.
---

# Arena Reviewer

## Purpose
Formulate an isolated design challenge, request max 2-3 candidate plans on low-end hardware, score performance/complexity/testability, choose one strategy with rationale. Do not run competing agents against same working files; deliver a handoff to implementer.

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
