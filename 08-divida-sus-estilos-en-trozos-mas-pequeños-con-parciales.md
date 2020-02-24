# Sass: divide tus estilos en fragmentos más pequeños con parciales

Los _parciales_ en Sass son archivos separados que contienen segmentos de código CSS. Estos se importan y se usan en otros archivos Sass. Esta es una excelente manera de agrupar código similar en un módulo para mantenerlo organizado.

Los nombres para los parciales comienzan con el carácter de subrayado (___), que le dice a Sass que es un pequeño segmento de CSS y que no debe convertirlo en un archivo CSS. Además, los archivos Sass terminan con la extensión de archivo `.scss`. Para llevar el código parcial a otro archivo Sass, use la directiva `@import`.

Por ejemplo, si todos sus mixins se guardan en un parcial llamado "_mixins.scss", y se necesitan en el archivo "main.scss", esta es la forma de usarlos en el archivo principal:

````
// En el archivo main.scss

@import 'mixins'
````

Tenga en cuenta que el subrayado y la extensión de archivo no son necesarios en la declaración `import`: Sass entiende que es parcial. Una vez que se importa un parcial a un archivo, todas las variables, mixins y otros códigos están disponibles para su uso

----

# Desafío
Escriba una instrucción `@import` para importar un parcial llamado `_variables.scss` en el archivo main.scss.

## Requisitos
+ Su código debe usar la directiva `@import` y no debe incluir el guión bajo en el nombre del archivo.

[Ver el código](https://codepen.io/sebastiantorres86/pen/eYNgreY)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/09-extienda-un-conjunto-de-estilos-css-a-otro-elemento.md)