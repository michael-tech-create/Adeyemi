# Performance Contract

Targets, **not** observed measurements: low-end 30 FPS, capable desktop 60 FPS, first-load transfer ~15 MB, level assets ~35 MB. Capture hardware/browser/date and reproduce measurement before claiming success. Reduce targets if actual test hardware proves unattainable without sacrificing core playability.

Low: renderer pixel ratio <= 0.75 * device ratio (capped appropriately), no shadows, minimal particles, near fog and view range 35–50 game units, 3–5 active enemies. Medium: moderate shadows/visibility, 6–8 enemies. High: optional enhanced shadows/effects only when measured.

Use `InstancedMesh` for repeated tree/rock meshes, share materials, small GLB with optimized geometry and textures, avoid per-frame UI layout, avoid scene cloning. Sample renderer.info.render.calls and frame-time. Set a maximum object count per encounter and monitor spikes rather than average FPS alone.

Measure 30-second idle, forest traversal, worst combat, pause/resume, reload, 10 level loads/unloads. Record avg/p95 frame time, FPS range, draw calls, heap where available, transfer size, browser GPU info if accessible. Never invent benchmarks.
