# Guion del video (inglés, máx. 3 min) — PENDIENTE de grabar con voz

`demo_defrost_fog.mp4` en esta carpeta es solo una captura automática sin voz (headless, ~20 s) que sirve de referencia; el reto exige un video con voz en inglés usando el guion `demo/` de cabina-abierta. Súbelo a YouTube (no listado) o Drive y pega el enlace en el PR.

Preparación: `npm run dev` en prompt-drive; `python3 -m http.server 3100 -d ../cabina-abierta/demo`; abrir
`http://localhost:3100/?sim=http://localhost:3000/%3Fautostart%3D1%26hideMenu%3D1`; grabar con OBS con audio del sistema.

1. (0:00-0:20) "Hi, I'm Daniel, team DanielMolina, cohort COH-4. In the workshop, asking the assistant to defrost or turn on the fog lights changed the car state but nothing in the cabin. I built feedback for both."
2. (0:20-1:10) Defrost: show the clean cabin. Run the demo step "está empañado". "Notice the soft fan sweep, the amber defrost tell-tale with an F at the bottom edge, and a light mist over the top of the windshield clearing bottom-up over ten seconds, like real vent airflow." Then console: `PromptDrive.vehicle.set({window_rear_defrost:true})` — "rear defrost adds amber heater lines where the mirror is, and an R in the tell-tale."
3. (1:10-1:50) Fog lights: run the fog lights step. "A double relay click, a green ISO fog-lamp tell-tale at the lower left, and a low, wide warm band at the bottom of the road — never in the centre of the view."
4. (1:50-2:20) Reload with state on/off to show initial state; show reference features still working.
5. (2:20-2:50) Key decision: "I kept everything in the periphery and capped the mist at low opacity on the top 42% because a full-screen fog effect would block the road exactly when driving. Limitation: clearing time is fixed and does not depend on fan speed."
