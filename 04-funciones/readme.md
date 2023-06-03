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


## Block Scope o alcance de bloque

Durante nuestro analisis de cuando utilizar var let y const tocamos un tema que no habiamos escuchado hasta este punto `El BlockScope` o `El alcance de bloque` ¿Pero a que se refiere el alcance de bloque?
