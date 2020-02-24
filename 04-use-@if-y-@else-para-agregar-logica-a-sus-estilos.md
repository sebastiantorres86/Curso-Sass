# Sass: use @if y @else para agregar lógica a sus estilos

La directiva `@if` en Sass es útil para probar un caso específico: funciona igual que la instrucción `if` en JavaScript.

````
@mixin make-bold($bool) {
  @if $bool == true {
    font-weight: bold;
  }
}
````

Y al igual que en JavaScript, `@else if` y `@else` prueban para más condiciones:

````
@mixin text-effect($val) {
  @if $val == danger {
    color: red;
  }
  @else if $val == alert {
    color: yellow;
  }
  @else if $val == success {
    color: green;
  }
  @else {
    color: black;
  }
}
````

----

# Desafío
Cree un mixin llamado `border-stroke` que tome un parámetro `$val`. El mixin debe verificar las siguientes condiciones usando `@if`, `@else if` y `@else`:
````
light - 1px solid black
medium - 3px solid black
heavy - 6px solid black
````
Si `$val` no es `light`, `medium` o `heavy`, el borde debe establecerse en `none`.

## Requisitos
+ Su código debe declarar un mixin llamado `border-stroke` que tiene un parámetro llamado `$val`.
+ Su mixin debe tener una declaración `@if` para verificar si `$val` es light y establecer el `border` en 1px solid black.
+ Su mixin debe tener una declaración `@else if` para verificar si `$val` es medium y establecer el `border` en 3px solid black.
+ Su mixin debe tener una declaración `@else if` para verificar si `$val` es heavy y establecer el `border` en 6px solid black.
+ Su mixin debe tener una instrucción `@else` para establecer el `borde`r en none.

[Ver el código](https://codepen.io/sebastiantorres86/pen/yLNgKKE)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/05-use-%40for-para-crear-un-bucle-sass.md)