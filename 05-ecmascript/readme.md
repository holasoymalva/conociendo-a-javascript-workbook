# Explorando JavaScript antes de ECMAScript 6: Un Vistazo a las Características Previas al Estándar Moderno

ECMAScript es el estándar en el que se basa JavaScript, y su versión más reciente, ECMAScript 6 (también conocido como ES6 o ES2015), introdujo muchas características nuevas y
poderosas al lenguaje. Sin embargo, antes de ES6, JavaScript ya era un lenguaje versátil y ampliamente utilizado.

### Variables y Declaración de Funciones:
Antes de ES6, la forma de declarar variables y funciones era utilizando las palabras clave var y function, respectivamente. Las variables declaradas con var tenían alcance de función o alcance global, lo que significaba que estaban disponibles dentro de la función o en todo el programa. Las funciones declaradas con function podían ser declaradas en cualquier parte del código y se les podía invocar en cualquier momento.

``` javascript
var nombre = "Juan";
function saludar() {
  console.log("Hola, " + nombre + "!");
}
saludar(); // Salida: Hola, Juan!
``` 

### Arreglos:
Los arreglos en JavaScript antes de ES6 eran objetos indexados con propiedades numéricas. Podíamos acceder a los elementos de un 
arreglo utilizando la notación de corchetes y manipularlos mediante métodos como push, pop, splice, entre otros.


``` javascript
var frutas = ["manzana", "plátano", "naranja"];
console.log(frutas[0]); // Salida: manzana
frutas.push("uva");
console.log(frutas); // Salida: ["manzana", "plátano", "naranja", "uva"]
``` 


### Ciclos de Bucle:
Los ciclos de bucle en JavaScript antes de ES6 incluían el bucle for, el bucle while y el bucle do-while. Estos bucles nos permitían repetir un 
bloque de código mientras se cumpliera una determinada condición.

``` javascript
for (var i = 0; i < 5; i++) {
  console.log(i);
}

var j = 0;
while (j < 5) {
  console.log(j);
  j++;
}

var k = 0;
do {
  console.log(k);
  k++;
} while (k < 5);
``` 

### Objetos Literales:
Los objetos literales en JavaScript antes de ES6 eran una forma de crear objetos utilizando la sintaxis de llaves {}. Podíamos definir 
propiedades y métodos dentro del objeto y acceder a ellos mediante la notación de punto.

``` javascript
var persona = {
  nombre: "Juan",
  edad: 25,
  saludar: function() {
    console.log("Hola, soy " + this.nombre);
  }
};

console.log(persona.nombre); // Salida: Juan
persona.saludar(); // Salida: Hola, soy Juan
``` 
