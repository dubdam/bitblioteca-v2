---
titulo: "En defensa de la prueba de trabajo y su (in)justo lanzamiento"
autor: "nic-carter"
traductor: "Jacky Rivero"
traductor_url: "https://twitter.com/imjackyrivero"
fuente_original: "https://medium.com/@nic__carter/in-support-of-the-proof-of-work-un-fair-launch-cd6e8f06358f"
fecha: "2022-01-26"
original: "2019-12-29"
nivel: "experto"
portada: "../imagenes/2022/01/fractal-36.jpg"
resumen: "Aclaratoria: no tengo ningún interés actual o futuro en el lanzamiento de una nueva criptomoneda, ni personal ni profesionalmente. Esta pieza está pensada generalmente como un experimento mental y NO significa el respaldo de ningún proyecto específico. No recomiendo ni apruebo la creación de nuevas criptomonedas de capa base. Prefacio La presencia de ASIC…"
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/en-defensa-de-la-prueba-de-trabajo-y-su-injusto-lanzamiento/"
---

*Aclaratoria: no tengo ningún interés actual o futuro en el lanzamiento de una nueva criptomoneda, ni personal ni profesionalmente. Esta pieza está pensada generalmente como un experimento mental y NO significa el respaldo de ningún proyecto específico. No recomiendo ni apruebo la creación de nuevas criptomonedas de capa base.*

### Prefacio

La presencia de ASIC en los sistemas de Prueba de Trabajo (*PoW*) siempre ha sido muy polémica. En la madurez, los ASIC mejoran la seguridad de la red (al obligar a los mineros a participar a largo plazo en el éxito del protocolo), pero en la fase de transición, el primer fabricante de hardware en construir ASIC tiene casi el monopolio de las monedas nuevas acuñadas. Esto puede llevar a la existencia de una forma informal de señoreaje: acuñación de dinero con descuento respecto a su valor de mercado. Los protocolos que se bifurcan con frecuencia también están expuestos a este riesgo; los desarrolladores tienen efectivamente la capacidad de determinar hacia qué función de PoW se moverá la cadena, dándoles la capacidad de monetizar su influencia sobre el protocolo. Esta es una forma de corrupción potencialmente muy insidiosa y perjudica la calidad de “justicia” por la que se conoce al *PoW*. Las cadenas de GPU también tienen la cualidad indeseable de ser “aptas para el *hash* agradable”, es decir, pueden ser atacadas alquilando *hardware* básico durante un breve período de tiempo. No se requiere un vínculo a largo plazo para extraer una moneda de minería de GPU, ya que el *hardware* es reutilizable y vendible.

Consciente de estos problemas, el año pasado comencé a pensar en cómo podría funcionar un lanzamiento de ASIC. No porque tenga interés en participar en uno, sino simplemente porque me parece interesante pensar en estas compensaciones. Esto culminó en este tweet:

> [!tweet] https://twitter.com/nic__carter/status/994203692827062272?ref_src=twsrc%5Etfw
> It’s only a matter of time (<12 months) until we see a fair launch with an exotic PoW released by a dev team that has also made ASICs that work exclusively with that PoW. No details of the algorithm will be released until genesis block.

  
*Dicho tweet traducido:* 

*Es solo cuestión de tiempo (<12 meses) hasta que veamos un lanzamiento justo con un PoW exótico creado por un equipo de desarrolladores que también han creado ASICs y que funcionan exclusivamente con ese PoW. No se darán a conocer detalles del algoritmo hasta el bloque génesis.*

Aproximadamente un mes después, *Obelisk* (una subsidiaria de *Nebulous*) publicó su propuesta para un servicio comercial, denominado *Launchpad*, que podría facilitar los lanzamientos de *PoW* con ASIC preconstruidos personalizados.

Puse mi tweet en este artículo para demostrar que he estado trabajando estas ideas durante mucho tiempo, y no estoy escribiendo esto de manera oportunista para brindar “apoyo moral” a ningún lanzamiento específico. He tenido este artículo principalmente escrito durante mucho tiempo, pero lo descuidé porque pensé que los lanzamientos de *PoW* estaban esencialmente desaparecidos y que no habría mucho interés en ellos.

De hecho, estaba equivocado con respecto a la línea de tiempo; no tengo conocimiento de que lanzamientos ocurrieron en un período de 12 meses después del *tweet*. Pero me ha llamado la atención que algunos equipos están contemplando lanzamientos similares hoy. Por lo tanto, sentí que mis pensamientos sobre este asunto podrían ser útiles. No para el beneficio de ningún equipo en particular, sino porque esto nos brinda un lienzo interesante para evaluar problemas que son críticos para la escalabilidad social y la seguridad de estas redes, ya sea Bitcoin u otras cadenas de PoW.

Si alguien tiene la intención de lanzar una nueva cadena de bloques pública, creo firmemente que utilizar una Prueba de Trabajo sin preminado es la mejor manera de hacerlo, por varias razones, a las que me referiré más adelante en el artículo. Pero siento que los lanzamientos de cadenas de bloques que utilicen GPU son cada vez más difíciles y arriesgadas. No puedo evitar que nadie lance una cadena. Pero creo que un análisis cuidadoso de las compensaciones podría alentar a los equipos a hacer las cosas de manera más responsable o, al menos, a explorar otras partes del espacio de diseño.

Por último, algunos de ustedes se sentirán molestos por mis reflexiones sobre cómo podría lanzarse una nueva cadena de bloques genérica. Si este es el caso, recomendaría simplemente cerrar la pestaña y desconectarse. Además, aunque creo que Bitcoin es suficiente en lo que respecta al dinero no estatal, tampoco estoy dispuesto a descartar permanentemente la posible aparición de alguna otra cadena de bloques de *PoW*. No veo por qué necesitaríamos otro ahora, pero me cuesta creer que Bitcoin sea la primera y la última cadena de bloques viable que se haya creado. Tampoco le tengo miedo a la competencia. Creo que Bitcoin tiene sus propios méritos únicos, y los lanzamientos más pequeños no compiten con él ni lo perjudican de ninguna manera. Dado que para mí es completamente posible que terminemos con otra cadena de *PoW* en algún momento, vale la pena pensar en cómo lanzarlas.

Para que quede absolutamente claro en esto: no estoy respaldando ningún lanzamiento o moneda específicos, ni siquiera nuevos lanzamientos de *PoW* en general. De hecho, generalmente desalentaría a cualquiera de lanzar una nueva cadena de bloques. Suelen ser despilfarros o pueblos fantasmas. Pero no descarto la posible existencia de una nueva cadena de bloques en algún momento en el futuro.

### Introducción

Los lanzamientos de nuevas criptomonedas se ven acosados ​​por una extraña paradoja: generalmente requieren una entidad única y autorizada para encabezar el desarrollo, administrar el proceso de lanzamiento y coordinar el desarrollo durante un período significativo durante su infancia. Por lo general, se requiere una inversión inicial considerable en R & D (siglas en inglés para investigación y desarrollo) para crear un protocolo diferenciado. Todas estas características tienden a requerir los esfuerzos organizativos y financieros de una sola entidad.

Pero, por supuesto, el respaldo de una entidad corporativa (o el modelo más sutil, pretendamos que no hay ninguna organización que mueve los hilos aquí) es un punto crítico de centralización. Esto significa que los adversarios tienen botones muy obvios que presionar si el protocolo se vuelve demasiado grande o disruptivo; en términos generales, cualquier persona hostil a la red tendrá una gran capacidad para interferir con ella. Además, estas entidades administrativas a menudo optan por retener no solo una gran fracción de la oferta, sino también la discreción sobre la toma de decisiones, las marcas registradas y los vetos sobre las futuras direcciones de desarrollo. Al igual que la cita de Engels sobre el “estado fulminante” como resultado final de una utopía socialista, el pretendido “camino hacia la descentralización” en los protocolos monetarios está más cerca de la retórica que de la realidad.

Para comprometerse verdaderamente a entregar el poder, los fundadores de estos proyectos deben sentirse cómodos con la austeridad y la eventual irrelevancia. A veces se dice que la segunda idea más brillante de Satoshi, detrás de la creación de Bitcoin, fue dejar el proyecto. Lamentablemente, prácticamente ningún fundador de criptomonedas desde entonces ha seguido su ejemplo, prefiriendo un lucro sucio y una oportunidad de unirse a la clase de Davos, junto con sus compañeros banqueros centrales.

Se han intentado numerosos modelos de financiación de protocolos a lo largo de los años: la premine de *bitcointalk*, la *ICO* (siglas en inglés para Oferta Inicial de Criptomonedas) más sofisticada, la recompensa de los fundadores, el preminado encubierto y el documento técnico retroactivo, la *instamine*, la bifurcación fusionada. Los puristas sostendrán que nada además de un lanzamiento de una justa Prueba de Trabajo (que no garantice señoreaje, ni siquiera para los desarrolladores) es suficiente para conferir al equipo fundador la legitimidad para crear un protocolo mundial.

Tienen un punto: es muy poco probable que, si una parte significativa del mundo cambia a un protocolo de criptomoneda neutral, los futuros compradores de la moneda encuentren aceptable enriquecer a los fundadores que se asignaron el 20% o más de esta moneda global de forma gratuita. El señoreaje, más generalmente, el sentimiento distintivo de injusticia o de ser engañado, deja un sabor particularmente desagradable en la boca. Esto, más que cualquier debilidad técnica, será la perdición de la mayoría de esos nuevos y atractivos protocolos de capa base con altas transacciones por minuto, respaldados por firmas de capital de riesgo. Estas no son startups: son dinero que compite en credibilidad, neutralidad, estabilidad institucional y equidad. El capital privado está concentrado y es injusto, pero no necesita usar acciones de Uber para comprar su pan de cada día. Para algo tan esencial como el dinero, la equidad es fundamental. Un lanzamiento profundamente injusto es un feo miasma que persiste de manera desagradable y envenena la autenticidad del proyecto.

El atractivo singular de un lanzamiento de Prueba de trabajo no se encuentra simplemente en la ventaja de distribución que le brinda la minería en el hogar (aunque esta es una característica potente y subestimada). No, la característica más importante del lanzamiento de la *PoW* justo es que asegura que es imposible adquirir monedas por debajo de la tasa del mercado. Puedes comprar las monedas en el mercado o con electricidad; nadie tiene derecho a un trato con información privilegiada. Compare esto con un equipo de desarrollo que prepara un *ERC20* y luego lo lanza al mercado durante un período de años. Esto se ve cosméticamente igual que un *PoW*. Pero no lo es, porque ese equipo pudo adquirir todas las monedas por un costo de $0. Sería similar a un mecanismo de Prueba de Trabajo, si el equipo de desarrollo tomara los fondos que recibieron a cambio de las monedas y los quemaran.

Por supuesto, la desventaja inherente al “lanzamiento justo” es el hecho de que es un desafío monetizar la red, especialmente al principio. Esto está bien si los desarrolladores están felices de trabajar de manera idealista o altruista. En Bitcoin, finalmente surgieron patrocinadores, ya que la red llegó a ser sistémicamente importante. Hoy en día, un conjunto rico y diverso de patrocinadores subsidia a docenas de desarrolladores centrales para que la cadena funcione sin problemas y trabaje en la infraestructura a largo plazo. Este es quizás el modelo ideal; pero Bitcoin tiene la ventaja de ser el primero, el más críticamente importante, y no tener patrocinadores de capital de riesgo con los que contar. Hoy en día, cualquier nueva criptomoneda lucha por distinguirse. Obtener suficiente tracción para sobrevivir gracias al patrocinio o donaciones es una tarea difícil. Y en lo que respecta a la investigación y desarrollo de carga inicial, esto es prácticamente imposible de financiar sin algún tipo de venta de derechos futuros sobre tokens de protocolo. Muchos señalarán aquí el estudio del caso de Grin. Habiendo tomado la decisión un tanto anacrónica de apuntar a un lanzamiento justo de Prueba de Trabajo dirigido a GPU, el equipo de Grin luchó por monetizar. Hasta ahora, las donaciones han sido relativamente escasas. Una advertencia para muchos.

Por supuesto, aquellos que se burlan con aire de suficiencia de las debilidades del modelo de lanzamiento justo tienden a hacerlo con la intención implícita de publicitar sus propios modelos de lanzamiento directamente explotadores. El que no tiene preminado, que lance la primera piedra. A pesar de que Grin ha luchado por obtener financiamiento hasta ahora, sus probabilidades de convertirse en un activo monetario significativo no se ven obstaculizadas por cuestiones de leyes de valores, por el riesgo de que el fundador sea arrestado o por el desencanto de la comunidad al ser explotados por los capitalistas de riesgo que los abandonan en la primera oportunidad (para aquellos que no me creen, lea las barajas de recaudación de los cripto-fondos de financiamiento dedicados a estrategias de token. Ese lenguaje sobre el bajo “tiempo de liquidez”, es un código para decir “planeamos salir de nuestras posiciones de token en el venta pública, porque queremos asegurar una rentabilidad sin riesgo y deshacernos de este activo lo antes posible”).

Entre  2014 y 2018 las Ofertas Iniciales de Criptomonedas (*ICO*, por sus siglas en inglés) fueron, en su mayor parte, un instrumento financiero desastroso. Nunca me he encontrado con una sola persona que sienta que se emitió de manera responsable al público. Una vez que dejaron de ser accesibles para el público en general, perdieron su única ventaja: distribución amplia y sin permisos (tenga en cuenta que esta es una característica nativa de *PoW*). Los problemas con las ICO, especialmente aquellas que optan inmediatamente por un modelo de autoridad de Prueba de Participación (en lugar de un arranque de *PoW*, como Ethereum optó sabiamente), son numerosos:

-   Las personas con información privilegiada pueden comprar su propia venta colectiva y obtener de forma encubierta una fracción arbitrariamente alta de la oferta de forma gratuita (porque también pueden recaudar los fondos comprometidos con la venta colectiva). 
-   Los compradores pueden obtener tokens a precios arbitrariamente bajos, ya que no se crean de manera costosa a través de una prueba de trabajo, sino que se convocan de la nada. Por lo tanto, las rondas privadas que son anteriores a las ventas públicas a menudo consisten en señoreaje puro.
-   Los tokens a menudo terminan siendo una mezcla extraña de un contrato de inversión informal y un token de arcade para desbloquear recursos de red. Esto hace que la especulación desplace el uso y conduce a teorías muy confusas sobre la acumulación de valor.
-   Los tokens vendidos al público (o de forma indirecta, por Telegram) se parecen mucho a los contratos de inversión en las jurisdicciones más sensibles, y esto tiende a hacer que los emisores estén sujetos a las leyes de valores, les guste o no.
-   Los emisores que retienen una gran fracción de la oferta tienden a conservar la autoridad en la red, especialmente si se opta por un modelo de Prueba de Participación (*PoS*). Esto dificulta el camino hacia la descentralización de la autoridad, ya que los emisores tienden a resistirse a deshacerse de su parte de la red.
-   Los primeros patrocinadores pueden obtener porciones desproporcionadas de suministro de forma esencialmente gratuita y luego retener sin costo esa ventaja a perpetuidad si la red sigue un modelo de *PoS*. Esta es una fuerza potente que enfría la dispersión de tokens, ya que los apostadores no están obligados a vender. En *PoW*, por el contrario, los mineros deben gastar e invertir constantemente para retener una autoridad de red proporcional. En *PoS*, retener la participación es simplemente el costo de ejecutar un servidor.

Mi punto central es este: el principal desafío en la administración de un nuevo producto monetario no es técnico. Por supuesto, su *blockchain* debe tener características técnicas convincentes. Pero, en última instancia, la dificultad radica en escalar el muro de la indiferencia. Al principio, nadie se preocupaba por su sistema. En la madurez, necesita decenas y posiblemente cientos de millones de personas a las que cuidar. Si les da a los primeros inversores acceso con descuento a una fracción significativa de la oferta, y luego les otorga poderosos derechos anti-dilución (mientras espera que los futuros individuos usen su red como capital de trabajo y toleren alguna dilución, que de hecho, subsidie a los primeros compradores que apuesta pasiva), corre el riesgo de crear un sistema claramente injusto en el que los ganadores son una función de la prehistoria arbitraria de la cadena.

Atraer a alguien a una red como esta me parece profundamente improbable. ¿Por qué tu cadena? ¿Por qué no un lanzamiento justo equivalente, donde todos los propietarios trabajaron por sus monedas, en lugar de recibir una asignación a través de alguna proximidad al equipo fundador?

Pero las ICO, las criptomonedas con preminado y las monedas de impuestos del fundador tienen una ventaja crucial: la capacidad de subsidiar el trabajo en el protocolo, incluso antes de su lanzamiento. Suponiendo ingenuamente que, en 2019, no se han lanzado ya todos los protocolos de criptomonedas que alguna vez existirán, se podría llegar a decir que subsidiar el trabajo en un protocolo antes de su lanzamiento podría ser una propiedad deseable. Entonces, ¿se pueden mezclar y combinar las cualidades deseables del lanzamiento de una moneda mientras se evitan las peores? Ciertamente creo que sí. Repasemos tres modelos populares:

Oferta Inicial de Criptomonedas y modelo de tesorería 

Pros

Contras

El equipo de desarrolladores puede financiarse a sí mismo a través de los ingresos de la tesorería y las ventas futuras de los tokens retenidos.

La forma más conveniente de lanzar una nueva cadena; la seguridad se puede subcontratar de Ethereum u otro protocolo de contratos inteligentes si la moneda es un token

Las preventas permiten plazos de entrega más prolongados, ya que los equipos de desarrolladores pueden trabajar durante años antes del lanzamiento gracias a la solidez de las asignaciones de tokens en el futuro.

El equipo fundador tiene total discreción sobre todos los parámetros del sistema.

Prácticamente garantizado para ser considerado un contrato / garantía de inversión. Riesgo regulatorio inmenso y posiblemente prohibitivo.

La oferta tiende a concentrarse; ventanas de ventas más cortas significan menos compradores y el equipo tiende a retener una participación. La Prueba de Participación (*PoS*) es además concentrativa.

Las asignaciones a menudo se venden por adelantado con importantes descuentos; esto introduce señoreaje masivo en el sistema y hace que el lanzamiento sea fundamentalmente injusto.

Las personas con información privilegiada o el comprador de preventa pueden retener su parte del sistema a perpetuidad si PoS está presente; los tokens de PoS son equivalentes a derechos permanentes de antidilución.

Existen importantes asimetrías de información; los desarrolladores controlan virtualmente todos los aspectos del sistema y la divulgación en general deficiente.

Los usuarios deben comprar tokens para participar; sin medios de adquisición sin confianza en terceras partes.

El emisor puede comprar su propia ICO, obteniendo una ventaja injusta (y encubierta).

Ciertamente hay más contras que pros en este caso. En los Estados Unidos, la venta de derechos sobre una criptomoneda, especialmente para el público en general, parece estar fuera del favor de nuestros reguladores de valores. No es recomendado. Además, otorgar a los primeros patrocinadores o grandes tenedores derechos antidilución permanentes y económicos entorpece la dispersión de los tokens, lo que limita su alcance. Tenemos datos bastante buenos sobre esto, gracias a la transparencia que nos ofrecen las *blockchains*. (Me encantaría ver un trabajo serio que compare la dispersión de la propiedad en las cadenas de *PoS* frente a las cadenas de *PoW*. Si es un investigador que está interesado en abordar esto, póngase en contacto con nosotros. Tengo datos).

“Lanzamiento justo” de Prueba de Trabajo (*PoW*)

Pros

Contras

La cadena tiene una seguridad de *PoW* aceptable y bien entendida en el lanzamiento, incluso si la emisión no vale mucho.

El 100% de las tarifas / emisión se destina a la seguridad; el protocolo es más eficiente para convertir la emisión en seguridad de *PoW*.

La emisión es justa y el señoreaje no existe; suponiendo un mercado de hardware competitivo y márgenes de minería estrechos, todas las unidades deben comprarse a su valor nominal (ya sea minado o en casas de cambio).

La falta de monetización o protocolo de los desarrolladores significa que es más probable que los proyectos atraigan a desarrolladores de software libre entusiastas e intrínsecamente motivados.

El estilo de lanzamiento otorga a la cadena un barniz permanente de legitimidad; es el más justo de los métodos conocidos para lanzar un nuevo dinero.

Riesgo muy bajo de ser calificado como un contrato / valor de inversión.

Se beneficia de la dispersión natural de PoW, especialmente si se lanza en una cadena compatible con GPU.

Los usuarios pueden adquirir tokens sin procesos KYC (siglas en inglés para conoce a tu cliente) o registro en casas de cambio.

El conocimiento previo de la función hash se puede monetizar a expensas de los inversores.

Si mina en un hardware básico, es probable que la seguridad sea débil en el lanzamiento.

Los cambios arbitrarios en la función PoW antes del lanzamiento generan sospechas de que los desarrolladores se confabulan con los fabricantes de ASIC.

Los desarrolladores no tienen la capacidad directa de monetizar su trabajo; su incentivo es monetizar sutilmente a través de los pagos de los grupos de presión, haciendo cambios favorables en el protocolo.

Los desarrolladores tienen un incentivo para buscar alquileres a través de su discreción sobre los atributos básicos, incluida la función hash.

La red depende en última instancia del patrocinio para la monetización de los desarrolladores.

Un clásico. El modelo Bitcoin, Litecoin, Monero y Grin. Un enfoque sensato, pero difícil de arrancar el apoyo, y que depende de la financiación o el patrocinio de la comunidad para obtener apoyo continuo. Muy efectivo y difícil de matar si puedes lograrlo, pero requiere una gran cantidad de construcción de comunidad para obtener tracción. Estos parecen volverse cada vez menos viables con el tiempo, especialmente a medida que han crecido las apuestas financieras. Esperaría que prácticamente todos los lanzamientos de GPU de hoy estén sujetos al riesgo de personas con información privilegiada con conocimiento previo del algoritmo que crea ASIC de forma encubierta. 

“Lanzamiento justo” de Prueba de Trabajo (PoW) y recompensas a los fundadores

Pros

Contras

Las probabilidades de ser calificado como un valor son posiblemente más bajas que las de una Oferta Inicial de Criptomonedas.

Existe un presupuesto para financiar proyectos de infraestructura / bienes públicos a largo plazo.

Las reglas del juego se entienden completamente y, si se cumple el contrato social, las entidades que reciben las recompensas financiadas por el protocolo pueden ser consideradas legítimas por los usuarios.

El impuesto al desarrollo es equivalente a la concesión lenta exigida por el protocolo; el ritmo es altamente auditable, a diferencia de los modelos de tesorería en los que no se cumple con la adjudicación reclamada.

La existencia del presupuesto discrecional permite recompensas de protocolo de uso más general, en lugar de solo seguridad.

Existe cierto señoreaje, que podría afectar los sentimientos de equidad.

La motivación intrínseca de la comunidad de FOSS para contribuir al proyecto puede ser canibalizada: ¿por qué trabajar gratis cuando otros desarrolladores reciben recompensas basadas en el protocolo para los trabajadores de una manera socialmente escalable?

Verificar la calidad del trabajo realizado para la financiación del protocolo no es una operación trivial; mucho más diferente que verificar una colisión hash exitosa (trabajo realizado en una versión vanilla de PoW)

Los desarrolladores / administradores tienen un incentivo para buscar alquiler a través de su capacidad para influir en los pagos del fondo de desarrolladores.

La existencia de “dinero suelto” podría crear dependencia de la ayuda en las organizaciones beneficiarias, que se reconfiguran para explotar este grifo de dinero.

Una “fuga” de seguridad a través de la asignación del presupuesto de seguridad a objetivos no relacionados con la seguridad.

Este es este modelo híbrido, pionero de Zcash. Esto es esencialmente equivalente a una prima adquirida. Alinea mejor los incentivos que una prima pura, ya que las asignaciones no se desbloquean durante varios años. Sin embargo, la propuesta tiene sus propios problemas: en el caso de Zcash, el protocolo ha estado plagado de controversias sobre si el administrador debería recibir fondos adicionales derivados del protocolo. El grifo del señoreaje es muy difícil de apagar, una vez activo.

En este punto, es posible que se pregunte por qué no me limito a agitar los lanzamientos justo de PoW en su versión vainilla. Según esta rúbrica, parecen claramente superiores. Pero no están exentos de problemas. Creo que vale la pena ser realista sobre los lanzamientos de PoW con equipos de GPU. Veamos un par de estudios de casos recientes.  

### Por qué los lanzamientos de la justos para minería de GPU podrían ser cosa del pasado

Como alguien que siguió el lanzamiento de Grin bastante de cerca, debo admitir que se sintió como una última incursión nostálgica en una era anterior. Tuve una punzada decididamente proustiana al ver cómo se desarrollaba el proceso. Como si hubiera sumergido mi magdalena en el té y me hubiera transportado a los días de gloria de los lanzamientos de PoW de 2012 a 2014.

Los rumores que rondan los “$100 millones en vehículos de propósito especial respaldados por capitales de riesgo” fueron hiperbólicos, pero el lanzamiento ciertamente tuvo problemas. Inicialmente con la esperanza de seguir siendo resistentes a la minería de ASIC a perpetuidad, los desarrolladores finalmente optaron por un enfoque pragmático por fases para cambiar de minería de GPU a ASIC, imaginando una transición lenta a una red dominada por ASIC, pero con la esperanza de comenzar con una minería de GPU más accesible. Hubo un período de minería de GPU, pero algunos mineros ahora me informan que los ASIC, o al menos los hardware más eficientes (FPGA), han comenzado a tomar una parte significativa del hashrate, algo por delante del cronograma deseado. Esto no es exactamente un fracaso, pero ilustra la enorme dificultad inherente a la noción de la resistencia a los ASIC.

Está creando una enorme recompensa para que cualquiera pueda anticipar el cambio de Prueba de Trabajo o presionar a los desarrolladores para obtener un resultado favorable. Los desarrolladores de Grin titubearon un poco sobre el modelo definitivo de PoW (esto, naturalmente, fue una discusión bastante tensa) y esta ambigüedad provocó mucho rechinar de dientes y esfuerzos de cabildeo. Habría sido mucho más eficiente, en general, si no se hubieran asignado recursos para presionar a los desarrolladores para obtener una función hash favorable. En última instancia, los desarrolladores tuvieron mucho cuidado para hacer que la cadena fuera hostil a los ASIC al inicio, pero no pudieron detener el flujo. No optaron por los ASIC de inmediato debido a una visión ingenua de que las GPU dominarían la historia temprana de Grin (y la dificultad para coordinar este modelo con un equipo distribuido no corporativo), pero aparecieron los ASIC (o al menos los FPGA) de todas formas.

La mayoría de las cadenas resistentes a los ASIC se ven afectadas por esta misma dificultad. Crean efectivamente una recompensa masiva para que los equipos creen FPGA o ASIC y vuelen por debajo del radar, con la esperanza de que no sean descubiertos. 

Podrías imaginar que los equipos futuros aprenderían de esto y morderían la bala, emitiendo protocolos para minería con ASIC de inmediato.

### Una propuesta

Habiendo divagado lo suficiente, compartiré lo que tengo en mente. Revisemos para qué nos gustaría optimizar:

-   Nos gustaría limitar el señoreaje; es decir, queremos que prácticamente todos los participantes tengan la capacidad de obtener los tokens a precio de mercado, con relativamente pocas excepciones a esta regla.
-   Queremos que el período de distribución sea lo más largo posible.
-   Si ser uno de los primeros patrocinadores de la red confiere una ventaja, debería ser temporal y erosionarse con el tiempo.
-   Mantener una posición de autoridad en el sistema debería ser costoso; no debería ser gratuito ejercer influencia a perpetuidad.
-   Ser uno de los primeros patrocinadores de la red no debería otorgarle derechos permanentes contra la dilución.
-   Queremos que el sistema funcione según las leyes de valores existentes en los Estados Unidos: queremos separar el contrato de inversión del activo emitido por el protocolo.
-   Queremos que la red sea segura al inicio (desde una perspectiva cripto-económica).
-   Queremos que el equipo fundador pueda despojar significativamente de poder y autoridad a la red.
-   Queremos inculcar un sentimiento de justicia y minimizar las asimetrías de información que rodean el lanzamiento de la red.

Creo que prácticamente todas estas cualidades se pueden obtener en un modelo que no se ha probado antes:

### El modelo de preventa de ASIC

La idea básica es:

1.  Algunos desarrolladores crean un nuevo protocolo de criptomonedas.
2.  Para financiar esto, venden derechos no sobre tokens, sino sobre ASIC físicos.
3.  Junto con socios confiables de la cadena de suministro, fabrican estos ASIC antes del lanzamiento.
4.  Estos ASIC se venden a inversores o, mejor aún, a la comunidad de usuarios que quieren apoyar explícitamente a la red en sus inicios. Posiblemente sean valores, aunque aquí no he hecho el análisis legal. (No estoy seguro de esta parte). Estas ventas se registran como ingresos para la corporación emisora.
5.  Los ASIC admiten una función hash personalizada (que no está siendo empleada por ninguna otra cadena de bloques).
6.  Los desarrolladores mantienen esta función hash en secreto hasta el día del lanzamiento.
7.  En el lanzamiento, se revela la función hash y comienza una carrera entre los fabricantes de ASIC para construir la segunda generación de ASIC.
8.  En 4 o 6 meses, el primer lote se vuelve obsoleto a medida que se fabrican nuevos ASIC y se erosiona el monopolio temporal sobre el suministro emitido que disfrutaban los primeros patrocinadores.
9.  Con el tiempo, la ventaja que disfrutaban los primeros mineros se desvanece.
10.  Los desarrolladores se comprometen a no cambiar nunca la función del PoW.
11.  Los desarrolladores tienen pocas monedas o ninguna y pueden salir del proyecto si es necesario o adoptar un enfoque de código abierto comercial / de Red-Hat para administrar la cadena, sin retener ninguna autoridad explícita en el protocolo.

Consideremos los pros y los contras del modelo.

Pre-venta de ASICs 

Pros

Contras

La cadena tiene una seguridad de PoW muy buena y bien entendida en el lanzamiento, incluso si la emisión no vale mucho.

Los activos similares a valores y monetarios se separan; riesgo regulatorio reducido.

Los desarrolladores pueden financiar sus esfuerzos con un pago único.

La falta de un subsidio continuo pagado por la cadena lo transforma en un modelo convencional de software libre, motivación intrínseca para contribuir sin canibalización.

Los compradores de ASIC asumen el riesgo y los costos operativos de monetizar su privilegio temporal; los ASIC se deprecian, por lo que los derechos de señoreaje son temporales.

Los desarrolladores no pueden subvencionarse a sí mismos de forma continua.

Los inversores de ASIC deben tener un alto grado de confianza en la recuperación de la inversión a partir de seis meses de emisión.

Se debe confiar en que el equipo de desarrollo y el proveedor de hardware mantendrán en secreto la función hash hasta el lanzamiento

La cadena debe lanzarse como un sistema PoW.

El equipo de desarrollo y los proveedores de hardware deben demostrar que no han fabricado de forma convergente más hardware del que afirman.

La emisión durante los primeros seis meses es injusta por definición; no se garantiza que los participantes posteriores en el mercado de hardware se comporten de manera justa.

Creo que las principales ventajas del modelo de preventa de ASIC son las siguientes:

### Obtienes seguridad de nivel ASIC al inicio

Esta es una gran ventaja sobre los lanzamientos justos de GPU para Prueba de Trabajo. A medida que aprendemos más sobre el modelo de seguridad de PoW, queda claro que todas, excepto las redes más grandes minadas por GPU, son simplemente inseguras. Ethereum es probablemente una excepción porque representa una fracción tan grande de las GPU del mundo y no se pueden vender ni alquilar en cantidades suficientes. Aparte de la dificultad estructural de adquirir suficiente poder hash, esto significa que atacar Ethereum con éxito haría que el valor de las GPU en todo el mundo se depreciara, lo que es un fuerte desincentivo para cualquier atacante. Sin embargo, aparte de Ethereum, la mayoría de las monedas extraídas de GPU están expuestas a este riesgo de que se utilice hardware alquilado para atacar la cadena, y hemos visto abundantes ejemplos de esto. Si cree que el hardware dedicado ayuda con la seguridad, entonces preferirá el modelo ASIC. Este enfoque le brinda una seguridad férrea desde el principio.

### El elemento similar al contrato de inversión está firmemente desenredado de las monedas reales

En el caso de una Oferta Inicial de Criptomonedas, tiene tokens que se venden previamente a los compradores. Si se entiende que son contratos de inversión o valores, esto potencialmente compromete todo el suministro de tokens e inhibe su capacidad para circular en los intercambios. En un intento por eludir esto, se ha argumentado que el contrato de inversión cubre solo los derechos para tokens futuros, y que los tokens en sí mismos no son los sujetos del contrato de inversión. Es bajo este razonamiento que se entiende que el ETH en la preventa probablemente haya sido objeto de un contrato de inversión, pero las unidades en circulación de ETH en el momento de la entrega de las cadenas de bloques no eran en sí mismas valores. Realmente no compro esta distinción; por decir lo menos, la encuentro como una tortura. Me resulta más fácil distinguir los dos.

En el caso de la preventa de ASIC, se distingue muy claramente el contrato de inversión de las propias monedas. Si hay algo que sea similar a un título valor, serían los ASIC vendidos a los inversores (aunque, como se señaló, es muy posible que estos ni siquiera sean valores, ya que los usuarios finales tienen que operarlos y alimentarlos con electricidad, obviando los ‘esfuerzos de la punta de terceros de Howey). Las monedas reales en sí mismas están totalmente claras, en mi opinión, ya que son emitidas por el protocolo en la forma de un lanzamiento justo convencional. Creo que tenemos abundante evidencia de que la Comisión de Bolsa y Valores de Estados Unidos no entiende que los tokens de lanzamiento justos sean valores. Esto brinda a los usuarios potenciales garantías realmente convenientes de que la negociación del activo no se limitará repentinamente a los lugares de negociación de tokens de valores. Esta es una de las mayores ventajas del modelo.

### Obtiene distribución del PoW y los desarrolladores pueden financiarse a sí mismos con una capacidad limitada

Las ventajas distributivas del PoW, hasta la fecha, no han sido muy bien documentadas, pero tengo una fuerte intuición de que conducen a una mejor dispersión de la oferta. En relación con el lanzamiento de un protocolo de PoW vainilla, los desarrolladores también pueden financiar los costos administrativos y de investigación y desarrollo involucrados en el lanzamiento de una nueva cadena. Y no están violando la ley de valores. ¡Genial!

### Obtienes un período de distribución arbitrariamente largo

Muchos han notado que, en lo que respecta a los nuevos dineros, la existencia de contingencia temporal en la distribución introduce una arbitrariedad que limita la dispersión de la moneda. En otras palabras, las emisiones cortas (algunas ICO terminaron en minutos) garantizan que la oferta estará altamente concentrada. Las emisiones más largas dan a todos la oportunidad de obtener las unidades de monedas. Esto fue parte de la intuición detrás del ICO de EOS de un año, que fue una idea bastante inteligente (aparte del hecho de que los monederos de venta colectiva tuvieron salidas continuas durante ese tiempo, lo que llevó a conspiraciones sobre el reciclaje de fondos del tesoro de vuelta a la ICO). Si lo piensas bien, la venta de tokens EOS por un año de fue algo similar a un lanzamiento de PoW (con la excepción de que las monedas que contribuyeron a la venta colectiva no se quemaron). La Prueba de Trabajo le brinda una fase de distribución extendida sin permiso, aunque la recompensa de bloque en descomposición significa que el nuevo suministro es mucho más abundante desde el principio. La emisión de Bitcoin durará más de 100 años, pero más del 80% de todos los Bitcoins ya se han extraído.

Al comparar un lanzamiento de PoW con una ICO genérica, está muy claro que el acceso sin permiso en una ICO recién lanzada es imposible. Tezos se situó a horcajadas en esta transición, luego de una venta colectiva sin KYC, luego con un proceso posterior de KYC posterior para desbloquear al usuario Tezzies. Me imagino que todas las ICO posteriores (en la medida en que ocurran) seguirán su ejemplo. La diferencia con PoW es que está adquiriendo monedas de un protocolo. Si bien los proveedores de ASIC pueden solicitar KYC, en términos generales, la minería es un entorno mucho menos autorizado que las ICO o las ventas colectivas. Agregue la realidad de que la electricidad está mucho más disponible a nivel mundial que el acceso a los mercados de capital, y el PoW parece muy atractivo. Un protocolo que vende monedas a cambio de electricidad durante un largo período de tiempo es un medio extremadamente potente para emitir un activo a una audiencia global. Nadie ha ideado una forma mejor hasta ahora.

### Las reglas del juego son muy claras

Uno de los mayores problemas con las cadenas de PoW en la actualidad es la ambigüedad, especialmente en torno al cambio de funciones hash. Cuando tiene ambigüedad, tiene debate y cabildeo, y la posibilidad de que los desarrolladores exploten su estado privilegiado dentro del sistema. Esto es generalmente desastroso y reduce la escalabilidad social, así como la credibilidad del sistema. Si se descubre que un pequeño grupo de personas está abusando de su protocolo de acceso para monetizar, la credibilidad del sistema se ve comprometida. Una alternativa es simplemente configurar la función PoW y comprometerse a no cambiarla nunca (esto es esencialmente por lo que Bitcoin ha optado y por qué Bitcoin nunca debería cambiar su PoW a menos que ocurra algo catastrófico). Eso es lo que exige este modelo. Sin debate; sin cabildeo; sin explotación encubierta.

### La ventaja inicial se deprecia con el tiempo, proporcionando al sistema una dispersión natural

A diferencia de algo como un token de Prueba de Participación (PoS) vendido en una preventa, el equilibrio inicial de poder en el sistema de lanzamiento de ASIC cambia drásticamente con el tiempo. Inicialmente, unos pocos tienen derechos de cuasi monopolio sobre el suministro. Pero esta es una ventaja temporalmente limitada, y la aparición de nuevos ASIC, o incluso simplemente el paso del tiempo, y la depreciación que eso conlleva, erosiona esa ventaja inicial. Quiero enfatizar que considero que esta es una buena característica. Demasiado poder otorgado a las primeras partes interesadas en la red, además de la capacidad de retener este poder, sin costo, a perpetuidad, es una característica disgénica. Esto inhibe enormemente la dispersión de la base del soporte. La presencia del PoW es útil aquí. Induce la venta constante por parte de los mineros, reduciendo su privilegio próximo al protocolo. No se puede decir lo mismo de las apuestas. Si bien en el caso del lanzamiento de ASIC tenemos unos pocos privilegiados desde el principio, su ventaja se deprecia rápidamente.

Unámos todo en un gráfico grande para comparar cómo los métodos de lanzamiento alternativos afrontan las diversas desventajas.

 

Contrato de inversión y monedas combinadas

Contrato de inversión y monedas combinadas

El emisor retiene una fracción desproporcionada de la oferta

Alcance del señoreaje

Los inversores conservan los derechos permanentes de anti-dilución.

Venta a inversores poco sofisticados

La seguridad de la cadena es débil al inicio

Los desarrolladores no pueden financiar su trabajo

Incentivos de los desarrolladores para sacar la moneda

Los iniciados pueden beneficiarse del acceso al protocolo

Lanzamiento justo 

(Bitcoin, Litecoin, Monero)

No, sin contrato de inversión

Perpetuo en algunos casos; generalmente, muy largo

El emisor no tiene la capacidad de adquirir ni retener el acceso a grandes fracciones de suministro a bajo costo

No presente

No

Nada se vende

Generalmente, sí, especialmente con el lanzamiento de una GPU.

Generalmente no. Se requiere patrocinio o modelo de Red Hat

No, los desarrolladores no tienen acceso con descuento a las monedas

En ciertos casos, p. Ej. con conocimientos previos de PoW algo

Preventa de ASICs

(condiciones especificadas en el artículo)

No, los ASIC se venden, no se venden monedas

Similar a un lanzamiento justo

Los emisores no tienen acceso privilegiado al suministro; el monopolio temporal temprano se vende a los inversores. 

De alcance limitado y temporal. No está presente después de la depreciación de los ASIC iniciales

No, los ASICS son costosos de operar, depreciarse y volverse obsoletos

A discreción del emisor; los emisores podrían vender ASIC solo a inversores sofisticados.

No, siempre que la cadena sea un monopolista en su función hash.

Los desarrolladores pueden financiar los esfuerzos iniciales con los ingresos de ASIC, pero el financiamiento es de una sola vez

Solo antes del lanzamiento, pago único al inicio

Solo de forma estructurada y transparente, e incluso así solo mínimamente

Recompensa a los fundadores y lanzamiento con PoW

(Zcash, Beam)

Poco claro pero magro si

Similar a un lanzamiento justo

Sí, y los emisores pueden presionar de manera persuasiva para aumentar su participación.

Sí, siempre que exista la recompensa del fundador

Sí, o al menos se puede configurar de esa manera

Nada se vende explícitamente al público

Depende, pero probablemente sí, ya que no hay ASIC precompilados

Los desarrolladores toman parte de los derechos de señoreaje

Sí, ya que se pagan de forma continua.

Si, explícitamente

ICO + PoS

(Tezos, Cardano, muchos otros)

Si

Abreviado, solo puede durar unos minutos. Algunas excepciones (EOS)

Sí, y los grandes propietarios pueden aumentar su participación en la oferta con el tiempo si participan (y algunos no lo hacen)

De manera inequívoca, el potencial de señoreaje ilimitado

Sí, los tokens de PoS son derechos permanentes de anti-dilución.

Una amplia distribución requiere la eventual venta a inversores minoristas.

La seguridad en PoS aún no se comprende bien

Los desarrolladores generalmente se financian con los ingresos de la venta colectiva + el tesoro

Sí, ya que normalmente retienen una parte de la oferta.

Si, explícitamente

Token de modelo dual

(Sia/Sia Fund, MRK/Dai)

No, existe un instrumento similar a un valor separado junto con la moneda emitida de manera justa.

El “token de utilidad” tiende a tener una emisión extendida, el token de flujo de efectivo se abrevia

Depende, no si la moneda se distribuye con PoW no preminado

No en la capa de “token de utilidad”. El token de flujo de efectivo se asemeja a la equidad y se emite como tal

Sí, especialmente si el suministro está limitado

No, si se tiene cuidado de vender el token de seguridad a una audiencia no minorista

Depende de la elección del modelo de validación

Financiar de forma continua con ventas de token de seguridad.

No si los flujos de efectivo del token de valor no son una función del precio (por ejemplo, Sia)

Si

Si bien creo que este es un modelo interesante y atractivo para un nuevo lanzamiento, ciertamente quedan algunas preguntas abiertas, especialmente porque nunca lo hemos visto en la naturaleza. Estos son algunos de los míos:

-   ¿Es posible extraer un margen suficiente en los ASIC para hacer de esta una empresa rentable?
-   ¿Cómo se debe ver la curva de oferta para que el monopolio temporal de la oferta se considere aceptable para los futuros usuarios?
-   ¿Cómo pueden los compradores de ASIC tener la confianza de que no se crearon de forma encubierta otros ASIC?
-   ¿Puede el financiamiento de una sola vez ser suficiente para impulsar una empresa que construye un protocolo de código abierto?
-   ¿Es la cantidad limitada de señoreaje descalificante en términos de creación de un activo monetario?
-   ¿Son los propios ASIC contratos de inversión / valores, o están libres de problemas?
-   ¿Es posible construir una cadena de suministro ASICs que no se concentre con una o dos entidades que tengan control unilateral sobre el proceso de producción de hardware?

¿Qué piensas? ¿Vale la pena intentarlo o una pérdida de tiempo inútil? Tengo curiosidad por escuchar tus pensamientos. Siento que los métodos de lanzamiento generalmente no están cubiertos, por lo que espero que esta publicación inicie alguna discusión, independientemente de si este modelo se considera viable.

### Objeciones

Consideraré algunas objeciones aquí.

### Si aplicara este modelo a Bitcoin, seis meses de minería representarían 1,3 millones de BTC, que es una fracción excesivamente grande de la oferta.

Puede ajustar la forma de la curva de oferta como desee, para dar a los monopolistas en esos primeros 4 a 6 meses una fracción arbitraria de la oferta. Puede diseñar la curva de modo que obtengan el 0,1% de la oferta o el 99,5% de la oferta. Creo que un emisor probablemente apuntaría a algo como el 5-10% de la oferta para ese período inicial, pero esa es una suposición totalmente descabellada.

### ¿Por qué esperar que el lote inicial de ASIC dure entre 4 y 6 meses? ¿Por qué no duraría esencialmente para siempre y no darían a los compradores de ASIC una ventaja permanente?

Si el protocolo en realidad termina siendo relativamente significativo, en términos de capitalización de mercado, los fabricantes de ASIC inevitablemente intervendrán y fabricarán ASIC para ellos. De las conversaciones con los fabricantes de ASIC que conozco, el período más corto que se necesita para hacer un ASIC útil para un nuevo algoritmo de criptomonedas es de aproximadamente cuatro meses, aunque con mucho gusto recibiría información de expertos aquí. Los FPGA ([Field-programmable gate away](https://es.wikipedia.org/wiki/Field-programmable_gate_array), que son un tipo de dispositivos programables) en este ejemplo no serían suficientes, porque la existencia de ASIC al inicio significa que hay un listón relativamente alto que superar en términos de hardware competitivo. De cualquier manera, el punto sigue siendo: espero que los primeros mineros se enfrenten a la competencia dentro de seis meses a más tardar.

### Los ASIC de este ejemplo en realidad no son valores

Esta no es exactamente una objeción, pero quería abordarla de todos modos. Debo admitir que no conozco la respuesta aquí. Definitivamente, debe mezclar los ASIC con su propia mano de obra (y electricidad) para obtener un rendimiento, por lo que su valor no se deriva únicamente de los esfuerzos de un tercero. Solo estoy adivinando vagamente que los ASIC podrían parecerse a un contrato de inversión. Yo no soy un abogado. Este no es un consejo legal. De cualquier manera, si no fueran valores, sería incluso mejor para el modelo. Estamos tratando de evitar violar la ley de valores, recuerde.

### Los emisores están dando poder total a los fabricantes de ASIC. Estos podrían crear ASIC adicionales y engañar el proceso

Definitivamente, esto es un riesgo, por lo que los fabricantes de ASIC deben estar vinculados contractualmente o tener una estrecha confianza por parte del equipo emisor. El riesgo es que creen de forma encubierta demasiados ASIC. Hay formas potenciales de mitigar esto. No he pensado mucho en ello, pero creo que el equipo podría configurar un protocolo similar al autenticador de Google en el que le dan a los mineros texto cifrado para incluirlo en las salidas de la base de monedas durante los primeros meses, para garantizar que los bloques se extraigan. están siendo creados solo por los ASIC que se contabilizan. No estoy seguro. Creo que alguien inteligente podría encontrar una mejor manera de garantizar que solo los miembros de un conjunto autorizado de ASIC puedan minar durante el período en el que tengan un monopolio temporal.

### No necesitamos más cadenas de bloques. Deje de ayudar a las personas a descubrir cómo emitir nuevas criptomonedas

Básicamente estoy de acuerdo, pero no voy a dejar de explorar estos temas solo porque no te guste la idea de que existan nuevas monedas. Es posible que descubramos una razón para crear otra cadena de bloques en algún momento. Quién sabe.

### Este lanzamiento es bastante injusto, ya que está sugiriendo crear una preminado

Definitivamente, esto no es un pre-minado. No hay un “minado previo”. (Admito que las objeciones sobre las definiciones no son el caso). Lo que tenemos son los emisores que monetizan su ventaja informativa. Saben qué función de hash se utilizará y están vendiendo esa información en forma de hardware especialmente diseñado. La minería depende de quienquiera que se vendan los ASIC. Obtienen un monopolio temporal. Piense en ello como un medallón de taxi que se descompone después de seis meses. Es claramente injusto. Pero habiendo observado el lanzamiento de Grin y el debate de ProgPoW, y las muchas bifurcaciones duras de Monero y la “resistencia a ASIC” de Vertcoin, me queda muy claro que los desarrolladores son extremadamente susceptibles a ejercer presión sobre el PoW. Preferiría que la función hash nunca sea cambiada, de modo que las reglas del juego sean fijas y los retornos al cabildeo sean 0.

Entonces, en este caso, tenemos un modelo claramente injusto, en contraste con una situación (potencial) encubiertamente injusta que la gente piensa ingenuamente que es justa. Esto último sería desastroso. Imagine una cadena que fuera resistente a ASIC, bifurcada a un nuevo PoW, por lo que más tarde se supo que los desarrolladores tenían hardware diseñado a medida, mientras que todos los demás utilizaban GPU. Esto constituiría una explotación de la comunidad y un abuso de confianza. Esto es completamente posible dentro del marco de las monedas resistentes a ASIC, y espero que suceda en algún momento. Propongo una situación con injusticia limitada temporalmente, que se descompone con el tiempo y se vuelve bastante explícitamente justa a partir de entonces.

### Los desarrolladores no deberían monetizar. Deberían trabajar en estas cosas de forma altruista. De lo contrario, puedes canibalizar la motivación intrínseca

¡Estoy bastante de acuerdo! Creo que uno de los resultados más perversos con las recompensas financiadas por el protocolo es que los desarrolladores de programas libres y código libre pierden su incentivo para contribuir al protocolo, dejándolo todo a los profesionales a quienes se les paga directamente desde ese grifo financiado por el protocolo. Básicamente, esto convierte un proyecto de software libre en uno corporativo, obviando todas las ventajas de usar software libre en primer lugar.

Esta configuración específica es una monetización muy limitada. Los desarrolladores venden ASICs al precio que el mercado tolerará, y esa es la única oportunidad que tienen de monetizar directamente su acceso al protocolo. Más adelante, pueden pensar en adoptar el modelo Red Hat, de COSS o un modelo como el de Blockstream, donde monetizan su experiencia específica en protocolos. Pero este modelo también permite a los emisores o desarrolladores iniciales salir del proyecto sin destruirlo. Porque no tienen autoridad permanente en la red, como sería el caso de un equipo emisor que retiene una gran fracción de tokens de PoS, por ejemplo.

### Los desarrolladores no pueden monetizar lo suficiente con esta configuración

La monetización excesiva por parte de los desarrolladores de un protocolo monetario que desarrollan es algo muy peligroso, en mi opinión. En un cierto umbral, tiene una operación que se dedica principalmente a extraer rentas, en lugar de brindar servicios computacionales a precios de productos básicos. Cualquier cosa que los desarrolladores hagan abusar de su autoridad en el sistema, incluida la extracción de valor en exceso del mínimo requerido (que bien puede ser 0), socava su credibilidad y aumenta la probabilidad de que los usuarios se vayan por un sistema menos extractivo. En general, creo que ninguna monetización financiada por protocolos es óptima. Pero si hay alguno, lo toleraría bajo las condiciones de que es temporal, limitado y no otorga a los desarrolladores autoridad permanente dentro del sistema. Esto cumple con esas restricciones.

### Es demasiado caro lanzarlo de esta manera. Los emisores no podrán financiarse lo suficiente

Esta es una crítica justa. En lugar de crear los tokens gratis y venderlos, los desarrolladores tienen que crear literalmente hardware y venderlo. Los ASIC son generalmente bastante caros. Supongo que puede variar según el tipo, pero una carrera decente costará millones de dólares. Por lo tanto, los emisores deberán poder cobrar un precio suficientemente alto para extraer un margen. Esto tiene el interesante efecto de “fijar el precio” de la oferta.

Si se espera que los ASIC tengan el monopolio de la emisión en los primeros seis meses, y se emitirá el 10 por ciento del suministro en ese período, el valor del suministro completamente diluido será aproximadamente 10 veces lo que los compradores pagan por los ASIC. Esto establece un piso para la valoración requerida de un proyecto para que los emisores puedan monetizar de esta manera. Supongamos que crear una ejecución de 1000 ASIC cuesta $5 millones (bien puede ser mucho más, no sé mucho sobre hardware). Los desarrolladores deben recolectar una buena cantidad para financiar la investigación y desarrollo, digamos otros $5 millones. Por lo tanto, deben poder vender los ASIC por $10 millones en conjunto, o $10,000 cada uno. Supongamos también que deciden emitir el 10% del suministro en los primeros 6 meses y creen que los ASIC se mantendrán durante ese período. Esto significa que el mercado debe fijar el precio de la cadena con una valoración de 100 millones de dólares en total (en el momento de la venta de ASIC) para que los emisores obtengan márgenes suficientes.

### ¿Por qué pasar por todos estos problemas para lanzar de esta manera complicada? ¿Por qué no simplemente hacer una ICO y retener una tesorería para la alineación de incentivos a largo plazo?

En primer lugar, las ICO parecen ser una violación de la ley de valores en prácticamente todas las jurisdicciones sensibles. Ir “al extranjero” probablemente no sea suficiente, como muchos emisores probablemente descubrirán en 2020. Esta publicación es una propuesta para una alternativa al lanzamiento “justo” de PoW, y se afirma que mejora en un par de direcciones. No es una alternativa a las ICO. Creo que en la época actual (en realidad, en cualquier momento después del informe de la Comisión de Bolsa y Valores sobre las Organizaciones Descentralizadas Autónomas (publicado en julio de 2017)), las ICO son en gran medida inviables desde una perspectiva regulatoria. Además, creo que el método de lanzamiento de ICO tendrá muchas dificultades para crear dinero duradero.

Esta sigue siendo una hipótesis, pero creo firmemente que el rasgo más importante de un sistema monetario novedoso es una propiedad muy dispersa. Comienza con un GINI de 1 y su objetivo es llegar a un nivel razonable de dispersión con el tiempo. Ahora bien, no me refiero a la perfecta igualdad de resultados; tal cosa es imposible y no está claro cómo funcionaría. ¿Todos los adultos en 2019 reciben el mismo derecho a una parte del nuevo sistema monetario? ¿Qué pasa con los humanos del futuro? ¿Niños por nacer? Incluso si fuera mecánicamente posible, una UBI global todavía estaría expuesta a una inmensa contingencia temporal, privilegiando los intereses de las personas de hoy.

Los airdrops no parecen funcionar muy bien. El intento de Stellar de distribuir sus monedas lo más ampliamente posible ha sido un fracaso verdaderamente lamentable. Algo que se recibe de forma gratuita no suele ser valorado por el destinatario. No es una sorpresa. La Prueba de Trabajo es un sistema potencialmente superior. Los mineros deben trabajar por su parte. Deben dedicar tiempo y esfuerzo a la minería. Este método de distribución es realmente subestimado. Si Ethereum tiene éxito, será en gran parte porque se pudo extraer rentabilidades durante más de 5 años en GPU. En mi opinión, retrasar el cambio a PoS (que discuto anteriormente entorpece la dispersión de las monedas) fue una gracia salvadora. Como se dijo, esto sigue siendo solo una intuición. Pero creo que las cualidades de distribución de PoW están muy subestimadas. Muchos de estos protocolos monetarios cerrados se enfrentarán a la tarea de lograr que los usuarios almacenen valor en su moneda.

### La fabricación de ASIC es una industria concentrada donde las asignaciones de fundición y las conexiones políticas determinan a los ganadores. Te aseguras de que los fabricantes de ASIC serán los creadores de reyes aquí.

Es cierto que la fabricación de ASIC de criptomonedas es actualmente bastante oligopólica. Para obtener una visión bastante reveladora de cómo opera la industria desde un fabricante de ASIC con sede en Estados Unidos lea aquí [la opinión de David Vorick](https://blog.sia.tech/the-state-of-cryptocurrency-mining-538004a37f9b?gi=cb4c19b75706). Lo interesante del lanzamiento de ASIC es que, en realidad, le quita el poder a los grandes fabricantes como Bitmain y lo devuelve a los emisores de la moneda. Un lanzamiento justo de GPU solo establece una carrera armamentista entre los grandes fabricantes de ASIC sobre quién puede construir ASIC más rápido. Cuando llegan allí, presionan intensamente al equipo para que no cambie el algoritmo (ver el debate ProgPoW en Ethereum).

En esta situación, el equipo trabaja con un fabricante de ASIC de su elección para crear ASIC para su lanzamiento, y los fabricantes de ASIC tienen la oportunidad de fabricar hardware específico de la cadena posteriormente. Lo que está muy claro es que los primeros rendimientos de la minería no se acumularán para los grandes fabricantes de ASIC. Si existen, se acumularán para los miembros de la comunidad que compraron los ASIC de los emisores. En general, se trata de una mejora significativa. Agregaré que hay una transición incómoda que prácticamente todas las cadenas resistentes a ASIC tienen que hacer y harán a medida que finalmente capitulen y adopten a los ASIC. Elegir anunciar la resistencia de ASIC, coordinar un par de bifurcaciones duras y, finalmente, aceptar la inevitabilidad de los ASIC es crear una gran cantidad de ambigüedad que los fabricantes de ASIC pueden explotar y explotan. Prefiero un juego donde las reglas sean explícitas desde el día 0.

Por último, existe la posibilidad de crear ASIC que no estén tan expuestos a las idiosincrasias de la cadena de suministro que los ASIC SHA-256 requieren actualmente. Los reyes de los ASIC de Bitcoin son las fundiciones, que privilegian a los grandes fabricantes de ASIC que pueden pagar por adelantado el acceso y competir por las asignaciones. Algunas tecnologías alternativas, como la [Prueba de Trabajo óptica](https://arxiv.org/abs/1911.05193), pretenden inculcar procesos de fabricación ASIC más justos. No he verificado esto de forma independiente, pero este es el reclamo. Si es así, los ASIC de ese tipo serían más fáciles de producir en masa en una mayor variedad de entornos.

### Cualquier cantidad de señoreaje es descalificante

No estoy del todo seguro de llamar a esto señoreaje, ya que es muy posible que los compradores de ASIC pierdan dinero y terminen pagando efectivamente $1,10 por cada dólar que acuñen. No es señoreaje garantizado, al menos. Los compradores de ASIC están asumiendo cierto riesgo. Dicho esto, si el modelo funciona bien, los compradores de ASIC acuñarán monedas por debajo de la tasa de mercado; si no hubiera la posibilidad de hacerlo, no participarían. Entonces hay señoreaje potencial. Si cree que incluso la más mínima cantidad de señoreaje arruina permanentemente la credibilidad del proyecto, este modelo no funcionará para usted. Pero si usted siente, como yo, que una pequeña cantidad de señoreaje puede ser muy útil, incluso si va en contra de la credibilidad, puede encontrar atractivo este modelo.

### ¿Por qué pierdes el tiempo pensando en esto? Ya tenemos Bitcoin y no necesitamos nuevas cadenas

¡Me reservo el derecho de pensar y escribir sobre lo que me parezca interesante!
