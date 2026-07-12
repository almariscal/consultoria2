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

## Motor de generación (decidido 2026-07-12)

**HTML/CSS renderizado con Chromium headless (Playwright), capturado a PNG.** Es gratuito y ya integrado en el flujo de trabajo. Se probó generación vía API de Google (Nano Banana / Nano Banana Pro / Nano Banana 2 / Imagen 4) y **se descartó**: todos esos modelos tienen cuota gratuita de 0 peticiones — requieren facturación activada en Google Cloud, con coste real por imagen. Mermaid se integra con el mismo mecanismo (se carga la librería vía CDN dentro del HTML y se captura igual), así que no hace falta una herramienta nueva.

## Qué evitar (para no parecer genérico o "hecho con IA sin criterio")

- Nada de iconos de banco de imágenes ni ilustraciones tipo clipart.
- Nada de emojis como elemento decorativo.
- Nada de sombras/degradados exagerados ni efectos 3D — la sobriedad es parte del mensaje de autoridad.
- Mucho espacio en blanco/negro — no llenar el lienzo por llenarlo.
- Una sola idea por imagen. Si hace falta explicar dos cosas, son dos imágenes (carrusel), no una imagen saturada.
