# Registro de sesiones

Estado vivo del proceso. Se actualiza cada vez que trabajamos, aunque sea de forma asíncrona.

## Estado por módulo

| Módulo | Estado |
|---|---|
| 1. Problema | 🟢 Cerrado |
| 2. Solución | 🟢 Cerrado |
| 3. Oferta | 🟢 Cerrado |
| 4. Mensaje | 🟡 Próximo a abrir |
| 5. Audiencia | ⚪ No iniciado |
| 6. Canal | ⚪ No iniciado |

## Preguntas abiertas activas (no cerradas)

1. Conseguir un caso piloto real con una pyme, buscándolo activamente en la red (excompañeros, amigos, la consultoría itinerante del compañero data scientist, asociaciones/cámaras de comercio) — Alberto no tiene contacto directo hoy, pero la vía es pedirlo, no fabricarlo. Ver regla en `CLAUDE.md`.
2. Pulir los nombres de trabajo de cada escalón ("Diagnóstico de Datos" / "Implementación") — tarea del Módulo 4.
3. Explorar registro como "agente digitalizador" (pago vía Kit Digital) — no bloqueante, más adelante.

## Decisiones ya cerradas

- **Vertical vs. horizontal (Módulo 1):** horizontal, forzado por incompatibilidad real de Alberto con el sector energía/utilities. Vertical descartado, no por preferencia sino por restricción.
- **Problema (Módulo 1), cerrado**: pyme familiar sin equipo de datos/IT, presupuesto acotado, decide a ojo porque tiene datos y procesos dispersos sin conectar/automatizar, y no sabe si necesita comprar algo, que le construyan algo, o que le organicen lo que ya tiene. No autoreconocido — problema tipo "unknown unknown", GTM tiene que ser contenido de autoridad, no intención de búsqueda.
- **Solución/valor diferencial (Módulo 2), cerrado**: el "enemigo" real es la inercia (caos disperso, no la competencia), no las consultoras/becarios/SaaS. Alberto gana enseñando alternativas que la pyme no conoce (framing de acceso a conocimiento, no de prescripción de compra), decidiendo con criterio agnóstico comprar/construir/organizar, y ejecutando con rigor técnico real. Frase-gancho de venta pulida se aplaza al Módulo 4, apoyada en la Oferta del Módulo 3.
- **LinkedIn — perfil único**, contenido siempre en formato caso/evidencia (nunca pitch de venta), sirve a la vez a la búsqueda de empleo (activa desde feb 2027) y a la consultoría. Ver `contenido-linkedin/estrategia-contenido.md`.
- **Formato de ejecución (Módulo 3):** Alberto único punto de contacto, colaboradores (Data Architect parcial, Data Scientist completa) se activan y facturan solo si el proyecto lo requiere. Sin estructura fija.
- **Estructura de oferta (Módulo 3):** dos escalones — Diagnóstico (entrada, bajo riesgo) → Implementación (proyecto real por horas).
- **Pricing del Diagnóstico (Módulo 3):** 1-2 clientes fundacionales gratis/precio simbólico a cambio de caso documentado + testimonio real, luego 3.000-8.000€ estándar — rango validado con el programa público Kit Digital (categoría BI y Analítica, subvenciona ~2.000-9.000€ según tamaño de pyme).
- **Regla no negociable (2026-07-10):** nunca se fabrican casos, cifras o testimonios falsos, aunque nadie los vaya a comprobar — riesgo legal (publicidad engañosa) y reputacional real, agravado por la búsqueda de empleo paralela de Alberto. Añadido a `CLAUDE.md`.
- **Oferta (Módulo 3), cerrada**: dos escalones. "Diagnóstico de Datos" (1-2 semanas, fundacionales gratis/simbólico → 3-8k€ estándar, garantía "no se cobra si no hay recomendación clara") → "Implementación" (comprar/construir-automatizar/organizar, precio cerrado de proyecto calculado a 90-120€/h interno, nunca tarifa visible al cliente; facturación por hitos sin contrato largo). Alcance confirmado: incluye automatización de procesos/pipelines/tareas recurrentes, no solo analítica — ya estaba dentro del problema/solución cerrados, no es ampliación nueva.

## Bitácora

### 2026-07-09 — Kickoff
- Repo creado y configurado como workspace del proyecto.
- Se adaptó la estructura del protocolo de 6 módulos (sin reproducir el copy comercial original).
- Se extrajo evidencia de CV/wiki a `materia-prima/evidencia-experiencia.md`.
- Módulo 1 (Problema) abierto: se identificaron 3 candidatos de problema y se lanzaron 5 preguntas de diagnóstico a Alberto.
- Se señaló la tensión LinkedIn (búsqueda de empleo activa vs. arranque de consultoría) como decisión pendiente antes de publicar contenido.

### 2026-07-09 — Cierre Módulo 1 (propuesto) + decisión LinkedIn
- Alberto respondió las 5 preguntas de diagnóstico. Vertical energía descartado por incompatibilidad real (no preferencia) → foco horizontal confirmado.
- Síntesis: el problema tiene dos capas (síntoma en el cliente = decide a ojo / causa estructural = datos y herramientas dispersas sin conectar) y es un problema de tipo "unknown unknown" — el cliente no lo busca activamente porque no sabe que existe. Esto fija una restricción de diseño para todo el GTM posterior: no vale marketing de intención de búsqueda, tiene que ser contenido de autoridad/exposición.
- Cierre del Módulo 1 redactado en `01-diagnostico/modulo-1-problema.md`, pendiente de confirmación final de Alberto antes de abrir el Módulo 2.
- LinkedIn: decidido perfil único (no separar identidad de búsqueda de empleo y de consultoría) con contenido siempre en formato caso/evidencia, nunca venta directa — sirve a ambas audiencias sin conflicto.
- Alberto matiza con dos casos (eloficash: diagnóstico → recomendar comprar software en vez de construir; automatización de búsquedas/webscraping) antes de cerrar. Se incorporan como precisión del "qué duele" (capa C amplia a "comprar / construir / organizar") y como evidencia en `materia-prima/evidencia-experiencia.md`, sin reabrir el problema a una lista de servicios.
- **Módulo 1 cerrado formalmente.** Módulo 2 (Solución) abierto — próxima sesión.

### 2026-07-10 — Cierre Módulo 2 (Solución)
- Mapeadas las 5 alternativas reales de una pyme; Alberto confirma que la alternativa real dominante es la inercia (no hacer nada), no la competencia entre proveedores — refuerza el hallazgo "unknown unknown" del Módulo 1.
- Cifra fuerte conseguida (estimación propia, no auditada): caso eloficash evitó un desarrollo de ~300-400k€ frente a una herramienta de ~1.500€/mes.
- Gap detectado: no existe ningún caso con recursos reales de pyme — queda como tarea prioritaria en paralelo, no bloqueante.
- Se descartó "reportar a C-level" como argumento de autoridad, y se reformuló "te digo qué comprar" (prescriptor, genera barrera) por "te enseño lo que usan las grandes empresas" (acceso a conocimiento).
- Alberto pidió una versión de gancho de funnel/curiosidad; se rechazó explícitamente hacerlo en este módulo por ser trabajo del Módulo 4 y necesitar la Oferta (Módulo 3) detrás para no sonar a "vendehumos". Queda anotado como pendiente del Módulo 4.
- **Módulo 2 cerrado.** Próxima sesión: abrir Módulo 3 (Oferta), empezando por decidir el formato de ejecución (Alberto solo / con ayuda subcontratada / solo diagnóstico).

### 2026-07-10 — Módulo 3 (Oferta) en curso
- Formato de ejecución cerrado: Alberto + Data Architect (parcial, cubre ETLs) + Data Scientist (completa). Se aclaró que "el chico de negocio" es de la consultoría itinerante externa, no del equipo.
- Estructura de oferta en dos escalones (Diagnóstico → Implementación) confirmada por Alberto.
- Tensión detectada entre el precio propuesto (3-8k€) y la preocupación de Alberto de "parecer humo" en la primera venta: resuelta separando clientes fundacionales (gratis/simbólico, a cambio de caso real) del precio estándar (3-8k€, validado con datos de Kit Digital).
- Alberto propuso fabricar referencias de pymes inventadas al no tener contacto directo con ninguna real. **Rechazado explícitamente** — riesgo legal y reputacional, y contradice toda la disciplina de evidencia del proyecto. Se ofrecieron vías reales para conseguir un piloto (red cercana, consultoría itinerante del compañero, asociaciones/cámaras de comercio). Regla añadida a `CLAUDE.md` para que ninguna sesión futura lo plantee como opción.
- Pendiente para cerrar Módulo 3: nombres de cada escalón, entregables/duración, precio de Implementación, garantía.
- Cerrada la tarifa interna (90-120€/h, tras señalar que 55€/h infravaloraba el perfil) y resuelta la inconsistencia con el Módulo 2: la Implementación se presenta al cliente como precio cerrado de proyecto, nunca como tarifa/hora. Confirmado que el alcance ya incluía automatización de procesos/pipelines/tareas recurrentes.
- **Módulo 3 cerrado.** Canvas actualizado con la Oferta completa. Próxima sesión: abrir Módulo 4 (Mensaje) — frase de posicionamiento + narrativa de autoridad, recogiendo los pendientes ya anotados (no usar "reporté a C-level", framing de "acceso a conocimiento", vigilar exceso de detalle técnico, pulir nombres de los escalones).
