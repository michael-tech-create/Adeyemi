# Architecture Contracts

Vite vanilla ESM. `src/main.js` boots Game. Core: `Game`, `GameLoop`, `Config`, `GameState`, `ResourceManager`. World: `SceneManager`, `CameraController`, `CollisionWorld`. Entities: `Player`, `Enemy`, `NPC`. Systems: `Input`, `Movement`, `Combat`, `EnemyAI`, `Interaction`, `Mission`, `Inventory`, `Save`, `Audio`. UI remains HTML/CSS.

## Data flow
DOM/Input → player intent → fixed-step simulation → events/state → visual mesh/camera render + HUD updates. Pure state/rules cannot import Three.js. Mission JSON declares objectives and rewards. Event dispatch is typed/documented with examples; validate input JSON.

## Game loop
Use a capped fixed-step accumulator to avoid spiral of death. Clamp long tab-suspension deltas. Process input coherently, simulate in fixed steps, render once per animation frame. Respect visibility pause. Document interpolation if implemented.

## State machine
Player: idle, moving, attack, block, dodge, hit, dead. Enemy: patrol, notice, chase, windup, attack, recover, stagger, dead. Explicit transition guards and timers. Block impossible transitions.

## Collision
First use simple circular/capsule-like XY-plane approximation on a flat ground, AABBs for props and range/angle checks for melee; document coordinate convention (Y up). Adopt Rapier only after evidence complex rigid-body physics is needed.

## Resource ownership
Scene owns unique assets and listeners it creates. Shared asset caches have explicit refcounts or lifetime boundaries. Unload level cleanly, do not duplicate GPU geometries/materials.

## Save format
Versioned JSON: schemaVersion, timestamp, checkpoint, unlockedWeapons, inventory, missionProgress, settings. Validate or recover corrupt payload. Save on defined checkpoints/events, not every frame. Never trust saved numbers without clamping.

## Suggested structure
`src/core`, `src/world`, `src/entities`, `src/systems`, `src/ui`, `src/levels`, `src/data`, `src/utils`, `src/styles`, `public/models`, `public/audio`, `public/textures`, `tests`, `docs`.
