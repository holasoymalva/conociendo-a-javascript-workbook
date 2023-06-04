# Operadores Aritméticos y Lógicos

En el mundo de la programación, los operadores son herramientas esenciales que nos permiten realizar operaciones matemáticas y evaluaciones lógicas en nuestros programas. JavaScript, como lenguaje de programación, ofrece una amplia gama de operadores aritméticos y lógicos para manipular datos y realizar decisiones basadas en condiciones. En este artículo, vamos a adentrarnos en el fascinante mundo de los operadores aritméticos y lógicos en JavaScript y aprender cómo aprovechar su potencial en nuestros programas.

Operadores Aritméticos:
Los operadores aritméticos en JavaScript se utilizan para realizar cálculos matemáticos básicos. Aquí están los operadores aritméticos más comunes:

* Suma (+): El operador de suma se utiliza para sumar dos valores.

* Resta (-): El operador de resta se utiliza para restar un valor de otro.

* Multiplicación (*): El operador de multiplicación se utiliza para multiplicar dos valores.

* División (/): El operador de división se utiliza para dividir un valor entre otro.

* Módulo (%): El operador de módulo se utiliza para obtener el resto de una división entre dos valores.

* Incremento (++): El operador de incremento se utiliza para aumentar en uno el valor de una variable.

* Decremento (--): El operador de decremento se utiliza para disminuir en uno el valor de una variable.

Ejemplo:


``` javascript
let x = 5;
let y = 2;

let suma = x + y; // 7
let resta = x - y; // 3
let multiplicacion = x * y; // 10
let division = x / y; // 2.5
let modulo = x % y; // 1

let incremento = ++x; // 6
let decremento = --y; // 1
``` 

Operadores Lógicos:
Los operadores lógicos en JavaScript se utilizan para realizar evaluaciones lógicas y combinar condiciones. Aquí están los operadores lógicos más comunes:

* AND lógico (&&): El operador AND lógico devuelve true si ambas expresiones son verdaderas.

* OR lógico (||): El operador OR lógico devuelve true si al menos una de las expresiones es verdadera.

* NOT lógico (!): El operador NOT lógico invierte el valor de una expresión. Si es true, lo convierte en false y viceversa.

Ejemplo:


``` javascript
let a = true;
let b = false;

let andLogico = a && b; // false
let orLogico = a || b; // true
let notLogico = !a; // false
``` 

Los operadores lógicos son especialmente útiles cuando se trata de tomar decisiones basadas en condiciones. Nos permiten combinar múltiples expresiones lógicas y evaluar si se cumplen ciertas condiciones o no.

## Estructuras de control

En la programación, las estructuras de control son fundamentales para controlar el flujo de ejecución de un programa. En JavaScript, disponemos de diversas estructuras de control que nos permiten tomar decisiones, repetir bloques de código y realizar acciones condicionales.

#### Estructura de control if-else:
La estructura if-else nos permite tomar decisiones basadas en una condición. Si la condición se evalúa como verdadera, se ejecuta un bloque de código especificado. En caso contrario, se ejecuta otro bloque de código definido por el else.

``` javascript
let edad = 18;

if (edad >= 18) {
  console.log("Eres mayor de edad");
} else {
  console.log("Eres menor de edad");
}
``` 

#### Estructura de control switch:
La estructura switch nos permite evaluar una expresión y ejecutar diferentes bloques de código según el valor de la expresión. Cada bloque de código está asociado a un caso específico.


``` javascript
let diaSemana = 1;

switch (diaSemana) {
  case 1:
    console.log("Lunes");
    break;
  case 2:
    console.log("Martes");
    break;
  case 3:
    console.log("Miércoles");
    break;
  default:
    console.log("Día no válido");
    break;
}
``` 

#### Estructura de control for:
La estructura for se utiliza para repetir un bloque de código un número específico de veces. Es especialmente útil cuando se conoce el número exacto de iteraciones necesarias.

``` javascript
for (let i = 0; i < 5; i++) {
  console.log("Iteración: " + i);
}
``` 


#### Estructura de control while:
La estructura while se utiliza para repetir un bloque de código mientras una condición se evalúe como verdadera. Es útil cuando no se conoce el número exacto de iteraciones necesarias.


``` javascript
let contador = 0;

while (contador < 5) {
  console.log("Contador: " + contador);
  contador++;
}
``` 


#### Estructura de control do-while:
La estructura do-while es similar a la estructura while, pero garantiza que el bloque de código se ejecute al menos una vez antes de verificar la condición.

``` javascript
let numero = 0;

do {
  console.log("Número: " + numero);
  numero++;
} while (numero < 5);
```
