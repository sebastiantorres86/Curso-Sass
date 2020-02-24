# Sass: use @for para crear un bucle Sass

La directiva `@for` agrega estilos en un bucle, muy similar a un bucle `for` en JavaScript.

`@for` se usa de dos maneras: "start through end" o "start to end". La principal diferencia es que el "start __to__ end" _excluye_ el número final como parte del recuento, y el "start __through__ end" _incluye_ el número final como parte del recuento.

Aquí hay un ejemplo de start __through__ end:

````
@for $i from 1 through 12 {
  .col-#{$i} { width: 100%/12 * $i; }
}
````

La parte `#{$i}` es la sintaxis para combinar una variable (`i`) con texto para formar una cadena. Cuando el archivo Sass se convierte a CSS, se ve así:

````
.col-1 {
  width: 8.33333%;
}

.col-2 {
  width: 16.66667%;
}

...

.col-12 {
  width: 100%;
}
````

Esta es una forma poderosa de crear un diseño de grid. Ahora tiene doce opciones para anchos de columna disponibles como clases CSS.

----

# Desafío
Escriba una directiva `@for` que tome una variable `$j` que va del 1 __al__ 6.

Debería crear 5 clases llamadas `.text-1` a `.text-5` donde cada una tiene un `font-size` establecido en 15px multiplicado por el índice.

## Requisitos
+ Su código debe usar la directiva `@for`.
+ Su clase `.text-1` debe tener un `font-size` de 15px.
+ Su clase `.text-2` debe tener un `font-size` de 30px.
+ Su clase `.text-3` debe tener un `font-size` de 45 px.
+ Su clase `.text-4` debe tener un `font-size` de 60px.
+ Su clase `.text-5` debe tener un `font-size` de 75px.

[Ver el código](https://codepen.io/sebastiantorres86/pen/PoqWRLj)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/06-use-%40each-para-mapear-elementos-en-una-lista.md)