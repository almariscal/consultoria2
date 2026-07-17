# Claudio — Agente de Ventas de Optimouse

Claudio es un agente autónomo que cada día investiga empresas, verifica un contacto
público, y deja un candidato en **"Pendiente aprobación"** con el correo redactado dentro de la
tarjeta. **No envía nada por su cuenta.** Un correo solo sale cuando Alberto lo revisa y mueve el
ticket a **"Pendiente envío"**; entonces Claudio lo envía y lo pasa a **"Enviados"**.

Firma como **"Claudio – Agente de Ventas"** (correos en español) y
**"Claudio – Agentic Sales Representative"** (correos en inglés).

> Esta carpeta es el **cerebro** de Claudio (proceso, tono, criterios, guardarraíles).
> Es la fuente de verdad del sistema, igual que el resto de `consultoria2`.

## Arquitectura (tres capas, ningún repo nuevo)

| Capa | Dónde vive | Qué es |
|------|-----------|--------|
| **Cerebro** | `consultoria2/agente-ventas-claudio/` (este directorio, privado) | Playbook, tono, ICP, guardarraíles, plantillas y el prompt de la sesión diaria. |
| **Manos** | `almariscal/mcp-servers` → `gmail-mcp` (público) | Servidor MCP que lee, redacta borradores y envía correo con la API de Gmail. Cuenta `optimouseeu@gmail.com`. |
| **CRM / tablero** | Notion → página **"Optimouse — Ventas (Claudio)"** → base **Prospectos** | El backlog y el seguimiento de estados. |
| **Orquestación** | Una sesión diaria de Claude (manual ahora, programada después) | Corre el playbook de principio a fin. |

**Por qué no hay repo nuevo:** el único código real (el servidor de email) ya vive en
`mcp-servers`; Notion es el CRM; y todo lo demás es documentación + un prompt. Un repo
aparte solo fragmentaría la fuente de verdad que queremos mantener aquí.

## Enlaces de referencia

- **Tablero Notion (Prospectos):** https://app.notion.com/p/0158e22748a342a2b930c412600e94e1
- **Página raíz Notion:** https://app.notion.com/p/3a08161dfd4a81a3b472f305219ff187
- **Data source id (para queries):** `f61120cd-e957-4263-b9dd-76c779fd3f27`
- **Web:** https://optimouse.eu · **Calendario de reuniones:** https://calendar.app.google/JsAp8YLcphyeCLzh8
- **Cuenta de envío:** `optimouseeu@gmail.com` · **Contacto público de la web:** `optimouse@proton.me`

## Los documentos

| Archivo | Para qué |
|---------|----------|
| `playbook.md` | El proceso diario paso a paso (las 4 fases). |
| `tono-de-voz.md` | La voz de Claudio y la estructura de cada correo. |
| `icp-y-criterios.md` | A quién sí y a quién no (las dos vías: pymes ES y lobbys UE). |
| `guardrails.md` | Reglas no negociables: verificación, no fabricar, GDPR, volumen. |
| `plantillas-email.md` | Esqueletos ES/EN con firma y pie legal. |
| `prompt-sesion-diaria.md` | El prompt exacto que corre la sesión diaria. |

## Estado

- **Fase actual: MVP — solo borradores.** Claudio investiga y redacta; deja el candidato en
  **"Pendiente aprobación"** con el mail dentro de la tarjeta. El envío es 100% manual (Alberto mueve
  a "Pendiente envío"). Volumen objetivo: **1 pyme española + 1 lobby UE al día**.
- **Flujo del tablero:** Backlog → **Pendiente aprobación** (Claudio) → **Pendiente envío** (Alberto
  aprueba) → **Enviados** (Claudio envía y mueve) → Respondido / Reunión / Ignorado (+10 días).
- **Cómo se invoca:** ver `prompt-sesion-diaria.md`. De momento se lanza a mano en una sesión
  con las conexiones (repo `consultoria2` + Notion + `gmail-mcp`); cuando validemos varios días,
  se convierte en una Routine programada.

## Acciones pendientes de Alberto

1. **Cambiar `GMAIL_FROM_NAME`** (variable de entorno del `gmail-mcp`): hoy es *"Alberto Mariscal"*,
   debe ser algo como **"Claudio (Optimouse)"** para no romper la marca ni la firma.
2. Conectar el `gmail-mcp` como servidor MCP en la sesión donde se lance a Claudio (las
   credenciales OAuth ya están como variables de entorno).
