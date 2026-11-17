# Release and operations

1. `npm run build`; run tests; manually play full game from new save to victory; check clean console.
2. For Vite build host: deploy `dist/` to Cloudflare Pages (build command `npm run build`, output `dist`).
3. For itch.io build, use relative base for built assets (`npm run build -- --base=./`), zip the CONTENTS of `dist/` so `index.html` is at root, upload as HTML5 game and test embed.
4. Confirm all assets use legal licenses, credits visible, screenshots/trailer accurate.
5. Add accessibility basics: subtitles, controls guide, camera-shake toggle, readability, mute, reduced motion when possible.
6. Record release version, test hardware, known issues, and rollback strategy (re-deploy last known-good artifact).
7. Only introduce telemetry/leaderboards later with an explicit privacy and abuse prevention design.

Official refs: https://developers.cloudflare.com/pages/ ; https://itch.io/docs/creators/html5 ; https://vite.dev/guide/static-deploy.html
