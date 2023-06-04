# Funciones y BlockScope

——————— Aqui va Funciones en Javascript





## Diferencias entre var, let y const

Dentro de JavaScript, la declaración de variables juega un papel fundamental en el manejo de datos. Anteriormente, se utilizaba la palabra clave `var` para declarar variables, pero con la introducción de ECMAScript 6 (ES6), se agregaron las palabras clave `let` y `const`.

#### var: El enfoque tradicional

Antes de la llegada de ES6, `var` era la única palabra clave para declarar variables en JavaScript. Sin embargo, var tiene algunas particularidades que pueden conducir a comportamientos inesperados. Una de las principales diferencias es que las variables declaradas con `var` tienen un alcance de función o global, lo que significa que pueden ser accesibles fuera del bloque en el que fueron declaradas. Por ejemplo:


```javascript

function ejemploVar() {
  if (true) {
    var x = 10;
  }
  console.log(x); // 10
}
```

#### let: Introduciendo el alcance de bloque
Con la introducción de `let`, se resolvió uno de los problemas de `var`: `el alcance de bloque`. Cuando declaras una variable con `let`, esta solo está disponible dentro del bloque en el que se declaró. Por ejemplo:

```javascript

function ejemploLet() {
  if (true) {
    let x = 10;
  }
  console.log(x); // Error: x no está definido
}
```

Además, `let` permite reasignar valores a la misma variable en el mismo ámbito sin ningún problema.

#### const: Variables inmutables
La palabra clave `const` se utiliza para declarar variables cuyos valores no cambiarán una vez asignados. Al igual que let, const tiene un alcance de bloque, pero a diferencia de var y let, no se puede reasignar un nuevo valor a una variable declarada con const. Por ejemplo:

```javascript

function ejemploConst() {
  const pi = 3.1416;
  pi = 3.14; // Error: no se puede reasignar un valor a una variable constante
}
```

Sin embargo, ten en cuenta que si declaras un objeto o un array con const, los elementos internos pueden ser modificados. La inmutabilidad solo se aplica a la variable en sí misma, no a sus propiedades o elementos.

Elección adecuada de palabras clave
A la hora de elegir entre `var`, `let` y `const`, es importante considerar el alcance y la mutabilidad de las variables en tu código. En general, se recomienda utilizar `let` en lugar de `var` para evitar problemas con el alcance y aprovechar `el alcance de bloque`. Además, utiliza const cuando desees asegurarte de que una variable no cambie su valor.


## Explorando el Block Scope en JavaScript: Una introducción al alcance de bloque

Durante nuestro analisis de cuando utilizar `var`, `let` y `const` tocamos un tema que no habiamos escuchado hasta este punto `El BlockScope` o `El alcance de bloque` ¿Pero a que se refiere el alcance de bloque?

El alcance (scope) en JavaScript determina la accesibilidad y visibilidad de variables y funciones en diferentes partes del código. Anteriormente, JavaScript solo tenía alcance de función, lo que significa que una variable declarada dentro de una función era accesible en todo el cuerpo de la función. Sin embargo, con la introducción de ECMAScript 6 (ES6), se agregó el alcance de bloque. En este artículo, exploraremos el concepto del Block Scope (alcance de bloque) en JavaScript y cómo afecta la declaración y accesibilidad de variables.

¿Qué es el Block Scope?
El Block Scope se refiere al alcance de una variable cuando está declarada dentro de un bloque de código delimitado por llaves {}. Un bloque puede ser una función, una declaración condicional if, un bucle for, entre otros. Dentro de un bloque, las variables declaradas con let y const tienen un alcance limitado al bloque en el que fueron declaradas.

```javascript
function ejemploBlockScope() {
  var x = 10;
  let y = 20;

  if (x === 10) {
    var x = 30;
    let y = 40;

    console.log(x); // 30
    console.log(y); // 40
  }

  console.log(x); // 30
  console.log(y); // 20
}
```

En el ejemplo anterior, `x` se declara inicialmente como `10` en el ámbito de la función. Dentro del bloque condicional `if`, `x` se redefine como `30` utilizando `var`, lo que afecta su valor tanto dentro como fuera del bloque. Por otro lado, `y` se declara tanto dentro como fuera del bloque `if` utilizando `let`, lo que crea una nueva variable `y` con un valor diferente dentro del bloque.

### Ventajas del Block Scope:

El alcance de bloque proporciona una mayor claridad y control en la gestión de variables en JavaScript. Al limitar el alcance de las variables a un bloque específico, se evitan posibles conflictos y se mejora la legibilidad del código. Además, al utilizar `let` y `const` en lugar de `var`, se evitan problemas comunes relacionados con el alcance en JavaScript.

Consideraciones importantes:

* Las variables declaradas con `var` tienen un alcance de función o global, no de bloque. Por lo tanto, no se ven afectadas por el alcance de bloque.
* La redeclaración de una variable con `var` en el mismo bloque no crea una nueva variable, sino que modifica la existente.
* Las variables declaradas con `let` y `const` tienen un comportamiento de "temporal dead zone" (zona temporalmente muerta), lo que significa que no pueden ser accesibles antes de su declaración en el código.

En conclusión, el Block Scope en JavaScript es una adición valiosa al lenguaje que te permite tener un control más preciso sobre el alcance de tus variables. Utilizar `let` y `const` dentro de bloques específicos ayuda a evitar conflictos y errores, y mejora la legibilidad y mantenibilidad del código. Aprovecha al máximo el alcance de bloque para escribir código más robusto y claro en tus proyectos de JavaScript.










