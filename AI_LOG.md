# Registro de uso de IA

> Declaración honesta: el código, las notas de diseño, las capturas, este registro y el borrador de reflexión de esta entrega fueron generados por un agente de IA (**Claude Code**, modelo Claude de Anthropic) ejecutándose en el computador de Daniel Molina por encargo suyo, el 12-oct-2026, en una sola sesión de ~1 h. Daniel debe revisar todo antes de entregar.

**Asistentes usados** y para qué: Claude Code (agente en terminal) para leer el reto, escoger las acciones, escribir `src/feedback/features/defrost.js` y `fog_lights.js`, regenerar el bundle, verificar en Chrome headless con puppeteer-core (instalado en `/tmp`, fuera del repo), tomar capturas, generar un video corto con ffmpeg a partir de frames de CDP screencast, y redactar las notas de diseño y estos documentos.

**Tres prompts que me sirvieron:**

1. Encargo principal al agente: "completa el reto Cabina Abierta: lee los README, implementa 2 features sólidas copiando la estructura de referencia, verifica en Chrome headless, escribe notas de diseño, intenta un video, AI log honesto, borrador de reflexión, haz commit sin push". Salió: las dos features, notas y verificación.
2. (Interno del agente) Elegir acciones según los campos existentes en `docs/CATALOGO.md`: `window_front_defrost`/`window_rear_defrost` y `fog_lights`, porque el guion `demo/guion.json` las dispara.
3. (Interno) Script de puppeteer que llama `PromptDrive.vehicle.set({...})` por cada feature, guarda capturas y frames y recoge errores de consola.

**Uno que me engañó / qué falló:**
- El script buscaba un botón "begin" para pulsarlo y no lo encontró (`begin clicked: null`); con `?autostart=1` el simulador arrancó solo, así que no afectó, pero la verificación no prueba el clic manual.
- La primera versión de `defrost.js` repetía la animación de vaho si llegaba un `set` con el mismo valor; se corrigió guardando el estado previo.
- El resplandor de antiniebla quedó muy sutil en la cámara en tercera persona de día: casi no se ve en las capturas. Es una decisión (no tapar la vía), pero hay que revisarla al grabar.
- La consola mostró un único error `404 (File not found)` de un recurso; no es de las features (sucede al cargar la página), pero no se investigó cuál era.
- El video automático no tiene voz ni sigue el guion `demo/`; no cumple el requisito del video y hay que grabarlo a mano.

**Porcentaje aproximado del texto/código final escrito por la IA sin cambios:** ~100 % al momento de este commit (antes de la revisión humana).
