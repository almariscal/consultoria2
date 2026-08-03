# Calendario — backlog e inventario de publicaciones

Dos tablas: **Backlog** (borradores listos o en curso, sin publicar todavía) e **Inventario** (lo ya publicado, con resultado). Cuando algo pasa de un estado a otro, se mueve de tabla, no se duplica.

**Convención de carpetas:** cada post con imagen vive en su propia carpeta dentro de `posts/` (`posts/YYYY-MM-DD-tema/`), con el texto en `post.md` y las imágenes dentro de la misma carpeta — todo junto y versionado en git, nada suelto ni solo mandado por chat.

## Backlog (sin publicar)

| Estado | Título/Tema | Carpeta | Fecha prevista | Notas |
|---|---|---|---|---|
| Listo | Esa nunca fue tu comparación: código a mano vs. código con IA | `posts/2026-08-03-fallos-silenciosos/` | 2026-08-03 (lun) | **Actualidad comentada + opinión con criterio**. Primer post del perfil que defiende una tesis discutible en vez de divulgar. El fallo de Coldcard lo escribieron humanos expertos y estuvo cinco años sin verse: eso desmonta el "lo hecho a mano es más fiable". Giro clave: no es IA contra el mejor ingeniero, es IA contra lo que ibas a contratar con tu presupuesto real. Lleva límite honesto (dónde la IA no es mejor) y marco "la IA sube el mínimo", nunca "los desarrolladores sobran". **Seis versiones**, dos con especialistas en copywriting. ~2.650 caracteres. **Caduca**: revisar la cifra antes de publicar. Incluye `frase.png` (azul noche, bloque de comparación) |
| Listo | La IA no se ha encarecido: es que ahora vas a ver el contador (Siri de pago) | `posts/2026-08-05-ia-de-pago/` | 2026-08-05 (mié) | **Actualidad comentada** (línea nueva). Cook dijo el 30/07 que los usuarios intensivos de Siri irán a iCloud+ de pago; el post lo usa para decir que la fase de IA gratis se acaba y hay que tratarla como coste variable. Precios/fechas **no confirmados**: el post no da cifras. Cierra el arco DNI → APIs/MCP → factura. Incluye `frase.png` |
| Listo | Las mejores decisiones nacen de centralizar y relacionar los datos, no de analizar por separado | `posts/2026-07-16-herramientas-desconectadas/` | 2026-08-04 (mar) | **Replanificado**: no se publicó el 16/07; Alberto lo lleva a la semana del 3 de agosto. El nombre de la carpeta conserva la fecha original (no se renombra para no romper referencias). Reformulado dos veces tras feedback: (1) evitar sonar a queja de la empresa actual, (2) precisar que la visión estratégica sale de centralizar y relacionar datos entre departamentos, no solo de "conectar" |
| Listo | Cada vez más clientes van a querer sus datos fuera, y las empresas tendrán que adaptarse (APIs y MCPs) | `posts/2026-08-06-apis-y-mcps/` | 2026-08-06 (jue) | Caso/evidencia real: `almariscal/seguimiento_economico` (herramienta propia para unificar inversiones). Segunda parte del post del DNI: si cualquiera se construye su herramienta con IA, la demanda de sacar los datos crece y quien los guarda tendrá que permitir cada vez más extracción. Contrapunto verificado: Revolut abrió Revolut X a asistentes de IA vía MCP (anuncio 10/07/2026). **Sin enlace** (repo privado) y **sin detalle de las plataformas** que usa Alberto. Incluye `frase.png` (tarjeta-cita) |
| Idea sin desarrollar | Herramientas gratis/baratas de IA para automatizar tareas en una pyme (n8n, Zapier free, Claude/ChatGPT, Canva IA) | — | — | Salido de una búsqueda real de prueba (2026-07-12) — pendiente de convertir en post |

## Inventario (publicado)

| Fecha real | Título/Tema | Archivo | Impresiones | Reacciones | Comentarios | Mensajes de leads/reclutadores | Notas |
|---|---|---|---|---|---|---|---|
| 2026-07-14 (aprox.) | ¿Qué es un datalake? | `posts/2026-07-14-datalake/` | — | — | — | — | Publicado (Alberto lo confirma el 30/07). Día exacto y métricas pendientes de reportar |
| 2026-07-23 (aprox.) | Me construí mi propia herramienta (marca de agua para el DNI) en vez de pagar por software | `posts/2026-07-23-crea-tus-herramientas/` | — | — | — | — | Publicado (Alberto lo confirma el 30/07). Día exacto y métricas pendientes de reportar |

_(Las métricas las reporta Alberto cuando las tenga — LinkedIn no da acceso automático. Igual que en `seguimiento/prospectos.md`, se cuenta en la conversación y se registra aquí.)_
