---
titulo: "Bitcoin está escalando exponencialmente con Lightning Network"
autor: "hans-hauge"
traductor: "Jose Antonio Mayol"
traductor_url: "https://twitter.com/Eljamp__"
fuente_original: "https://seekingalpha.com/article/4203403-bitcoin-is-scaling-exponentially-lightning-network"
fecha: "2022-01-27"
original: "2018-08-31"
nivel: "basico"
portada: "../imagenes/2022/01/fractal-55.jpg"
resumen: "Muchos han afirmado que Bitcoin y blockchain no pueden escalar. Hay algo de verdad en esto, pero como veremos, la escala es un objetivo en movimiento. Hay muchos aspectos para escalar y muchos enfoques para “resolver” el problema de escala. Uno de estos enfoques es el Lightning Network, que también es multifacético. Si Lightning Network…"
borrador: true
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/bitcoin-esta-escalando-exponencialmente-con-lightning-network/"
---

Muchos han afirmado que Bitcoin y [blockchain no pueden escalar](https://hackernoon.com/blockchains-dont-scale-not-today-at-least-but-there-s-hope-2cb43946551a). Hay algo de verdad en esto, pero como veremos, la escala es un objetivo en movimiento. Hay muchos aspectos para escalar y muchos enfoques para “resolver” el problema de escala. Uno de estos enfoques es el Lightning Network, que también es multifacético. Si Lightning Network puede cumplir con las capacidades que afirman sus creadores, entonces el argumento de que Bitcoin / blockchain no puede escalar se habrá disipado (la velocidad teórica es [miles de millones de transacciones](https://www.youtube.com/watch?v=8zVzw912wPo) por día); al menos un rato.

### ¿Por qué las cadenas de bloques son lentas?

En el desarrollo de software, comenzamos pensando en qué problema estamos tratando de resolver antes de escribir una línea de código. Cada pieza de software (idealmente) debe escribirse para resolver un determinado problema de la manera más efectiva posible. Les daré un ejemplo.

Supongamos que su problema es que necesita almacenar y recuperar datos. Por lo general, este problema se resuelve mediante una base de datos. Sin embargo, las bases de datos tienen ciertas limitaciones. Una de esas limitaciones es que incluso las bases de datos más grandes tienen límites de almacenamiento. Además, si sus datos (o la consulta que necesita ejecutar en esos datos) son complejos, el tiempo que lleva sacar sus datos de esa base de datos podría ser más largo de lo que sus clientes desean esperar.

Imagine que es Google ( [GOOGL](https://seekingalpha.com/symbol/GOOGL?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) ). Alguien busca el término “bicicleta”. Resulta que hay al menos 744.000.000 de resultados para este término de búsqueda y sus usuarios esperan una respuesta en una fracción de segundo. Le ahorraré los detalles técnicos, pero hay ciertas estrategias que Google utilizará para que esto suceda. Algunas de sus estrategias podrían ser [desnormalizar](https://msdn.microsoft.com/en-us/library/cc505841.aspx) los datos, hacer uso [del almacenamiento en caché](https://www.tutorialspoint.com/asp.net/asp.net_data_caching.htm) y entregarle los datos desde la [CDN más cercana posible](https://www.cloudflare.com/learning/cdn/what-is-a-cdn/).

### ¿Qué diablos tiene esto que ver con blockchain?

Bueno, recuerde que blockchain es una estructura de datos lenta y distribuida, en la que es difícil agregar datos (las computadoras potentes deben competir las 24 horas del día, los 7 días de la semana para tener la oportunidad de agregar una sola entrada cada 10 minutos) y el historial no se puede reescribir sin recalcular el toda la estructura de datos ([es inmutable](https://en.wikipedia.org/wiki/Persistent_data_structure)).

El propósito de una cadena de bloques no era ser rápido. El propósito de una cadena de bloques era ser difícil de cambiar (prueba de trabajo, solo escritura) y ser a prueba de manipulaciones. Esto significa que si realiza una entrada falsa en la cadena de bloques (enviándole monedas falsas, por ejemplo), puedo probar que su entrada es falsa y la red rechazará su entrada dudosa porque la mayoría de la red también encontrará que esta transacción no es válida.

Cualquiera puede descargar la cadena de bloques y hacer un cambio, pero el problema es que todos los demás pueden ver el cambio cuando intentas sincronizar con la red. Si su cambio no es válido, entonces el resto de la comunidad “votará por usted fuera de la isla”, por así decirlo. En realidad, el hecho de que la cadena de bloques es un libro contable distribuido es lo que lo hace inmutable en la práctica. La prueba de trabajo más larga gana, esto se llama [Consenso de Nakamoto](https://medium.com/@interlogica/the-nakamoto-consensus-ccdb7288169a) .

### El problema del general bizantino

Para comprender por qué es necesario este nivel de robustez, considere el problema del general bizantino.

El Consenso de Nakamoto es la primera solución conocida al problema del general bizantino; creando [tolerancia a fallas bizantinas](https://medium.com/loom-network/understanding-blockchain-fundamentals-part-1-byzantine-fault-tolerance-245f46fe8419). Básicamente, el problema es, ¿cómo se envía o recibe un mensaje en un entorno hostil?

### La velocidad de la cadena de bloques de Bitcoin es una decisión de diseño.

La cadena de bloques es lenta porque no está diseñada para ser rápida, es lenta porque está diseñada para ser duradera y a prueba de manipulaciones. Es lenta porque necesita poder resistir el asalto constante y permanecer como una fuente de verdad.

### ¿Qué es Lightning Network?

Lightning Network es una colección de protocolos sinérgicos. En un documento técnico presentado [en 2016](https://lightning.network/lightning-network-paper.pdf), Joseph Poon y Thaddeus Dryja sugieren que es posible tener [pagos instantáneos](https://lightning.network/lightning-network-summary.pdf), escalabilidad y micropagos prácticos mediante el uso de una solución de escala de dos capas. La cadena de bloques de Bitcoin existente formaría la capa base, siendo la principal fuente de verdad para las transacciones de valor. Mientras tanto, Lightning Network formaría una segunda capa, donde las transacciones podrían ocurrir de forma rápida y segura, sincronizándose ocasionalmente con la capa base.

Este enfoque adopta la escala de dos formas.

1.  La actividad se mueve de la capa base a la capa dos (Lightning Network), lo que reduce la necesidad de procesar cada transacción en la cadena de bloques.
2.  En la segunda capa, las transacciones se mueven mucho más rápido y más barato, creando un resultado atractivo para proveedores y usuarios, lo que refuerza el poder de la capa base al tiempo que permite el escalado enraizado en Bitcoin pero órdenes de magnitud más barato y rápido.

### ¿Dónde puedo obtener más información sobre Lightning Network?

No puedo proporcionar una guía completa de Lightning Network en este artículo. Sin embargo, puedo darle un resumen de los puntos clave y una lista de lugares a los que puede ir para aprender más y ampliar su comprensión. A continuación se muestra una breve lista que debería ayudarlo a comenzar.

-   [Lightning Labs](https://lightning.engineering/): una empresa fundada por la brillante ingeniera [Elizabeth Stark](https://twitter.com/starkness). Su proyecto en Github [es muy activo](https://github.com/lightningnetwork) y son muy conocidos en las redes sociales e incluso ocasionalmente [en las noticias](https://www.bloomberg.com/news/videos/2017-12-21/how-lightning-labs-is-building-on-top-of-bitcoin-video) .
-   [Blockstream](https://blockstream.com/): con el protocolo [Eltoo](https://blockstream.com/eltoo.pdf) Lightning Network, creado por una de las mayores empresas relacionadas con Bitcoin en el espacio; fundada por el [Dr. Adam Back](https://twitter.com/adam3us), un cypherpunk de la vieja escuela.
-   [Zap](http://zap.jackmallers.com/): una billetera Bitcoin alimentada por un rayo de [Jack Mallers](https://twitter.com/JackMallers), un ingeniero de software que codificó, probó y publicó con éxito muchos de los primeros vídeos de Lightning Network que se utilizan en la naturaleza.
-   [Lightning Network Bolt](https://github.com/lightningnetwork/lightning-rfc): este es un lugar para ver las especificaciones de Lightning Network propuestas o aceptadas por la comunidad. El código es todo de código abierto y las discusiones sobre las especificaciones ocurren en público.
-   Estadísticas de Lightning Network: puede obtenerlas de varios lugares, pero prefiero [P2SH en Grafana](https://p2sh.info/dashboard/db/lightning-network?orgId=1&from=now%2Fy&to=now%2Fy). Las dos estadísticas clave son el número de canales y la suma del valor del canal. Como puede ver, ambos están aumentando muy rápidamente, pero la red aún es joven (no hay datos antes del 18 de enero de 2018).
-   [Visualizaciones de Lightning Network](https://lnmainnet.gaben.win/) : una imagen vale más que mil palabras. ¿Cómo se veía Lightning Network en el pasado frente a ahora? Echar un vistazo…

### ¿Cómo funciona realmente Lightning Network?

Lightning Network es un protocolo peer-to-peer, que tiene muchas implementaciones de software diferentes, en las que los usuarios pueden transmitir bitcoin entre sí a través de una red de canales de pago. Los pagos se enrutan automáticamente de forma rápida y anónima mediante la [tecnología TOR](https://github.com/lightningnetwork/lightning-onion) (el enrutador de cebolla). En cualquier momento, un usuario puede cerrar su canal de pago y devolver sus fondos a la red principal (la capa base de Bitcoin).

### Considere el siguiente ejemplo, solo con fines ilustrativos.

Imagine que está en la casa de su amigo. Decide jugar un juego de póquer, por lo que todos ponen $5 y obtienen 50.000 fichas en diferentes denominaciones. Muchas manos de póquer se juegan usando esas fichas. Al final de la noche, todo el mundo se instala y se va a casa con (o sin) dólares. Cada mano representaría una transacción de Lightning Network (una transferencia de valor que su cónyuge no necesita saber), mientras que la cantidad de dólares con los que la gente se va a casa representaría una transacción en la red principal de bitcoin.

### Beneficios para proveedores y usuarios

Si tiene una pequeña empresa, digamos un puesto de café; entonces sabrá que la mayoría de sus clientes pagarán con tarjeta. La tarifa promedio que pagará es de alrededor del 3%, lo cual es doloroso si tiene un negocio con bajos márgenes.

Si pudiera hacer que la gente pagara en Bitcoin, usando Lightning Network, podría estar pagando 0.1%. Esa es la diferencia entre ir de vacaciones este año o no. Esa es la diferencia entre permanecer en el negocio durante la próxima recesión o no. Tiene mucha importancia.

Si es un “Joe promedio”, puede que también le guste esto. ¿Por qué? Bueno, a veces, el promedio de Joe compra en Target ( [TGT](https://seekingalpha.com/symbol/TGT?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) ) y Home Depot ( [HD](https://seekingalpha.com/symbol/HD?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) ). Usó su tarjeta como siempre lo hace, ¿cuál es el problema?

Bueno, [Home Depot](https://www.cnet.com/news/home-depot-offers-19m-to-settle-customers-hacking-lawsuit/) y [Target](https://www.nbcnews.com/business/business-news/target-settles-2013-hacked-customer-data-breach-18-5-million-n764031) fueron pirateados y tuvo que pasar horas en el teléfono y semanas enviando correos electrónicos y cartas tratando de arreglar su crédito porque los sistemas de PoS en esas tiendas estaban comprometidos. Seguro, eventualmente recuperó el dinero, pero tomó una eternidad y su crédito se hundió mientras tanto. Usando Bitcoin, eso no es un problema. ¿Por qué?

Porque cuando usa Bitcoin en la capa base, o en Lightning Network, no transmite ninguna información que pueda usarse para realizar una compra en una fecha posterior. Al deslizar su tarjeta de crédito en un sistema de punto de venta, el número de la tarjeta puede simplemente almacenarse y venderse más tarde en la web oscura. Con una transacción de Bitcoin, la información transmitida sólo es válida para esa única transacción. Incluso si alguien tuviera esa información, no podría usarla para hacer nada más.

Además, debido a que el proveedor no tiene que pagar tarifas de tarjetas de crédito del 3%, es posible que incluso bajen sus precios, lo que al Joe promedio también le gusta.

### Críticas a Lightning Network

Muchos han expresado su preocupación sobre Lightning Network. El grupo más grande de disidentes parece ser el grupo Bitcoin Cash ( [BCH-USD](https://seekingalpha.com/symbol/BCH-USD?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) ), que cree que el escalamiento en cadena será el futuro. Tengo mis reservas sobre esto, pero Lightning Network está siendo utilizado hoy por algunos de los primeros usuarios. Entonces, o funcionará o no, pero a juzgar por lo que ha estado sucediendo hasta ahora, el crecimiento y el entusiasmo en torno a la nueva tecnología parecerían sugerir que está funcionando.

### Lightning Network y descentralización

Una preocupación sobre Lightning Network es que [no estará descentralizada](https://medium.com/@jonaldfyookball/mathematical-proof-that-the-lightning-network-cannot-be-a-decentralized-bitcoin-scaling-solution-1b8147650800). Esto está por verse, pero me gustaría señalar que Bitcoin en sí no está completamente descentralizado. Naturalmente, debido a la ventaja competitiva, habrá grupos de concentración de muchas formas. Por ejemplo, los mineros acuden en masa a áreas con bajo costo de energía donde el clima tiende a ser más fresco. Los usuarios tienden a agruparse en torno a su aplicación o intercambio favorito, y el hardware más exitoso para almacenamiento en frío y minería tiende a atraer a las multitudes más grandes.

No creo que la *verdadera* descentralización sea posible en nuestro mundo. Nunca habrá una distribución perfectamente uniforme en un entorno competitivo. Pero creo que sigue siendo significativo que hoy en día tengamos sistemas más descentralizados y, por lo tanto, más robustos que los que están altamente centralizados. A veces, los sistemas centralizados son algo bueno, a veces, no tanto.

Si piensa en las carreteras y la red eléctrica, hay dos enfoques que podría adoptar para construir estas redes.

1.  Podría optimizar para obtener menos recursos.
2.  Puede optimizar la robustez.

Al planificar la red eléctrica de Estados Unidos, teníamos que tener en cuenta que si nos atacaban sería una debilidad estratégica que toda la red pasará por un solo punto. Este único punto de falla sería un objetivo óptimo para los adversarios. Al hacer que la red eléctrica esté menos centralizada, es posible tener áreas inactivas, pero posibilita desviar la energía en algunos casos y evitar una falla total del sistema.

Esta compensación cuesta más, necesita ejecutar más líneas, necesita nuevas formas de conectarse. Pero también proporciona protección contra interrupciones, que por supuesto necesitamos porque la electricidad es un sistema crítico para el mundo de hoy.

La red eléctrica y nuestro sistema de carreteras no están realmente centralizados y descentralizados;; son una mezcla de ambos. Cuando pensamos en cosas en un espectro como este, queda claro que el equilibrio de las compensaciones es la verdadera decisión de diseño y no debe tomarse a la ligera.

¿Qué tan centralizado es demasiado centralizado? Dejaré que la gente más inteligente que yo lo descubra. Sin embargo, sostengo que incluso con algunos grupos de centralización en Bitcoin, sigue siendo la red más robusta del mundo.

### ¿Otras criptomonedas funcionan con tecnología similar?

¡Sí! Escribí [sobre esto](https://seekingalpha.com/article/4182050-inverted-fibonacci-bat-wings-death-eth-usd-ta?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) brevemente en mi artículo sobre Etereum ( [ETH-USD](https://seekingalpha.com/symbol/ETH-USD?source=content_type%3Areact%7Csection%3Amain_content%7Cbutton%3Abody_link) ). Vitalik Buterin y Joseph Poon (de Lightning Network) han propuesto [Plasma](https://plasma.io/) , que podría hacer algo similar para la red Ethereum, aumentando la cantidad de rendimiento en órdenes de magnitud y permitiendo el intercambio de muchos tipos diferentes de tokens a la velocidad del rayo.

### Conclusión

Es difícil subestimar el potencial de Lightning Network. Acabo de arañar la superficie con este artículo; podríamos perdernos en la maleza con intercambios atómicos de cadena cruzada, cadenas laterales, etc., pero esa madriguera de conejo sería demasiado profunda hoy. A medida que Lightning Network crece, estaré observando de cerca, porque creo que el futuro de Bitcoin estará determinado en gran parte por lo que suceda con Lightning Network.
