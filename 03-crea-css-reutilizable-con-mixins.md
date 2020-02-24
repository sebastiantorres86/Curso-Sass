# Sass: Crear CSS reutilizable con Mixins

En Sass, un _mixin_ es un grupo de declaraciones CSS que se pueden reutilizar en toda la hoja de estilos.

Las nuevas funciones de CSS toman tiempo antes de que se adopten por completo y estén listas para usar en todos los navegadores. A medida que se agregan características a los navegadores, las reglas CSS que las usan pueden necesitar prefijos de proveedor. Considere "box-shadow":

````
div {
  -webkit-box-shadow: 0px 0px 4px #fff;
  -moz-box-shadow: 0px 0px 4px #fff;
  -ms-box-shadow: 0px 0px 4px #fff;
  box-shadow: 0px 0px 4px #fff;
}
````

Es una gran cantidad de tipeo reescribir esta regla para todos los elementos que tienen un `box-shadow`, o cambiar cada valor para probar diferentes efectos. Los mixins son como funciones para CSS. Aquí está cómo escribir uno:

````
@mixin box-shadow ($x, $y, $blur, $c) {
  -webkit-box-shadow: $x, $y, $blur, $c;
  -moz-box-shadow: $x, $y, $blur, $c;
  -ms-box-shadow: $x, $y, $blur, $c;
  box-shadow: $x, $y, $blur, $c;
}
````

La definición comienza con `@mixin` seguido de un nombre personalizado. Los parámetros (`$x`, `$y`, `$blur` y `$c` en el ejemplo anterior) son opcionales. Ahora, cada vez que se necesita una regla de box-shadow, solo una línea que llama al mixin reemplaza tener que escribir todos los prefijos de proveedor. Se llama a un mixin con la directiva `@include`:

````
div {
  @include box-shadow (0px, 0px, 4px, #fff);
}
````

----

# Desafío
Escriba un mixin para `border-radius` y dele un parámetro `$radius`. Debería usar todos los prefijos de proveedor del ejemplo. Luego use el mixin de `border-radius` para darle al elemento `#awesome` un border-radius de 15px.

## Requisitos
+ Nuestro código debe declarar un mixin llamado `border-radius` que tiene un parámetro llamado `$radius`.
+ Su código debe incluir el prefijo de proveedor `-webkit-border-radius` que usa el parámetro `$radius`.
+ Su código debe incluir el prefijo de proveedor `-moz-border-radius` que usa el parámetro `$radius`.
+ Su código debe incluir el prefijo de proveedor `-ms-border-radius` que usa el parámetro `$radius`.
+ Su código debe incluir la regla general de `border-radius` que usa el parámetro `$radius`.
+ Su código debe llamar al `mixin de border-radius` usando la palabra clave `@include`, configurándolo en 15px.

[Ver el código](https://codepen.io/sebastiantorres86/pen/yLNgKMv)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/04-use-%40if-y-%40else-para-agregar-logica-a-sus-estilos.md)