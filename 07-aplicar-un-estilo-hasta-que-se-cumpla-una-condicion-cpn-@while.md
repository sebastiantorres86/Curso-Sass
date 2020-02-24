# Sass: aplique un estilo hasta que se cumpla una condición con @while

La directiva `@while` es una opción con una funcionalidad similar al bucle `while` de JavaScript. Crea reglas CSS hasta que se cumpla una condición.

El desafío `@for` dio un ejemplo para crear un sistema de cuadrícula simple. Esto también puede funcionar con `@while`.

````
$x: 1;
@while $x < 13 {
  .col-#{$x} {width: 100%/12 * $x;}
  $x: $x + 1;
}
````

Primero, defina una variable `$x` y configúrela en 1. Luego, use la directiva `@while` para crear el sistema de cuadrícula mientras `$x` es menor que 13. Después de configurar la regla CSS para `width`, `$x` se incrementa en 1 para evitar un Bucle infinito.

----

# Desafío
Use `@while` para crear una serie de clases con diferentes `font-sizes`.

Debe haber 5 clases diferentes desde `text-1` hasta `text-5`. Luego establezca el `font-size` en `15px` multiplicado por el número de índice actual. ¡Asegúrate de evitar un bucle infinito!

## Requisitos
+ Su código debe usar la directiva `@while`.
+ Su código debe usar una variable de índice que comience en un índice de 1.
+ Su código debe incrementar la variable del contador.
+ Su clase `.text-1` debe tener un `font-size` de 15px.
+ Su clase `.text-2` debe tener un `font-size` de 30px.
+ Su clase `.text-3` debe tener un `font-size` de 45 px.
+ Su clase `.text-4` debe tener un `font-size` de 60px.
+ Su clase `.text-5` debe tener un `font-size` de 75px.

[Ver el código](https://codepen.io/sebastiantorres86/pen/MWwJGeR)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/08-divida-sus-estilos-en-trozos-mas-peque%C3%B1os-con-parciales.md)