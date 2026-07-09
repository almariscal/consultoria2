# Módulo 1 — Problema

**Fase:** Diagnóstico
**Estado:** 🟢 Cerrado (2026-07-09)
**Sale con:** un problema elegido — qué duele, a quién, cómo se reconoce, qué cuesta no resolverlo.

---

## Punto de partida (lo que Alberto trajo)

Del mensaje inicial de Alberto: "automatizar procesos a partir de un jira/notion, ingestar datos en un datalake, analítica... estratégico dentro pero no a nivel estrategia de empresa".

Esto es una **lista de capacidades**, no un problema elegido. Es exactamente el patrón que este módulo existe para romper: cuando alguien puede hacer muchas cosas, la tentación es venderlas todas ("hago datos, automatizaciones, analítica..."), y el resultado es que nadie tiene claro qué comprarle. Antes de seguir, hay que aislar **un** problema.

## Lo que sabemos por la evidencia (ver `materia-prima/evidencia-experiencia.md`)

El patrón que se repite en toda la carrera de Alberto no es "sabe de datos" en abstracto. Es más concreto:

> Entra en organizaciones donde el dato vive disperso, en manual o en la cabeza de alguien, sin que nadie tenga el mandato ni el tiempo de arreglarlo — y construye, sin equipo grande, la infraestructura y automatización que lo soluciona, mostrando resultado rápido (días → segundos, manual → automático).

Eso apunta a un problema candidato:

> **Candidato A**: "La pyme opera con datos y procesos dispersos entre herramientas (Jira, Notion, Excel, CRM...) que nadie tiene tiempo ni perfil para conectar y explotar — y lo delega en gente cara (consultoras grandes) o en nada (se queda sin hacer)."

Pero hay al menos dos formas más de recortar esto, y elegir entre ellas es el trabajo real del módulo:

> **Candidato B** (vertical): "Pymes del sector energía/utilities que necesitan pricing y analítica de cliente pero no pueden montar el equipo que eso requiere" — aprovecha al máximo la profundidad de experiencia real de Alberto (pricing, márgenes, coberturas), pero reduce mucho el mercado direccionable si el objetivo es "pymes en general".

> **Candidato C** (por función/dolor, no por herramienta): "El fundador/gerente de la pyme toma decisiones a ojo porque no confía en sus datos, y no sabe si el problema es 'necesito un dashboard' o 'necesito un ingeniero' — y no puede permitirse averiguarlo con una consultora grande." Este es más amplio que A y no depende de qué herramienta usa la pyme.

No cerramos esto todavía. Se cierra con las respuestas de Alberto abajo.

## Preguntas abiertas para Alberto (responder para poder cerrar el módulo)

1. **¿A quién has ayudado ya, aunque no fuera formalmente "consultoría"?** (un amigo con su negocio, un conocido, algo dentro de niba que no estaba en tu rol...) — necesitamos un caso real de pyme, aunque sea pequeño, no solo tu experiencia en Endesa/niba.
2. De los tres candidatos de arriba (A: integración de herramientas dispersas / B: vertical energía / C: "no confío en mis datos"), **¿cuál te reconoces diciendo en voz alta a un desconocido en una comida?** Si dudas entre dos, dilo — es información.
3. **¿Qué le cuesta a una pyme *no* resolver este problema?** ¿Tiempo, dinero, decisiones malas, oportunidades perdidas? Necesitamos algo concreto, no "ineficiencia".
4. **¿Cómo se reconoce el problema desde fuera, antes de hablar contigo?** Es decir: ¿qué ve/dice/hace un gerente de pyme que tiene este problema, que tú reconocerías al instante?
5. **¿Prefieres arrancar con foco horizontal (cualquier pyme con este dolor) o vertical (un sector donde ya tienes autoridad real, como energía)?** — ligado a la tensión que ya está anotada en `materia-prima/evidencia-experiencia.md`.

## Respuestas de Alberto (2026-07-09)

1. No ha ayudado todavía a ninguna pyme formalmente. Dentro de niba ha dado servicio de facto a *todos* los departamentos (negocio/producto vía reporting, marketing vía Braze/marketing automation, deuda vía gestión y reporting, ventas y gestión de la energía) — es decir, su patrón real no es "especialista de un departamento", es "el que conecta y explota datos para cualquier área que lo necesite".
2. Se reconoce en **A** (integrar herramientas dispersas y convertirlas en datos explotables) y en **C** ("no confío en mis datos, no sé si necesito un dashboard o un ingeniero"). Explícitamente descarta **B**: no puede dirigirse a empresas de energía por incompatibilidad (cláusula/conflicto con su empleo actual). Esto **cierra la tensión vertical vs. horizontal**: la opción vertical queda descartada por una restricción real, no por preferencia. Foco horizontal, fuera de energía/utilities.
3. El coste de no resolverlo no es que "duela" de forma reconocible: es que la pyme **ni siquiera sabe que el problema es resoluble**. Pymes familiares, presupuesto acotado, que necesitan optimizar pero desconocen que existe una solución a su alcance.
4. No hay una señal externa auto-reconocible ("no lo sé, tienen que conocerme"). Confirma el punto 3: esto no es un dolor que el cliente busca activamente (no va a googlear la solución) — es un problema invisible hasta que alguien se lo muestra.
5. Horizontal, forzado por la incompatibilidad con energía (ver punto 2).

## Precisión de última hora (2026-07-09, antes de cerrar)

Alberto añade dos matices con ejemplos concretos — **no cambian el problema, lo afinan**:

- **Caso eloficash**: unos compañeros de deuda pidieron un desarrollo a medida para gestionar deuda con proveedores (envío de ficheros, gestión de a quién se lleva a juicio...). Alberto identificó que lo que de verdad necesitaban era comprar eloficash (software ya existente) — la consultoría, en ese caso, fue el diagnóstico y la recomendación, no construir nada. Esto confirma y **amplía la capa C**: la incertidumbre del cliente no es solo "¿dashboard o ingeniero?", es más ampliamente "¿necesito comprar algo que ya existe, que me construyan algo a medida, o que me organicen lo que ya tengo?".
- **Automatización de procesos y búsquedas (p.ej. webscraping)**, además de la parte de datalake/explotación de datos — esto ya estaba cubierto por la causa estructural (capa A: procesos manuales/dispersos sin nadie que los automatice), se deja explícito para no perderlo.

Importante — esto es **material para el Módulo 2 (Solución)**, no un cambio del problema: el hecho de que la respuesta correcta a veces sea "compra esto" y no "te lo construyo yo" es precisamente lo que puede convertirse en diferencial (un consultor agnóstico, sin incentivo a vender desarrollo si no hace falta) — pero eso se decide y se redacta en el Módulo 2, no aquí. Si esto se coló en el problema, volveríamos al punto de partida: "hago de todo".

## Síntesis — qué significa esto de verdad

Dos cosas importantes que salen de aquí y que no estaban en los candidatos iniciales:

- **A y C no son alternativas, son las dos caras del mismo problema**: C es el problema tal y como lo vive el cliente (incertidumbre, decisiones a ojo, no sabe qué necesita), A es la causa estructural que lo produce (datos y procesos dispersos entre herramientas sueltas, sin nadie con el perfil o el tiempo para conectarlos). No hay que elegir entre las dos — el problema completo necesita ambas capas.
- **Esto NO es un problema de dolor reconocido, es un problema de "unknown unknown".** El cliente no tiene el síntoma que le empuje a buscar solución por su cuenta (a diferencia de "se me cae el pelo" → busca clínica capilar). Esto tiene una consecuencia directa e ineludible para todo lo que viene después: **el marketing de esta consultora no puede apoyarse en intención de búsqueda (SEO, anuncios "solución a X")** — tiene que ser un canal de autoridad/exposición que **enseñe al cliente que el problema existe**, antes de venderle nada. Esto confirma (y ahora justifica con datos, no por defecto) que LinkedIn con contenido educativo/autoridad es el canal correcto, no una elección de conveniencia.

## Problema elegido (cierre propuesto)

> **A quién duele:** al dueño/gerente de una pyme de gestión familiar, con presupuesto acotado, sin equipo de datos ni IT dedicado, de cualquier sector excepto energía/utilities.
>
> **Qué duele:** toma decisiones a ojo porque sus datos y procesos operativos viven dispersos en herramientas sueltas (hojas de cálculo, Notion, Jira, lo que use cada área) sin conectar ni automatizar — y no tiene forma de saber si lo que necesita es comprar una herramienta que ya existe, un desarrollo/automatización a medida, o simplemente que le organicen lo que ya tiene.
>
> **Cómo se reconoce:** no se autoreconoce. No hay síntoma que el gerente busque activamente — el problema es invisible hasta que alguien se lo muestra desde fuera (contenido, autoridad, recomendación directa). Esto es una restricción de diseño para todo el go-to-market, no un detalle menor.
>
> **Qué cuesta no resolverlo:** presupuesto que podría optimizarse y no se optimiza, decisiones tomadas sin datos o tarde, tiempo de alguien de confianza cruzando información a mano. *(Cualitativo por ahora — pendiente de cuantificar con un caso piloto real; ver tarea abierta en `materia-prima/evidencia-experiencia.md`.)*

**Confirmado por Alberto — módulo cerrado.** Continúa en `01-diagnostico/modulo-2-solucion.md`.
