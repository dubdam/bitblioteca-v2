# Cómo colaborar con la Bitblioteca

No hace falta saber programar. Todo se hace desde el navegador, en GitHub, con una cuenta gratuita.

Podés colaborar de cuatro formas:

1. [Corregir un texto que ya está](#1-corregir-un-texto)
2. [Subir una traducción nueva](#2-subir-una-traducción-nueva)
3. [Publicar un artículo original](#3-publicar-un-artículo-original)
4. [Republicar un artículo publicado en otro lado](#4-republicar-un-artículo-publicado-en-otro-lado)

Cada propuesta la revisa un editor antes de publicarse. Cuando se acepta, aparece en el sitio en uno o dos minutos, con tu nombre.

**Licencia:** al proponer un texto aceptás publicarlo bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es): cualquiera puede compartirlo y adaptarlo, siempre que te dé crédito. Si traducís, eso cubre tu traducción; el texto original sigue siendo de su autor, por eso hace falta su permiso o una licencia libre.

---

## 1. Corregir un texto

Para una errata, una frase mal traducida o un dato viejo.

1. En el sitio, al final del artículo, tocá **"Corregir esta traducción"**. Si ya estás en GitHub, abrí el archivo en `articulos/` y tocá el lápiz ✏️.
2. Si es tu primera vez, GitHub te pide crear una copia propia del repositorio ("Fork this repository"). Aceptá.
3. Hacé el cambio.
4. Abajo, en **"Commit changes"**, escribí en una línea qué cambiaste. Por ejemplo: *"Corrijo 'mil millones' por 'billón'"*.
5. Tocá **"Propose changes"** y después **"Create pull request"**.

Listo. Cuando se revise, vas a recibir un aviso.

**Si algo quedó desactualizado** (un servicio que cerró, una ley que cambió), no reescribas al autor: agregá una aclaración debajo del párrafo.

```md
> [!actualizacion]
> LocalBitcoins cerró en febrero de 2023.
```

**Si no querés editar**, abrí un aviso en [Issues](../../issues) contando qué viste y en qué artículo.

---

## 2. Subir una traducción nueva

1. Antes de empezar, fijate que el texto no esté ya en `articulos/` y buscá en [Issues](../../issues) si alguien lo está traduciendo. Si no, abrí un aviso: *"Traduzco: título del original"*. Así nadie duplica trabajo.
2. Asegurate de poder publicarlo. Muchos autores de Bitcoin permiten traducir sus textos, pero no todos. Si el original no tiene una licencia libre (por ejemplo, Creative Commons), pedile permiso al autor y contalo en la propuesta.
3. En GitHub, entrá a la carpeta `articulos/`, tocá **"Add file" → "Create new file"** y ponele de nombre el título en minúsculas y con guiones: `bitcoin-es-dinero.md`.
4. Copiá el contenido de [`plantillas/articulo.md`](plantillas/articulo.md), completá la ficha y pegá tu traducción debajo.
5. Si el autor no tiene archivo en `autores/`, creá uno con [`plantillas/autor.md`](plantillas/autor.md).
6. **"Commit changes" → "Propose changes" → "Create pull request"**.

### Criterios de traducción

- Español neutro, que se entienda en toda Latinoamérica y España.
- No traduzcas de forma automática y publiques sin revisar. Una herramienta puede ayudar, pero cada frase tiene que sonar natural.
- Cuidado con los números grandes: *billion* = mil millones; *trillion* = billón.
- Términos que no se traducen: *Bitcoin*, *Lightning*, *hash*, *halving*, *hodl*. Si hace falta, explicalos una vez con una nota del traductor.
- Respetá el texto del autor. Tus aclaraciones van en recuadros aparte (ver [recuadros](#recuadros-y-citas)).

---

## 3. Publicar un artículo original

¿Escribiste algo sobre Bitcoin en español? También tiene lugar acá, si es educativo y no promocional.

Seguí los pasos de la [traducción nueva](#2-subir-una-traducción-nueva), con dos diferencias:

- En la ficha, dejá afuera `traductor` y `fuente_original`.
- En `autor` poné tu propio archivo de `autores/` (creá uno con tu nombre, foto y una bio corta).

---

## 4. Republicar un artículo publicado en otro lado

Para textos en español que ya salieron en otro medio o blog y que valga la pena conservar acá.

- Tenés que ser el autor o tener su permiso.
- En la ficha, `fuente_original` es el link a la publicación original y `original` es su fecha.
- Si el texto es tuyo, no pongas `traductor`.

---

## La ficha de cada artículo

Es el bloque entre `---` al principio de cada archivo. Copiala de [`plantillas/articulo.md`](plantillas/articulo.md).

| campo | qué va | ¿obligatorio? |
|---|---|---|
| `titulo` | Título en español | sí |
| `autor` | Nombre del archivo del autor en `autores/`, sin `.md` | sí |
| `traductor` | Tu nombre, como querés que aparezca | si es traducción |
| `traductor_url` | Link a tu perfil (X, Nostr, web) | no |
| `fuente_original` | Link al texto original | si es traducción o republicación |
| `original` | Fecha del texto original: `"2021-05-12"` o solo `"2021"` | si es traducción o republicación |
| `fecha` | Fecha en que se publica acá | sí |
| `nivel` | `"basico"`, `"medio"` o `"experto"` | sí |
| `resumen` | Una o dos frases para los listados | sí |
| `portada` | Imagen de portada, ej. `"../imagenes/2026/mi-imagen.jpg"` | no |
| `series` | Si forma parte de una serie, ej. `["plantando-bitcoin"]` | no |
| `borrador` | `true` para guardarlo sin publicar | no |

**Niveles:**
- **básico:** para quien recién llega;
- **medio:** economía, energía, privacidad;
- **experto:** criptografía, historia del protocolo, análisis técnico.

## Recuadros y citas

```md
> Una cita común.

> [!destacada]
> Una frase para resaltar. También rota en la portada del sitio.

> [!nota-traductor]
> Una aclaración de quien tradujo.

> [!dato]
> Un dato o una definición.

> [!actualizacion]
> Algo que cambió desde que se escribió el original.

> [!tweet] https://x.com/usuario/status/123
> Texto del tweet.
```

En GitHub se ven como citas comunes. En el sitio cada una tiene su diseño.

## Imágenes

1. Entrá a `imagenes/`, creá o abrí la carpeta del año (`2026/`) y tocá **"Add file" → "Upload files"**.
2. Usá nombres sin espacios ni acentos: `grafico-halving.png`.
3. En el texto: `![Descripción de la imagen](../imagenes/2026/grafico-halving.png)`.

Preferí imágenes livianas (menos de 500 KB) y con derecho a usarse.

## Qué no se publica

- Promociones, links de referido o recomendaciones pagas.
- Textos sobre otras criptomonedas que no sean Bitcoin.
- Guías que recomienden servicios sin aclarar sus riesgos (por ejemplo, monederos custodiales para guardar ahorros).
- Contenido sin permiso de su autor.

## ¿Dudas?

Abrí un aviso en [Issues](../../issues). Toda pregunta es bienvenida.
