# Post — El fallo llevaba cinco años ahí y el aparato funcionaba perfectamente

**Estado:** Listo para publicar
**Fecha prevista:** lunes 2026-08-03
**Línea de contenido:** **Actualidad comentada** (línea nueva, ver `estrategia-contenido.md`). No es un post de cripto ni de seguridad informática: el caso Coldcard es la excusa para hablar de **fallos silenciosos** — los que no dan señal porque el sistema sigue funcionando. Doble lectura: reclutador lee criterio de riesgo y juicio de ingeniería; dueño de pyme se lleva una acción concreta (probar una restauración). No es pitch de venta.
**Imágenes:** `frase.png` — tarjeta-cita azul noche, siguiendo `contenido-linkedin/guia-estilo-visual.md`.
**Aviso de encuadre:** Alberto **no** aparece como usuario de Coldcard ni de ningún dispositivo concreto — no lo sabemos y no se inventa. El post comenta una noticia pública, sin atribuirse experiencia propia en el caso.

## Hechos verificados (2026-08-01)

Fuente primaria: [aviso de seguridad de Coinkite](https://blog.coinkite.com/coldcard-mk3-seed-generation-warning/) y su [análisis técnico](https://blog.coinkite.com/entropy-technical-backgrounder/).

- **Qué falló**: el generador de números aleatorios de las carteras físicas COLDCARD no era lo bastante aleatorio al crear la semilla. Coinkite estima ~72 bits de entropía efectiva en Mk4/Mk5/Q frente a los 128 que debería tener una semilla BIP-39 de 12 palabras; peor en Mk2/Mk3.
- **Desde cuándo**: firmware posterior a marzo de 2021 — unos cinco años.
- **El robo**: el 30 de julio, entre las 01:10 y las 01:51 UTC (41 minutos), se vaciaron cerca de 1.200 direcciones, empezando por las mayores. Las cifras se movieron durante días: los primeros informes hablaban de ~594 BTC (~38 M$) y [Galaxy Research elevó el total a ~1.158 BTC (~75 M$)](https://www.cryptotimes.io/2026/08/01/coldcard-hack-hits-75m-after-alleged-second-attack-wave-galaxy-research/) tras una segunda oleada. **En el post se usa "más de 1.100 bitcoin, unos 70 millones" — cifra conservadora y a fecha de hoy.** Si al publicar el lunes la cifra ha cambiado, ajustarla.
- **Estado**: los fondos siguen sin moverse. Coinkite publicó firmware corregido el 31/07 (Mk4/Mk5 ≥ 5.6.0, Q ≥ 1.5.0Q, Mk3 ≥ 4.2.0).
- **Hipótesis, no confirmación**: NVK, cofundador de Coldcard, apunta a que la revisión de código asistida por IA ya encuentra fallos latentes más rápido que los mejores expertos humanos. [Bitcoin Magazine](https://bitcoinmagazine.com/business/coinkite-releases-fixed-firmware-after-coldcard-bug-ai-likely-involved-in-the-hack) lo recoge como *creencia* del sector, no como hecho probado. **En el post va marcado explícitamente como hipótesis.**

---

La semana pasada alguien vació casi 1.200 carteras de bitcoin en 41 minutos. Más de 1.100 bitcoin, unos 70 millones de dólares.

No hubo contraseñas robadas, ni correos de phishing, ni nadie que se dejara el ordenador abierto. El fallo estaba dentro del propio aparato: al crear las claves, no generaba números tan aleatorios como debía. Menos combinaciones posibles de las prometidas. Y quien lo descubrió pudo reconstruirlas.

Lo que me parece lo importante de esta historia no es el dinero.

Es que el fallo llevaba ahí desde 2021. Cinco años. Y en esos cinco años el aparato funcionó perfectamente: se encendía, generaba sus claves, guardaba el dinero, no dio ni un error. Nadie tenía nada que mirar, porque no había nada que se viera mal.

(Un apunte, y lo digo como hipótesis, no como hecho: el propio cofundador de la empresa apunta a que hoy la revisión de código con IA encuentra fallos latentes más rápido que los mejores expertos humanos. Si eso es así, todo el código viejo que "lleva años funcionando" acaba de volverse mucho más fácil de leer. Por quien llegue primero.)

Y aquí es donde esto deja de ir de bitcoin y empieza a ir de tu empresa.

Los riesgos que de verdad te tumban casi nunca hacen ruido. Son la copia de seguridad que se hace cada noche y que nadie ha intentado restaurar jamás. La fórmula de un Excel que alguien tocó hace tres años y que desde entonces suma mal una columna. El proceso automático que dejó de ejecutarse en marzo y del que nadie se ha dado cuenta porque nadie esperaba un aviso. El usuario del empleado que se fue hace dos años y sigue activo.

Todo eso "funciona". Nadie ve nada raro. Exactamente igual que el aparato.

Y la diferencia es que a Coldcard alguien le publicó un aviso de seguridad. A tu Excel no te lo va a publicar nadie.

Lo único que funciona contra un fallo silencioso es ir a buscarlo a propósito: coger la cosa sin la que no podrías trabajar mañana y comprobar, de verdad, que está donde crees que está.

¿Cuándo fue la última vez que probasteis a restaurar una copia de seguridad?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
