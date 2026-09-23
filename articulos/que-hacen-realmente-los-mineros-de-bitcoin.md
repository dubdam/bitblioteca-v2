---
titulo: "¿Qué hacen realmente los mineros de Bitcoin?"
autor: "nameless"
traductor: "Jacky Rivero"
traductor_url: "https://twitter.com/imjackyrivero"
fuente_original: "https://bitcoinmagazine.com/technical/what-are-bitcoin-miners-doing"
fecha: "2022-01-27"
original: "2021-06-27"
nivel: "basico"
portada: "../imagenes/2022/01/fractal-71.jpg"
resumen: "Antes de entrar en detalles, veamos rápidamente cómo han evolucionado los mineros. Al principio, el nivel de dificultad de la minería era extremadamente bajo (en breve veremos lo que eso realmente significa). En los primeros días de Bitcoin, cada bitcoin podía extraerse de forma rentable en una computadora personal simple (CPU). En menos de dos…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/que-hacen-realmente-los-mineros-de-bitcoin/"
---

**Antes de entrar en detalles, veamos rápidamente cómo han evolucionado los mineros.**

Al principio, el nivel de dificultad de la minería era extremadamente bajo (en breve veremos lo que eso realmente significa). En los primeros días de Bitcoin, cada bitcoin podía extraerse de forma rentable en una computadora personal simple (CPU). En menos de dos años, la gente comenzó a minar en tarjetas de procesamiento gráfico (GPU) porque, con la instalación de algún *software*, se adaptaban mejor a las velocidades de procesamiento requeridas. Es decir, pudieron realizar más cálculos por segundo a través del procesamiento en paralelo. Al igual que las CPU, solo fueron rentables durante unos años. En 2012, salió al mercado el primer minero ASIC (circuito integrado de aplicación específica).

El rendimiento del minero se mide en *hashes* por segundo o H/s. Esto se debe a lo que están haciendo: literalmente, aplicar la fuerza bruta para generar millones de funciones de hash válidas.  
  
Al momento de escribir este artículo, los mineros más rápidos del mercado tienen una calificación de más de [100 terahashes por segundo (TH/s)](https://www.asicminervalue.com/miners/bitmain/antminer-s19j-pro-100th), o 100 billones de secuencias hash por segundo.

Los ASIC son así de rápidos porque están diseñados específicamente con el propósito (minar bitcoins). Los ASIC se crearon para resolver una única función criptográfica *hash*, que, en el caso de Bitcoin, es SHA-256.  
  
Teóricamente, un minero de bitcoin puede extraer cualquier otra criptomoneda que también use SHA256, pero probablemente no sería rentable debido al alto consumo de energía de un minero.  
  
El requerimiento de consumir altos volúmenes de energía es lo que incentiva a los operadores mineros a buscar la energía más barata en el mundo, que con frecuencia es renovable o es energía varada.

Un bloque de Bitcoin consta de dos partes generales: un encabezado o cabecera de bloque, y una lista de transacciones. Dentro del encabezado hay información de *software*, la información de la transacción combinada, el *nonce*, el *hash* del bloque anterior y el objetivo. Todo el contenido del bloque está codificado. El *nonce*, un número aleatorio entre cero y 2³², se agrega al final de ese hash. Ambos combinados tienen hash una vez más.

Veamos cuál es el significado de la dificultad de la minería. Esta es la razón fundamental por la que las CPU y GPU ya no son rentables.

La dificultad está determinada por el objetivo, en forma de ceros a la izquierda. Debido a la teoría de la probabilidad, cuantos más ceros a la izquierda haya en el objetivo, más “raro” será el hash. Para demostrar con un ejemplo más identificable a la base 10 (el sistema numérico que usamos en la vida cotidiana,  es decir, un número de nueve dígitos sin dígito repetido (como 102345678) es mucho más raro que un número de la misma longitud con un dígito repetido.

Posteriormente, la dificultad aumenta a medida que se agregan más ceros iniciales al objetivo. Este cambio de dificultad es exponencial, pero ya estamos hablando de grupos masivos de posibles respuestas. El objetivo se calcula individualmente por nodos, según el período de dificultad anterior. Pero, como todos usan la misma cadena de bloques, todos calculan el mismo objetivo. O, más específicamente, todos calculan objetivos del mismo nivel de dificultad.

Si se pregunta por qué toma 10 minutos para probar 4,3 mil millones de *nonce* que son posibles *hashes*, se debe a que un buen minero puede hacer 100 billones de *hashes* por segundo, por lo que sería una observación muy astuta. Si ninguna de las 4.000 millones de posibilidades *nonce* da como resultado el *hash* objetivo, se debe ajustar alguna otra información para ajustar el *hash*. Se pueden agregar *nonce* adicionales, se pueden agregar o eliminar transacciones, o se puede ajustar la hora de inicio de la minería.

Los operadores mineros, si implementan varios mineros, con frecuencia usan un *software* específico para delegar operaciones a mineros individuales con el fin de ser más competitivos.

Con todo, Satoshi hizo un trabajo increíble al darse cuenta del aumento de la potencia informática a lo largo del tiempo. Parece haber cubierto todas las bases.
