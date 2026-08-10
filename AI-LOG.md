# AI Log — HW02

## Uso de inteligencia artificial

Se utilizó inteligencia artificial para revisar las instrucciones, planear la arquitectura semántica y crear un primer borrador de `index.html`, `about.html` y este registro.

## Prompts proporcionados

### Prompt 1

```text
ok, siguiente tarea, verifica super bien todos los archivos y las instrucciones, primero planeación de que hacer y como hacerlo
```

### Prompt 2

```text
ok, entonces la idea ya es usar un html un poco más avansado propuesto en las siguientes páginas:

https://developer.mozilla.org/en-US/docs/Learn_web_development/Getting_started/Your_first_website/Creating_the_content
https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms

En la segunda páginas hay muchos links para redireccionar a varios artículos más específicos, presupongo que puedes también acceder a esos

con esto ya listo, vuelve a hacer la planeación de todo
```

### Prompt 3

```text
ok empezemos
```

## Pregunta sobre elementos semánticos

Pregunta considerada durante la planeación:

> ¿Para presentar las tres funciones principales de Disneco dentro de una misma parte de la página conviene usar `section`, `article` o `div`?

Elementos utilizados:

- Se utilizó una `<section>` para agrupar la parte temática "Nuestra solución".
- Se utilizó un `<article>` para cada función: comparación, comunicación y seguimiento.
- No se utilizó `<div>`, porque existían elementos con un significado semántico más preciso.

## Partes generadas con IA

- La estructura inicial de las dos páginas HTML.
- La organización de las secciones y los artículos.
- El primer borrador del formulario de contacto.
- La adaptación del contenido de Disneco a una landing page semántica.

## Revisión y cambios

El borrador se revisó para asegurar que cada página tuviera un solo `h1`, que la jerarquía continuara con `h2` y `h3`, y que los elementos `section` y `article` se usaran de acuerdo con el significado de su contenido.

El formulario se mantuvo corto y se estructuró con `fieldset`, `legend`, `label`, `input`, `select`, `textarea` y `button`. Cada control tiene un `id` y un `label` asociado mediante el atributo `for`. También se utilizaron tipos de entrada y atributos de validación nativos de HTML.

Durante la validación inicial, el W3C mostró avisos informativos por el uso de barras finales en elementos vacíos, por ejemplo `<meta />` e `<input />`. Las barras se retiraron porque no tienen efecto en HTML y así el reporte queda más limpio.

No se agregaron estilos CSS ni código JavaScript porque la tarea evalúa exclusivamente la estructura HTML.

## Revisión con WAVE

WAVE detectó en `index.html` una alerta de enlace redundante. El enlace hacia
`about.html` aparecía tanto en la navegación principal como en el pie de página.
Se conservó el enlace de la navegación y se retiró la repetición del pie de
página, porque ambas opciones dirigían al mismo destino.

La evaluación de `about.html` obtuvo 0 errores, 0 errores de contraste y 0
alertas, con una puntuación AIM de 10 sobre 10. WAVE no señaló una segunda alerta
real en las páginas del proyecto, por lo que no se introdujeron errores
artificiales para producirla. La revisión manual sigue siendo necesaria, tal
como indica la propia herramienta.
