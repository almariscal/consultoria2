# Post — Si cada uno puede montarse su software, las empresas van a tener que abrir sus datos

**Estado:** Listo para publicar
**Fecha prevista:** jueves 2026-08-06 (el martes 04/08 va el post de "cada departamento con su propio reporting")
**Línea de contenido:** Caso/evidencia real + reflexión. Segunda parte natural del post del DNI (23/07): si cualquiera puede construirse su herramienta, el software deja de competir por la interfaz y pasa a competir por si deja salir los datos. Doble lectura: reclutador (Head of Data) lee criterio de arquitectura y competencia práctica con IA agéntica; dueño de pyme lee un criterio de compra para su próximo software. No es pitch de venta.
**Imágenes:** `frase.png` — tarjeta-cita sobre fondo azul noche, siguiendo `contenido-linkedin/guia-estilo-visual.md`.
**Proyecto referenciado:** `almariscal/seguimiento_economico` — herramienta local para unificar inversiones repartidas en seis plataformas. **Repositorio privado: no se enlaza** (contiene la estructura de sus finanzas personales). A diferencia del post del DNI, aquí no hay enlace en comentarios; el post se sostiene solo con la historia.
**Hecho verificado (fuentes externas, 2026-07-30):** Revolut conectó Revolut X a asistentes de IA (Claude, Gemini, Cursor, OpenClaw) vía MCP; anuncio del 10 de julio de 2026. El usuario tiene que aprobar cada orden antes de que se ejecute; Revolut no responde del comportamiento de los asistentes de terceros. Fuentes: [DiarioBitcoin](https://www.diariobitcoin.com/criptomonedas/revolut-integra-asistentes-de-ia-para-trading-cripto-con-indicaciones-de-texto/), [CoinGape](https://coingape.com/revolut-to-let-traders-use-claude-gemini-and-cursor-for-crypto-trades/), [Finance Magnates](https://www.financemagnates.com/forex/analysis/revolut-built-a-trading-desk-with-ai-in-30-minutes-will-prompts-replace-broker-platforms/).

---

Llevo unas semanas montándome una herramienta para ver todas mis inversiones en un solo sitio.

Nada sofisticado: tengo el dinero repartido entre seis plataformas —tres brokers, un banco, un exchange de cripto y una wallet propia— y ninguna me responde lo único que quiero saber: cuánto tengo en total y cuánto ha rendido de verdad. Cada una enseña su trocito. La foto completa no existe en ningún sitio.

Así que me la construí. Y la parte interesante no fue programarla.

Fue lo que costó sacar los datos.

Cada banco exporta su extracto a su manera, así que acabé escribiendo un fichero de traducción por banco. El valor de los fondos lo leo de una web pública, porque no hay forma oficial de pedirlo. Y para valorar un piso monté un pequeño robot que abre un navegador, entra en la página de precios de la zona y me pide que resuelva yo el captcha a mano.

Nada de eso es tecnología difícil. Es fontanería para rodear una puerta cerrada. Y los datos que hay detrás de esa puerta son míos.

Con una excepción que me llamó la atención: hace unas semanas Revolut conectó su plataforma de cripto a asistentes de IA como Claude o Gemini a través de MCP, un estándar abierto que permite a una IA usar herramientas de fuera. Puedes pedirle a tu asistente que te resuma la cartera, que te avise si algo baja de un precio, o que te prepare una orden — que tú tienes que aprobar antes de que se ejecute.

Lo relevante ahí no es el trading con IA. Es la decisión de fondo: Revolut ha aceptado que su app deje de ser el único sitio desde el que se usan sus propios datos.

Y creo que esa es la dirección.

Hace unas semanas contaba aquí que hoy cualquiera se monta en una tarde la herramienta que necesita, describiéndosela a una IA. Si eso es verdad —y lo es—, el software deja de competir solo por su interfaz. Empieza a competir por algo más incómodo: si te deja sacar la información o no.

Y esto no va de cripto. Va de tu empresa.

Piensa en los programas que usáis: el ERP, el CRM, el TPV, el de la gestoría, el de rutas, el de fichajes. ¿Cuántos te dejan sacar tus datos sin que alguien los copie a mano en un Excel el último viernes de cada mes? Ese trabajo manual es un impuesto que pagas todos los meses y no aparece en ninguna factura.

Por eso la pregunta al contratar software está cambiando. Ya no es solo "¿qué sabe hacer?". Es "¿me deja llevarme lo que es mío?". ¿Tiene API? ¿Le puedo conectar un asistente? ¿O mis datos solo existen dentro de sus pantallas?

Mi apuesta: los proveedores que abran —API, MCP, exportaciones decentes— se van a quedar, porque pasan a ser la pieza sobre la que sus clientes construyen. Los que encierren la información van a perder clientes más rápido de lo que creen, ahora que irse ya no exige tener un equipo de desarrollo.

¿Cuál de vuestros programas os deja hoy sacar los datos sin pelear?

---

_(Cuando se publique: mover a "Publicado" en `contenido-linkedin/calendario.md` con fecha real y, más adelante, las métricas.)_
