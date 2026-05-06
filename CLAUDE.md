# Conferencia IA: Revolución en el Desarrollo

## Autor
Rinaldo Julio Sassaroli — Senior Software Developer & Tech Leader, +25 años de experiencia.

## Qué es este proyecto
Presentación para una clase magistral virtual sobre IA en el desarrollo de software, programada para el 06/05/2026 a las 20:00 ART.

## Archivos

- `IA Revolucion Desarrollo.html` — Deck de 24 slides. Usa el web component `<deck-stage>` para navegación. Diseño: dark tech aesthetic, 1920x1080, IBM Plex Sans + JetBrains Mono, paleta blue/cyan (#4d8dff, #6ee7ff) sobre fondo #0b1020. Speaker notes embebidas como JSON. Broadcast de cambios de slide via BroadcastChannel `deck-presenter`.
- `deck-stage.js` — Web component reutilizable para decks HTML. Maneja teclado (←→, Space, PgUp/PgDn, Home/End, 1-9, R), tap zones mobile, auto-scaling, print-to-PDF.
- `presenter.html` — Vista de presentador sincronizada con el deck. Muestra: speaker notes, puntos clave con bullets codificados por color (▸ azul=decir, ◆ verde=hacer, ! amarillo=enfatizar, ● rojo=demo), preview del próximo slide, timer con pausa/reset, barra de progreso. Se conecta al deck via BroadcastChannel.

## Estructura de slides
1. Portada
2. 92% de adopción (dato de apertura)
3-4. Fundamentos: qué es un LLM, motor de razonamiento
5. Taxonomía: LLM vs Copilot vs Agente
6. Demo 1: mismo prompt, dos modelos
7. Advertencia: el error más común (analogía del gimnasio)
8-10. 4 usos saludables: tutor, revisor, boilerplate, par de debug
11. Demo 2: anatomía de un buen prompt (fórmula)
12-14. Reglas de oro: no copiar sin entender, alucinaciones, datos sensibles, versiones
15. Nuevo ciclo de desarrollo
16. Agentic AI
17. Vibe coding
18. Habilidades que cambiaron de valor
19. El dev como supervisor (tesis central)
20. Ecosistema de herramientas
21. Demo 3: Copilot en el editor
22. MCP: Model Context Protocol (el USB-C de la IA)
23. Skills: instrucciones reutilizables para agentes
24. Cierre + Q&A 45 min

## Cómo mantener consistencia
- Los números de slide aparecen en: chrome labels (`NN / 24`), author chips (`RJS · NN / 24`), y el array SLIDES del presenter.html. Si se agrega o quita un slide, actualizar los tres.
- Design system: usar las CSS variables de `:root`. Componentes reutilizables: `.card`, `.compare`, `.flow`, `.prompt-block`, `.mark`, `.eyebrow`, `.demo-banner`.
- Speaker notes: array JSON en `#speaker-notes` dentro del HTML del deck. El presenter.html tiene su propia copia en el array NOTES — mantener sincronizados.
- Idioma del contenido: español argentino (vos, voseo).
