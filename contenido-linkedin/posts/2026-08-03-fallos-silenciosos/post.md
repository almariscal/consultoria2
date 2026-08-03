# Post — ¿Habrían hackeado Coldcard si el código lo hubiera escrito una IA?

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada + opinión con criterio**. Primer post del perfil que defiende una tesis discutible en vez de explicar un concepto. El caso Coldcard es la prueba, no el tema.
**Imágenes:** `frase.png` — fondo claro y deliberadamente **sobrio**. La pregunta de Alberto como titular, una bajada con el hecho, y los datos en letra pequeña abajo. Sin cifras gigantes ni bloques de comparación: la imagen **pregunta**, el post argumenta.
**Longitud:** ~2.050 caracteres (venía de 2.650).

## Séptima versión (2026-08-02) — tres cosas de Alberto, y una de ellas es una pregunta de fondo

### 1. La infografía era rimbombante
La versión anterior tenía titular gigante con la cifra, acentos azules y un bloque de comparación "la comparación que todos hacen / la comparación real". Demasiado énfasis para un post que defiende una idea discutible: **el hype en la imagen le quita autoridad al argumento**. Alberto propone directamente el titular, y es mejor que lo que había: *"¿Habrían hackeado Coldcard si lo hubiera desarrollado una IA?"*. Funciona porque es **honestamente una pregunta abierta** — nadie sabe la respuesta — así que invita a discutir en vez de sentar cátedra. La tarjeta se queda casi vacía a propósito.

### 2. Demasiado largo, y más para dummies
Recortado de 2.650 a ~2.050. Fuera: la mención a la herramienta del DNI (desvío), la hipótesis de NVK sobre la revisión de código con IA (es un matiz de un matiz y confundía), y la explicación larga del funcionamiento del aparato, que ahora ocupa tres frases.

### 3. "Es el típico post de frases cortas muy de IA/LinkedIn, ¿esto es así por algo?"
**Pregunta buena, y la respuesta es: en parte sí, pero se ha pasado de rosca — y en este perfil nos estaba haciendo daño.**

- **La razón real que hay detrás**: LinkedIn se lee en el móvil, en un feed, con una mano. Los saltos de línea dan descanso visual y mejoran que la gente llegue al final. Eso es cierto.
- **El problema**: se ha usado tanto que ha dejado de ser una técnica y se ha convertido en una **firma**. Hoy el staccato de una frase por párrafo es exactamente lo que identifica a (a) contenido generado por IA y (b) contenido de gurú de LinkedIn. Lo que servía para leer mejor ahora señala "esto es fabricado". Es justo lo que Alberto venía detectando desde la tercera versión cuando decía "suena artificial".
- **Y encima choca con lo que él pide**: el staccato **elimina los conectores** ("porque", "pero", "así que", "si… entonces"), que son precisamente lo que hace fácil de seguir un texto para alguien que no es del sector. O sea que troceado no es más para dummies: es más difícil de seguir, porque el lector tiene que reconstruir él solo la relación entre frases.
- **La solución adoptada**: párrafos normales de 2-4 líneas con conectores, y el salto de línea **reservado para los dos o tres momentos que de verdad pesan**. Una frase corta solo golpea si contrasta con las largas; si todo es corto, no destaca nada. Esto resuelve el punto 2 y el 3 con el mismo cambio.
- **Queda como regla de estilo del perfil** (llevado también a `estrategia-contenido.md`).

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras COLDCARD no era lo bastante aleatorio al crear la semilla (~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 de una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3).
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: 30 de julio, 01:10–01:51 UTC (41 minutos).
- **Cifra**: se movió de ~594 BTC (~38 M$) a [~1.158 BTC (~75 M$) según Galaxy Research](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **Se usa "unos 70 millones". Revisar el lunes antes de publicar.**
- **La tesis se apoya en un hecho confirmado**, no en la hipótesis de que una IA encontrara el fallo: ese código lo escribieron humanos expertos y estuvo cinco años sin que nadie lo viera.
- **Marco obligatorio por la búsqueda de empleo**: "la IA ha subido el mínimo", nunca "los desarrolladores sobran".

---

El 30 de julio alguien se llevó 70 millones de dólares en 41 minutos, aprovechando un fallo que llevaba cinco años escondido.

Y lo interesante no es el robo. Es quién escribió ese código.

Las COLDCARD son unos aparatos del tamaño de una calculadora donde la gente guarda las llaves de sus bitcoins, fuera de internet, y se supone que son de lo más seguro que hay. Para crear tu llave, el aparato elige un número al azar entre tantísimas opciones que nadie podría probarlas todas. Ese es todo el truco, y desde 2021 estaba mal: elegía entre muchísimas menos de las que prometía, así que sí se podían probar todas. Nadie se dio cuenta en cinco años.

Ese código lo escribieron programadores buenos, a mano, en una empresa que vive de la seguridad y que se juega su reputación en ello.

Lo cuento porque me encuentro mucha desconfianza cuando el código lo escribe una IA, y casi siempre por la misma comparación: la IA contra un ingeniero excelente. Pero esa no es la comparación que hace nadie en la vida real. Si tienes una empresa de veinte personas y necesitas una herramienta interna, tú nunca ibas a contratar a un ingeniero excelente: ibas a contratar lo más barato que encontraras, y encima sin nadie dentro que supiera revisar lo que te entregan. Contra eso, hoy, la IA gana bastantes veces.

Dicho lo cual, no me trago que valga para todo. La IA no sabe cómo funciona tu negocio: no sabe que las facturas de ese cliente van aparte porque lleváis quince años haciéndolo así. Eso se lo tienes que explicar tú, y si se lo explicas mal hace la chapuza rapidísimo y con una seguridad tremenda. Y cuanto más te juegues —dinero, datos de personas, nóminas— más falta hace alguien que sepa leer lo que ha salido y responda de ello.

Lo que tengo claro es que la IA no ha hecho mejores a los mejores. Lo que ha hecho es subir el mínimo. Y el mínimo es lo que compra la mayoría de las empresas.

Para una herramienta de tu empresa, ¿de quién te fías más hoy: del desarrollador más barato que puedas contratar o de alguien con criterio trabajando con IA?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
