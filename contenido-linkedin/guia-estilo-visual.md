# Guía de estilo visual — imágenes de acompañamiento

Objetivo: que cada imagen se reconozca como suya sin necesidad de leer la firma, y que transmita **autoridad y seriedad**, no "startup con Canva". Coherente con la regla de fondo del proyecto (evidencia, no ruido) — el diseño también tiene que ser sobrio, no llamativo por llamar la atención.

## Paleta de colores

Colores que transmiten confianza y tecnología, sin caer en lo genérico-corporativo ni en lo "IA generada":

| Uso | Color | Hex |
|---|---|---|
| Fondo oscuro (variantes tipo cita/autoridad) | Azul noche | `#0F172A` → `#1E293B` (degradado sutil) |
| Fondo claro (variantes tipo concepto/diagrama) | Gris muy claro, casi blanco | `#F8FAFC` |
| Acento principal (highlights, líneas, marca) | Azul confianza | `#2563EB` |
| Acento secundario (uso puntual, nunca dominante) | Cian dato | `#0891B2` |
| Texto sobre oscuro | Blanco roto | `#F8FAFC` |
| Texto sobre claro | Gris oscuro casi negro | `#0F172A` |
| Texto secundario/subtítulos | Gris medio | `#64748B` |

**Regla:** nunca más de dos colores de acento en la misma imagen. Nada de arcoíris ni gradientes multicolor — eso es lo que hace que algo parezca generado sin criterio.

## Tipografía

- **Familia:** Inter (o system-ui como respaldo) — limpia, muy legible en móvil, la usan marcas de tecnología serias sin ser fría.
- **Titulares/citas:** peso 800 (extra bold), tamaño grande, interlineado ajustado (1.2-1.3).
- **Subtítulos/etiquetas:** peso 600, tamaño pequeño, mayúsculas con tracking amplio, solo como apoyo — nunca protagonista.
- **Cuerpo/notas:** peso 400-600, tamaño moderado.

## Formato

- **1080×1080** (cuadrado) por defecto — funciona en cualquier sitio del feed.
- Alternativa **1080×1350** (vertical 4:5) cuando el contenido necesite más aire vertical (ej. pasos de un tutorial) — ocupa más espacio en el feed de LinkedIn.

## Firma

- Solo el nombre: **Alberto Mariscal**. Sin eslogan ni etiqueta de "para pymes" — la identidad pública de posicionamiento no se activa hasta tener un cliente fundacional (Módulo 4). Mientras tanto, la firma es neutra: nombre y ya.
- Siempre en la misma posición (abajo, con una línea/marca discreta al lado) — la repetición de un elemento fijo es lo que construye reconocimiento de marca con el tiempo, no el logo en sí.

## Tipos de plantilla (variedad dentro de la consistencia)

1. **Cita/idea fuerte** — fondo oscuro, una frase corta con una palabra clave resaltada en color de acento. Para conceptos o reflexiones.
2. **Concepto/comparación** — fondo claro, título + subtítulo + visual simple (antes/después, dos columnas). Para explicar algo con claridad.
3. **Dato/cifra destacada** (a usar cuando haya una cifra real que mostrar) — número grande como protagonista, contexto breve alrededor.
4. **Diagrama de proceso/flujo** — vía Mermaid (flowchart, sequence), útil para contenido de automatización (mostrar un pipeline, un antes/después de un proceso con pasos). Se aplica la misma paleta y tipografía que el resto — no el estilo por defecto de Mermaid.
5. **Tarjeta-pregunta** (añadida 2026-08-02, la que más le gusta a Alberto) — **una pregunta abierta como único titular**, una bajada corta con el hecho que la provoca, y los datos en letra pequeña abajo. Casi todo el lienzo vacío. Para posts de opinión: la **imagen pregunta y el post argumenta**. Ejemplo: *"¿Habrían hackeado Coldcard si el código lo hubiera escrito una IA?"*.
6. **Lista aplicable** (añadida 2026-08-02) — titular + 3-4 puntos numerados que se puedan poner en práctica. Es la plantilla para posts didácticos, y está pensada para **guardarse**: quien la ve suelta en el feed ya se lleva algo aunque no lea el post. Solo si los puntos son de verdad accionables; si no, es una lista de relleno.

## Menos énfasis = más autoridad (regla añadida 2026-08-02)

Alberto rechazó una tarjeta por **rimbombante**: cifra gigantesca, varios acentos y un bloque de comparación. El aprendizaje, que vale para todas:

> Cuanto más discutible es lo que afirma un post, **más sobria** tiene que ser su imagen. El énfasis visual en un argumento opinable se lee como hype, y el hype resta exactamente la autoridad que el post pretende construir.

En la práctica: un solo elemento protagonista por tarjeta, un único toque de acento, y espacio vacío sin miedo. Si la tarjeta necesita gritar, probablemente el texto no se sostiene solo.

## Motor de generación (decidido 2026-07-12)

**HTML/CSS renderizado con Chromium headless (Playwright), capturado a PNG.** Es gratuito y ya integrado en el flujo de trabajo. Se probó generación vía API de Google (Nano Banana / Nano Banana Pro / Nano Banana 2 / Imagen 4) y **se descartó**: todos esos modelos tienen cuota gratuita de 0 peticiones — requieren facturación activada en Google Cloud, con coste real por imagen. Mermaid se integra con el mismo mecanismo (se carga la librería vía CDN dentro del HTML y se captura igual), así que no hace falta una herramienta nueva.

## Cómo se escribe el titular de una tarjeta (regla añadida 2026-08-01)

Feedback real de Alberto sobre un borrador (*"El fallo llevaba cinco años ahí. Y el aparato funcionaba perfectamente"*): **sonaba a IA**. El diagnóstico, para no repetirlo:

- **La antítesis simétrica de dos tiempos es el tic delatador.** "No es X. Es Y." / "A no pasó. Y B sí." Escrita una vez tiene fuerza; usada en todas las tarjetas, se reconoce como plantilla de modelo de lenguaje. Se puede usar, pero no siempre.
- **Sujeto abstracto = ninguna imagen mental.** "El fallo", "el aparato", "el software" no le pasan a nadie. "Tu Excel", "la copia que nunca has restaurado", "lo que hoy automatizas" sí.
- **Regla de reparto**: el **titular habla de la realidad del lector**; el **caso de la noticia va en la bajada**, como prueba de lo que afirma el titular. No al revés. Si la tarjeta se lee sola en el feed, quien pasa tiene que reconocerse en ella antes de saber de qué noticia va.
- **Prueba rápida**: si el titular podría ir en la tarjeta de cualquier otra persona del sector sin cambiar una palabra, no sirve. Tiene que oler a alguien que se ha peleado con eso.

## Tira de datos (elemento nuevo, 2026-08-01)

Bajo la bajada, separada por una línea fina, una fila de 2-3 pares **cifra + etiqueta** (cifra en azul de acento peso 800; etiqueta en gris, mayúsculas pequeñas con tracking). Ejemplo: `5 AÑOS oculto · 41 MIN de robo · ~70 M$ en bitcoin`.

Para qué sirve: ancla la tarjeta en hechos verificables y da variedad visual sin romper la sobriedad. **Solo con cifras reales y contrastadas** — es la misma línea roja de siempre. Si no hay dato que poner, la tarjeta va sin tira, no se rellena por rellenar.

## Qué evitar (para no parecer genérico o "hecho con IA sin criterio")

- Nada de iconos de banco de imágenes ni ilustraciones tipo clipart.
- Nada de emojis como elemento decorativo.
- Nada de sombras/degradados exagerados ni efectos 3D — la sobriedad es parte del mensaje de autoridad.
- Mucho espacio en blanco/negro — no llenar el lienzo por llenarlo.
- Una sola idea por imagen. Si hace falta explicar dos cosas, son dos imágenes (carrusel), no una imagen saturada.
