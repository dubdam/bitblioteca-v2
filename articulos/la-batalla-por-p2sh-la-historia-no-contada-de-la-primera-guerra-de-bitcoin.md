---
titulo: "La batalla por P2SH: La historia no contada de la primera guerra de bitcoin"
autor: "pete-rizzo"
traductor: "Camo_Rai-PoW"
traductor_url: "https://twitter.com/Rai_PoW"
fuente_original: "https://bitcoinmagazine.com/technical/the-battle-for-p2sh-the-untold-story-of-the-first-bitcoin-war"
fecha: "2022-01-26"
original: "2020-12-04"
nivel: "experto"
portada: "../imagenes/2022/01/fractal-24.jpg"
resumen: "La saga de P2SH muestra la distintiva comunidad de desarrolladores de Bitcoin, la dificultad para realizar tales cambios y el tono de los debates de protocolo que se avecinan. “Retrasa la fecha dos meses. OP_EVAL todavía no está listo”. Era el veredicto que Gavin Andresen había trabajado durante tanto tiempo para evitar. Con una sola…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/la-batalla-por-p2sh-la-historia-no-contada-de-la-primera-guerra-de-bitcoin/"
---

La saga de P2SH muestra la distintiva comunidad de desarrolladores de Bitcoin, la dificultad para realizar tales cambios y el tono de los debates de protocolo que se avecinan.

> ***“Retrasa la fecha dos meses. OP\_EVAL todavía no está listo”.***

Era el veredicto que Gavin Andresen había trabajado durante tanto tiempo para evitar. Con una sola reprimenda enviada desde el teclado de Russell O’Connor, un esfuerzo de meses para actualizar Bitcoin, el primero tras la salida del fundador Satoshi Nakamoto, se estancó abruptamente antes de la implementación.

Como reveló O’Connor, el comando propuesto, anunciado por Andresen como el “camino más rápido” hacia carteras Bitcoin más seguras, podría explotarse para crear transacciones que enviarían el software a un *loop* computacional infinito en un intento de validarlas.

En resumen, se podría abusar de OP\_EVAL para bloquear los nodos de Bitcoin y, por lo tanto, la red de Bitcoin.

> **“Me tomó 70 minutos de búsqueda encontrar este error”**, escribió O’Connor, condenando un proceso que había fusionado –y casi empujado– código incorrecto al software vivo. **“Ustedes deben dejar de hacer lo que están haciendo y comprender realmente Bitcoin”**.

Fue el primer revés serio para Andresen, el nuevo líder del proyecto, que se apresuró a protestar. En su opinión, abandonar OP\_EVAL no solo desperdiciaría meses de codificación y revisión, dejaría a los usuarios sin herramientas para protegerse contra los troyanos y virus que luego saquearían sus monederos digitales.

Este era el núcleo del atractivo de OP\_EVAL: las carteras fáciles con múltiples firmas permitirían a los usuarios recuperar sus bitcoin, incluso cuando se perdieran las copias de seguridad; se podrían crear servicios para enviar alertas similares a las de un banco, disuadiendo el fraude y el robo; y mejor aún, todo esto podría lograrse en transacciones que se verían y se comportarían como esos usuarios conocían y entendían.

Pero las palabras de advertencia de O’Connor fueron suficientes para aquellos que habían visto validadas sus preocupaciones sobre el ritmo creciente del desarrollo.

> **“Me gustaría recordarles a todos que estamos jugando con una cosa de más de 20 millones de dólares”**, escribiría el desarrollador Alan Reiner. **“Hay más que una simple pieza de software en juego: todo lo que ingrese debe ser tan duro como un diamante”.**

El fracaso de OP\_EVAL tendría aún mayores implicaciones. Era cierto que Nakamoto había lanzado la primera moneda digital descentralizada del mundo, pero su promesa estaba lejos de cumplirse. A fines de 2011, pocos entendían su código y menos aún poseían la habilidad y la familiaridad para salvaguardarlo.

*¿Cómo deberían organizarse estos desarrolladores? ¿Qué responsabilidades tenían con los usuarios? ¿Y cómo promulgarían el cambio cuando no estuviera claro quién –si es que alguien– debería tener la última palabra?*

Estas preguntas pronto pasarán a primer plano en la primera gran batalla por el software de Bitcoin.

### Una sucesión poco ortodoxa

Los proyectos gratuitos y de código abierto suelen estar dirigidos por fundadores, quienes a su vez deben alinear los esfuerzos con los contribuyentes de quienes depende su trabajo. Aun así, cuando surgen disputas de dirección, están imbuidos de una autoridad natural para actuar como tomadores de decisiones para sus creaciones.

Bitcoin, al principio, no fue una excepción. Durante los primeros dos años de su existencia, Nakamoto desempeñó el papel de desarrollador líder y dictador benevolente. Como líder indiscutible de Bitcoin, promulgó hasta ocho cambios de protocolo sin parecerse mucho a un discurso más amplio \[1\]. Es decir, hasta que poco a poco se alejó del proyecto.

A finales de 2010, Nakamoto borraría su seudónimo del sitio web Bitcoin.org, dejando al veterano desarrollador de gráficos 3D Gavin Andresen para reclamarse como el “líder de facto” del proyecto \[2\].

La elección de palabras preferida por Andresen fue apropiada, ya que las circunstancias que rodearon esta transición fueron inusuales, equivalentes a un breve mensaje público, un traspaso privado de deberes y el intercambio de una clave que permite al usuario enviar un mensaje de alerta en todo el sistema.

Aun así, en ese momento, esto planteó pocas dificultades para el pequeño pero creciente grupo de desarrolladores de Bitcoin. La mayoría estaban preocupados por las soluciones críticas, y Andresen, el esposo de una profesora titular, tuvo el tiempo y el entusiasmo para dirigir el trabajo \[3\].

De hecho, había muchas necesidades urgentes – sincronización más rápida, mejores pruebas – pero el “aumento de informes de carteras robadas” y las “malas relaciones públicas” que causaron los robos rápidamente surgieron como una de las principales preocupaciones.

Durante un tiempo, fue un objetivo en el que toda la nueva banda de contribuyentes de Bitcoin parecían estar de acuerdo\[4\].

### Multifima básico

Afortunadamente, Nakamoto había proporcionado el plan de una solución. Como aprendería Andresen, el código de Bitcoin ya permitía a los usuarios crear transacciones seguras que solo podían gastarse cuando se firmaban con varias claves privadas \[5\].

Con firma múltiple, o multifirma (*multisig*) para abreviar, las llaves privadas podrían almacenarse en múltiples dispositivos, en extremos opuestos del mundo, o compartirse entre un usuario y un servicio de carteras, lo que significa que los *hackers* tendrían que comprometer múltiples objetivos para robar las monedas.

Enamorado de la idea, Andresen se convertiría en su primer campeón, escribiendo una súplica apasionada en la lista de correo para inspirar a los colaboradores a la acción.

> **“Mi mayor preocupación es que diremos, ‘Claro, solo tomará un par de días acordar cómo hacerlo bien’, y dentro de seis meses todavía no habrá consenso”**, escribió \[6\]. Y las carteras de las personas \[seguirán\] perdiéndose o siendo robadas”.

Las preocupaciones no carecían de peso: tal como lo implementó Nakamoto, la función *multisig* tenía importantes inconvenientes. El más urgente de ellos fue que las transacciones eran incompatibles con el formato de dirección estándar de Bitcoin y, en cambio, requerían direcciones mucho más largas.

Debido a esto, las transacciones que financiaban las carteras multifirma eran mayores y requerían tarifas más altas. Es más, estas tarifas debían ser pagadas no por la persona que recibía bitcoin con la billetera multifirma, sino por la persona que les enviaba bitcoin.

Debido a estas propiedades sub-óptimas, las transacciones de firma múltiple se designaron como “no estándar” en el software, lo que significa que no necesariamente se propagarían a los nodos de la red. Si un nodo recibió una transacción de firma múltiple, simplemente la ignoraría. Del mismo modo, no había garantía de que los mineros incluirían estas transacciones en bloques.

Si estuvieran incluidos, los nodos los aceptarían (las transacciones multifirma eran finalmente válidas). Pero en la práctica, la designación hizo que fuera casi imposible confirmar estas transacciones.

### *Enter* OP\_EVAL

Para desbloquear el potencial que vio, Andresen continuaría promoviendo un nuevo “código de operación” (op-code), un tipo de comando que los nodos podrían usar para decidir si los nuevos tipos de transacciones deberían ser válidos y cuándo.

Diseñado para adaptarse a transacciones más avanzadas como *multisig*, OP\_EVAL se apoyó en gran medida en los *hashes*, el truco criptográfico que codifica y comprime datos de forma determinista, pero irreversible, en una única secuencia de números.

Propuesto por [primera vez](https://bitcointalk.org/index.php?topic=46538.0) por el desarrollador seudónimo ByteCoin, la idea básica era que los usuarios pudieran aplicar *hash* a las instrucciones que detallaran las condiciones bajo las cuales se podrían gastar bitcoins más adelante (incluso hacia y desde carteras multifirma) al incluir este *hash* en una transacción. Básicamente, las monedas se enviarían “a” un *hash*.

Las condiciones requeridas para gastar posteriormente el bitcoin solo se revelarían cuando las monedas se gasten “desde” el *hash*. Un usuario de múltiples firmas pagaría por el tamaño adicional de la transacción cuando gastara las monedas, mientras que los datos adicionales requeridos suponían una carga menor en la red.

Como la propuesta recibió comentarios positivos, Andresen no perdió el tiempo y prefirió implementar OP\_EVAL más temprano que tarde.

“La seguridad es realmente alta en la lista de prioridades; me gustaría ver direcciones de Bitcoin seguras en las firmas de foros de la gente dentro de un año”, escribió \[7\].

Sin embargo, no todos compartían el sentido de urgencia de Andresen. OP\_EVAL sería una gran actualización en un sistema en vivo que ya tiene un valor de millones de dólares. Al otro lado del océano desde Andresen, un joven [Amir Taaki](https://bitcoinmagazine.com/articles/bitcoin-technology-worth-nothing-interview-dark-wallet-front-man-amir-taaki-1412722833) sugirió a los desarrolladores que se tomen un tiempo para revisar la propuesta.

“Parece bueno a primera vista”, escribió Taaki \[8\]. “Pero acelerar esto en la cadena de bloques probablemente no sea una buena idea … Bitcoin no explotará mañana, por lo que no hay una gran pérdida si se retrasan cambios trascendentales como estos”.

Para complicar aún más las cosas, los desarrolladores asumieron que agregar OP\_EVAL al protocolo representaría un desafío de coordinación significativo. En esencia, promulgarlo requeriría arriesgarse a que la cadena de bloques, el registro definitivo de todas las transacciones de Bitcoin, impuesta por el consenso compartido sobre sus reglas de software, pudiera dividirse en redes incompatibles.

Esto significaba que tan pronto como OP\_EVAL se pusiera en marcha, todos los usuarios tendrían que cambiar a una nueva versión del software y una nueva cadena de bloques, en lo que se denominó una actualización de “bifurcación dura” (*hard fork)*.

Si no se actualiza al unísono, los mineros podrían producir bloques “no válidos” sin saberlo. Peor aún, los usuarios pueden aceptar sin saberlo transacciones “inválidas”.

### Un nuevo tipo de bifurcación suave (Soft Fork)

Sin embargo, muy pronto Andresen se dio cuenta de que era posible apaciguar a sus detractores.

Como un truco ingenioso, descubrió que OP\_EVAL podría implementarse redefiniendo uno de varios códigos de operación inactivos originalmente incluidos por Nakamoto como marcadores de posición para comandos futuros.

Para sorpresa de todos, incluido Andresen, esto también sería compatible con los nodos que no se actualizaron para aceptar OP\_EVAL. Estos nodos verificarían que el *hash* coincidiera con las nuevas instrucciones, pero no las impondrían, sino que aceptarían las transacciones de forma predeterminada.

Siempre que la mayoría de los mineros hicieran cumplir las nuevas reglas, esto significaba que la nueva cadena de bloques sería considerada válida tanto por los nodos actualizados como por los no actualizados. Los nodos actualizados aceptarían la cadena de bloques porque se estaban aplicando las nuevas reglas, mientras que los nodos que no se actualizaron aceptarían la cadena de bloques porque no les importaban las nuevas reglas de ninguna manera.

Nakamoto ya había implementado tales actualizaciones compatibles con versiones anteriores, o “bifurcaciones suaves”, pero a medida que la red crecía en tamaño, los desarrolladores habían comenzado a preocuparse por la gran cantidad de personas que tendrían que participar en cualquier actualización.

Como era de esperar, la comprensión de Andresen de que esto podría evitarse fue bien recibida por otros colaboradores establecidos, con quienes rápidamente compartió la noticia.

**“Guau. El punto de Gavin de que \[OP\_EVAL\] se puede hacer sin una división me dejó alucinado “**, comentó Gregory Maxwell, reaccionando al descubrimiento en tiempo real \[9\]. **“Trae la champaña”**.

Con esto, los desarrolladores crearon un método aún más seguro para activar bifurcaciones suaves. Teorizaron que podrían realizar algo así como una encuesta para determinar cuándo una función tenía un apoyo suficientemente amplio de los mineros, que luego podrían usar para garantizar una actualización segura.

A los mineros se les pedirá que incluyan un poco de datos en los bloques que extrajeron para indicar que harían cumplir las nuevas reglas. Cuando la mayoría estuviera lista, se podría activar el cambio \[10\].

### El defecto fatal

Pero todo este trabajo fue deshecho por los hallazgos de O’Connor \[13\].

El resultado fue una división en facciones, con algunos sosteniendo que OP\_EVAL se estaba retrasando innecesariamente y otros argumentando que las soluciones rápidas propuestas afectarían ciertas propiedades deseadas del lenguaje de programación *script* esencial de Bitcoin \[14\].

Desarrolladores como Luke Dashjr, Pieter Wuille y Maxwell sugirieron alternativas que, como OP\_EVAL, utilizaron el concepto de enviar monedas “a” un *hash*. Pero el desafío seguía siendo conseguir esta lógica, a la que empezaron a denominar “pagar por *hash* de script” o “P2SH”, en Bitcoin como una bifurcación suave y evitar una división en la blockchain.

Los códigos de operación existentes solo podían llegar hasta cierto punto: los nodos no actualizados necesitarían aceptar transacciones que gastaran monedas provenientes de *hashes*, sin comprender las nuevas reglas.

Fue Andresen quien encontró un camino a seguir, y su solución P2SH específica no requeriría un nuevo código de operación en absoluto. Más bien, la idea de Andresen era que Bitcoin podría programarse para reconocer un cierto formato de transacciones y luego interpretar este formato de una manera poco convencional para validarlo usando nuevas instrucciones.

Cualquier nodo que no se actualice interpretaría el formato no convencional utilizando la lógica convencional. Al igual que con OP\_EVAL, los nodos no actualizados siempre considerarían válida la transacción. Esto significaba que P2SH podría implementarse como una bifurcación suave: siempre que la mayoría del poder hash hiciera cumplir las nuevas reglas, tanto los nodos antiguos como los nuevos estarían de acuerdo en la misma cadena de bloques.

La propuesta de Andresen pareció satisfactoria para la mayoría. “Parece… aceptable a primera vista”, respondió O’Connor \[15\]. Taaki, refiriéndose al enfoque poco convencional del código, dijo: “La idea es un truco… pero me gusta”.

En una reunión de desarrolladores posterior, el sentimiento se mantuvo y los asistentes acordaron implementar la propuesta P2SH de Andresen. Los mineros serían encuestados en la semana previa al 1 de febrero, y si la mayoría del poder de hash (55 por ciento) indicaba soporte, un cliente sería liberado para activar la bifurcación suave solo dos semanas después.

La paz duraría unos pocos días.

### ¿Por qué no utilizar USD?

Para romper el consenso estaría rompiendo estaría Dashjr, quien tuvo que abandonar la reunión temprano y solo más tarde se enteró de que la versión de Andresen de P2SH había sido el compromiso aceptado.

La naturaleza poco convencional de la solución de Andresen molestó a Dashjr, quien creía que complicaba el protocolo y traería consecuencias inciertas en el futuro. Le planteó el problema a Andresen, pero este último no estaba convencido de que sus preocupaciones merecieran un cambio de planes \[16\].

Despreciadas sus sugerencias, Dashjr iría en erupción en el foro público BitcoinTalk a mediados de enero, denunciando P2SH y acusando a Andresen de que estaba “por su cuenta” para apoyar el cambio \[17\].

> **“Gavin está obligando a todos los que utilizan el último código de Bitcoin a votar por \[P2SH\]”**, escribió. **“Si desea oponerse a este loco cambio de protocolo, deberá modificar su código fuente de BitcoinD o estará votando A FAVOR DE ÉL de forma predeterminada”**.

Por el matiz de sus objeciones, el tono descarado en el que se pronunciaron y sus acusaciones sobre Andresen, las respuestas al post fueron menos que positivas. En lugar de limitar el debate técnico a los desarrolladores, algunos percibieron que Dashjr intentaba incitar una violenta manifestación popular.

No ayudó que Dashjr fuera uno de los colaboradores más quijotescos del proyecto, conocido por sus largos argumentos en defensa de sistemas numéricos alternativos y una fuerte fe cristiana. Un usuario del foro dijo que los comentarios de Dashjr le hacían parecer “mentalmente inestable \[18\]”. Otro dijo que no quería molestarse con los detalles en absoluto; simplemente confió en Andresen \[19\].

En respuesta, Dashjr lanzó una objeción sostenida a la propuesta de P2SH por motivos filosóficos, disputando no solo sus méritos técnicos sino sus implicaciones para la gobernanza.

*“Si desea una moneda monárquica, ¿por qué no utilizar el USD de la Fed?”* Dashjr preguntó a sus detractores, solo para ser perseguido por otros que decían que era él quien estaba compitiendo por el poder \[20\].

Sin retroceder, Dashjr codificaría una versión alternativa de P2SH, llamada CheckHashVerify (CHV). CHV era esencialmente una implementación P2SH diferente, pero no requería una interpretación poco convencional de los resultados de las transacciones. En cambio, CHV agregó un nuevo código de operación que, como OP\_EVAL, podría “disfrazarse” como un código de operación temporal (*placeholder op-code*).

Pero para Andresen, era demasiado tarde para un mayor debate \[21\]. Furioso por el arrebato público, respondió con el suyo, escribiendo:

> ***“Luke, pruebas mi paciencia. Voy a alejarme del código durante unos días para calmarme antes de hacer algo estúpido”.***

### GENJIX se hace público

Como el diseño P2SH de Andresen (ahora denominado simplemente P2SH) fue visto en gran medida como una solución suficientemente buena preferida por el desarrollador principal del proyecto, Dashjr se encontró con pocos defensores.

Taaki tendría que ser la voz de la minoría para tomar en serio las preocupaciones marginales, pero no porque se opusiera a la solución de Andresen o necesariamente estuviera de acuerdo con la de Dashjr.

El desarrollador, que entonces tenía poco más de 20 años, ya era uno de los contribuyentes más abiertos de Bitcoin, y aunque aún no se había convertido en el anarquista que acaparaba titulares que hackeaba en sentadillas y viajaba con pistolas impresas en 3D, su visión del software como un movimiento antisistema ya lo había expulsado del círculo íntimo del proyecto.

Esto, a su vez, hizo que Taaki desconfiara del acelerado proceso de desarrollo del proyecto. Prefería que el proceso de toma de decisiones se tomara su tiempo e involucrara a una base de usuarios más amplia.

En su opinión, Bitcoin no fue bien atendido por una pequeña camarilla de desarrolladores que tomaban las decisiones. Taaki sintió firmemente que cualquier persona interesada en el proyecto debería estar al tanto de las compensaciones y, en la medida de lo posible, participar en la toma de decisiones.

> **“Prefiero que la gente tenga voz en el asunto, incluso si a los desarrolladores les resulta más difícil explicar sus decisiones”**, dijo a otros desarrolladores \[22\]. **“Me siento un poco preocupado por decirles a nuestros usuarios que así es como será, no tienes nada que decir y luego insultarlos”.**

Incluso si Taaki estuvo de acuerdo en que la diferencia entre las propuestas P2SH de Andresen y CHV de Dashjr era pequeña, insistió en que involucrar a los usuarios en el proceso de desarrollo era un ejercicio importante.

> **“Mi preocupación es que algún día Bitcoin se corrompa. Consideren este escrutinio adicional como una oportunidad para construir una cultura de apertura”**, argumentó.

A tal efecto, Taaki escribió una publicación de blog en la que presentaba las actualizaciones de P2SH y CHV y las diferencias entre las dos \[23\].

Los usuarios tenían una opción, era el mensaje de Taaki, y: **“La votación se basa en el poder de minería”**.

### Una situación j\*dida

Con su elección de palabras, Taaki había dejado al descubierto un elefante en la habitación. Era cierto, Nakamoto había promulgado bifurcaciones suaves, pero a fines de 2011, la red ya no operaba como lo hacía en esos primeros días.

Cuando Nakamoto publicó el documento técnico en 2008, asumió que la Prueba de Trabajo, PoW, por sus siglas en inglés, la proporcionarían los usuarios que contribuirían con los cálculos a través de computadoras personales. “PoW es esencialmente un voto por cada CPU”, había escrito Nakamoto.

Bajo este diseño, cualquier usuario podría ser un minero y asegurar la red proponiendo bloques, validando transacciones enviadas por pares y haciendo cumplir el código creado por los desarrolladores.

Pero en los años transcurridos desde el lanzamiento del software, los emprendedores habían dejado obsoleto este modelo. Desde que Lazlo Hanyesz (famoso por la pizza Bitcoin) había descubierto cómo generar bitcoins con unidades de procesamiento de gráficos más potentes, los especialistas habían estado ocupados convirtiendo la minería de un pasatiempo en una pequeña empresa.

Casi al mismo tiempo, Marek “Slush” Palatinus introdujo un método para permitir a los mineros juntar el poder de hash necesario para proponer bloques y compartir las ganancias. Esto hizo que la minería fuera menos una lotería y más una fuente estable de ingresos.

A finales de 2011, solo tres grupos (DeepBit, Slush Pool y BTC Guild) controlaban más de la mitad del poder de hash global. En lugar de una CPU, un voto, la mayoría de los “votos” ahora se concentraban en unos pocos operadores de grupos de minería, como si fueran representantes de sus ciber-constituyentes.

Para algunos, fue una prueba de que algo andaba mal en la red Bitcoin. “Veo \[un grupo de minería\] decidir un cambio en la red como una farsa de un voto”, argumentó Midnightmagic, una de las primeras mineras \[24\].

Para otros, la centralización minera fue una muleta desafortunada, una forma de hacer que una actualización de bifurcación suave sea más manejable y, por lo tanto, menos riesgosa. (Después de todo, una implementación segura ahora requería la participación de solo un puñado de operadores de grupos de minería).

Maxwell, por ejemplo, estaba más resignado a una realidad insatisfactoria \[25\].

> **“Si hubiera un retroceso no trivial, tanto los desarrolladores como los grupos retrocederían, pero nadie parece oponerse a ello ahora en ningún caso”**, respondió. **“Es un buen mecanismo para usar en el futuro… cuando, con suerte, no tendremos esta jodida situación en la que Bitcoin ya no está descentralizado”**.

### Vitar o no votar

Que las propuestas en conflicto de Andresen y Dashjr lleguen a incorporar puntos de vista opuestos sobre la gobernanza de Bitcoin solo complicaría las cosas.

Hasta entonces, los desarrolladores siempre se habían referido a la actualización de la bifurcación suave por venir como una especie de voto: los mineros podían hacer cumplir las nuevas reglas descritas por P2SH (u OP\_EVAL) con una mayoría de poder *hash*, por lo que una votación estaba destinada a medir la probabilidad de este resultado.

Pero si bien la terminología se había convertido en parte del léxico, esto omitió algunos matices técnicos. Al realizar una encuesta, los desarrolladores no preguntaban exactamente a los mineros qué pensaban de las nuevas reglas. Más bien, vieron esto como una forma de ver si los mineros estaban listos para garantizar una actualización segura.

Desde esa perspectiva, tenía sentido para los desarrolladores que solo se agregaría una propuesta al software que los usuarios y los mineros ejecutarían para hacer cumplir las reglas de la red.

*“El sistema Bitcoin \_NO\_ está listo para una elección mayoritaria. Ni una mayoría de poder de hash**, ni una mayoría de personas, ni una mayoría de dinero”*, argumentó Maxwell, molesto por la forma en que Taaki formuló la decisión como un voto \[26\].

Maxwell sentía firmemente que los “votos” de los mineros deberían limitarse, como estaban en el software mismo, a hacer cumplir el orden de las transacciones, no las reglas de toda la red.

> “**¿Qué pasa si una supermayoría, incluso el 100%, de los mineros actuales decide que el subsidio debería ser de 50 BTC para siempre? NADA. Los mineros que cambian esa regla en su software simplemente dejan de existir desde la perspectiva de la red Bitcoin”**, escribió.

Dashjr no estaba en desacuerdo con Maxwell, pero en la práctica era difícil para él ver cómo Bitcoin permanecería seguro si los desarrolladores impulsaran cambios sin el apoyo de los mineros.

> **“Los mineros pueden simplemente negarse a extraer transacciones P2SH para ser inmunes a los ‘cambios del equipo de desarrollo’”**, respondió \[27\]. **“Si los ‘desarrolladores’ bloquean a todos los mineros, ¿adivinen qué sucede? Ataques fáciles del 50%, ¡la red no está protegida! “**

Visto desde esta perspectiva, es más fácil entender por qué Dashjr creía que Andresen estaba abusando de su papel como desarrollador líder al intentar impulsar P2SH solo. Si un minero usara el software estándar para extraer un bloque, emitiría un “voto” a favor de P2SH automáticamente \[28\].

En respuesta, Dashjr escribió parches que incluirían su propuesta preferida en la “elección” del poder *hash*, introduciendo la opción para que los mineros voten tanto a favor como en contra de P2SH y CHV.

Aunque pocos mineros usaron el código, la oposición de Dashjr tuvo un efecto. Tycho, el operador de DeepBit, entonces el grupo de minería más grande de la red, comenzó a sentirse incómodo con su papel en la evaluación del código de la competencia.

Argumentando que estaba claro que aún no se había llegado a un consenso entre los desarrolladores, escribió: “No quiero convertirme en la única entidad que decida sobre esto \[29\]”.

### Punto muerto

Al rechazar la idea de que un grupo de minería podría, incluso por conveniencia, usarse para influir en una decisión de actualización, Tycho agregó otro giro al debate en cuestión. Sin su apoyo, que representa más del 30 por ciento de todo el poder hash, P2SH tendría dificultades para activarse.

A fines de enero, la primera ronda de votación P2SH estaba llegando a su fin y no parecía que fuera a alcanzar el umbral requerido. La actualización tendría que retrasarse, una realidad que frustraba no solo a Andresen, sino también a otros desarrolladores.

En IRC, Maxwell lamentó públicamente que no parecía haber un final a la vista para el punto muerto.

> **“Este meme de ‘prisa’ es una mierda, Gavin comenzó en la ruta \[*Pay-to-Script-Hash (P2SH)*****\] en, ¿qué, octubre?”** escribió \[30\]. **“Por lo que puedo decir, a menos que alguien establezca una fecha límite, este proceso nunca convergerá porque siempre habrá alguna otra persona cuya gran idea se haya quedado fuera”**.

Andresen atribuiría la culpa del retraso no al advenimiento de los grupos de minería, sino al operador de DeepBit, Tycho, personalmente. “En este momento, parece que una persona tiene suficiente poder *hash* para vetar cualquier cambio”, escribió \[31\].

Esto molestó a Andresen, quien vio la postura de Tycho como poco ética. *“Creo que está mal por su parte utilizar su posición como el mayor operador de pool para ir en contra del consenso general”*, escribió \[32\].

De hecho, incluso cuando Andresen llegó a ejercer presión pública, presionando a los usuarios para que solicitaran a sus grupos de minería que se actualizaran –y  ofreciéndose a reembolsar todos los fondos de DeepBit en caso de que P2SH generara una pérdida financiera– Tycho no estaba dispuesto a “votar” la propuesta \[33\].

Ante la demora, Andresen intentó acercar al público a la causa, persistiendo en su convicción de que la elección entre P2SH y CHV tendría poco impacto en los usuarios.

Andresen escribió:

> **“Todo lo relacionado con \[P2SH / CHV\] son ​​principalmente ingenieros que discuten sobre si es mejor usar un clavo, un tornillo o pegamento para unir dos piezas de madera. Cualquiera de las soluciones funcionaría y los usuarios normales no notarían ninguna diferencia \[34\]”.**

A juzgar por las respuestas en el hilo, los usuarios de Bitcoin aceptaron el marco de Andresen, culpando a Tycho por retener la bifurcación y presionándolo para activar.

Tycho, a su vez, se opuso ferozmente a la afirmación de Andresen. Incluso con el 30 por ciento del poder de *hash*, sabía que los mineros restantes podrían anularlo y no quería ser el factor decisivo.

### Segunda ronda

Dado que P2SH no ha logrado acumular suficiente apoyo de poder *hash*, Andresen se vería cada vez más obligado a discutir abiertamente la estrategia para su propuesta, y en particular comenzó a aceptar CHV como una alternativa potencial para salir del punto muerto.

Aun así, las respuestas trazaron una línea divisoria entre aquellos que creían que la elección entre P2SH y CHV era para que la hicieran los mineros, y aquellos que estaban a favor de una toma de decisiones más meritocrática.

*“En última instancia, los mineros son las ÚNICAS personas que tienen algo que decir sobre temas como este”*, argumentó el usuario de BitcoinTalk dooglus \[35\]. *“Son los únicos que deciden qué transacciones se bloquean”*.

El administrador del foro, Theymos, rechazó esta idea de plano. *“Los no mineros pueden rechazar bloques. Si suficientes clientes hacen esto, las monedas de los mineros perderán su valor. \[36\]”*

En cambio, Theymos propuso que cierto círculo interno de expertos debería participar en un debate de dos semanas y emitir una votación al final \[37\]. Ya sea por la sugerencia o por casualidad, Dashjr pronto creó una Wiki donde una lista de desarrolladores respetados podía expresar sus preferencias.

Durante los días siguientes, Maxwell, Thomas y Wuille indicaron que estarían felices de aceptar P2SH o CHV, aunque dejaron en claro que preferían P2SH. O’Connor y Dashjr estuvieron de acuerdo en que P2SH era aceptable, pero expresaron su preferencia por CHV \[38\].

Quizás como era de esperar, Andresen se aseguró de influir en la votación a favor de P2SH, registrando un rotundo “no” contra la propuesta de CHV.

Más importante, quizás, muy pocos mineros apoyaban a CHV. A mediados de febrero, P2SH contaba con el respaldo del 30 por ciento del poder de *hash*, mientras que la alternativa de Dashjr estaba estancada alrededor del 2 por ciento.

Durante una reunión sobre IRC, Dashjr dijo que estaba considerando la posibilidad de retirar CHV por completo, aceptando a regañadientes el dominio de P2SH \[39\]. En esa misma reunión, los asistentes acordaron establecer una segunda fecha límite de votación para el 1 de marzo.

A medida que se acercaba la nueva fecha límite, más mineros se reunieron detrás de P2SH, lo que acercó el soporte de poder de *hash* al umbral del 55 por ciento. Pronto, tanto Tycho como Dashjr no tuvieron otra opción que aceptar las preferencias de sus compañeros \[40\].

Con eso, Andresen anunció que la bifurcación suave se desplegaría y activaría dentro de los 10 días, y para el 1 de abril de 2012, se hicieron cumplir las nuevas reglas \[41\].

P2SH, la primera actualización de protocolo desde la partida de Satoshi, se había promulgado.

### Tormenta en un vaso de agua

El difícil proceso político que había llevado a la aprobación de P2SH continuaría teniendo un impacto duradero fuera del software en sí.

Al final, Andresen pudo implementar la solución que diseñó y favoreció. Si se puede decir que su liderazgo fue cuestionado en medio de la crisis, al final, estaba firmemente cimentado.

La opinión pública, indiferente a los detalles, se unió en gran medida en contra de las acciones de Dashjr y, en menor medida, de Taaki, considerándolas innecesarias e incendiarias \[42\]. Andresen fue tan lejos como para pedirle a Dashjr que dejara de contribuir a Bitcoin por completo, aunque parece que se retractó de esa amenaza o Dashjr simplemente la ignoró \[43\].

Mientras tanto, Maxwell se convirtió en uno de los “desarrolladores centrales” de Bitcoin, compartiendo acceso de escritura al repositorio del proyecto con Andresen y los colaboradores Wladimir van der Laan y Jeff Garzik.

Se había establecido el tono: en lo que respecta al desarrollo de Bitcoin, se recompensó una actitud pragmática de apoyo y se descartó a los contribuyentes contrarios. Si bien habían surgido diferencias ideológicas, permanecieron –y  posiblemente solo se afianzaron por– los procedimientos.

Con más usuarios acudiendo en masa a Bitcoin cada día, P2SH pronto pasó a la tradición, aunque en particular continuaría sirviendo como un punto de ignición en los desacuerdos entre los desarrolladores.

Recordando los eventos un año después en respuesta a otra crisis emergente, Andresen se jactaría de formas que sugieren que él creía que P2SH validaba su liderazgo y visión para el proyecto \[44\].

> ***“Se aumentará el tamaño del bloque”***, escribió, en respuesta a un video producido por el desarrollador Peter Todd que abogaba contra el aumento del límite a principios de 2013 \[45\]. ***“Tu video hará que mucha gente se preocupe por nada, exactamente de la misma manera que la propuesta de Luke-Jr \[CHV\] el año pasado no hizo más que causar una tormenta en un vaso de agua”.***

¿Cómo se deben tomar las decisiones para la primera moneda digital descentralizada? Si finalmente se hubiera formulado la pregunta, se necesitaría una guerra más amplia, aún años en el futuro, para resolverla…

---

### Referencias

\[1\] [https://blog.bitmex.com/bitcoins-consensus-forks/](https://blog.bitmex.com/bitcoins-consensus-forks/) 

\[2\] [https://soundcloud.com/twistartups/bitcoin-discussion-with-gavin](https://soundcloud.com/twistartups/bitcoin-discussion-with-gavin) 

\[3\] [https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/BANLkTimZ5j7%253D1G89uRO9f7fHPdmDMpLMqg%2540mail.gmail.com/#msg27661223](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/BANLkTimZ5j7%253D1G89uRO9f7fHPdmDMpLMqg%2540mail.gmail.com/#msg27661223) 

\[4\] [https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201106&viewday=13](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201106&viewday=13)

\[5\] [https://bitcointalk.org/index.php?topic=38903.0](https://bitcointalk.org/index.php?topic=38903.0)

\[6\] [https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/) 

\[7\] [https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/thread/CAJ1JLttqEnCjALadESmpntxSobD8Lj1zcXL4S7ghqdhyBrwVNw%2540mail.gmail.com/) 

\[8\] [https://bitcointalk.org/index.php?topic=46538.msg553903#msg553903](https://bitcointalk.org/index.php?topic=46538.msg553903#msg553903) 

\[9\] [https://web.archive.org/web/20131201200245/http://bitcoinstats.com/irc/bitcoin-dev/logs/2011/10/02](http://bitcoinstats.com/irc/bitcoin-dev/logs/2011/10/02) 

\[10\] [https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201112](https://sourceforge.net/p/bitcoin/mailman/bitcoin-development/?style=flat&limit=250&viewmonth=201112) 

\[13\] [https://sourceforge.net/p/bitcoin/mailman/message/28617066/](https://sourceforge.net/p/bitcoin/mailman/message/28617066/) 

\[14\] [https://sourceforge.net/p/bitcoin/mailman/message/28617066/](https://sourceforge.net/p/bitcoin/mailman/message/28617066/) 

\[15\] [https://sourceforge.net/p/bitcoin/mailman/message/28617230/](https://sourceforge.net/p/bitcoin/mailman/message/28617230/) 

\[16\] [https://bitcointalk.org/index.php?topic=58579.msg690145#msg690145](https://bitcointalk.org/index.php?topic=58579.msg690145#msg690145) 

\[17\] [https://bitcointalk.org/index.php?topic=58579.0](https://bitcointalk.org/index.php?topic=58579.0)

\[18\] [https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009](https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009) 

\[19\] [https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009](https://bitcointalk.org/index.php?topic=58579.msg690009#msg690009)

\[20\] [https://bitcointalk.org/index.php?topic=58579.msg690042#msg690042](https://bitcointalk.org/index.php?topic=58579.msg690042#msg690042) 

\[21\] [http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-14.html](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-14.html)  

\[22\] [https://buildingbitcoin.org/bitcoin-dev/log-2012-01-14.html](https://buildingbitcoin.org/bitcoin-dev/log-2012-01-14.html) 

\[23\] [https://bitcointalk.org/index.php?topic=61705.20](https://bitcointalk.org/index.php?topic=61705.20) 

\[24\] [https://buildingbitcoin.org/bitcoin-dev/log-2011-12-20.html](https://buildingbitcoin.org/bitcoin-dev/log-2011-12-20.html) 

\[25\] [https://buildingbitcoin.org/bitcoin-dev/log-2011-12-19.html](https://buildingbitcoin.org/bitcoin-dev/log-2011-12-19.html) 

\[26\] [https://bitcointalk.org/index.php?topic=61922.msg723476#msg723476](https://bitcointalk.org/index.php?topic=61922.msg723476#msg723476) 

\[27\] [https://bitcointalk.org/index.php?topic=61922.msg723520#msg723520](https://bitcointalk.org/index.php?topic=61922.msg723520#msg723520) 

\[28\] [https://bitcointalk.org/index.php?topic=58579.0](https://bitcointalk.org/index.php?topic=58579.0) 

\[29\] [https://bitcointalk.org/index.php?topic=61125.msg714231#msg714231](https://bitcointalk.org/index.php?topic=61125.msg714231#msg714231) 

\[30\] [http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-22.html](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-22.html) 

\[31\] [https://bitcointalk.org/index.php?topic=61125.0](https://bitcointalk.org/index.php?topic=61125.0) 

\[32\] [http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html) 

\[33\] [http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-23.html) 

\[34\] [https://bitcointalk.org/index.php?topic=61125.msg712822#msg712822](https://bitcointalk.org/index.php?topic=61125.msg712822#msg712822) 

\[35\] [https://bitcointalk.org/index.php?topic=61922.msg722860#msg722860](https://bitcointalk.org/index.php?topic=61922.msg722860#msg722860) 

\[36\] [https://bitcointalk.org/index.php?topic=61922.msg722874#msg722874](https://bitcointalk.org/index.php?topic=61922.msg722874#msg722874) 

\[37\] [https://bitcointalk.org/index.php?topic=61922.msg722833#msg722833](https://bitcointalk.org/index.php?topic=61922.msg722833#msg722833) 

\[38\] [https://en.bitcoin.it/w/index.php?title=P2SH\_Votes&oldid=23259](https://en.bitcoin.it/w/index.php?title=P2SH_Votes&oldid=23259) 

\[39\] [https://buildingbitcoin.org/bitcoin-dev/log-2012-02-14.html#](https://buildingbitcoin.org/bitcoin-dev/log-2012-02-14.html) 

\[40\] [https://bitcointalk.org/index.php?topic=68677.0](https://bitcointalk.org/index.php?topic=68677.0) 

\[41\] [https://bitcointalk.org/index.php?topic=71226.0](https://bitcointalk.org/index.php?topic=71226.0) 

\[42\] [https://bitcoin.stackexchange.com/questions/2682/why-are-the-majority-of-miners-not-voting-on-on-p2sh](https://bitcoin.stackexchange.com/questions/2682/why-are-the-majority-of-miners-not-voting-on-on-p2sh) 

\[43\] [http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-31.html](http://azure.erisian.com.au/~aj/tmp/irc/log-2012-01-31.html) 

\[44\] [https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890](https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890) 

\[45\] [https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890](https://bitcointalk.org/index.php?topic=189792.msg1967890#msg1967890)
