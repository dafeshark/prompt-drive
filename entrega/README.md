# Entrega Cabina Abierta — DanielMolina (COH-4)

| | |
| --- | --- |
| Equipo | DanielMolina (GitHub `dafeshark`) |
| Cohorte | COH-4 |
| Repositorio base | `https://github.com/ignacioalvmar/prompt-drive`, etiqueta `cabina-abierta-v1.0` |
| Rama | `cabina-abierta/DanielMolina` |
| Canal de ayuda | https://discord.gg/q2U5AY4qC |

Features: `defrost` (`window_front_defrost`, `window_rear_defrost`) y `fog_lights` (`fog_lights`). Notas en `docs/feedback/defrost.md` y `docs/feedback/fog_lights.md`.

## Reproducir

```bash
npm run build          # o solo: npm run build:feedback
npm run dev            # http://localhost:3000  (o python3 -m http.server 3000)
```

Abrir `http://localhost:3000/?autostart=1&hideMenu=1` (pulsar **begin** si aparece) y en la consola:

```js
PromptDrive.vehicle.set({ window_front_defrost: true })  // vaho arriba que se despeja en ~10 s, testigo ámbar "F", sonido de ventilador
PromptDrive.vehicle.set({ window_rear_defrost: true })   // líneas ámbar arriba al centro, testigo "R", clic
PromptDrive.vehicle.set({ fog_lights: true })            // testigo verde abajo a la izquierda, banda cálida baja, clic de relé
PromptDrive.vehicle.set({ window_front_defrost: false, window_rear_defrost: false, fog_lights: false })
```

O con el guion: `python3 -m http.server 3100 -d ../cabina-abierta/demo` y abrir `http://localhost:3100/?sim=http://localhost:3000/%3Fautostart%3D1%26hideMenu%3D1`.

Capturas de verificación (Chrome headless) y `demo_defrost_fog.mp4` (captura automática sin voz) en esta carpeta. Esta carpeta, `REFLEXION.md` y `AI_LOG.md` no forman parte del PR.
