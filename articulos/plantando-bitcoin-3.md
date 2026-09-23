---
titulo: "Plantando Bitcoin 3: Suelo"
autor: "dan-held"
traductor: "Jacky Rivero"
traductor_url: "https://twitter.com/imjackyrivero"
fuente_original: "https://www.danheld.com/blog/2019/1/6/planting-bitcoinsoil-34"
fecha: "2022-01-27"
original: "2018-10-29"
nivel: "basico"
series: ["dan-held-series","plantando-bitcoin"]
portada: "../imagenes/2022/01/fractal-59.jpg"
resumen: "Los Cypherpunks Introducción En mi último artículo, “Temporada”, cubrí el momento preciso en el que Satoshi plantó Bitcoin, la crisis financiera de 2008. En este artículo, cubro los Cypherpunks o el “Suelo” en el que plantó la semilla de Bitcoin, lo que le da la mejor oportunidad de supervivencia. Cypherpunks Enviar el documento técnico…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/plantando-bitcoin-3/"
---

> **Los Cypherpunks**

### Introducción

En mi último artículo, “Temporada”, cubrí el momento preciso en el que Satoshi plantó Bitcoin, la crisis financiera de 2008. En este artículo, cubro los Cypherpunks o el “Suelo” en el que plantó la semilla de Bitcoin, lo que le da la mejor oportunidad de supervivencia.

### Cypherpunks

Enviar el documento técnico de Bitcoin a la lista de correo de criptografía el 31 de octubre de 2008 fue la elección obvia. Este era el grupo adecuado para recopilar comentarios, el canal adecuado para interactuar. La lista estaba poblada predominantemente por los Cypherpunks \*, que eran activistas que abogan por el uso generalizado de la criptografía fuerte, como una ruta hacia el cambio social y político.

***\* "Cypherpunks" es un juego de palabras "cifrado”, de encriptación; y cyberpunk, un género de ciencia ficción.***

El grupo estaba compuesto originalmente por Eric Hughes, Tim May y John Gilmore. Al principio, las reuniones eran reuniones en persona en el Área de la Bahía de San Francisco, pero decidieron expandir el grupo a través de la lista de correo de criptógrafos que les permitiría comunicarse con otros Cypherpunks. La lista de correo era un lugar para intercambiar ideas libremente mediante el uso de métodos de cifrado, como PGP, para garantizar una privacidad total. Las ideas básicas detrás de este movimiento se pueden encontrar en el manifiesto Cypherpunk escrito por Eric Hughes en 1993. El principio clave que sustenta el manifiesto es la importancia de la privacidad y la finalidad en las transacciones. – PetriB

> ***“Por lo tanto, la privacidad en una sociedad abierta requiere sistemas de transacciones anónimos. Hasta ahora, el efectivo ha sido el principal sistema de este tipo “.** – Manifiesto de Cypherpunk*

Queremos tener la capacidad de asegurarnos de que otros no puedan utilizar la información del historial de nuestras transacciones en nuestra contra. Por ejemplo: una compra que indica que alguien es rico, una compra vergonzosa o una que lo sometería a spam o acoso. No queremos que nuestra compra financiera nos persiga más adelante. Queremos un punto final más allá del cual no tengamos que preocuparnos por futuras contingencias. En el mundo de los pagos, esto está estrechamente relacionado con el concepto de “finalidad” – idealmente queremos poder afirmar con certeza que en algún momento se ha realizado el pago, se ha liquidado la deuda y los fondos están seguros. Pero los desarrollos recientes han aumentado la capacidad de las partes más poderosas para recuperar fondos (a través de terceros confiables, fondos legales, etc).

Esperamos que las leyes existentes brinden protección contra estas dificultades. Sin embargo, podemos eliminar ese riesgo moral al no tener que confiar en terceros o adversarios más poderosos que pueden revertir las transacciones únicamente en función de sus capacidades. Esto es por lo que luchaban los Cypherpunks con la criptografía. Eran los “Hombres de palabras”, o intelectuales *anti-establishment* que sentaron las bases para que aparecieran individuos como Satoshi.

> ***“Las palabras de los intelectuales antisistema siembran las semillas de la revolución. Presentan ideas y, a veces, desacreditan al establecimiento, allanando el camino para que un líder carismático agrupe su pensamiento en un movimiento “.** – Tony Sheng*

Los primeros intentos de crear un sistema de transacciones anónimo fueron realizados por Cypherpunks en esa lista de correo de criptógrafos, que incluyen:

-   Adam Back, el inventor del hashcash, el sistema de Prueba de Trabajo (PoW) utilizado por varios sistemas anti-spam. Se utiliza un sistema PoW similar en bitcoin.
-   Nick Szabo, diseñó un mecanismo para una moneda digital descentralizada que llamó “bit gold”. Bit Gold nunca se implementó, pero se lo ha llamado “un precursor directo de la arquitectura de Bitcoin”.
-   Wei Dai, quien publicó “b-money”, un “sistema de efectivo electrónico distribuido anónimo”.
-   Hal Finney, quien creó el primer sistema de Prueba de Trabajo reutilizable antes de Bitcoin (y en enero de 2009 se convirtió en el primer destinatario de transacciones de la red Bitcoin). También fue un desarrollador del método de comunicación segura conocido como Pretty Good Privacy (PGP).
-   David Chaum, fundó DigiCash (1989) como una forma de “dinero electrónico” centralizado que desplegaba los mismos tipos de protocolos criptográficos (criptografía de llave pública) que respaldan la naturaleza de las transacciones bitcoin. A menudo se le llama “Chaumian eCash”.

Satoshi cita a muchos de estos Cypherpunks en el documento técnico de Bitcoin y hace referencia a su influencia en el desarrollo de Bitcoin en declaraciones públicas realizadas después del lanzamiento del código.

> ***“Bitcoin es una implementación de la propuesta b-money de Wei Dai … y la propuesta Bitgold de Nick Szabo”** – Satoshi Nakamoto*

De hecho, **¡Satoshi pensó que llegaba tarde a las criptomonedas!** Si bien los Cypherpunks habían intentado muchas veces modificar genéticamente una especie de dinero que sobreviviría, ninguno había tenido éxito.

> ***“Mucha gente descarta automáticamente la moneda electrónica como una causa perdida debido a todas las empresas que fracasaron desde la década de 1990. Espero que sea obvio que fue solo la naturaleza de control centralizado de esos sistemas lo que los condenó. Creo que esta es la primera vez que probamos un sistema descentralizado que no se basa en la confianza”**. –* [*Satoshi Nakamoto*](http://p2pfoundation.ning.com/forum/topics/bitcoin-open-source?commentId=2003008%3AComment%3A9493)

Había escrito el documento técnico para adaptarse a su público objetivo, los Cypherpunks. Es por eso que usa las palabras “efectivo electrónico”, “prueba de trabajo”, etc, que se usaban anteriormente como terminología en los otros documentos técnicos de Cypherpunk. Utiliza un ejemplo de comercio electrónico para que sea más fácil de entender para todos. Está elaborando una narrativa que resonará con los Cypherpunks, para que se interesen e involucren. **Bitcoin era el santo grial: había resuelto el problema de la finalidad y proporcionó una pequeña medida de privacidad.** La implementación del código fuente fue su especificación de producto.

> ***“Los* *detalles funcionales*** ***no se tratan en el documento, pero el código fuente estará disponible pronto”**. – Satoshi Nakamoto*

Las siguientes cosas no se describen en el documento técnico, pero están incluidas en el código fuente: límite de emisión de 21 millones, bloques de 10 minutos, límite de bloque de 1 MB. Esos eran componentes increíblemente importantes de Bitcoin. El documento técnico fue simplemente un adelanto.

> ***“Si el Libro Blanco de Bitcoin es la Declaración de Independencia, el Código Fuente es la Constitución”** – Pierre Rochard*

En las verdaderas formas Cypherpunk, la publicación del documento técnico de Satoshi (octubre de 2008) fue seguida rápidamente por el lanzamiento del código en enero de 2009. La noción de que las buenas ideas deben implementarse, no solo discutirse, es una parte muy importante de la cultura de la lista de correo.

> ***“Los cypherpunks escriben código. Sabemos que alguien tiene que escribir software para defender la privacidad y, dado que no podemos obtener privacidad a menos que todos lo hagamos, lo vamos a escribir. Publicamos nuestro código para que nuestros compañeros Cypherpunks puedan practicar y jugar con él. Nuestro código es de uso gratuito para todos, en todo el mundo… Sabemos que el software no se puede destruir y que un sistema muy disperso no se puede cerrar “**. – Manifiesto de Cypherpunk*

Es importante destacar que Satoshi no estrenó Bitcoin. Satoshi les dio a los Cypherpunks un aviso de dos meses antes de minar el bloque Génesis. Para demostrar justicia, incluyó una prueba de que no hay una marca de tiempo premine en el Bloque Génesis de la cadena de bloques de Bitcoin. Llevaba un fuerte mensaje político. Lo que estaba tratando de lograr estaba claro: estaban construyendo un nuevo sistema financiero. Bitcoin no era simplemente efectivo digital, era una alternativa a los bancos.

**"The Times 03 / Ene / 2009 Canciller al borde de un segundo rescate bancario" - Bloque Génesis**
