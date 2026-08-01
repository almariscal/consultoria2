# Post — Un fallo puede estar cinco años dentro sin dar un solo error

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada**, en formato **didáctico** (ver `estrategia-contenido.md`). El caso Coldcard se usa para enseñar un concepto —*funcionar y estar bien no son lo mismo*— y termina en tres comprobaciones que el lector puede hacer esta semana. Doble lectura: reclutador lee criterio de observabilidad y calidad de dato; dueño de pyme se lleva una lista accionable. No es pitch de venta.
**Imágenes:** `frase.png` — **fondo claro** (primera vez; hasta ahora todas las tarjetas eran azul noche) con las tres comprobaciones numeradas. Es una tarjeta pensada para **guardarse**, no para citarse: en LinkedIn el guardado pesa mucho y una lista aplicable se guarda; una frase bonita no.

## Tercera reescritura tras feedback de Alberto (2026-08-01)

Alberto: *"no me gusta ni la imagen y el post demasiado artificial, quiero que sea más educativo y didáctico pero que el algoritmo lo premie"*. Qué se ha cambiado y por qué:

- **El problema era el registro, no el contenido.** La versión anterior estaba escrita como ensayo: analogía de apertura literaria ("Imagínate una caja fuerte…"), giros retóricos de transición ("Y aquí es donde esto deja de ir de bitcoin", "la parte que me interesa"), párrafos en tríada simétrica. Todo eso se lee como texto *construido para producir un efecto*, que es exactamente la sensación de artificial. **Ahora el post explica en vez de sugerir**: dice lo que pasó, por qué nadie lo vio, y qué hacer.
- **Estructura con secciones cortas** ("Qué pasó", "Por qué nadie lo vio", "Dónde tienes tú lo mismo", "Tres comprobaciones"). Es escaneable, sostiene la lectura hasta el final y da un cierre accionable.
- **Lo que hace que el algoritmo lo premie no es un truco, es la utilidad**: las tres comprobaciones son guardables y la pregunta final ("¿cuál de las tres no habéis hecho nunca?") se puede responder en tres palabras, que es lo que genera comentarios. El gancho va en las **dos primeras líneas**, antes del corte de "ver más".
- **La analogía de la caja fuerte se conserva**, pero ya no abre el post: pasa a estar dentro de la explicación técnica, que es donde hace falta.
- **Nota para Alberto**: en el punto 3 me he quedado corto a propósito. Si tu experiencia lo sostiene —y creo que sí, montando funciones de datos desde cero—, la frase natural sería *"es la que más veces me he encontrado"*. No la he puesto porque no me consta por escrito; si es cierta, dila tú, que gana mucho.

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras físicas COLDCARD no era lo bastante aleatorio al crear la semilla. Coinkite estima ~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 que debería tener una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3.
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: 30 de julio, 01:10–01:51 UTC (41 minutos), empezando por las carteras mayores.
- **Cifra**: se movió en dos días, de ~594 BTC (~38 M$) a [~1.158 BTC (~75 M$) según Galaxy Research](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **En el post se usa "unos 70 millones", conservadora. Revisar el lunes antes de publicar.**
- **Estado**: los fondos siguen sin moverse. Coinkite publicó firmware corregido el 31/07.

---

Un fallo puede estar cinco años dentro de un sistema sin dar un solo error.

Y luego costar 70 millones de dólares en 41 minutos.

Pasó la semana pasada. Lo explico entero, porque el mecanismo no es de bitcoin: lo tienes tú también.

**Qué pasó**

Hay unos aparatos, del tamaño de una calculadora, que sirven para guardar la llave de tus bitcoins sin conectarse a internet. Son de lo más seguro que existe, y por eso los usa quien tiene cantidades serias.

Para crear tu llave, el aparato tiene que elegir un número al azar. Enorme. Tan grande que nadie pueda adivinarlo probando.

Ahí estaba el fallo: desde 2021 no elegía tan al azar como creía. Escogía entre muchísimas menos posibilidades de las prometidas. Como una caja fuerte que por fuera es idéntica a las demás pero por dentro solo tiene unos cientos de combinaciones.

Alguien lo descubrió, generó todas esas combinaciones y fue abriendo. 41 minutos, unos 70 millones.

**Por qué nadie lo vio antes**

Esta es la parte que merece la pena aprenderse.

Durante cinco años, el aparato funcionó. Se encendía, guardaba, devolvía el dinero cuando tocaba, no dio ni un error. Podías revisarlo cada mañana y no habrías visto nada, porque no había nada que ver.

Funcionar y estar bien no son lo mismo.

Un sistema roto que además falla es el caso fácil: te avisa. El problema es el sistema roto que funciona, porque entonces el silencio se interpreta como que todo va bien. Y no es una señal de nada.

**Dónde tienes tú exactamente lo mismo**

Un informe que suma mal desde que alguien tocó una fórmula, y con el que llevas meses decidiendo.

Una copia de seguridad que se hace cada noche sin fallar y que nadie ha restaurado nunca.

Un proceso automático que dejó de ejecutarse en marzo. Cuando funcionaba no mandaba correos; cuando dejó de hacerlo, tampoco.

Ninguno da error. Por eso siguen ahí.

**Tres comprobaciones para esta semana**

1. Restaura una copia de verdad. Que se haga no significa nada. Coge la de anoche, recupera un fichero en otro sitio y ábrelo. Hasta que no has recuperado algo, no tienes una copia: tienes un proceso que dice que sí.

2. Recalcula a mano tu número más importante. Ese con el que decides cada mes. Sácalo otra vez desde el origen y por otro camino. Si no cuadra, ya has encontrado uno.

3. Haz que te avise el silencio. Casi todas las alertas saltan cuando algo falla. Casi ninguna salta cuando algo deja de ocurrir. Si tienes un proceso que debe ejecutarse cada lunes, lo que necesitas es un aviso el lunes que no se ejecute.

La tercera es la más barata de montar y la que casi nadie tiene puesta.

¿Cuál de las tres no habéis hecho nunca?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
