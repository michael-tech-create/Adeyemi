# ADEYEMI — AI Game Development Agent Kit

A practical working kit for **Codex** and **Grok Build / Arena** to develop *ADEYEMI: Shadows of the Kingdom* as a low-budget Three.js browser game.

## How to use

1. Extract this kit into the **root of your game repository**. Do not replace existing code blindly; use Git.
2. Read `docs/GAME_DESIGN.md`, `docs/ROADMAP.md`, and `docs/ACCEPTANCE.md` yourself.
3. In Codex, run from the repo root. Codex reads `AGENTS.md` and can discover skills in `.agents/skills/<name>/SKILL.md`. For a specific task, ask it to use the named skill, e.g. `Use $threejs-foundation to perform the task in prompts/01-foundation.md`. If explicit invocation syntax differs in your version, simply tell it to read the file.
4. In Grok Build/Arena, paste `prompts/00-grok-bootstrap.md` as the first task. Ask it to **read** `AGENTS.md` and the chosen skill file. The common Markdown files are portable; **do not assume Grok automatically discovers Codex skill paths**. Check your current Grok documentation/settings for native skill configuration.
5. Only work on **one** numbered `prompts/` task per coding iteration. Do not use Grok Arena and Codex concurrently on the same working tree.
6. Before every task: `git status`; when current game works: `git add . && git commit -m "checkpoint: working game"`.
7. After every task: review diff, run `npm run build`, run relevant tests, **play the game manually**. Use `prompts/15-review-handoff.md` before moving on.

## Recommended division of labor

- **Grok Arena**: Compare designs or approaches for camera, combat, boss behavior or performance. Have candidates work in separate branches/worktrees if supported; choose one based on measured results, not aesthetics alone. Avoid 8 parallel agents on a slow PC.
- **Codex**: Implement the selected approach, run tests, refactor and fix bugs. Either tool can do implementation; avoid simultaneous changes to shared files.
- **You**: Own product scope, test real controls, check cultural accuracy and approve milestones.

## What is included

- `AGENTS.md`: permanent guardrails
- `.agents/skills/`: 15 independent Codex-compatible skills
- `prompts/`: 19 copy/paste phase prompts and operational prompts
- `docs/`: game design, roadmap, scope, architecture, performance, assets, acceptance, release and risks
- `templates/`: task, issue, asset and handoff templates

## Installation (after project setup)

```bash
npm create vite@latest adeyemi-warrior -- --template vanilla
cd adeyemi-warrior
npm install
npm install three
npm install -D vitest
npm run dev
```

**Do not install every optional package immediately.** Add only what a tested milestone needs.

## Sources to check for current behavior

- Codex project instructions and skills: https://developers.openai.com/codex/ ; https://learn.chatgpt.com/docs/build-skills
- Three.js: https://threejs.org/docs/
- Vite: https://vite.dev/guide/
- Three.js GLTFLoader: https://threejs.org/docs/pages/GLTFLoader.html
- Three.js InstancedMesh: https://threejs.org/docs/pages/InstancedMesh.html

`AGENTS.md` does not substitute for verification. A skill is a workflow guide, not a guarantee of working code. All budget numbers are targets subject to real hardware testing.
