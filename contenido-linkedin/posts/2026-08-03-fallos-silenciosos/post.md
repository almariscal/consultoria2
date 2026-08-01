# Post — Nada te avisa de que llevas años sumando mal

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada** (ver `estrategia-contenido.md`). No es un post de cripto ni de seguridad: el caso Coldcard es la excusa para hablar de **fallos que no dan error**. Doble lectura: reclutador lee criterio de riesgo de datos; dueño de pyme se lleva una acción concreta. No es pitch de venta.
**Imágenes:** `frase.png` — *"Nada te avisa de que llevas años **sumando mal**"*, con tira de datos reales (5 años sin dar error · 41 min de robo · ~70 M$).
**Aviso de encuadre:** Alberto **no** aparece como usuario de Coldcard ni de ningún dispositivo concreto — no lo sabemos y no se inventa.

## Reescritura tras feedback de Alberto (2026-08-01)

Se descartaron dos versiones anteriores. Los dos fallos, y las reglas que salen de ellos:

1. **Daba por sabido lo que es una cartera física de bitcoin.** El lector objetivo (dueño de pyme) no tiene ni idea, y con el primer párrafo lleno de jerga desconecta. **Regla: en actualidad comentada, si la noticia viene de un mundo que el lector no pisa, el post empieza con una analogía cotidiana y no usa ni una palabra técnica sin explicarla antes.** Aquí: la caja fuerte que por fuera es idéntica pero tiene muchas menos combinaciones.
2. **El puente al Excel era falso.** La versión anterior decía "a Coldcard le mandaron un aviso de seguridad, a tu Excel no". Alberto: *"¿alguien se siente identificado? Si nadie te va a hackear el Excel."* Tiene razón — y el fallo es de fondo, no de redacción: Coldcard es un caso de **robo**, y a una pyme no le van a robar el Excel. Convertir la analogía en amenaza de seguridad hacía el post inverosímil. **El paralelismo correcto no es el ladrón, es el silencio**: algo puede llevar años roto sin dar un solo error. En una pyme la consecuencia no es un robo, es haber decidido meses con un número equivocado. El post lo dice ahora explícitamente ("no te lo cuento para que te preocupes de que te hackeen").
3. **Se cortó el apunte sobre IA** (la hipótesis de NVK de que la revisión de código con IA encuentra fallos latentes más rápido que los expertos). Es interesante y está bien traído, pero era una segunda idea en un post que tiene que entenderse a la primera. Guardado como posible post propio más adelante.
4. **Se quitó el recuento de carteras.** Decir "vació casi 1.200 carteras" mezclaba direcciones con dispositivos (fueron ~1.196 *direcciones*, de un número menor de aparatos). Se dejan solo los dos datos limpios y verificados: 41 minutos y ~70 M$.

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras físicas COLDCARD no era lo bastante aleatorio al crear la semilla. Coinkite estima ~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 que debería tener una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3.
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: 30 de julio, entre las 01:10 y las 01:51 UTC (41 minutos), empezando por las carteras mayores.
- **Cifra**: se movió mucho en dos días — de ~594 BTC (~38 M$) en los primeros informes a [~1.158 BTC (~75 M$) según Galaxy Research](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **En el post se usa "unos 70 millones", conservadora. Revisarla el lunes antes de publicar y, si cambia, cambiarla también en `frase.png`.**
- **Estado**: los fondos siguen sin moverse. Coinkite publicó firmware corregido el 31/07.

---

Imagínate una caja fuerte que, en lugar de tener millones de combinaciones posibles, solo tiene unos cientos. Por fuera es idéntica a cualquier otra: pesa lo mismo, abre igual, cierra igual. Nadie que la mire por fuera puede notar la diferencia. Ni el que la fabricó.

Algo así ha pasado esta semana con un aparato que mucha gente usa para guardar bitcoins. Es un cacharro pequeño, del tamaño de una calculadora, que no se conecta a internet y cuya única función es guardar la llave de tu dinero. Se supone que es de lo más seguro que existe.

Para funcionar, ese aparato tiene que inventarse un número al azar enorme, imposible de adivinar. Ese número es tu llave. Y resulta que llevaba desde 2021 sin elegirlo tan al azar como debía: escogía entre muchísimas menos posibilidades de las prometidas. La caja fuerte con pocas combinaciones.

Alguien se dio cuenta. En 41 minutos se llevó unos 70 millones de dólares.

Pero la parte que me interesa de esta historia no es el robo.

Es que el fallo llevaba cinco años dentro. Cinco. Y en todo ese tiempo el aparato funcionó perfectamente: se encendía, guardaba, devolvía el dinero cuando tocaba, no dio ni un solo error. Nadie podía verlo mirándolo, porque no había nada que ver. Funcionaba.

Y aquí es donde esto deja de ir de bitcoin.

No te lo cuento para que te preocupes de que te hackeen. En tu empresa lo más probable es que no haya ningún ladrón esperando. Lo que hay es algo mucho más aburrido, y bastante más frecuente:

Un informe que suma mal desde que alguien tocó una fórmula hace tres años, y con el que llevas desde entonces tomando decisiones.

Una copia de seguridad que se hace todas las noches sin fallar y que nadie ha intentado restaurar jamás, así que en realidad nadie sabe si sirve.

Un proceso automático que dejó de ejecutarse en marzo y del que nadie se ha enterado, porque cuando algo funciona no manda ningún correo — y cuando deja de funcionar, tampoco.

Nada de eso da error. Nada de eso se ve raro. Y esa es exactamente la razón por la que lleva ahí tanto tiempo.

La diferencia con la caja fuerte es que a esa empresa alguien acabó publicándole un aviso. A ti no te lo va a publicar nadie: tus cosas no salen en las noticias.

Contra un fallo que no avisa solo funciona una cosa, y es ir a buscarlo a propósito aunque no haya pasado nada. Coger lo que no te puedes permitir perder y comprobar que de verdad está donde crees que está.

Empieza por lo más fácil: ¿cuándo fue la última vez que alguien probó a restaurar una copia de seguridad, de verdad, hasta el final?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
