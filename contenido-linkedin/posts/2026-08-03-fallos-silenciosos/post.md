# Post — Cómo validar algo que siempre parece correcto

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada**, en formato **didáctico** (ver `estrategia-contenido.md`). El caso Coldcard es el arranque, pero el cuerpo del post es **cómo se valida y se corrige la IA**. Doble lectura: reclutador lee criterio serio de evaluación y observabilidad de modelos (competencia directa de Head of Data); dueño de pyme se lleva un método aplicable. No es pitch de venta.
**Imágenes:** `frase.png` — fondo claro, cuatro pasos de validación numerados. Tarjeta pensada para **guardarse**.

## Cuarta versión: el giro a IA (feedback de Alberto, 2026-08-01)

Alberto: *"floja la reflexión, igual mejor enlazarlo con la IA, y cómo se valida y corrige"*. Tenía razón y el giro mejora el post entero:

- **El puente es real, no forzado**, y esto es lo que lo sostiene: el fallo de Coldcard **no producía errores, producía resultados plausibles**. Llaves que parecían aleatorias, funcionaban y restauraban bien. Ese es, exactamente, el modo de fallo de un modelo de lenguaje: no devuelve un error, devuelve una respuesta bien escrita y segura. Una cifra inventada tiene el mismo aspecto que una buena. **No hay pantalla roja en ninguno de los dos casos.**
- **La reflexión anterior era floja porque era genérica** ("revisa tus copias, recalcula tus números"). Servía para cualquiera y no usaba nada de lo que Alberto sabe. El cuerpo ahora es evaluación de modelos, que es terreno suyo: medir contra verdad conocida, volver a medir por deriva del proveedor, permitir la abstención, y cruzar por una segunda vía.
- **Se recupera el apunte sobre IA que se había cortado**, ahora sí con función: cierra el círculo (la IA es lo que hay que validar y a la vez lo que está encontrando fallos latentes de años). Sigue **etiquetado como hipótesis**, porque no está confirmado.
- **Punto 2, el que más se salta la gente**: el proveedor actualiza el modelo por debajo y nadie avisa. Mismo prompt, mismo proceso, resultados distintos. Es un fallo silencioso idéntico al de Coldcard, y por eso encaja tan bien con el arranque.

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras físicas COLDCARD no era lo bastante aleatorio al crear la semilla (~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 de una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3).
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: 30 de julio, 01:10–01:51 UTC (41 minutos).
- **Cifra**: se movió de ~594 BTC (~38 M$) a [~1.158 BTC (~75 M$) según Galaxy Research](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **Se usa "unos 70 millones". Revisar el lunes antes de publicar.**
- **Hipótesis, no hecho**: NVK, cofundador de Coldcard, apunta a que la revisión de código asistida por IA encuentra fallos latentes más rápido que los expertos humanos. [Bitcoin Magazine](https://bitcoinmagazine.com/business/coinkite-releases-fixed-firmware-after-coldcard-bug-ai-likely-involved-in-the-hack) lo recoge como creencia del sector. **Va etiquetado como tal en el post.**

---

Un fallo puede estar cinco años dentro de un sistema sin dar un solo error.

Y luego costar 70 millones de dólares en 41 minutos.

Pasó la semana pasada, y creo que es la mejor forma de explicar el problema que tenemos ahora mismo con la IA.

**Qué pasó**

Los aparatos que guardan la llave de tus bitcoins tienen que elegir, al crearla, un número al azar enorme, imposible de adivinar probando.

Desde 2021 no lo elegían tan al azar como debían: escogían entre muchísimas menos posibilidades de las prometidas. Alguien se dio cuenta, generó todas esas posibilidades y fue abriendo. 41 minutos, unos 70 millones.

**El detalle que importa**

El aparato nunca dio un resultado erróneo.

Daba resultados perfectamente plausibles: llaves que parecían aleatorias, que funcionaban, que guardaban y devolvían el dinero. Cinco años así. Si lo revisabas, no veías nada, porque no había nada que ver.

Ese es el fallo más caro que existe: el que no produce errores, produce resultados creíbles.

**Y esto es exactamente la IA**

Un modelo no te devuelve un error cuando se equivoca. Te devuelve una respuesta bien escrita, segura y con el formato correcto. Una cifra inventada tiene el mismo aspecto que una cifra buena. No hay pantalla roja.

Si tu forma de validar la IA es leer lo que sale y ver si suena bien, no estás validando: estás midiendo lo plausible que es. Que es justo lo que el modelo está optimizando.

**Cómo se valida de verdad**

1. Contra la fuente, no contra tu criterio. Coge 50 casos reales, resuélvelos a mano y compara. Ahora tienes una tasa de acierto. Antes tenías una sensación.

2. Vuelve a medirlo cada cierto tiempo. Esto se lo salta casi todo el mundo: el proveedor actualiza el modelo por debajo y nadie te avisa. Mismo prompt, mismo proceso, resultados distintos. Lo que iba al 95% en marzo puede ir al 80% en julio sin que hayas tocado nada.

3. Deja que pueda decir "no lo sé". Si la única salida posible es una respuesta, siempre habrá respuesta, también cuando no la hay. Un sistema que puede parar y pasarle el caso a una persona se equivoca muchísimo menos que uno obligado a contestar.

4. Cruza por otro camino. Si el número importa, sácalo también por una vía distinta. Si las dos coinciden, te lo crees. Si no, acabas de encontrar algo.

**Un apunte para terminar**

Sobre cómo se descubrió el fallo de esas carteras no hay confirmación, pero el cofundador de la empresa apunta a algo que ya se está viendo en el sector: la revisión de código con IA encuentra fallos latentes más rápido que los mejores expertos humanos.

Así que la IA es las dos cosas a la vez. Lo que más cuidado hay que tener en validar, y lo que mejor está encontrando lo que llevaba años sin que nadie lo validara.

¿Cómo estáis comprobando hoy que lo que os devuelve la IA es correcto?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
