# Información útil:

## Dataview query:

### Variables:

- **indice**: Si se pone a True esa nota quedará marcada como indice.
- **marca**: fabricante del producto en cuestión.
- **howto**: Si se pone a True indica que no es una página de indice, si no de "tutorial"
- **equipo**: Tipo de equipo sobre el que va el tutorial, ej: HMI
- **descripcion**: Breve descripción del contenido de la nota, introducir entre " "

### Sintaxis:
Al comienzo de cada nota se deberán introducir las variables del dataview, de la siguiente manera:

```
---
marca: Siemens
equipo: HMI
howto: True
descripcion: "Configuración del acceso remoto al HMI"
---
```

Los guiones son obligatorios, tanto para abrir como para cerrar.


## Markdown:

Las notas se guardan en formato .md, esto significa que son documentos de tipo "markdown", tiene una sintaxis propia y el resultado es muy similar al HTML.

[Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet/)
