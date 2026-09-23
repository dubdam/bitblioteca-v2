---
titulo: "La anatomía de la Prueba de Trabajo"
autor: "hugo-nguyen"
traductor: "Jacky Rivero"
traductor_url: "https://twitter.com/imjackyrivero"
fuente_original: "https://bitcointechtalk.com/the-anatomy-of-proof-of-work-98c85b6f6667"
fecha: "2022-01-27"
original: "2018-02-11"
nivel: "medio"
portada: "../imagenes/2022/01/fractal-64.jpg"
resumen: "La Prueba de Trabajo (PoW) se inventó originalmente como una medida contra los correos electrónicos no deseados. Más tarde se adaptó para ser utilizado en efectivo digital [1]. Lo que realmente hace la minería de PoW bajo el capó es convertir la energía cinética (electricidad) en un bloque de contabilidad. Una máquina minera realiza repetidamente…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/la-anatomia-de-la-prueba-de-trabajo/"
---

La Prueba de Trabajo (PoW) se inventó originalmente como una [medida contra los correos electrónicos no deseados.](https://es.wikipedia.org/wiki/Sistema_de_prueba_de_trabajo) Más tarde se adaptó para ser utilizado en efectivo digital \[1\].

Lo que realmente hace la minería de PoW bajo el capó es convertir la energía cinética (electricidad) en un bloque de contabilidad. Una máquina minera realiza repetidamente operaciones hash hasta que resuelve un rompecabezas criptográfico. Todas las operaciones hash se descartan excepto el hash que lo resuelve.

Este pequeño hash, cuya computación requiere muy poca energía, es una representación directa de la enorme bola de energía que se requirió para producirlo. La “prueba” de que el bloque fue acuñado. Para reescribir el bloque, un atacante más tarde tendrá que gastar una cantidad aproximadamente equivalente de operaciones hash que originalmente se requirió.

Digámoslo de nuevo: la reversión requiere una cantidad equivalente de operaciones hash, no una cantidad equivalente de energía. Eso se debe a que el hash es solo una representación de la energía utilizada, no la energía en sí.

Con el tiempo, esta representación de la energía se vuelve menos y menos precisa, a medida que el hardware mejorado se vuelve más eficiente. La energía en sí no cambia, pero sus viejas representaciones “se filtran”.

Otra forma de visualizar este proceso es pensar en la minería de PoW como adjuntar pesos físicos a bloques virtuales. Con el tiempo, los bloques más antiguos se dañan y se vuelven más y más ligeros. Esto también reduce el peso total de la cadena, en igualdad de condiciones.

Bitcoin combate este proceso de desgaste creando constantemente nuevos bloques con nuevos pesos. Esto asegura que la punta de la cadena sea siempre pesada en el presente, protegiendo la integridad de toda la cadena. Cadena pesada = cadena segura.

**(Algunos han sugerido que "cadena más pesada" es una terminología mejor que "cadena más larga" de Satoshi. La cadena más larga puede ser muy engañosa cuando no nos referimos a la longitud en el sentido literal).**

SHA256 es la función de hash que respalda la minería de Bitcoin PoW. SHA256 protege el libro mayor para que no se vuelva a escribir. Un hash dentro (al minar), un hash fuera (para revertir). Esto es lo que le da a Bitcoin su propiedad de inmutabilidad \[2\].

Es asombroso cuando lo piensas. ¡Las operaciones hash dedican toda su existencia al propósito de asegurar el libro mayor de Bitcoin! Rara vez cualquier cosa en el mundo real tiene un 100% de dedicación y eficiencia. (por ejemplo: contraste esto con la gasolina y el motor de combustión).

En realidad, probablemente no sea el 100%, sino algo parecido. Porque la irreversibilidad se basa en que los resultados de hash sean uniformemente aleatorios (como cuando se lanza un dado normal), y los algoritmos no pueden simular realmente la aleatoriedad del mundo real.

Afortunadamente para nosotros, las funciones de hash como SHA256 han demostrado ser [suficientemente aleatorias](https://www.eecs.harvard.edu/~michaelm/postscripts/soda2008b.pdf), también son conocidas como “pseudoaleatorias”. SHA256 ha sido revisado y probado durante años, y tiene una rica literatura de investigación detrás. Así que no es algo de lo que debamos estar demasiado preocupados (todavía).

Fundamentalmente, creo que la idea de “adjuntar energía” a los bloques es la correcta y probablemente la única forma de simular la inmutabilidad virtualmente.

**El uso de energía quemada para respaldar un bloque nos permite ver la inmutabilidad de manera objetiva. Mientras que cualquier método no basado en la energía requiere en última instancia la interpretación** [**subjetiva de la inmutabilidad de alguien**](https://twitter.com/hugohanoi/status/953346280134029312)**. \[3\]**

Al adjuntar energía a un bloque, le damos “forma”, lo que le permite tener un peso real y consecuencias en el mundo físico. También podemos pensar en PoW como la magia que da vida a un montón de 0 y 1.

**En otras palabras, PoW es el puente entre lo digital y lo físico.**

Compare eso con algunos criptokitties que alguien crea, modifica y elimina como mejor le parezca. Su singularidad y existencia no están garantizadas ni son confiables.

Incluso si falla la variante actual de PoW, estoy seguro de que habrá otras formas de unir energía a un bloque.

En conclusión, la aplicación de PoW en blockchain podría resultar mucho más significativa y de mayor alcance que para lo que se inventó originalmente. PoW nos da inmutabilidad, lo que nos da dinero sin censura, lo que podría cambiar potencialmente la forma en que la sociedad se organiza. (Lea el maravilloso ensayo de Nick Szabo sobre [escalabilidad social para obtener más información al respecto](https://unenumerated.blogspot.com/2017/02/money-blockchains-and-social-scalability.html)).

---

#### Notas al pie

\* Esta es la parte 1 de la serie Bitcoin Fundamentals. Vea la serie completa aquí: parte 1, [parte 2](https://hugonguyen.medium.com/bitcoin-chance-and-randomness-ba49a6edf933), [parte 3](https://hugonguyen.medium.com/how-cryptography-redefines-private-property-34cd93d86036), [parte 4](https://hugonguyen.medium.com/bitcoins-incentive-scheme-and-the-rational-individual-dc20effa4715) y [parte 5.](https://hugonguyen.medium.com/bitcoin-two-parts-math-one-part-biology-b45ef48a0422)

\[1\]: La idea de usar PoW en efectivo digital podría haberse originado a partir de las propuestas b-money de Wei Dai y las propuestas bitgold de Nick Szabo a finales de los 90. Hal Finney creó la primera implementación de PoW en efectivo digital (RPOW) en 2004.

\[2\]: La inmutabilidad es un concepto relativo. Cuando decimos “inmutabilidad”, generalmente nos referimos a que es prácticamente inmutable, no absolutamente inmutable. Incluso el oro se puede sintetizar con suficiente energía.

\[3\]: Uno de esos métodos es la Prueba de Participación (PoS). Lea mi artículo sobre [Prueba de Participación](https://hugonguyen.medium.com/proof-of-stake-the-wrong-engineering-mindset-15e641ab65a2) para comprender sus dificultades y por qué podría ser inferior a la Prueba de trabajo.
