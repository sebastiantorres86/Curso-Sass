# Sass: Extienda un conjunto de estilos CSS a otro elemento

Sass tiene una característica llamada `extend` que facilita tomar prestadas las reglas CSS de un elemento y construir sobre ellas en otro.

Por ejemplo, el siguiente bloque de reglas CSS diseña una clase `.panel`. Tiene un `background-color`, `height` y `border`.

````
.panel{
  background-color: red;
  height: 70px;
  border: 2px solid green;
}
````

Ahora quieres otro panel llamado `.big-panel`. Tiene las mismas propiedades base que `.panel`, pero también necesita un `width` y un `font-size`. Es posible copiar y pegar las reglas CSS iniciales de `.panel`, pero el código se vuelve repetitivo a medida que agrega más tipos de paneles. La directiva `extend` es una manera simple de reutilizar las reglas escritas para un elemento, luego agrega más para otro:

````
.big-panel {
  @extend .panel;
  width: 150 px;
  font-size: 2em;
}
````

El `.big-panel` tendrá las mismas propiedades que `.panel` además de los nuevos estilos.

----

# Desafío
Haga una clase `.info-important` que extienda `.info` y que también tenga un `background-color` establecido en magenta.

## Requisitos
+ Su clase `.info-important` debe tener un `background-color` establecido en magenta.
Su clase `.info-important` debe usar `@extend` para heredar el estilo de la clase de `.info`.

[Ver el código](https://codepen.io/sebastiantorres86/pen/ZEGLoRY)
----
