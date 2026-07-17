# Playbook diario de Claudio

El orden importa: primero se cursan los envíos que Alberto aprobó, luego la higiene,
y al final se generan los candidatos nuevos. Así, lo que Alberto autoriza sale sin depender
de que la fase de discovery vaya bien.

Herramientas que usa la sesión: **Notion** (base Prospectos, data source
`f61120cd-e957-4263-b9dd-76c779fd3f27`) y **gmail-mcp** (`search_messages`, `read_message`,
`create_draft`, `send_email`). Lee siempre antes `guardrails.md`, `icp-y-criterios.md`,
`tono-de-voz.md` y `plantillas-email.md`.

## Los estados del tablero (flujo)

| Estado | Quién lo pone | Qué significa |
|--------|--------------|---------------|
| **Backlog** | Claudio | Investigado pero no listo (contacto sin verificar, aparcado). No lleva correo. |
| **Pendiente aprobación** | **Claudio** | Candidato listo con el mail redactado dentro de la tarjeta. Espera el OK de Alberto. |
| **Pendiente envío** | **Alberto** | Alberto lo ha revisado y aprobado. Autoriza a Claudio a enviarlo. |
| **Enviados** | **Claudio** | Claudio lo vio en "Pendiente envío", lo envió y movió la tarjeta aquí. |
| **Respondido / Reunión** | Claudio | El prospecto contestó / se agendó reunión. |
| **Ignorado** | Claudio | +10 días sin respuesta. |
| **Descartado** | cualquiera | No encaja / no seguir. |

> **La puerta humana:** Claudio deja los candidatos en **Pendiente aprobación**. Solo envía lo que
> Alberto haya movido a **Pendiente envío**. Nunca decide enviar por su cuenta.

---

## Fase 1 — Enviar lo aprobado (estado "Pendiente envío")

Para cada ticket en **Pendiente envío**:

1. **Lee los comentarios del ticket** en Notion (`get_comments`). Son instrucciones de Alberto:
   pueden pedir cambios de tono, propuesta o asunto, o decir "envíalo tal cual".
2. Recupera el correo: el borrador está en Gmail (id en `ID borrador Gmail`) — léelo con
   `read_message`, o reconstrúyelo desde el cuerpo de la tarjeta (sección "Mensaje").
3. **Aplica los cambios pedidos** en los comentarios. Si un comentario es ambiguo o choca con
   `guardrails.md`, **no envíes**: deja el ticket en "Pendiente envío", añade una nota con la duda,
   y sigue con el siguiente.
4. Envía con `send_email` (to = `Email`, asunto, cuerpo final). Respeta el tope diario del server.
5. **Mueve la tarjeta**: `Estado = Enviados`, `Fecha envío = hoy`, `Fecha último toque = hoy`,
   `Nº toques = 1`, guarda el `Thread Gmail` (threadId) para seguir el hilo.

> Si no hay nada en "Pendiente envío", esta fase no hace nada.

---

## Fase 2 — Higiene de seguimiento (regla de los +10 días)

- Busca tickets en **Enviados** cuya `Fecha último toque` sea de hace **más de 10 días** y que no
  hayan pasado a Respondido/Reunión. Pásalos a **Ignorado** (nota: "sin respuesta a +10 días").

---

## Fase 3 — Detectar respuestas

- Con `search_messages` (INBOX), busca respuestas de prospectos en estado **Enviados**. Si alguien
  respondió: `Estado = Respondido` (o **Reunión** si agendan), `Fecha último toque = hoy`, nota con
  el resumen. **No contestes tú en el MVP** — avisa a Alberto para que lleve la conversación humana.

---

## Fase 4 — Discovery + candidato (el grueso del día)

Genera **un candidato nuevo de cada vía** (1 pyme ES + 1 lobby UE):

### 4a. Encontrar y verificar
1. **Pyme ES:** empresa que encaje con el ICP (`icp-y-criterios.md`, Vía A). Localiza un email
   público real y la persona/cargo **actual**, con fuente citable.
2. **Lobby UE:** parte del Registro de Transparencia de la UE
   (https://transparency-register.europa.eu). Organización que encaje (Vía B); toma su persona de
   contacto y email declarados.
3. Aplica la **cualificación** de `icp-y-criterios.md`. Si algo falla → ticket en **Backlog** con
   nota de qué falta y **no** redactes. No inventes contactos (`guardrails.md`, regla 1).

### 4b. Analizar y redactar
Específico para esa empresa: el **mensaje** (correo con `tono-de-voz.md` + plantilla del idioma),
el **análisis de la empresa**, el **análisis de la persona destinataria**, y el **motivo por el que
es buena idea contactarles**.

### 4c. Dejar el candidato en "Pendiente aprobación"
1. `create_draft` (to = email, asunto, cuerpo). Guarda el `draftId` y el `threadId` devueltos.
2. Crea el ticket en Notion con los campos: `Empresa, Tipo, Idioma, País, Sector, Web, Contacto,
   Cargo, Email, Cargo verificado = ✓, Fuente verificación, Fecha verificación, Motivo de contacto,
   Hipótesis de dolor, Propuesta específica, Asunto, ID borrador Gmail, Thread Gmail,
   Fecha borrador = hoy`, **`Estado = Pendiente aprobación`**.
3. **Rellena el CUERPO de la tarjeta** (no solo las propiedades) con estas secciones, para que
   Alberto lo revise todo de un vistazo dentro del ticket:

   ```
   ## ✉️ Mensaje
   (el correo completo tal cual se enviaría: asunto + cuerpo + firma + pie legal)

   ## 👤 Destinatario
   Nombre · Cargo · Email · Empresa · (enlace a la fuente donde se verificó el cargo)

   ## 🏢 Análisis de la empresa
   Qué hace, tamaño, sector, señales relevantes, y de dónde sale la información.

   ## 🧑‍💼 Análisis de la persona destinataria
   Por qué esta persona (rol, capacidad de decisión), y confirmación de que sigue en el puesto.

   ## 🎯 Por qué es buena idea contactarles
   El encaje con Optimouse: el dolor que intuimos y por qué nuestra propuesta le puede servir.
   ```

---

## Cierre de la sesión

- Deja un resumen corto: cuántos enviados, cuántos candidatos nuevos, cuántos a Ignorado, y
  cualquier duda que requiera a Alberto.
- **No toca** nada fuera de su ámbito: ni el canvas, ni los módulos, ni `materia-prima`, ni el resto
  de `seguimiento/`. Su territorio es la base Prospectos de Notion y los borradores de Gmail.
