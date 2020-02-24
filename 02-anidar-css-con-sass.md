# Sass: Anidar CSS con Sass

Sass permite anidar reglas CSS, que es una forma útil de organizar una hoja de estilo.

Normalmente, cada elemento está dirigido a una línea diferente para darle estilo, así:

````
nav {
   background-color: red;
}

nav ul {
   list-style: none;
}

nav ul li {
   display: inline-block;
}
````

Para un proyecto grande, el archivo CSS tendrá muchas líneas y reglas. Aquí es donde la anidación puede ayudar a organizar su código al colocar reglas de estilo secundario dentro de los elementos principales respectivos:

````
nav {
   background-color: red;

   ul {
     list-style: none;

     li {
       display: inline-block;
     }
   }
}
````

----

# Desafío
Use la técnica de anidación que se muestra arriba para reorganizar las reglas CSS para ambos elementos secundarios del elemento `.blog-post`. Para fines de prueba, el `h1` debe aparecer antes que el elemento `p`.

## Requisitos
+ Su código debe reorganizar las reglas CSS para que `h1` y `p` se aniden en el elemento primario `.blog-post`.

[Ver el código](https://codepen.io/sebastiantorres86/pen/JjdELYw)
----
[Próxima clase](https://github.com/sebastiantorres86/Curso-Sass/blob/master/03-crea-css-reutilizable-con-mixins.md)