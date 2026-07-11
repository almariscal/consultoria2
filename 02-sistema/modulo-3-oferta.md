# Módulo 3 — Oferta

**Fase:** Sistema
**Estado:** 🟢 Cerrado (2026-07-10)
**Sale con:** tu propuesta empaquetada — transformación, entregables, formato, garantía, nombre y precio.

## Punto de partida (heredado del cierre de Módulos 1 y 2)

Problema: pyme sin equipo de datos/IT, decide a ojo por datos/procesos dispersos, no autoreconocido. Valor diferencial: diagnóstico agnóstico (comprar/construir/organizar) + rigor técnico real + acceso a alternativas que la pyme no conoce, frente a la inercia como competencia real.

Primera pregunta de esta sesión, ya anticipada: **formato de ejecución** — ¿Alberto solo, con ayuda subcontratada, o solo diagnóstico/diseño? Condiciona todo lo demás (cuántos clientes en paralelo, qué precio, qué garantía es razonable prometer).

Gap activo en paralelo (no bloqueante): conseguir un piloto real con una pyme antes de fijar precio en firme.

## Qué haremos aquí

- Decidir el **formato de entrega real**: ¿Alberto ejecuta él solo (sin equipo), ejecuta con ayuda puntual subcontratada, o vende diagnóstico/diseño y otro implementa? Esto es una decisión de negocio, no de marketing — condiciona cuántos clientes puede atender a la vez y qué precio tiene sentido.
- Definir 1–3 productos concretos (no un catálogo de servicios): con nombre propio, entregables cerrados, duración y precio.
- Pricing inicial en el contexto pyme español (no comparable al pricing del programa de Raúl, que vende a profesionales, no a empresas) — hay que investigar rangos reales de proyectos de datos/automatización para pyme en España.

## Formato de ejecución — decisión (2026-07-10)

**Equipo real disponible:**
- Alberto: punto único de contacto ante el cliente, analítica y programación con apoyo fuerte de IA (Claude Max).
- Data Architect (colaborador, disponibilidad parcial): arquitectura + **sí construye ETLs** — cubre el hueco que Alberto no domina (aunque Alberto podría defenderse con ayuda de Claude si hiciera falta).
- Data Scientist (colaborador, disponibilidad completa).
- ✅ Aclarado: "el chico de negocio" **no** es parte del equipo de Alberto — es de la consultoría itinerante del compañero data scientist (canal de referidos externo, ver `03-gtm/modulo-6-canal.md` cuando toque). Equipo real: solo Alberto + Data Architect + Data Scientist.

**Cómo se presenta al cliente:** ni "Alberto completamente solo" ni "equipo de 3-4 fijo desde el minuto uno" (esto último diluiría el diferencial de Módulo 2: "sin la estructura de una consultora grande"). Se presenta como **Alberto como único responsable del proyecto, con acceso a colaboradores especializados que se activan y facturan solo si el proyecto los necesita** — sin estructura fija, sin coste de plantilla en reposo. Resuelve la objeción real del cliente ("¿tienes recursos para esto?") sin sonar a consultora grande.

**Modelo de reparto (informal, a formalizar más adelante — no bloqueante ahora):** se estima el proyecto en horas de cara al cliente, y el reparto interno entre colaboradores se hace en función de las horas reales trabajadas por cada uno. No hay pacto de socios formal todavía.

**Capacidad:** no es un problema a resolver ahora — la prioridad es conseguir un primer proyecto, no diseñar para un volumen que aún no existe.

## Candidato de estructura de oferta (a validar)

Dado que el problema (Módulo 1) es "unknown unknown" — el cliente no sabe que lo tiene — un proyecto grande de entrada es difícil de vender en frío. Estructura candidata en dos escalones:

1. **Diagnóstico** (producto de entrada, precio y compromiso bajos, duración corta): Alberto audita procesos y datos de la pyme y entrega un informe con una recomendación concreta (comprar / construir / organizar), sin obligar a nada más. Es el producto que hace visible el problema — coherente con todo lo cerrado en Módulos 1 y 2.
2. **Implementación** (el proyecto real, una vez el cliente ya ve el problema): se ejecuta con estimación de horas y con el colaborador que corresponda según lo que haga falta (ETL → Data Architect, modelado → Data Scientist, analítica/coordinación → Alberto).

Estructura en dos escalones **confirmada por Alberto**.

## Pricing — tensión detectada y resuelta (2026-07-10)

Alberto propuso 3.000-8.000€ para el Diagnóstico, y en la misma sesión planteó como preocupación real "no sé cómo venderé el primer proyecto sin que parezca humo". **Ambas cosas son incompatibles tal cual**: cobrar varios miles de euros como primera venta, sin ningún caso real de pyme detrás (gap ya abierto desde el Módulo 2), es precisamente lo que generaría esa sensación de humo — nadie paga esa cifra a un desconocido sobre una promesa.

**Resolución — separar precio de arranque y precio estándar:**
- **1-2 clientes fundacionales**, buscados en red cercana y de confianza (no prospección en frío ni en LinkedIn), precio simbólico o gratuito, a cambio de libertad explícita para documentar el caso con cifras reales y conseguir un testimonio. Esto resuelve a la vez el gap de evidencia del Módulo 2 y el problema de credibilidad del arranque.
- **3.000-8.000€ como precio estándar del Diagnóstico**, aplicado ya con casos reales de respaldo. Este rango queda validado con un dato de mercado real (no solo intuición de Alberto): el programa público español **Kit Digital**, categoría "Business Intelligence y Analítica", subvenciona precisamente este tipo de servicio a pymes con importes de ~2.000€ a 9.000€ según tamaño de empresa — mismo rango. Fuente: [Business Intelligence y Analítica e IA asociada — Acelera Pyme](https://www.acelerapyme.gob.es/en/kit-digital/business-intelligence-y-analitica-e-ia-asociada).
- **Oportunidad anotada para más adelante (no decidida)**: registrarse como "agente digitalizador" permitiría a los clientes pagar con la subvención del Kit Digital en vez de con presupuesto propio — reduciría mucho la fricción de venta. Se retoma al cerrar precio/garantía en firme, o en el Módulo 6 (Canal).

## Tarifa interna de la Implementación — decisión (2026-07-10)

Alberto propuso 55€/hora. Señalado como infravaloración: no coherente con el precio ya anclado del Diagnóstico (3-8k€ por 1-2 semanas), con la evidencia ancla (evitar una decisión de 300-400k€ en el caso eloficash), ni con su perfil (reporta a C-level, ha montado una plataforma de datos completa desde cero). 55€/h es rango de freelance developer medio, no de este perfil.

**Cerrado: 90-120€/hora como cálculo interno**, usado para presupuestar y repartir entre colaboradores — nunca mostrado al cliente como tarifa/hora.

**Inconsistencia resuelta**: el Módulo 2 cerró "no vendo horas, vendo criterio". Enseñar una tarifa/hora al cliente contradice eso y abre la puerta a que regateen hora a hora. Por tanto: **de cara al cliente, la Implementación se presenta siempre como precio cerrado de proyecto**, calculado internamente a partir de las horas estimadas × 90-120€/h, nunca como una tarifa visible.

## Alcance de la Implementación — confirmado, no es ampliación nueva

Alberto preguntó si el alcance cubre también automatización de procesos/pipelines/tareas recurrentes, no solo analítica de datos. **Ya estaba incluido**: el problema cerrado en el Módulo 1 dice explícitamente "sin conectar **ni automatizar**", y la evidencia diferencial del Módulo 2 incluye automatización de tareas recurrentes (agentes de IA para scraping). Se deja explícito en los entregables para no dejarlo ambiguo.

## Paquete cerrado

### Escalón 1 — "Diagnóstico de Datos" (nombre de trabajo, se pule en el Módulo 4)
- **Qué es:** auditoría de cómo maneja hoy sus datos y procesos (herramientas usadas, cuellos de botella) + informe con recomendación concreta — comprar una herramienta existente, construir/automatizar algo a medida (incluye pipelines y tareas recurrentes, no solo analítica), o solo reorganizar lo que ya tiene — con estimación de la Implementación si decide seguir.
- **Duración:** 1-2 semanas.
- **Precio:** 1-2 clientes fundacionales a precio simbólico o gratuito (a cambio de caso documentado + testimonio real) → 3.000-8.000€ estándar después, con casos reales de respaldo.
- **Garantía:** si al final del diagnóstico no hay una recomendación clara y accionable, no se cobra.

### Escalón 2 — "Implementación" (nombre de trabajo)
- **Qué es:** ejecutar lo que salga del diagnóstico — comprar e integrar, construir/automatizar (incluye pipelines, integraciones, scraping, tareas recurrentes), o solo reorganizar — con el colaborador que corresponda (ETL/arquitectura → Data Architect, modelado → Data Scientist, resto → Alberto).
- **Duración y precio:** variable según alcance. Cálculo interno: horas estimadas × 90-120€/h. **De cara al cliente: precio cerrado de proyecto, nunca tarifa/hora visible.**
- **Garantía:** facturación y revisión por hitos — el cliente puede parar después de cualquier hito sin penalización ni contrato largo cerrado de entrada (contraste directo frente a consultoras grandes).

## Pendiente (no bloqueante, para más adelante)

- Conseguir el/los clientes fundacionales reales (tarea activa de Alberto, ver reglas en `CLAUDE.md`).
- Explorar registro como "agente digitalizador" para permitir pago vía Kit Digital.
- Pulir los nombres de cada escalón en el Módulo 4 (Mensaje).

Continúa en `02-sistema/modulo-4-mensaje.md`.
