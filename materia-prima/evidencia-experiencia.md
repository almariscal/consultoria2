# Materia prima — evidencia de experiencia (para posicionamiento de consultoría)

Extraído del CV y la wiki de carrera de Alberto. Reenfocado: aquí no importa lo que sirve para un CV de empleo, importa lo que sirve como **prueba de que puede resolver problemas de datos/automatización con recursos limitados** — que es exactamente la situación de una pyme.

⚠️ Nota de contexto importante: toda esta evidencia viene de una **gran empresa energética** (Endesa, niba/Iberdrola), no de pymes. Es un punto que el Módulo 1 (Problema) y el Módulo 2 (Solución) tienen que resolver explícitamente: ¿cómo se traduce "construí un datalake para una energética" en "confía en mí, pyme sin equipo de datos"? Probablemente la traducción no es el tamaño de la empresa sino la **condición de partida**: en los tres casos (Endesa, niba, y cualquier pyme) Alberto ha operado sin el equipo/recursos que el alcance del problema "debería" tener, y ha construido igualmente. Eso es lo vendible: no "he trabajado en grandes empresas", sino "sé construir con recursos de pyme, aunque lo haya hecho dentro de una grande".

## Logros con cifra o resultado demostrable

- **Datalake construido desde cero, sin equipo inicial**, en niba: de "cualquier dato tarda días" a "cualquier dato en segundos" (Redshift + Glue + Athena + S3). Empezó por iniciativa propia, sin que se lo pidieran.
- **Tiempo de entrega analítica: de días a 1 día de media**, mediante modelos de datos reutilizables y una capa de reporting centralizada (comercial, marketing, atención al cliente, cobros, regulatorio, KPIs ejecutivos).
- **Time-to-market de campañas de marketing: reducido a 2 días**, mediante automatización con AWS Lambda e integraciones basadas en eventos (Braze).
- **Segmentación y lifecycle de cliente diseñados desde cero** en Braze (perfil de hogar, comportamiento) — antes no existía nada de esto.
- **Presupuesto de infraestructura AWS de +20.000€/mes gestionado**, con ahorros de coste vía optimización de arquitectura.
- **Automatización Salesforce → Trustpilot**: contribuyó a subir la puntuación de la empresa de 4.4 a 4.6 — ejemplo directo y muy trasladable a pyme: "conecté dos sistemas y una métrica de negocio subió, sin intervención manual".
- **Sistema de web-scraping con 3 agentes de IA** (analista de negocio, tester, developer) con reporte diario automatizado de competencia — caso fuerte para hablar de automatización con IA aplicada a un proceso concreto (vigilancia competitiva), no "IA" en abstracto.
- **Herramienta de IA para procesar facturas de competidores** y estimar su nivel de precios — otro caso concreto de "documento no estructurado → dato explotable", un problema muy común en pymes (facturas, albaranes, contratos).
- **Automatización de reporting que antes era 100% manual en Excel** (etapa Endesa): extracciones SQL, scraping de competencia, rentabilidad cliente a cliente — el patrón "esto se hacía a mano y lo automaticé" es el más directamente vendible a una pyme.
- **Roadmap de datos construido y defendido ante dirección sin tener el mandato formal** (niba, 2025): identificó el vacío (no había función de datos) y consiguió recursos incrementales (Data Architect + Data Engineer) partiendo de cero.
- **Contratación y liderazgo de equipo técnico pequeño** (2 personas) — entrevistó y decidió personalmente, seguimiento semanal (dailies, sprints). Relevante para vender "puedo liderar/montar tu función de datos", no solo "puedo programar".

## Piezas que sirven para autoridad narrativa (no para venta directa a pyme, pero sí para credibilidad)

- Profesor de Machine Learning en ICAI y en el Máster de Audit & Business Analytics de ICADE (en colaboración con Deloitte) — comunicador técnico, no solo ejecutor.
- Perfil "bisagra" negocio-técnico: entiende pricing, márgenes, comisiones de canal, economía de adquisición de cliente — no es un perfil IT puro. Esto es diferencial frente a consultoras grandes que separan "los de negocio" de "los técnicos".

## Gaps a tener en cuenta al construir la oferta (Módulo 2/3)

- No es un data engineer de formación ni tiene certificación AWS formal — su valor es **criterio + liderazgo + capacidad de especificar y validar**, no picar código de infraestructura él mismo. Esto debe ser explícito en la oferta: ¿va a ejecutar él directamente para pymes (sin equipo detrás), o va a vender criterio/diseño y ejecutar con ayuda (subcontratar implementación puntual)? Esto cambia completamente el formato de la oferta del Módulo 3.
- Todos sus casos son de una industria concreta (energía retail) y de una sola empresa a la vez (nunca ha tenido varios clientes en paralelo). El Módulo 5 (Audiencia) tiene que decidir si eso es una limitación a ocultar o una historia a contar ("primera pyme como banco de pruebas").

## Casos internos con forma de "consultoría", aunque no fueran para una pyme

- **Caso eloficash (niba, departamento de deuda)**: pidieron un desarrollo a medida para gestionar deuda con proveedores (envío de ficheros, gestión de expedientes a juicio...). Alberto diagnosticó que la necesidad real era comprar un software ya existente (eloficash), no construir nada — la consultoría fue el diagnóstico y la recomendación correcta, ahorrando un desarrollo innecesario. Caso fuerte para Módulo 2: evidencia de que Alberto no vende desarrollo por defecto, vende la solución correcta aunque sea "cómprate esto". **Estimación de ahorro (propia de Alberto, no auditada, nadie puede certificarla por escrito): desarrollo evitado de ~300.000–400.000€ (consultores de datos + SAP) frente a la herramienta ya existente, de ~1.500€/mes.**
- **Automatización de vigilancia competitiva con webscraping** (ver logro de "3 agentes de IA" más arriba) — ejemplo de automatización de una búsqueda/proceso manual, no solo de integración de datos.

## Casos reales de pymes (a rellenar conforme aparezcan)

_(vacío por ahora — cada vez que Alberto haga un proyecto, un favor, o un piloto para una pyme real, se documenta aquí con el mismo formato: qué problema, qué hizo, qué cambió, con cifra si es posible.)_
