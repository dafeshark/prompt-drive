# Reflexión (300 a 500 palabras)

> **BORRADOR — revisar y reescribir con tus propias palabras.** Este texto lo redactó un agente de IA (Claude Code) como punto de partida. La rúbrica premia especificidad y honestidad personal: reemplaza todo lo que no hayas vivido tú.

**Equipo:** DanielMolina
**Integrantes:** Daniel Molina (GitHub: dafeshark)
**Features entregadas (ids):** `defrost`, `fog_lights`
**Enlace al pull request:** (pendiente)

## Qué quería lograr

En el estudio, pedir "desempaña el parabrisas" o "prende las exploradoras" era un acto de fe: el asistente decía "listo" y nada cambiaba en la cabina. Escogí estas dos porque son acciones relacionadas con la visibilidad, justo donde la duda del conductor es más peligrosa: si no sé si el desempañador está actuando, sigo mirando el vidrio en vez de la vía.

## Qué diseñé y qué pasó

Para ambas usé el mismo patrón: confirmación inmediata y corta por sonido, testigo persistente en la periferia (ámbar para desempañador, verde para antiniebla, siguiendo los símbolos ISO de un tablero real) y un efecto "físico" sutil (vaho que se despeja de abajo hacia arriba; banda de luz baja y ancha). Lo más importante fue limitar el vaho al tercio superior y a opacidad baja: un efecto a pantalla completa era más vistoso pero tapaba la carretera. Al ver las capturas, el haz de antiniebla quedó casi invisible de día; lo dejé así porque en un carro real también lo es, pero es algo a discutir.

## Dónde la IA me ayudó y dónde me engañó

[Completar con tu experiencia. Ejemplo de lo que pasó: el agente generó y verificó todo en Chrome headless, pero su script no encontró el botón "begin" y el video automático no tiene voz, así que no cumple el requisito por sí solo.]

## Qué haría con un segundo día

Relacionar el tiempo de despeje con `fan_speed` y `fan_airflow_direction`; llevar el haz de antiniebla a la escena 3D y modularlo con la luz del día; probar con 3-5 personas cuántas miradas fuera de la vía necesitan para confirmar cada acción.

## Qué aprendí sobre la retroalimentación en el carro, o sobre cómo trabajo yo

[Completar. Idea: la retroalimentación buena en un carro se parece más a un testigo que a una animación; el reto es confirmar sin pedir atención.]
