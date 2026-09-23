# Bitblioteca — traducciones

Textos sobre Bitcoin traducidos al español. Este repositorio es la fuente del sitio [bitblioteca.com](https://bitblioteca.com): cada cambio aceptado acá se publica solo.

## Estructura

```
articulos/   un archivo .md por texto
autores/     un archivo .md por autor (nombre, foto, web y bio)
paginas/     páginas fijas del sitio (nosotros, etc.)
imagenes/    imágenes usadas en los textos
```

## Ficha de cada artículo

```md
---
titulo: "Bitcoin es dinero"
autor: "beautyon"              # nombre del archivo en autores/, sin .md
traductor: "Tu nombre"
traductor_url: "https://…"     # opcional
fuente_original: "https://…"   # link al texto en inglés
fecha: "2022-03-11"             # cuándo se publicó la traducción
original: "2020-05-01"         # cuándo se publicó el texto original
nivel: "basico"                # basico | medio | experto
destacado: true                # opcional: aparece en "Para leer primero"
series: ["parker-lewis-series"] # opcional
portada: "../imagenes/2022/01/fractal-32.jpg"
resumen: "Una o dos frases."
borrador: true                 # opcional: no se publica
---

El texto traducido, en Markdown.
```

## Citas y recuadros

```md
> Una cita común.

> [!destacada]
> Frase grande que corta el texto. También rota en la portada del sitio.

> [!nota-traductor]
> Aclaración de quien tradujo.

> [!dato]
> Recuadro con un dato o una definición.

> [!actualizacion]
> Algo que cambió desde que se escribió el original (servicio cerrado, dato viejo).

> [!tweet] https://x.com/usuario/status/123
> Texto del tweet.
```

## Cómo colaborar

- **Corregir**: en cada artículo del sitio, "Corregir esta traducción" abre el archivo acá para editarlo.
- **Traducir**: agregá un `.md` nuevo en `articulos/` con la ficha de arriba y abrí un pull request.

Los textos originales pertenecen a sus autores; cada traducción enlaza a su fuente.
