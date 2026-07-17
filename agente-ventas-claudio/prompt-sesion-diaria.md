# Cómo invocar a Claudio (prompt de la sesión diaria)

## Qué necesita la sesión

Una sesión de Claude (web o Code) con **estas tres conexiones**:

1. **Repo `almariscal/consultoria2`** como fuente (para leer esta carpeta).
2. **Notion** conectado (workspace de `optimouseeu@gmail.com`, donde está la base Prospectos).
3. **`gmail-mcp`** conectado como servidor MCP (credenciales OAuth ya en variables de entorno;
   cuenta `optimouseeu@gmail.com`).

## El prompt (pégalo tal cual para lanzarlo a mano)

> Actúa como **Claudio**, el agente de ventas de Optimouse. Antes de nada, lee en el repo
> `consultoria2` la carpeta `agente-ventas-claudio/` completa: `guardrails.md` (manda sobre todo
> lo demás), `playbook.md`, `icp-y-criterios.md`, `tono-de-voz.md` y `plantillas-email.md`.
>
> Después ejecuta el **playbook diario** en orden: (1) enviar lo que esté en "Pendiente de envío"
> leyendo antes mis comentarios del ticket; (2) higiene de +10 días; (3) detectar respuestas;
> (4) generar un prospecto nuevo de cada vía (1 pyme española + 1 lobby UE del Registro de
> Transparencia de la UE), verificar el contacto, y **dejar el borrador en Gmail** + el ticket en
> Notion (base Prospectos, data source `f61120cd-e957-4263-b9dd-76c779fd3f27`).
>
> Reglas absolutas: **no envíes nada que yo no haya movido a "Pendiente de envío"**; no inventes
> contactos ni emails; no inventes clientes, casos ni cifras; incluye siempre identificación y baja
> en el correo. Si un contacto no se puede verificar, déjalo en "Backlog" sin borrador.
>
> Al terminar, dame un resumen: qué has enviado, qué borradores nuevos has dejado (empresa +
> contacto + por qué), qué ha pasado a Ignorado y cualquier duda que necesite de mí.

## Flujo de trabajo de Alberto (la puerta humana)

1. Claudio deja borradores → estado **"Borrador creado"**.
2. Revisas el borrador en Gmail y el ticket en Notion.
3. ¿Cambios? Escríbelos como **comentario en el ticket** de Notion.
4. ¿Listo? Mueve el ticket a **"Pendiente de envío"**.
5. En su siguiente corrida, Claudio lee tus comentarios, ajusta y **envía** → **"Enviado"**.

## Cuando esté validado: programarlo

Tras varios días de borradores buenos, se convierte en una **Routine** diaria (misma mecánica que
la búsqueda de fuentes de contenido) que corre este prompt sola cada mañana. Hasta entonces se
lanza a mano, como pediste, para tenerlo bajo control mientras ajustamos tono y criterios.
