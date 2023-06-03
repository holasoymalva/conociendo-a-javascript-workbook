# Sintaxis basica del lenguaje

JavaScript es un lenguaje de programación fundamental en el desarrollo web. Con su capacidad para agregar interactividad y dinamismo a las páginas web, se ha convertido en una herramienta esencial para los desarrolladores. En este capitulo, exploraremos la sintaxis básica de JavaScript, brindándote los fundamentos necesarios para comenzar a programar en este lenguaje versátil.

### Variables y tipos de datos:

En JavaScript, las variables se utilizan para almacenar valores. Puedes declarar una variable usando las palabras clave var, let o const. Por ejemplo:

``` javascript
var nombre = "Juan";
``` 


JavaScript tiene varios tipos de datos, como cadenas de texto (strings), números, booleanos, arrays y objetos. Puedes asignar valores a variables y combinar diferentes tipos de datos. Por ejemplo:

``` javascript
var mensaje = "¡Hola, mundo!";
var numero = 42;
var esValido = true;
var lista = [1, 2, 3, 4, 5];
var persona = { nombre: "Juan", edad: 25 };
```


——————— Aqui va Diferencias entre var, let y const

Dentro de JavaScript, la declaración de variables juega un papel fundamental en el manejo de datos. Anteriormente, se utilizaba la palabra clave `var` para declarar variables, pero con la introducción de ECMAScript 6 (ES6), se agregaron las palabras clave `let` y `const`.

Antes de la llegada de ES6, `var` era la única palabra clave para declarar variables en JavaScript. Sin embargo, var tiene algunas particularidades que pueden conducir a comportamientos inesperados. Una de las principales diferencias es que las variables declaradas con `var` tienen un alcance de función o global, lo que significa que pueden ser accesibles fuera del bloque en el que fueron declaradas. Por ejemplo:

——————— Aqui termina Diferencias entre var, let y const
