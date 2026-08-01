# Estrategia de contenido en LinkedIn — fase temprana

**Estado del mensaje de fondo:** el posicionamiento final (Módulo 4) todavía no existe. Esto NO es excusa para esperar — se puede y se debe publicar ya, con una regla clara:

> Mientras el Módulo 4 no cierre, cada post se apoya en **evidencia concreta** (un caso, un resultado, una decisión técnica real) — nunca en un pitch de venta ni en una promesa de posicionamiento que todavía no hemos definido por escrito.

## Decisión: perfil único, contenido de doble lectura (2026-07-09)

Alberto confirma: quiere buscar empleo activamente a partir de febrero 2027 (coincide con la fase "Entrevistas" de su wiki de carrera) y **no quiere que las publicaciones interfieran con eso**. Su propuesta: publicar en formato "autoridad" que sirva a la vez para reforzar la búsqueda de empleo (como experto) y para vender la consultoría, sin caer en un tono agresivo/vendehumos.

Esto es viable y **encaja exactamente con lo que ya cerramos en el Módulo 1**: el problema que vende Alberto es un "unknown unknown" — el cliente no sabe que el problema existe hasta que se lo enseñan. Eso obliga, de todas formas, a que el contenido sea educativo/evidencia (mostrar un caso, explicar un concepto, enseñar un antes/después), nunca un pitch de venta. Un reclutador que lee "así reduje el time-to-market de campañas a 2 días" lee una señal de competencia para un rol de Head of Data. Un dueño de pyme que lee el mismo post lee una prueba de que Alberto sabe resolver justo su problema. **Es el mismo post para las dos audiencias — no hacen falta dos tonos ni dos perfiles.**

Por tanto: **un único perfil de LinkedIn**, con esta regla de contenido:
- Todo post es caso/evidencia/concepto explicado — nunca "contrátame" ni "tengo plazas libres".
- Ninguna mención explícita de "consultoría", precios, ni disponibilidad — el CTA implícito es "así pienso yo", no una oferta comercial. Eso se activa formalmente en el Módulo 6 (funnel), y ahí es donde se revisa si hace falta algo más explícito (p.ej. un "contáctame" discreto en la bio, no en el post).
- La bio/titular del perfil sí puede (y probablemente debe) reflejar ambas cosas a la vez ("Data & Analytics Leader — construyo funciones de datos desde cero, y ayudo a pymes a hacer lo mismo a su escala"), porque ahí no hay ambigüedad de intención como sí la hay en un post activo de venta. Esto se termina de aterrizar en el Módulo 6, como hacía el programa original con el bonus de perfil/bio/titular.

**Riesgo a vigilar:** si en algún momento el volumen o el tono de los posts empieza a leerse como "está montando su propio negocio, ya no busca curro", se ajusta de inmediato — prioridad es no dañar la búsqueda de empleo desde ahora hasta que arranque en febrero 2027.

## Líneas de contenido posibles (borrador, pendiente de validar tras Módulo 1)

- **Caso real**: qué problema tenía [empresa/situación], qué hizo Alberto, qué cambió (usar `materia-prima/evidencia-experiencia.md`, traducido a lenguaje pyme, sin tecnicismos innecesarios).
- **Detrás del dato**: explicar en lenguaje llano un concepto (qué es un datalake, por qué "automatizar con Jira/Notion" no es magia, etc.) — construye autoridad sin vender directamente.
- **Diagnóstico en público**: compartir (de forma anónima/generalizada) el propio proceso de definir el problema/oferta de la consultora — meta, pero coherente con "esto no es teoría, lo estoy haciendo".
- **Actualidad comentada** (línea añadida el 2026-08-01, a petición de Alberto): coger una noticia real de tecnología/IA y traducirla a lo que significa para una pyme. Es la única línea que **no** se apoya en evidencia propia de Alberto, así que tiene reglas extra para no chocar con la regla de fondo del repo:
  - **Los hechos se verifican contra la fuente primaria** (el aviso de la empresa, la nota oficial, la transcripción), no contra titulares de medios. Los enlaces se dejan escritos en la cabecera del `post.md`.
  - **Lo que es hipótesis se etiqueta como hipótesis** dentro del propio post, no se cuela como hecho.
  - **Sin cifras no confirmadas**: si un precio o una cantidad es especulación de analistas, no entra (o entra dicho como lo que es).
  - **Alberto no se atribuye implicación en el caso**: comenta una noticia pública, no se pone como afectado ni como usuario de un producto que no sabemos que use.
  - **Caducan**: un post de actualidad vale para esa semana. Si se cae del calendario, se revisa o se tira — no se publica un mes después con datos viejos.
  - **La noticia es la excusa, no el tema**: el post tiene que aterrizar en algo que un dueño de pyme pueda hacer o decidir. Si no aterriza, no es un post nuestro, es un recorte de prensa.
  - **Mascado desde la primera línea** (regla de Alberto, 01/08): si la noticia viene de un mundo que el lector no pisa (cripto, infraestructura, seguridad), el post arranca con una **analogía cotidiana** y no usa ni una palabra técnica sin haberla explicado antes. Nada de dar por sabido qué es una cartera física, un modelo, un token o una API. Quien lee es un dueño de pyme, no alguien del sector.
  - **El puente tiene que ser verdad, no sonar bien** (misma sesión): al traducir una noticia a la realidad de una pyme, comprobar que el paralelismo se sostiene de verdad. Se descartó una versión que equiparaba un robo de criptomonedas con "a tu Excel no te mandan un aviso de seguridad": a una pyme no le van a robar el Excel, así que la analogía era falsa y hacía inverosímil el post entero. Lo transferible era el **silencio** (algo roto durante años sin dar un error), no la amenaza. Si el paralelismo solo funciona como frase, se tira.
  - **Una idea por post**: en un post de actualidad que ya tiene que explicar la noticia, no caben dos tesis. Lo que sobre se guarda como post propio.

## Cadencia

Publicación: martes, miércoles y jueves, a partir de septiembre 2026 (Módulo 6, `03-gtm/modulo-6-canal.md`).

**Hora recomendada: 8:00-9:00 (hora de Madrid).** Es cuando más se revisa LinkedIn antes de empezar el día — válido tanto para dueños de pyme como para reclutadores (la otra audiencia del mismo perfil). Es una recomendación estándar, no basada en datos propios todavía — se ajusta en cuanto haya unas semanas de métricas reales de Alberto.

**Semana de prueba (14-18 julio 2026):** solo martes y jueves, sin miércoles, para tener una primera muestra de datos antes de decidir si se amplía a los 3 días — ver resultados en `contenido-linkedin/calendario.md` (Inventario) y decisión la semana siguiente.

**Semana del 3 de agosto de 2026 — cuatro posts (aviso abierto).** Con los dos posts de actualidad encargados el 01/08, la semana queda en lunes, martes, miércoles y jueves. Es un salto de 2 a 4 publicaciones **sin tener todavía ni una sola métrica** de los dos ya publicados. Riesgos concretos: (1) se compite consigo mismo por el alcance, y con cuatro posts sin datos no se podrá saber qué funcionó; (2) el propio documento marca como riesgo que el volumen empiece a leerse como "está montando su negocio", justo lo que hay que evitar hasta febrero de 2027. **Recomendación de Raúl**: mover el post de departamentos (`posts/2026-07-16-herramientas-desconectadas/`, atemporal, no caduca) a la semana siguiente y dejar lunes-miércoles-jueves. Decisión de Alberto, pendiente — si decide mantener los cuatro, se mantiene y se anota el resultado.

## Fuente de material: búsqueda automática diaria (activa desde 2026-07-12)

Tarea programada (Routine) que corre todos los días a las 7:00 (hora de Madrid), en una sesión nueva cada vez: busca en blogs especializados, foros, X y medios de actualidad (español e inglés) 3-5 novedades de IA/datos, las traduce a lenguaje llano pensado para dueños de pyme, y las añade a `contenido-linkedin/fuentes/YYYY-MM.md`.

**Por qué está separado de este documento**: es material bruto de trabajo, no una decisión de estrategia — así no se mezcla con la documentación pensada (ver `contenido-linkedin/fuentes/README.md`). Cuando algo de ahí se convierte en un post real, se referencia desde `contenido-linkedin/calendario.md`.

Activada nada más cerrar el Módulo 6, para tener semanas de validación (julio-agosto) antes de depender de ella en el lanzamiento de septiembre — no para usar el material ya, sino para comprobar que lo que genera es realmente bueno.
