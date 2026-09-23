---
titulo: "Samourai Wallet + Ronin Dojo: un artículo sobre privacidad, anonimato y opciones"
autor: "econoalchemist"
traductor: "Luis David Esparragoza"
traductor_url: "https://twitter.com/criptoluis"
fuente_original: "https://www.econoalchemist.com/post/samourai-wallet-ronin-dojo-an-article-on-privacy-anonymity-options"
fecha: "2022-01-26"
original: "2020-09-16"
nivel: "experto"
categorias: ["tutoriales"]
portada: "../imagenes/2022/01/fractal-35.jpg"
resumen: "Tener Samourai Wallet en tu teléfono móvil y un Ronin Dojo en tu casa es una combinación poderosa para preservar la privacidad, que puede ayudar a los usuarios a interactuar con Bitcoin de una forma anónima. Quise escribir un artículo sobre utilizar Samourai Wallet y su herramienta Whirlpool por ser una herramienta enfocada en la…"
borrador: true
archivo: "https://web.archive.org/web/2023/https://bitblioteca.com/samourai-wallet-ronin-dojo-un-articulo-sobre-privacidad-anonimato-y-opciones/"
---

Tener Samourai Wallet en tu teléfono móvil y un Ronin Dojo en tu casa es una combinación poderosa para preservar la privacidad, que puede ayudar a los usuarios a interactuar con Bitcoin de una forma anónima.

![](../imagenes/2022/01/35-1.jpg)

Quise escribir un artículo sobre utilizar Samourai Wallet y su herramienta Whirlpool por ser una herramienta enfocada en la privacidad. Pero también a medida que investigaba, seguí descubriendo más y más herramientas y capacidades. Realmente es un logro increíble el que estos equipos de desarrolladores han alcanzado. Este artículo terminó siendo mucho más extenso de lo que intenté originalmente, pero pensé que era de suma importancia reunir toda la información junta en la misma pieza. Este artículo cubre los siguientes aspectos del paquete Samourai Wallet + Ronin Dojo:

-   Monedero para móviles Samourai 
-   Ronin CLI
-   Nodo completo Dojo
-   Ronin UI
-   Whirlpool GUI
-   Electrum
-   Explorer
-   OXT
-   KYCP

[@SamouraiWallet](https://twitter.com/SamouraiWallet) y [@RoninDojoUI](https://twitter.com/RoninDojoUI) son dos equipos diferentes de desarrolladores. Dojo tiene la función de ser utilizado como nodo completo que soporta al monedero Samourai (SW), para mejorar la privacidad y mitigar la confianza en terceros. Ronin es la Interfaz de Usuario (UI) para interactuar con tu Dojo.

-   [https://samouraiwallet.com](https://samouraiwallet.com)
-   [https://ronindojo.io/](https://ronindojo.io/) 

[@SamouraiWallet](https://twitter.com/SamouraiWallet) es un monedero móvil para Android exclusiva y únicamente para bitcoin. Al igual que cualquier otro monedero que utiliza semillas de 12, 18 o 24 palabras clave (Hierarchichal Deterministic Wallets o HD Wallet), la llave pública es utilizada para mostrar el balance de fondos de la cartera y generar direcciones. Como con cualquier otra wallet HD, si no estás corriendo tu propio nodo, estás confiando en un tercero al utilizar su nodo.

Sin embargo, como cualquier otra HD wallet, Samourai Wallet tiene una suite de herramientas disponibles para los usuarios, tales como Ricochet, PayNym, StoneWall & Whirlpool. Estas herramientas tienen ventajas significativas para los usuarios interesados en aumentar su privacidad y anonimato en la cadena de bloques.

![](../imagenes/2022/01/35-2.jpg)

![](../imagenes/2022/01/35-3.jpg)

Antes de adentrarnos en las herramientas y características de la cartera, el nodo completo Dojo necesita ser configurado en una PC de placa única o (Single Board Computer, SBC). Yo elegí la RasberryPi 4, pero estoy considerando usar la RockPro64 para una instalación más simple. También necesitamos una PC para correr la interfaz RoninUI.

> [https://wiki.ronindojo.io/en/hardware](https://wiki.ronindojo.io/en/hardware) 

![](../imagenes/2022/01/35-4.jpg)

La Wiki de Ronin Dojo tiene bastantes recursos útiles e instrucciones detalladas. Si te quedas atrapado en el proceso de instalación, solo acércate al grupo de Telegram. Los miembros de la comunidad brindan bastante apoyo y ayudan a los usuarios a instalar y correr esta interfaz.

> [https://t.me/RoninDojoUI](https://t.me/RoninDojoUI)  

Solamente estoy haciendo una revisión de alto nivel porque el proceso de instalación está en la página de RoninWiki, comenzando con el primer paso: primero ensamblamos y conectamos el hardware de la PC de placa única (SBC). Luego descargamos y verificamos la imagen de Ronin y cargamos ese archivo en una tarjeta MicroSD. Luego encendemos el hardware del SBC.

> [https://wiki.ronindojo.io/en/gui-setup/step1](https://wiki.ronindojo.io/en/gui-setup/step1) 

![](../imagenes/2022/01/35-5.jpg)

![](../imagenes/2022/01/35-6.png)

![](../imagenes/2022/01/35-7.jpg)

![](../imagenes/2022/01/35-8.jpg)

Yo utilicé Putty para establecer la conexión SSH con mi SBC RaspberryPI, y luego configuré un teclado, nombre de usuario, etc. Tan solo sigue las instrucciones, es bastante fácil. Luego corre las actualizaciones y clona el repositorio de Ronin como explican en el Ronin Wiki en el paso 2. Esto ejecutará el Ronin CLI (cliente). Desde allí, las dependencias de Dojo ya pueden ser instaladas, que sería el servidor back-end que interactúa con Bitcoin

> [https://wiki.ronindojo.io/gui-setup/step2](https://wiki.ronindojo.io/gui-setup/step2) 

![](../imagenes/2022/01/35-9.png)

![](../imagenes/2022/01/35-10.png)

Opcionalmente, un usuario puede instalar Indexador, una herramienta para consultar balances; y también el Servidor Rust de Electrum, una herramienta para interfaces de hardware wallets (monederos fríos). Estas opciones solo se pueden instalar después de que Dojo haya completado su descarga inicial de bloque (Initial Block Download, IBD) y tomarse 8 horas en línea, adicionalmente.

![](../imagenes/2022/01/35-11.png)

Dependiendo de un número de factores, la IBD tomará al menos 2 días, posiblemente una semana. Mientras tanto, es seguro comenzar la configuración de la Interfaz de Usuario. RoninDojoUI está diseñada para hacer la interacción con el nodo completo Dojo más amigable al usuario. La configuración de la UI se explica en el paso 3 de RoninWiki.

> [https://wiki.ronindojo.io/gui-setup/step3](https://wiki.ronindojo.io/gui-setup/step3) 

Se requieren dos computadoras para esto, la RaspberryPi u otra SBC, y una PC. Mientras que la SBC está corriendo el cliente Ronin CLI y el nodo completo Dojo, la PC estará corriendo RoninUI y Whirlpool GUI. Con RonindojoUI un usuario puede conectar su Samourai Wallet a través de un código QR y más. Con Whirlpool GUI, se pueden manejar la mezcla de monedas.

![](../imagenes/2022/01/35-13.png)

En la PC, habiendo instalado el navegador Tor, descarga y verifica con este browser la interfaz RoninUI. Copia y pega las credenciales de verificación del cliente Ronin CLI en el CLI de RoninDojo. Crea una contraseña en la interfaz RoninUI. Ahora SamouraiWallet puede emparejarse desde tu teléfono móvil hacia tu interfaz RoninUI. Descarga Samourai Wallet en Android, selecciona red principal (main-net) y Tor, selecciona Conectar a Dojo Existente y escanéa el código QR de RoninDojoUi.

![](../imagenes/2022/01/35-15.png)

![](../imagenes/2022/01/35-16.jpg)

Samourai Wallet se configura como cualquier otra wallet. Solo necesitas crear un código PIN para acceder a la aplicación y escribir de forma segura tu frase semilla de 12 palabras según la BIP39. No se pide ni almacena información personal. Puedes restaurar tus monederos externas también. ¡Y además obtienes un PayNym según la BIP-47!

![](../imagenes/2022/01/35-17.jpg)

### Cálmate y piensa.

Lo que tienes hasta ahora es un monedero de Bitcoin con una implementación interna de CoinJoin. Tienes una gran cantidad de herramientas post-mezcla disponibles. Usar una conexión Tor para comunicarte con tu propio nodo completo. Todo manejado por la Interfaz de Usuario en tu PC, de manera:

-   Privada  
-   Anónima
-   Sin terceros de confianza
-   Amigable al usuario

![](../imagenes/2022/01/35-18.jpg)

En la misma PC que RoninDojoUI, descarga la GUI Whirlpool. Asegúrate de que el navegador Tor está abierto primero. En la interfaz RoninUI selecciona *Iniciar Whirlpool*. En la WhirpoolGUI selecciona CLI Remoto. Luego copia y pega la dirección URL .onion de Whirlpool que extrajiste del RoninUI. Deja en blanco la llave del API en la conexión inicial. Luego pulsa conectar. Estos pasos son explicados con más detalle en el paso 4 de RoninWiki.

> [https://wiki.ronindojo.io/en/gui-setup/step4](https://wiki.ronindojo.io/en/gui-setup/step4) 

![](../imagenes/2022/01/35-20.png)

Una ventana del Whirlpool GUI te aparecerá preguntándote por la llave de emparejamiento de la Samourai Wallet. En esa wallet, ve a Menu>Settings>Transactions>Pair to Whirlpool GUI. Esto está en una sección experimental. Utiliza la cámara de la PC para escanear tu código QR. Pulsa el botón de Iniciar GUI. Introduce tu frase semilla de la wallet (BIP-39) y Whirlpool se conectará a tu wallet listo para operar. Ahora, tus salidas o outputs (UTXO) podrán seguir mezclándose 24/7 incluso cuando estés fuera. 

![](../imagenes/2022/01/35-22.jpg)

![](../imagenes/2022/01/35-23.png)

![](../imagenes/2022/01/35-24.png)

Whirlpool es una implementación de Coinjoin Zerolink. Cada mezcla tiene 5 entradas y 5 salidas. Dos salidas (UTXO) nunca comparten el mismo ciclo de mezcla. Se necesita como mínimo dos participantes nuevos, y hasta tres usuarios que participen gratuitamente. No se utilizan direcciones ni se crean links determinísticos en cada mezcla. Adicionalmente, cada mezcla tiene 1.496 interpretaciones sobre cuáles entradas y salidas están conectadas.

![](../imagenes/2022/01/35-25.jpg)

![](../imagenes/2022/01/35-26.png)

Gráfico por @P\_Hold.

El concepto es que los usuarios ganen anonimidad al mezclarse en un grupo de UTXO del mismo tamaño. Existen tres pools de mezcla a los que los usuarios pueden unirse: de 0,5 BTC, 0,05 BTC y 0,01 BTC. Por ejemplo, si quieres mezclar 1 BTC en la pool de 0,01 BTC, tendrás 99 salidas o outputs (UTXO) del mismo tamaño, ya que una pequeña cantidad del 1 BTC necesita utilizarse para pagar las comisiones de minería y la comisión de Whirlpool.

![](../imagenes/2022/01/35-28.png)

Una vez que los fondos son depositados y la wallet está sincronizada con Whirlpool, un usuario puede especificar la cantidad de ciclos de mezcla hasta el infinito. Las remezclas son gratis, así que solo tienes que pagar la comisión de Whirlpool y luego puedes continuar uniéndote a nuevas mezclas gratis mientras que nuevos participantes cubran las tarifas. Cada remezcla agrega más entropía a las UTXO, haciendo más difícil rastrear y terminar los links determinísticos.

![](../imagenes/2022/01/35-29.jpg)

El cambio sobrante es primero separado de las salidas participantes del Whirlpool antes de registrarse en el ciclo de mezcla. Existe una llave pública de lectura (xpub) para este cambio llamada Bad Bank (Mal Banco). Los usuarios son instados a marcar (flag) este cambio, pero si alguno quiere gastar esos fondos luego arriesgando su privacidad, entonces pueden hacerlo. Es crucial que el cambio sobrante no sea mezclado y no se devuelva en la misma transacción del CoinJoin.

![](../imagenes/2022/01/35-30.jpg)

Las salidas UTXO recién creadas son todas del mismo tamaño y son separadas de este cambio tóxico en lo que se llama Transaction Zero (Tx0). Las UTXO son registradas luego como una xpub para premezcla como entradas disponibles para hacer el Whirlpool correspondiente.

![](../imagenes/2022/01/35-31.jpg)

Los nuevos participantes del ciclo de mezcla pagan las tarifas de los mineros. Luego de la mezcla inicial, los que fueron participantes gratuitos pueden seguir mezclando gratuitamente. Solo deben seleccionar cuál UTXO de la lista post mezcla desean gastar en cualquier momento.

![](../imagenes/2022/01/35-32-485x1024.jpg)

Desde la página de inicio de Samourai Wallet, selecciona la señal “+” y luego Whirlpool > Whirlpool > Mix UTXOs > hacer tu selección > elige la prioridad y el pool > review > Dí que Sí a marcar el cambio tóxico > iniciar.

![](../imagenes/2022/01/35-33.jpg)

Las estadísticas de Whirlpool pueden monitorearse con solo enviar un comando al bot de @SW\_Whirlpool en Telegram. Asegúrate de revisar esta guía de @Crazyk\_031

> [https://t.me/SWInformational/502](https://t.me/SWInformational/502) 

![](../imagenes/2022/01/35-34.jpg)

> [@BitcoinQ\_A](https://twitter.com/BitcoinQ_A) escribió un artículo detallado sobre Whirlpool aquí: [https://www.bitcoinqna.com/post/whirlpool-faq](https://www.bitcoinqna.com/post/whirlpool-faq)  
> 
> [@P\_Hold](https://twitter.com/P_Hold) explora los detalles técnicos sobre Whirlpool en [este artículo](https://estudiobitcoin.com/como-entender-whirlpool-de-samourai-wallet-sin-morir-en-el-intento/?_x_tr_sl=auto&_x_tr_tl=en&_x_tr_hl=es-419&_x_tr_pto=nui,nv,op).

### Cálmate y piensa.

Las remezclas son gratuitas. Cada mezcla tiene 1.496 interpretaciones. Cada mezcla alcanza 10.546 bits de entropía. Todo sucede cuando el cliente de escritorio mezcla infinitamente las UTXO. Está conectado a tu monedero móvil. Todo sobre Tor. Con herramientas de post mezcla en tu wallet móvil.

![](../imagenes/2022/01/35-35.jpg)

Una vez que las UTXO del usuario han sido mezcladas, existe una variedad de herramientas post mezcla disponibles. Todas estas herramientas ayudan a los usuarios a mantener la privacidad alcanzada durante el ciclo de mezcla, empleando una variedad de técnicas como los saltos (hops), direcciones stealth y mini CoinJoins.

Ricochet fue diseñada para añadir saltos entre el gasto y la dirección final. Por ejemplo, si un usuario quisiera hacer un retiro de un exchange, y le preocupa que sus fondos sean marcados para hacerles seguimiento, esta herramienta añade una distancia desde la transacción CoinJoin. Las comisiones de minería para hacer los saltos son pagadas más adelante.

![](../imagenes/2022/01/35-36.png)

Aquí puedes encontrar sobre un una casa de cambio siguiendo los fondos de un usuario: https://6102bitcoin.com/coinjoin-flagging/

Y [aquí también](https://medium.com/@6102bitcoin/binance-coinjoin-strangeness-6ba7c0cb2dd0#:~:text=Binance%20Singapore%20has%20reportedly%20blocked,previously%20withdrawn%20from%20the%20exchange).

PayNym es una implementación de la BIP47. Esto le da a los usuarios un código de pago público reusable que les evita revelar sus direcciones o historial de transacciones. Al utilizar técnicas especiales de encriptado, una llave secreta combinada es generada entre los usuarios de PayNym.

![](../imagenes/2022/01/35-37.png)

Solo se requiere pagar la comisión una vez para establecer la conexión on-chain entre los PayNyms. Una vez establecida esta conexión, PayNyms permite a los usuarios hacer tantas transacciones anónimas como quieran, mientras que pagan comisiones de minería normales.

[https://video.wixstatic.com/video/e65a7a\_b09ea53808e6438b9a9bf7810a85f3a0/1080p/mp4/file.mp4](https://video.wixstatic.com/video/e65a7a_b09ea53808e6438b9a9bf7810a85f3a0/1080p/mp4/file.mp4)

Stonewall está diseñada para usar múltiples inputs y outpus de modo que exista una duda razonable sobre quién es el dueño de una UTXO. Las transacciones Stonewallx2 son hechas entre dos usuarios. Estos dividen el pago de la comisión por minería y ambos ganan anonimidad. Los fondos pueden ser enviados a una tercera parte además de los colaboradores.

[https://video.wixstatic.com/video/e65a7a\_b92a4752cdb848728a3cf4583143e9db/1080p/mp4/file.mp4](https://video.wixstatic.com/video/e65a7a_b92a4752cdb848728a3cf4583143e9db/1080p/mp4/file.mp4)

Para un observador externo hay dos tipos de transacciones: Stonewall & Stonewallx2, que son indistinguibles entre sí. Una transacción Stonewall tendrá un mínimo de 1.584 bits de entropía. Una transacción Stonewallx2 tendrá un mínimo de 4.643 bits de entropía. Esto es similar a los mini CoinJoins.

![](../imagenes/2022/01/35-39.png)

![](../imagenes/2022/01/35-40.jpg)

![](../imagenes/2022/01/35-41.png)

### Stonewall

es la herramienta de gasto post mezcla. Siempre tienen 4 outputs, donde 1 es el gasto, 1 es el señuelo, y los otros son los outputs de cambio que son devueltos al monedero del usuario. Los observadores externos no pueden saber si estas tx fueron hechas por individuos o colaboradores. Pueden ser enviadas a cualquiera.

### Stowaway

es usado entre dos usuarios de Samourai Wallet. Los detalles dejados en la blockchain hacen difícil determinar cuál UTXO es de cambio y cuál es de pago. Este tipo de transacción solo puede ser usada con la persona que recibe el pago. Los usuarios deberán intercambiar algunos códigos QR para hacer la transacción.

[https://video.wixstatic.com/video/e65a7a\_9f4d431b56da49c69758dca0a04df75d/1080p/mp4/file.mp4](https://video.wixstatic.com/video/e65a7a_9f4d431b56da49c69758dca0a04df75d/1080p/mp4/file.mp4)

Aquí está una transacción Stowaway tx según el sitio [KYCP](https://kycp.org/#/), con 4 inputs y 2 outputs. Los Inputs 0, 1, y 2 fueron señuelos para confundir la interpretación. Se enviaron 0.00806013 BTC, y se recibieron 0.00802 BTC. Se gastó 0.00004013 BTC en comisiones de minería.

![](../imagenes/2022/01/35-42.png)

Las transacciones PayJoin como Stonewallx2 y Stowaway estarán disponibles muy pronto en la capa de comunicaciones Tor/Soroban, eliminando la necesidad de escanear varios códigos QR entre los participantes.

> [!tweet] https://twitter.com/SamouraiDev/status/1304777018417000448?ref_src=twsrc%5Etfw
> https://t.co/4Fj249lIjx

### Cálmate y piensa.

El anonimato alcanzado durante las mezclas de Whirlpool. El cambio tóxico es separado. El gasto post mezcla de Stonewall tiene por defecto tres mínimas interpretaciones. Colabora con tus pares para obtener mayor anonimato. Haz de cada gasto un CoinJoin.

![](../imagenes/2022/01/35-43.jpg)

Electrum permite a los usuarios tener una interfaz para una wallet de hardware como [@COLDCARDWallet.](https://twitter.com/COLDCARDwallet) Descarga y verifica la aplicación, como dice el paso 5 de la RoninWiki. Una vez que se termine la sincronización de Indexer, Electrum puede dirigirse al Dojo como su servidor. Esto será materia para otro artículo sobre Electrum.

> [https://wiki.ronindojo.io/en/gui-setup/step5](https://wiki.ronindojo.io/en/gui-setup/step5)  

![](../imagenes/2022/01/35-45.png)

![](../imagenes/2022/01/35-46.png)

El explorador brinda una forma de usar los datos actualizados del Dojo como un explorador de bloques de Bitcoin enteramente desplegado. Copia la URL .onion y la contraseña de Dojo en la página de configuración, y pégala en el navegador Tor. Deja el nombre de usuario en blanco, pega la contraseña, guarda la página (*bookmark*).

> [https://wiki.ronindojo.io/en/gui-setup/step6](https://wiki.ronindojo.io/en/gui-setup/step6) 

![](../imagenes/2022/01/35-48.jpg)

OXT y KYCP son gratuitos y libres de usar. Proveen a los usuarios de herramientas de punta para el análisis de blockchain, para explorar, aprender y verificar. No se requiere información personal. Simplemente un nombre de usuario y una contraseña.

> [https://oxt.me](https://oxt.me) 
> 
> [https://kycp.org/#/](https://kycp.org/#/) 

Existen cientos de funciones y herramientas internas en OXT, tales como gráficos avanzados sobre transacciones donde inputs mezclados fueron convertidos en uno. Existe mucha actividad en torno a esta transacción, pero logró muy poco en términos de anonimidad.

![](../imagenes/2022/01/35-50.png)

![](../imagenes/2022/01/35-51.png)

Abajo encontrarás cómo luce una transacción Whirpool. No hay links determinísticos. No se reutilizan direcciones. Hay 1496 formas de interpretar estas transacciones.

![](../imagenes/2022/01/35-53.png)

![](../imagenes/2022/01/35-54.png)

> [@janeygak](https://twitter.com/janeygak) escribió un artículo detallado sobre KYCP que [puedes ver aquí](https://medium.com/samourai-wallet/knowing-your-coin-privacy-using-kycp-org-7b3b4385d8b). 

### Cálmate y Piensa.

Explora la blockchain sin exponer ninguna información personal. Respáldate en un nodo completo. Verifica varias interpretaciones de transacciones. El control completo sobre UTXO de alta entropía. Es un mezclador de bolsillo. Todo desde tu monedero móvil.

![](../imagenes/2022/01/35-55.jpg)

Samourai Wallet puede hacer mezcla de llaves privadas también, genial para @OPENDIME.

Algunas características notables: tiene Tor por defecto, la aplicación del monedero de solo lectura es Sentinel, soporta multi dirección, gasto en lote, PIN mezclado y comisiones inteligentes de minería. Hay tanto para listar, pero si comienzas a explorar verás el potencial que trae este paquete.  

Todo lo presentado aquí ha sido creado por desarrolladores dedicados a resistir la censura, privacidad y anonimidad. Las personas tienen la necesidad inmediata de acceder a estas herramientas, donde sea que las autoridades opresoras infrinjan las libertades individuales. Las personas están siendo arrestadas, la recolección de datos KYC es cada vez más común, la privacidad debe ser defendida. **Esto no es un simulacro.**

Si te interesa aprender más sobre las fuerzas detrás de la investigación anti lavado de dinero que buscan arrebatarte tus derechos, revisa este hilo por @J9Roem y verás lo importante que es para ti el trabajo de @SamouraiWallet y @RoninDojoUI.

> [https://twitter.com/J9Roem/status/1291092854174027777](https://twitter.com/J9Roem/status/1291092854174027777) 
> 
> [@stephanlivera](https://twitter.com/stephanlivera) ha grabado numerosos e interesantes podcasts con Samourai Wallet: 
> 
> [https://stephanlivera.com/episode/78/](https://stephanlivera.com/episode/78/) 
> 
> y aquí: [https://stephanlivera.com/episode/150/](https://stephanlivera.com/episode/150/) 
> 
> …y aquí: [https://stephanlivera.com/episode/209/](https://stephanlivera.com/episode/209/) 
> 
> Aquí tienes un episodio de [@TFTC21](https://twitter.com/TFTC21) sobre Ronin Dojo: [https://www.youtube.com/watch?v=MaC27vLnI7o](https://www.youtube.com/watch?v=MaC27vLnI7o) 
> 
> Aquí un episodio de [@ocbtcn](https://twitter.com/ocbtcn) sobre Samourai Wallet & Ronin Dojo con sus desarrolladores: [https://www.youtube.com/watch?v=jqFspCuacrA](https://www.youtube.com/watch?v=jqFspCuacrA)

¡Gracias por leer! Espero que encuentres todo esto inspirador y decidas incorporar algunas de las herramientas descritas aquí en tu uso de Bitcoin, para preservar tu privacidad e interactuar anónimamente.
