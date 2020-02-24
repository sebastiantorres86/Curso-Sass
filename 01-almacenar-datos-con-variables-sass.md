# Sass: almacenar datos con variables Sass

Una característica de Sass que es diferente de CSS es que usa variables. Se declaran y configuran para almacenar datos, de forma similar a JavaScript.

En JavaScript, las variables se definen con las palabras clave `let` y `const`. En Sass, las variables comienzan con un `$` seguido del nombre de la variable.

Aqui hay un par de ejemplos:

````
$main-fonts: Arial, sans-serif;
$headings-color: green;

// Para usar variables:
h1 {
   font-family: $main-fonts;
   color: $headings-color;
}
````

Un ejemplo en el que las variables son útiles es cuando varios elementos deben ser del mismo color. Si se cambia ese color, el único lugar para editar el código es el valor variable.

----

# Desafío
Cree una variable `$text-color` y configúrela en red. Luego cambie el valor de la propiedad de color para `.blog-post` y `h2` a la variable `$text-color`.

## Requisitos
+ Su código debe tener una variable Sass declarada para `$text-color` con un valor red.
+ Su código debe usar la variable `$text-color` para cambiar el color de los elementos `.blog-post` y `h2`.
+ Su elemento `.blog-post` debe tener un color red.
+ Sus elementos `h2` deben tener un color red.

[Ver el código](https://codepen.io/sebastiantorres86/pen/QWbdQXd)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/02-anidar-css-con-sass.md)