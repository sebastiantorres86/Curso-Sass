# Sass: use @each para asignar elementos en una lista

El último desafío mostró cómo la directiva `@for` usa un valor inicial y final para recorrer un cierto número de veces. Sass también ofrece la directiva `@each` que recorre cada elemento en una lista o mapa. En cada iteración, la variable se asigna al valor actual de la lista o mapa.

````
@each $color en blue, red, green {
  .#{$color}-text {color: $color;}
}
````

Un mapa tiene una sintaxis ligeramente diferente. Aquí hay un ejemplo:

````
$colors: (color1: blue, color2: red, color3: green);

@each $key, $color in $colors {
  .#{$color}-text {color: $color;}
}
````

Tenga en cuenta que la variable `$key` es necesaria para hacer referencia a las claves en el mapa. De lo contrario, el CSS compilado tendría `color1`, `color2`... en él. Los dos ejemplos de código anteriores se convierten en el siguiente CSS:

````
.blue-text {
  color: blue;
}

.red-text {
  color: red;
}

.green-text {
  color. green;
}
````
----

# Desafío
Escriba una directiva `@each` que pase por una lista: `blue, black, red` y asigne cada variable a una clase `.color-bg`, donde la parte "color" cambia para cada elemento. Cada clase debe establecer el `background-color` del color respectivo.

## Requisitos
+ Su código debe usar la directiva `@each`.
+ Su clase `.blue-bg` debe tener un `background-color` blue.
+ Su clase `.black-bg` debe tener un `background-color` negro.
+ Su clase `.red-bg` debe tener un `background-color` rojo.

[Ver el código](https://codepen.io/sebastiantorres86/pen/OJVWZJO)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/07-aplicar-un-estilo-hasta-que-se-cumpla-una-condicion-cpn-%40while.md)