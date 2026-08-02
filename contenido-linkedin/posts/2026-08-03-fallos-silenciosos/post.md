# Post — Cómo validar algo que siempre parece correcto

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada**, en formato **didáctico** (ver `estrategia-contenido.md`). El caso Coldcard es el arranque; el cuerpo del post es **cómo desconfiar bien de la IA sin ser técnico**. Doble lectura: el reclutador lee criterio real sobre modos de fallo de los modelos; el dueño de pyme se lleva tres hábitos que puede aplicar el lunes. No es pitch de venta.
**Imágenes:** `frase.png` — fondo claro. Titular *"La IA no tiene **pantalla roja**"* + los 3 hábitos numerados + tira de datos del caso (5 años oculto · 41 min de robo · ~70 M$) con el pie que dice de dónde salen. Tarjeta pensada para **guardarse**: quien la ve suelta en el feed ya se lleva algo aplicable sin leer el post.
**Revisión editorial (2026-08-02):** una sola corrección al copy entregado — *"Lo general casi siempre está bien"* → *"Lo general suele estar bien"*. La primera formulación afirmaba más de lo que se puede sostener sobre cómo fallan los modelos, y la regla del repo es no afirmar de más aunque suene mejor.

## Quinta versión: bajar el listón técnico (feedback de Alberto, 2026-08-02)

Alberto: *"lo de cómo validar algo es una chapuza, nadie se siente identificado con eso"*. Correcto. La cuarta versión acababa en una metodología de evaluación de modelos (50 casos etiquetados, tasa de acierto, deriva del proveedor). Un dueño de gestoría no va a montar eso jamás: era lenguaje de ingeniero disfrazado de consejo.

- **El punto de entrada humano no es un método, es una experiencia**: todo el mundo ha visto a una IA afirmar con total seguridad algo falso. Eso pasa a la primera línea del post, y la noticia queda como prueba, no como protagonista.
- **El cierre son hábitos, no procesos**: ¿me daría cuenta si estuviera mal? / comprobar el dato exacto, no lo general / pedir la fuente y abrirla. Cero herramientas, cero equipo técnico.
- **Punto de criterio final** (el que construye autoridad sin tecnicismos): desconfiar de una IA que nunca dice "no lo sé", porque el tono no cambia sepa o se lo invente.
- **Se cortan los titulillos en negrita y los giros retóricos de transición** ("y aquí es donde…", "la parte que me interesa"): son el tic que delata texto generado. El post va en párrafos cortos seguidos.
- **Se saca del post la hipótesis de la revisión de código con IA.** Añadía un concepto que a la audiencia objetivo no le dice nada y pisaba el cierre. Va como **primer comentario** del post (texto abajo), etiquetada como hipótesis.
- **Pregunta final cambiada** a una que se contesta en cinco palabras y que invita a contar una anécdota propia, en vez de a confesar que no validas nada.

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

Todos hemos preguntado algo a una IA y nos ha contestado, con una seguridad absoluta, algo que era mentira.

La semana pasada ese mismo tipo de fallo costó 70 millones de dólares en 41 minutos.

Te lo cuento sin tecnicismos, porque es la mejor forma que conozco de explicar el problema que tenemos con la IA.

Existen unos aparatos del tamaño de una calculadora, sin conexión a internet, donde se guarda la llave de tus bitcoins. De lo más seguro que hay.

Al crear esa llave, el aparato tiene que elegir un número al azar gigantesco, tan grande que nadie pueda dar con él probando.

Durante cinco años lo eligió entre muchísimas menos opciones de las que prometía.

El 30 de julio alguien generó todas esas opciones, las fue probando y vació las carteras. Entre la 01:10 y la 01:51 de la madrugada. Unos 70 millones de dólares.

En esos cinco años el aparato no dio ni un error. Se encendía, guardaba la llave, devolvía el dinero. Si lo revisabas no veías nada raro, porque no había nada raro que ver.

Los fallos que salen caros son estos: los que no rompen nada y siguen dando resultados creíbles.

La IA falla igual.

Cuando se equivoca no salta una alarma ni una pantalla roja. Sale un párrafo bien escrito, ordenado y seguro de sí mismo. Una cifra inventada tiene exactamente la misma pinta que una cifra buena. Un artículo de una ley que no existe se lee igual que uno que sí.

Y si tu manera de comprobarlo es leerlo y ver si suena bien, no estás comprobando nada. Sonar bien es justo lo que mejor se le da.

Tres cosas que puedes hacer el lunes, sin herramientas ni saber nada de tecnología:

1. Antes de usar la respuesta, pregúntate si te darías cuenta en caso de que estuviera mal. Si la respuesta es no, no la uses todavía.

2. Comprueba el dato exacto. Nombres, fechas, importes, plazos, artículos, referencias. Lo general suele estar bien; donde falla es en el detalle.

3. Pídele de dónde lo ha sacado y ábrelo tú. Si no puedes abrir la fuente, lo que tienes es un rumor muy bien redactado.

Y una de criterio, que vale más que las tres: desconfía de una IA que nunca dice "no lo sé". Cuando una persona duda, se le nota. Aquí el tono es idéntico lo sepa o se lo esté inventando.

¿Cuál es la última mentira que os ha colado una IA con total seguridad?

---

## Primer comentario (opcional, se publica junto al post)

> Un apunte que no cabía arriba: no hay confirmación de cómo se descubrió este fallo después de cinco años. El cofundador de la empresa apunta a la revisión de código con IA, que está encontrando cosas enterradas durante años más rápido que los mejores expertos humanos. Es una hipótesis, no un hecho, pero encaja con lo que se está viendo en el sector.

## Ganchos alternativos (por si se quiere probar otra apertura)

- *Un fallo puede pasar cinco años dentro de un sistema sin dar un solo error. / Y luego costar 70 millones de dólares en 41 minutos.*
- *El 30 de julio, entre la 01:10 y la 01:51 de la madrugada, alguien se llevó 70 millones de dólares. / El fallo que se lo permitió llevaba cinco años funcionando de maravilla.*
- *La IA no te avisa cuando se equivoca: te contesta igual de segura que cuando acierta. / La semana pasada, un fallo con esa misma forma costó 70 millones de dólares en 41 minutos.*

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
