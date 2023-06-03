# Sintaxis basica del lenguaje

JavaScript es un lenguaje de programación fundamental en el desarrollo web. Con su capacidad para agregar interactividad y dinamismo a las páginas web, se ha convertido en una herramienta esencial para los desarrolladores. En este capitulo, exploraremos la sintaxis básica de JavaScript, brindándote los fundamentos necesarios para comenzar a programar en este lenguaje versátil.

### Variables y tipos de datos:

En JavaScript, las variables se utilizan para almacenar valores. Puedes declarar una variable usando las palabras clave var, let o const. Por ejemplo:

``` javascript
var nombre = "Juan";
``` 

En JavaScript, los tipos de datos son fundamentales para almacenar y manipular información. Conocer los diferentes tipos de datos disponibles y saber cuándo utilizar cada uno es esencial para escribir código eficiente y preciso. JavaScript tiene varios tipos de datos, como cadenas de texto (strings), números, booleanos, arrays y objetos. Puedes asignar valores a variables y combinar diferentes tipos de datos. Por ejemplo:

``` javascript
var mensaje = "¡Hola, mundo!";
var numero = 42;
var esValido = true;
var lista = [1, 2, 3, 4, 5];
var persona = { nombre: "Juan", edad: 25 };
```
#### String (Cadenas de texto):

El tipo de dato `string` se utiliza para representar texto. Puedes crear cadenas utilizando comillas simples (''), comillas dobles ("") o a partir del constructor String(). Los strings son útiles para almacenar nombres, mensajes, direcciones de correo electrónico y cualquier otro tipo de información textual.

``` javascript
let nombre = "Juan";
let mensaje = '¡Hola, bienvenido!';
```


#### Number (Números):

El tipo de dato `number` se utiliza para representar valores numéricos, ya sean enteros o decimales. JavaScript no distingue entre enteros y flotantes, ambos se consideran números. Los números son útiles para realizar cálculos matemáticos y realizar operaciones aritméticas.

``` javascript
let edad = 25;
let pi = 3.1416;
```


#### Boolean (Booleanos):
El tipo de dato `boolean` representa un valor lógico y puede tener dos posibles valores: `true` o `false`. Los booleanos son útiles para realizar evaluaciones condicionales y controlar el flujo de ejecución en el código.
``` javascript
let esMayorDeEdad = true;
let usuarioAutenticado = false;
```


#### Array (Arreglos):
El tipo de dato `array` permite almacenar múltiples valores en una sola variable. Los elementos dentro de un arreglo se pueden acceder mediante un índice numérico. Los arreglos son útiles para almacenar listas de elementos relacionados, como nombres de usuarios, números de teléfono, etc.
``` javascript
let numeros = [1, 2, 3, 4, 5];
let frutas = ["manzana", "naranja", "plátano"];
```


#### Object (Objetos):
El tipo de dato `object` se utiliza para almacenar colecciones de pares clave-valor. Un objeto puede contener propiedades que describen sus características. Los objetos son útiles para representar entidades más complejas, como usuarios, productos, etc.

``` javascript
let persona = {
  nombre: "Juan",
  edad: 25,
  profesion: "programador"
};
```

#### Null y Undefined:

`null` y `undefined` son tipos especiales que representan la ausencia de valor. null se utiliza cuando se quiere asignar explícitamente la ausencia de valor a una variable, mientras que undefined se asigna automáticamente a las variables que no se les ha asignado ningún valor.

``` javascript
let datoNulo = null;
let datoNoDefinido;
```

