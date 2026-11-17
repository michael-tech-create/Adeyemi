# Acceptance gates

**Foundation:** `npm run dev` works, scene renders, refresh works, resize works, Low default, error overlay on WebGL failure, `npm run build` succeeds.

**Movement:** WASD directional movement, stable speed across observed 30/60 FPS, camera orbit and follow, pause restores pointer state, no gross terrain clip, restart works.

**Combat:** health/stamina limits, enemies cannot attack after death, damage applied once per hit, correct block/parry, dodge cost and cooldown, clear death/retry. Unit tests cover edge cases.

**Sacred Forest:** player can talk to elder, investigate three sites, defeat expected enemies, collect artifact, return, see success; checkpoint restores; no soft-lock if step retried.

**Content:** all third-party assets have license/source recorded, audio toggles/mutes, missing assets get fallback, no missing-file console errors.

**Launch:** clean production build, no blockers on at least two browsers, deployed path works, credit screen, feedback link, privacy statement if collecting analytics, rollback procedure documented.
