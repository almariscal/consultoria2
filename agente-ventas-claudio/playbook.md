# Playbook diario de Claudio

El orden importa: primero se cursan los envíos que Alberto aprobó ayer, luego la higiene,
y al final se generan los borradores nuevos. Así, lo que Alberto autoriza sale al día siguiente
sin depender de que la fase de discovery vaya bien.

Herramientas que usa la sesión: **Notion** (base Prospectos, data source
`f61120cd-e957-4263-b9dd-76c779fd3f27`) y **gmail-mcp** (`search_messages`, `read_message`,
`create_draft`, `send_email`). Lee siempre antes `guardrails.md`, `icp-y-criterios.md`,
`tono-de-voz.md` y `plantillas-email.md`.

---

## Fase 1 — Enviar lo aprobado (estado "Pendiente de envío")

Para cada ticket en **Pendiente de envío**:

1. **Lee los comentarios del ticket** en Notion (`get_comments`). Son instrucciones de Alberto:
   pueden pedir cambios de tono, de propuesta, de asunto, o decir "envíalo tal cual".
2. Recupera el correo: el borrador está en Gmail (id en `ID borrador Gmail`) — léelo con
   `read_message`, o reconstrúyelo desde los campos del ticket (`Asunto`, propuesta, etc.).
3. **Aplica los cambios pedidos** en los comentarios. Si un comentario es ambiguo o pide algo
   que choca con `guardrails.md`, **no envíes**: deja el ticket en "Pendiente de envío", añade
   una nota explicando la duda, y sigue con el siguiente.
4. Envía con `send_email` (to = `Email`, asunto, cuerpo final). Respeta el tope diario del server.
5. Actualiza el ticket: `Estado = Enviado`, `Fecha envío = hoy`, `Fecha último toque = hoy`,
   `Nº toques = 1`, guarda el `Thread Gmail` (threadId devuelto) para poder seguir el hilo.

> Si no hay nada en "Pendiente de envío" (lo normal al principio), esta fase no hace nada.

---

## Fase 2 — Higiene de seguimiento (regla de los +10 días)

- Busca tickets en **Enviado** cuya `Fecha último toque` sea de hace **más de 10 días** y que no
  hayan pasado a Respondido/Reunión. Pásalos a **Ignorado** (con nota "sin respuesta a +10 días").
- (Cuando se active el seguimiento en hilo, aquí iría el 2º toque antes de dar por ignorado. En el
  MVP no hay seguimiento automático: se marca Ignorado y punto.)

---

## Fase 3 — Detectar respuestas

- Con `search_messages` (INBOX, `newer_than_days` acorde a la última corrida), busca respuestas de
  prospectos con estado **Enviado**. Si alguien ha respondido:
  - `Estado = Respondido` (o **Reunión** si aceptan/agendan), `Fecha último toque = hoy`, nota con
    el resumen de la respuesta.
  - **No redactes tú la contestación en el MVP.** Avisa a Alberto (nota en el ticket) para que la
    conversación humana la lleve él. Claudio abre puertas; no negocia solo todavía.

---

## Fase 4 — Discovery + borrador (el grueso del día)

Genera **un prospecto nuevo de cada vía** (1 pyme ES + 1 lobby UE):

### 4a. Encontrar y verificar
1. **Pyme ES:** busca una empresa que encaje con el ICP (`icp-y-criterios.md`, Vía A). Localiza un
   email público real y la persona/cargo actual, con fuente citable.
2. **Lobby UE:** parte del Registro de Transparencia de la UE
   (https://transparency-register.europa.eu). Elige una organización que encaje (Vía B) y toma su
   persona de contacto y email declarados.
3. Aplica la **cualificación** de `icp-y-criterios.md`. Si algo falla → crea el ticket en **Backlog**
   con la nota de qué falta y **no** redactes. No inventes contactos (`guardrails.md`, regla 1).

### 4b. Analizar
Escribe, específico para esa empresa:
- **Motivo de contacto** — por qué esta empresa, en una o dos frases.
- **Hipótesis de dolor** — el pain concreto que intuimos.
- **Propuesta específica** — la mini-propuesta realista (sin cifras ni casos inventados).

### 4c. Redactar y dejar el borrador
1. Redacta el correo con `tono-de-voz.md` + la plantilla del idioma correcto. Personalízalo de verdad.
2. `create_draft` (to = email, asunto, cuerpo). Guarda el `draftId` y el `threadId` que devuelve.
3. Crea/actualiza el ticket en Notion con **todos** los campos:
   `Empresa, Tipo, Idioma, País, Sector, Web, Contacto, Cargo, Email, Cargo verificado = ✓,
   Fuente verificación, Fecha verificación, Motivo de contacto, Hipótesis de dolor,
   Propuesta específica, Asunto, ID borrador Gmail, Thread Gmail, Fecha borrador = hoy`,
   `Estado = Borrador creado`.

---

## Cierre de la sesión

- Deja un resumen corto de lo que ha hecho (cuántos enviados, cuántos borradores nuevos, cuántos
  a Ignorado, cualquier duda que requiera a Alberto).
- **No toca** nada fuera de su ámbito: ni el canvas, ni los módulos, ni `materia-prima`, ni el resto
  de `seguimiento/` — igual que la Routine de fuentes de contenido. Su territorio es la base
  Prospectos de Notion y los borradores de Gmail.

## Recordatorio de la puerta humana

Claudio **nunca** decide enviar. Solo pasa a "Enviado" lo que Alberto ha movido a "Pendiente de
envío". Todo lo demás se queda en borrador esperando revisión.
