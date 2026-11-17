# Game Design Document — ADEYEMI: SHADOWS OF THE KINGDOM

## Core identity
Single-player, third-person, stylized low-poly Nigerian historical-fantasy browser action-adventure. The protagonist Adeyemi is a legendary warrior tied to the Oyo Kingdom. He navigates conflicts, ancestral visions and supernatural threats. Target: mouse/keyboard desktop browser first, 30 FPS low-end floor. Browser game, not photorealistic FPS.

## Gameplay loop
Explore → receive objective → navigate terrain → fight/avoid enemy → interact with artifact/NPC → gain reward → checkpoint → next objective. Short clear feedback after each action.

## Five chapters (roadmap, not one sprint)
1. **Sacred Forest**: elder dialogue → investigate three corrupted markers → defeat five shadow warriors across small encounters → find ancestral seal → return. Initial public mission.
2. **Echoes of Benin**: supernatural historical-memory journey, stealth, ceremonial bronze retrieval.
3. **Spirits of Nok**: visions of an earlier culture, three guardian trials, puzzles/special moves.
4. **Kingdom Gates**: defending the city from coordinated assault, protection/escort choices. Timeline and colonial depiction require research before writing.
5. **Dark Sanctum**: final multi-phase curse boss, ending.

History policy: Oyo, Benin and Nok do not imply concurrent eras. Fictional visions/portal framework bridges places and periods. Clearly mark historic fact vs fiction in codex. Research architectural and clothing details before final art.

## Initial controls
WASD move; Shift sprint; mouse camera; left click attack; right click block; E interact; Tab mission/inventory; Esc pause; Space dodge. Jump can be introduced later with a separate mapping (e.g. J) after playtesting to avoid ambiguous Space behavior.

## Combat rules
Health/stamina, deterministic hit decisions, attack windup/active/recovery windows, readable telegraphs, light/heavy attacks, cooldowns, block/parry, dodge. Start with one melee enemy archetype; add ranged and spirits later.

## MVP visual approach
Procedural humanoids, trees, rocks and mud-brick-inspired structures until licensed GLB assets are ready. Ambient + directional light; optional one shadow-caster, none on Low. Minimal particles, no default postprocessing.

## MVP UX
Main menu, pause, health/stamina, objective hint, interaction prompt, death/restart, readable settings, save progress after checkpoints. Core UI in HTML/CSS.

## Not MVP
Multiplayer, online economy, crafting, complex AI formations, weather system, five complete chapters, voice acting, day/night cycle, massive map, large asset packs.
