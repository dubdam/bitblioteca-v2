---
titulo: "Cuál es el límite de tamaño del bloque de Bitcoin"
autor: "bitcoin-magazine"
traductor: "Jacky Rivero"
traductor_url: "https://twitter.com/imjackyrivero"
fuente_original: "https://bitcoinmagazine.com/guides/what-is-the-bitcoin-block-size-limit"
fecha: "2022-01-27"
original: "2020-08-17"
nivel: "basico"
portada: "../imagenes/2022/01/fractal-70.jpg"
resumen: "El límite de tamaño de bloque de Bitcoin es un parámetro en el protocolo que limita el tamaño de los bloques de Bitcoin y, por lo tanto, la cantidad de transacciones que se pueden confirmar en la red aproximadamente cada 10 minutos. Aunque Bitcoin se lanzó sin este parámetro, Satoshi Nakamoto agregó un límite de…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/cual-es-el-limite-de-tamano-del-bloque-de-bitcoin/"
---

El límite de tamaño de bloque de Bitcoin es un parámetro en el protocolo que limita el tamaño de los bloques de Bitcoin y, por lo tanto, la cantidad de transacciones que se pueden confirmar en la red aproximadamente cada 10 minutos. 

Aunque Bitcoin se lanzó sin este parámetro, Satoshi Nakamoto agregó un límite de tamaño de bloque de 1 megabyte cuando todavía era el desarrollador principal del proyecto. Esto se tradujo en alrededor de tres a siete transacciones por segundo, dependiendo del tamaño de las transacciones.

En 2017, el límite de tamaño de bloque de Bitcoin fue reemplazado por un *peso* límite de bloque de 4 millones de “unidades de peso”. Esto cambió la forma en que se “cuentan” los datos en bloques: algunos datos pesan más que otros. Quizás lo más importante es que también representó un aumento efectivo del límite de tamaño de bloque: los bloques de Bitcoin ahora tienen un tamaño máximo teórico de 4 megabytes y un tamaño máximo más realista de 2 megabytes. El tamaño exacto depende de los tipos de transacciones incluidas.

### ¿Por qué es controversial el límite de tamaño del bloque?

El límite de tamaño de bloque es controvertido porque existe un desacuerdo sobre si dicho límite “debería ser” parte del protocolo de Bitcoin y, de ser así, qué tan grande debería ser.

Satoshi Nakamoto nunca especificó públicamente por qué agregó un límite de tamaño de bloque al protocolo de Bitcoin. Se ha especulado que pretendía que fuera una medida anti-spam, para evitar que un atacante sobrecargara la red de Bitcoin con bloques de grandes artificialmente, llenos de transacciones falsas. Algunos también han especulado que pretendía que fuera una medida temporal, pero no está claro cuán temporal o bajo qué condiciones previas se aumentaría o se levantaría el límite de tamaño de bloque. El código en sí que aplica el límite de tamaño de bloque ciertamente no fue temporal.

Un par de años después de que Satoshi Nakamoto dejara el proyecto, los desarrolladores y usuarios comenzaron a no estar de acuerdo sobre la temporalidad y la necesidad del límite de tamaño de bloque. A medida que la base de usuarios de Bitcoin creció, algunos creyeron que era hora de aumentar o levantar el límite de tamaño de bloque por completo, específicamente antes de que los bloques de Bitcoin comenzaran a llenarse de transacciones. Otros llegaron a creer que el límite de tamaño de bloque representa un parámetro de seguridad vital del protocolo y creyeron que no debería levantarse, o al menos, debería levantarse de manera más conservadora. Sin embargo, otros piensan que el megabyte establecido por Satoshi Nakamoto era en realidad demasiado grande y abogaron por una disminución del límite de tamaño de bloque.

Agregando más complicaciones, dado que Bitcoin está descentralizado, ningún grupo o persona en particular está a cargo de decisiones como aumentar o disminuir el tamaño del bloque. Los desacuerdos sobre cómo deben tomarse tales decisiones, quién debe tomarlas o si deben tomarlas, probablemente ha generado al menos tanta controversia como el límite de tamaño de bloque en sí, pero este aspecto del debate está fuera del alcance de este artículo. 

### ¿Por qué los bloques de Bitcoin no deben ser demasiado pequeños?

*Nota: se cuestiona casi cualquier cosa sobre el límite de tamaño de bloque de Bitcoin y los riesgos de que sea demasiado grande o demasiado pequeño, pero estos son algunos de los argumentos más generales.*

Si los bloques de Bitcoin son demasiado pequeños, la red de Bitcoin no puede procesar muchas transacciones. En términos generales, los defensores de un aumento del límite de tamaño de bloque (conocidos como “*big blockers*“) argumentan que esto puede tener dos consecuencias negativas.

### ¿Sin espacio suficiente?

En primer lugar, tener bloques de Bitcoin más pequeños significaría que no hay suficiente espacio para incluir las transacciones de todos los participantes en estos bloques, y la tarifa de transacción se convertiría en una “guerra de ofertas” para confirmar las transacciones, lo que haría que la mayoría de las personas dejaran de usar bitcoin. Esto podría conducir a un futuro en el que solo las instituciones similares a los bancos realicen transacciones entre sí, mientras que los usuarios habituales tienen cuentas en estas instituciones. Esto, a su vez, abriría la puerta a la banca de reserva fraccionaria, la censura de transacciones y más problemas con las finanzas tradicionales de los que muchos *bitcoiners* esperaban escapar.

### Distribución de la adopción

En segundo lugar, y esto es probablemente lo que muchos “*big blockers*” consideran una preocupación más urgente, los usuarios simplemente abandonarían Bitcoin por completo porque los bloques son demasiado pequeños. Quizás los usuarios cambiarían a una criptomoneda de la competencia o abandonarían por completo este tipo de tecnología.

### ¿Por qué los bloques de Bitcoin no deben ser demasiado grandes?

*Nota: se cuestiona casi cualquier cosa sobre el límite de tamaño de bloque de Bitcoin y los riesgos de que sea demasiado grande o demasiado pequeño, pero estos son algunos de los argumentos más generales.*

Los que se oponen a un aumento del límite de tamaño de bloque (conocidos como “*small blockers*“) argumentan que existen, en términos generales, tres riesgos si los bloques son demasiado grandes, cada uno de los cuales tiene varios “sub-riesgos”, así como matices.

### Mayor costo para los nodos de Bitcoin

El primero de estos riesgos es que los bloques más grandes aumentan el costo de operar un nodo de Bitcoin. Aumenta este costo de cuatro formas:

-   Aumenta el costo de almacenar la cadena de bloques, ya que la cadena de bloques crecerá más rápido.
-   Aumenta los costos de ancho de banda para descargar (y cargar) todas las transacciones y bloques.
-   Aumenta los costos de CPU necesarios para validar todas las transacciones y bloques.
-   Cuanto más grande es la cadena de bloques total, más tiempo se tarda en iniciar un nuevo nodo en la red: tiene que descargar y validar todas las transacciones y bloques anteriores.

Si el costo de operar un nodo de Bitcoin se vuelve demasiado alto y los usuarios tienen que (o eligen) usar clientes ligeros en su lugar, ya no pueden verificar que las transacciones que reciben sean válidas. Por ejemplo, podrían recibir una transacción de un atacante que creó monedas de la nada; sin conocer la historia completa de la cadena de bloques de Bitcoin, no hay forma de notar la diferencia. En ese caso, los usuarios solo descubrirán que sus monedas son falsas una vez que intenten gastarlas más adelante. Incluso si los usuarios validan que el bloque que incluye la transacción se extrajo lo suficiente (lo cual es común), los mineros podrían estar en confabulación con el atacante.

Quizás podría surgir un riesgo aún mayor si, con el tiempo, tan pocos usuarios eligen ejecutar nodos de Bitcoin que las monedas fraudulentas se notan demasiado tarde o no se notan en absoluto. En ese caso, el protocolo de Bitcoin en sí mismo queda sujeto efectivamente a los cambios impuestos por los mineros. Los mineros podrían ir tan lejos como para aumentar el suministro de monedas o gastar monedas que no poseen. Solo un ecosistema saludable con una proporción significativa de usuarios que validan sus propias transacciones evita esto.

En el libro blanco de Bitcoin, Satoshi Nakamoto reconoció los problemas mencionados anteriormente y sugirió que los clientes ligeros podrían protegerse a través de una solución técnica llamada “pruebas de fraude”. Desafortunadamente, sin embargo, no detalló cómo serían exactamente estas pruebas de fraude, y hasta ahora nadie ha podido averiguarlo. (De hecho, algunos de los desarrolladores de Bitcoin de la actualidad no creen que las pruebas de fraude sean viables).

### Centralización minera

El segundo riesgo de bloques más grandes es que podrían conducir a la centralización minera. Cada vez que un minero encuentra un nuevo bloque, envía este bloque al resto de la red y, en circunstancias normales, los bloques más grandes tardan más en llegar a todos los demás mineros. Sin embargo, mientras el bloque encuentra su camino, el minero que lo encontró puede comenzar inmediatamente a minar encima del nuevo bloque él mismo, lo que le da una ventaja para encontrar el siguiente bloque. Los mineros más grandes (o grupos de minería) encuentran más bloques que los mineros más pequeños, por lo que obtienen más ventajas. Esto significa que los mineros más pequeños serán menos rentables y eventualmente serán superados, lo que conducirá a un ecosistema minero más centralizado. Si la minería se vuelve demasiado centralizada, algunos mineros podrían terminar en una posición en la que pueden realizar un ataque de 51% a la red.

Dicho esto, este es probablemente el argumento más complejo y matizado contra los bloques más pequeños. Por un lado, incluso los grandes mineros tienen un incentivo contra la creación de bloques que son demasiado grandes: si bien pueden beneficiarse de una ventaja inicial, demasiada demora puede ir en detrimento de ellos, ya que un bloque competidor puede encontrar su camino a través de la red más rápido, y otros mineros minarán desde ese bloque en su lugar. También existen soluciones técnicas para acelerar la retransmisión de bloques, así como soluciones técnicas para limitar el daño de la centralización minera en sí, pero estas soluciones tienen sus propias compensaciones.

### Los subsidios para bloques inferiores podrían conducir a una menor seguridad de la red

El tercer y último riesgo de los grandes bloques es que podrían desincentivar a los usuarios para que no agreguen tarifas a sus transacciones. Siempre que el espacio de bloque sea limitado, los usuarios deben superar sus ofertas para que sus transacciones se incluyan en bloques, y a medida que disminuya el subsidio de bloque de Bitcoin, esto tendrá que convertirse en una parte más significativa de la recompensa de bloque para respaldar el modelo de seguridad de Bitcoin. Sin un límite de tamaño de bloque, este incentivo se elimina. (Si bien los mineros individuales aún pueden optar por incluir solo tarifas con una tarifa mínima, otros mineros aún tendrían un incentivo para incluir transacciones por debajo de ese umbral, disminuyendo así el incentivo de la tarifa después de todo).

Los lectores atentos habrán notado que este último argumento en particular funciona en ambos sentidos. Mientras que los “*big blockers*” ven las tarifas altas como un problema, ya que haría que Bitcoin sea menos atractivo, los “*small blockers*” ven las tarifas altas como algo positivo, ya que beneficiarían la seguridad de Bitcoin.

### ¿Los desarrolladores básicos de Bitcoin aumentarán alguna vez el límite de tamaño del bloque?

*Bitcoin Core* es el cliente de Bitcoin predominante, aunque no la única, que se utiliza en la red Bitcoin en la actualidad. Por lo tanto, muchos “*big blockers*” han estado buscando a los desarrolladores de *Bitcoin Core* para implementar un aumento.

De hecho, los desarrolladores de *Bitcoin Core* aumentaron el límite de tamaño de bloque, a través de la [actualización del protocolo *Segregated Witness* (SegWit).](https://bitcoinmagazine.com/technical/the-long-road-to-segwit-how-bitcoins-biggest-protocol-upgrade-became-reality) Al reemplazarlo por un *límite de peso* por bloque, los bloques ahora tienen un límite teórico de 4 megabytes y un límite más realista de 2 megabytes. Inteligentemente, esta fue una actualización del protocolo de bifurcación suave compatible con versiones anteriores, lo que significaba que los usuarios podían optar por el cambio sin dividir la red. Sin embargo, precisamente porque se trataba de una bifurcación blanda, y no una bifurcación dura como preferían muchos “*big blockers*“, a veces no “cuentan” este aumento como un aumento del límite de tamaño de bloque en absoluto.

Ciertamente, los desarrolladores de *Bitcoin Core* no han implementado un aumento del límite de tamaño de bloque a través de un hard fork, que es una actualización de protocolo incompatible con versiones anteriores. Esto requeriría el consenso de todos los usuarios de Bitcoin o posiblemente dividiría la red de Bitcoin en dos: una versión de Bitcoin con el límite de peso de bloque actual y una versión de Bitcoin con el límite de peso o tamaño de bloque aumentado. Los usuarios de la versión de Bitcoin con el límite de peso de bloque actual probablemente ni siquiera considerarían que la versión de Bitcoin es “*Bitcoin*” en absoluto; podrían referirse a ella como “*Bitcoin Core Coin*” o algo por el estilo.

Quizás lo más importante es que el grupo actual de contribuyentes de *Bitcoin Core* parece no tener ningún deseo de dictar las reglas del protocolo de Bitcoin, ni tampoco quieren dividir la red. Por lo tanto, es poco probable que implementen una bifurcación dura (para el límite de tamaño de bloque o de otro tipo) sin un amplio consenso en toda la base de usuarios de Bitcoin para dicha actualización de protocolo. Dada la naturaleza controvertida del parámetro tamaño o peso del bloque, es poco probable que ese consenso se forme pronto, pero podría suceder en el futuro.

### Soluciones alternativas

Existen algunas soluciones alternativas para aumentar el límite de tamaño de bloque de Bitcoin, como los Bloques de extensión, así como soluciones que podrían lograr algo similar, como las cadenas laterales de *“big blocks”*. Sin embargo, tampoco está claro si alguna de estas soluciones verá la luz del día pronto; el enfoque actual parece más dirigido hacia soluciones de escalamiento de “segunda capa” como la Red *Lightning*.

### ¿Está censurada la discusión de límite de tamaño de bloque de Bitcoin?

La respuesta corta es no.

En cuanto a una respuesta un poco más larga …

Durante el calor del debate sobre el límite de tamaño de bloque, una de las plataformas de discusión de Bitcoin más populares en Internet, el *subreddit* [*r/bitcoin*](https://www.reddit.com/r/Bitcoin/) centrado en Bitcoin, impuso una moderación torpe. Esta moderación tenía la intención de evitar que los usuarios del foro promovieran soluciones de *software* que rompieran el consenso antes de que la mayoría de los usuarios llegara a un consenso sobre la mejor manera de avanzar.

En ese momento, no era obvio para todos que el uso de dicho *software* podría conducir a una división de la red (un hard fork no compatible con versiones anteriores), y a menudo se anunciaba como si no pudiera. Siempre se permitió argumentar a favor de un aumento del límite de tamaño de bloque y/o una bifurcación dura sin promover directamente un *software* que rompiera el consenso.

Si esto constituyó una forma de “censura” tal vez esté en el ojo del espectador, pero lo cierto es que cualquiera que no esté de acuerdo con esta política es libre de comenzar o contribuir a la competencia de subreddits de Bitcoin, y esto es exactamente lo que sucedió. El *subreddit* [*r/btc*](https://www.reddit.com/r/btc/), en particular, se convirtió en una plataforma de discusión popular para aquellos que estaban a favor de un límite de tamaño de bloque para aumentar la bifurcación.

Además, *Reddit* es solo una parte relativamente pequeña de Internet y una parte aún más pequeña del mundo entero. Si bien hay algunas otras plataformas que han sido acusadas de censura similar (como el foro de [*Bitcointalk*](https://bitcointalk.org/) y la lista de correo de desarrollo de Bitcoin), es difícil negar que el debate tuvo lugar alto y claro en las redes sociales, sitios de noticias, conferencias, grupos de chat y mucho más. Cualquiera interesado en escuchar acerca de los diferentes argumentos, tenía todas las oportunidades para informarse e incluso aquellos a los que no les importaba, tenían dificultades para escapar de las consecuencias del debate.

Al final, aquellos que estaban a favor de un límite de tamaño de bloque para aumentar el hard fork no pudieron convencer a suficientes personas de su propuesta, y parece que algunos de ellos han canalizado su frustración por esta decepción en ira hacia un *subreddit* en particular y sus moderadores.

*(O tal vez, al escribir esto, Bitcoin Magazine es solo parte de una gran conspiración de encubrimiento. ¡Espeluznante!)*

### ¿QUÉ ES BITCOIN CASH? ¿QUÉ ES BITCOIN SV?

Cuando quedó claro que Bitcoin aumentaría su límite de tamaño de bloque (entre otras cosas) a través de la actualización del protocolo de bifurcación suave de *SegWit*, algunos “*big blockers*” decidieron avanzar con un límite de tamaño de bloque para aumentar la bifurcación dura, incluso sabiendo que estarían en una minoría y se dividieron en su propia red para convertirse en una nueva criptomoneda. Esta nueva red y la criptomoneda resultante se llama *Bitcoin Cash*.

Desde que *Bitcoin Cash* se separó de Bitcoin, esta red ha implementado varias actualizaciones más de bifurcación dura, algunas de las cuales, a su vez, llevaron a más divisiones en la red y nuevas criptomonedas. El más notable de ellos es *Bitcoin SV*, vagamente centrado en Craig Wright, uno de los hombres que (casi con certeza de manera fraudulenta) afirma haber estado detrás del seudónimo Satoshi Nakamoto. Tiene un límite de tamaño de bloque aún mayor que el de *Bitcoin Cash*.
