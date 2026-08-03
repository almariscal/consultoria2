# Post — Esa nunca fue tu comparación (código hecho a mano vs. código con IA)

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada** + **opinión con criterio**. Primer post del perfil que defiende una tesis discutible en vez de explicar un concepto. El caso Coldcard es la prueba, no el tema.
**Imágenes:** `frase.png` — azul noche. Titular con los dos datos del caso + bloque de comparación ("la comparación que todos hacen" vs. "la comparación real"), que es la tesis del post en una imagen.

## Sexta versión: el giro de Alberto (2026-08-02)

Alberto reenfoca el post entero: *"hace 5 años era impensable que esto lo hiciera una IA y aún hay reticencia a que desarrolle el código, pero creemos que lo que hace la gente a mano es súper bueno y ya el nivel del desarrollo con IA es en muchos casos superior, porque se tiende a contratar barato"*. Encarga un segundo especialista en copywriting.

**Por qué el giro funciona**: es la primera vez que el post defiende una opinión propia y discutible en lugar de divulgar. Eso construye autoridad de verdad y, además, genera comentarios (la gente quiere opinar sobre esto).

**Tres correcciones aplicadas a la tesis antes de escribir** (si no, el post se vuelve en contra de Alberto):

1. **"El código con IA es superior" es indefendible tal cual** — cualquier ingeniero lo tumba en el primer comentario y un reclutador lee hype. La comparación que Alberto quiere hacer es otra y es mucho más fuerte: **no es IA contra el mejor ingeniero, es IA contra lo que ibas a contratar de verdad con tu presupuesto de verdad**. Ese es el giro del post.
2. **El pilar es un hecho confirmado, no la hipótesis.** Que la IA encontrara el fallo lo apunta el cofundador de Coldcard, pero **no está confirmado** y no puede sostener el argumento. El hecho que sí lo sostiene: **ese código lo escribieron humanos expertos, en una empresa cuyo negocio entero es la seguridad, y el fallo estuvo cinco años sin que nadie lo viera.** Eso desmonta el "lo hecho a mano es más fiable" sin depender de ninguna hipótesis. La hipótesis aparece en el post, etiquetada como tal.
3. **Límite honesto obligatorio.** Sin una frase que diga dónde el desarrollo con IA *no* es mejor, el post es humo y destruye la autoridad que pretende construir. El límite elegido es el bueno: la IA no conoce tu negocio, y a más riesgo (dinero, datos personales, nóminas) más falta hace alguien que sepa leer lo que ha salido.

**Aviso de encuadre para la búsqueda de empleo**: Alberto dirigirá equipos técnicos y busca Head of Data desde febrero de 2027. El marco es **"la IA ha subido el mínimo"**, nunca "los desarrolladores sobran". El post lo dice explícitamente ("la IA no ha hecho mejores a los mejores").

### Correcciones editoriales al copy entregado (2026-08-02)

- **Fuera la mención a la app de inversiones.** Alberto pidió dejar `seguimiento_economico` al margen, y además el post del jueves 06/08 va entero sobre ese proyecto: mencionarlo el lunes y el jueves es repetirse en la misma semana. Se queda solo la herramienta del DNI, que ya es pública y ya se contó en el post del 23/07 (da continuidad al perfil).
- **Se quita "con revisiones"** de la frase sobre Coinkite: no consta verificado que hubiera un proceso de revisión formal, y el argumento se sostiene igual sin ese detalle. Regla del repo: no afirmar de más aunque suene mejor.
- **Corregido un tiempo verbal** ("hace cinco años eso no existe" → "no habría sido posible").

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras COLDCARD no era lo bastante aleatorio al crear la semilla (~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 de una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3).
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: 30 de julio, 01:10–01:51 UTC (41 minutos).
- **Cifra**: se movió de ~594 BTC (~38 M$) a [~1.158 BTC (~75 M$) según Galaxy Research](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **Se usa "unos 70 millones". Revisar el lunes antes de publicar.**
- **Hipótesis, no hecho**: NVK, cofundador de Coldcard, apunta a que la revisión de código con IA encuentra fallos latentes más rápido que los expertos humanos ([Bitcoin Magazine](https://bitcoinmagazine.com/business/coinkite-releases-fixed-firmware-after-coldcard-bug-ai-likely-involved-in-the-hack)). **Va etiquetada como hipótesis en el post.**

---

El 30 de julio alguien robó 70 millones de dólares en 41 minutos.

El fallo que lo permitió llevaba cinco años ahí y lo escribieron humanos expertos.

Hay unos aparatos que se llaman COLDCARD. Del tamaño de una calculadora. Guardan las llaves de tus bitcoins fuera de internet y se supone que son de lo más seguro que existe. Hay gente que tiene ahí sus ahorros.

Para crear tu llave, el aparato elige un número al azar entre una cantidad brutal de opciones. Tan brutal que no puedes probarlas todas ni en mil años. Ese es todo el truco.

Desde 2021 elegía entre muchísimas menos de las que prometía. Un cajón pequeño. Y un cajón pequeño sí se vacía probando.

Nadie lo vio en cinco años. Ni la empresa, ni sus clientes, ni la gente de fuera que busca estos fallos por deporte.

Ese código lo escribieron programadores buenos, en una empresa cuyo negocio entero es la seguridad y con su reputación en juego.

Lo cuento porque me encuentro mucha desconfianza con el código escrito con IA. Y detrás casi siempre está la misma comparación: la IA contra un ingeniero excelente.

Esa no es la comparación de casi nadie.

Si tienes una empresa de veinte personas y necesitas una herramienta interna, tú nunca ibas a contratar a un ingeniero excelente. Ibas a contratar lo más barato que encontraras, sin nadie dentro capaz de revisar lo que te entregan. Contra eso, hoy, la IA gana muchas veces.

Yo me he montado alguna cosa para mí en un rato. Una utilidad para ponerle marca de agua a mi DNI antes de mandarlo por ahí. Hace cinco años eso no habría sido posible: o le dedicaba tres fines de semana o me quedaba sin ello.

Ahora, lo que no me trago.

La IA no sabe cómo funciona tu negocio. No sabe que las facturas de ese cliente van aparte porque lleváis quince años haciéndolo así. Eso se lo explicas tú, y si se lo explicas mal, hace la chapuza rapidísimo y con una seguridad enorme.

Y cuanto más te juegas, más falta hace alguien que sepa leer lo que ha salido y responda de ello. Dinero, datos personales, nóminas: ahí no basta con que funcione en la demo.

El cofundador de COLDCARD apunta a que revisar código con IA está sacando fallos escondidos más rápido que los mejores expertos. Es una hipótesis suya, no un hecho, y me la tomo como tal.

Lo que sí tengo claro es que la IA no ha hecho mejores a los mejores. Ha subido el mínimo. Y el mínimo es lo que compra la mayoría de las empresas.

Dime en una línea: para una herramienta de tu empresa, ¿de quién te fías más hoy — del desarrollador más barato que puedas contratar, o de alguien con criterio trabajando con IA?

---

## Ganchos alternativos (por si se quiere probar otra apertura)

- *Un fallo tardó cinco años en aparecer y 41 minutos en costar 70 millones de dólares. / Lo escribieron humanos expertos, en una empresa que vive de la seguridad.*
- *Cinco años. Ese es el tiempo que un fallo estuvo escondido en uno de los cacharros más seguros del mundo. / El 30 de julio alguien lo encontró y se llevó 70 millones de dólares.*
- *Se supone que lo hecho a mano por expertos es más fiable. / El 30 de julio ese argumento perdió 70 millones de dólares en 41 minutos.*

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
