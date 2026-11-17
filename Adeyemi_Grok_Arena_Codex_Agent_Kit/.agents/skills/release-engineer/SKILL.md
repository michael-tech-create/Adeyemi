---
name: release-engineer
description: Prepare production browser build, legal checks and deployment. Use when working on this part of the ADEYEMI Three.js browser game.
---

# Release Engineer

## Purpose
Audit build, assets license, origin-relative paths, credits, privacy, loading errors, two-browser checks; prepare Cloudflare Pages and itch.io upload artifacts, verify published URLs, record release and rollback.

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
