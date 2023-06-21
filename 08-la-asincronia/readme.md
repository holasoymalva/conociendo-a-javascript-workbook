# Navegando la Asincronía en JavaScript: Event Loop y Call Stack

La asincronía es una parte fundamental de JavaScript, ya que nos permite realizar operaciones sin bloquear la ejecución del programa. 
En JavaScript, la asincronía se maneja mediante el Event Loop y el Call Stack.

### El Call Stack

El Call Stack, o pila de llamadas, es una estructura de datos que rastrea las funciones en ejecución. 
Cada vez que se llama a una función, se agrega a la parte superior del Call Stack. Cuando una función termina de ejecutarse, se elimina del Call Stack. Esto significa que JavaScript ejecuta las funciones en orden secuencial, una tras otra.

``` javascript
function sumar(a, b) {
  return a + b;
}

function multiplicar(a, b) {
  return a * b;
}

function calcular() {
  var resultadoSuma = sumar(2, 3);
  var resultadoMultiplicacion = multiplicar(resultadoSuma, 4);
  console.log(resultadoMultiplicacion);
}

calcular(); // Salida: 20
```

En el ejemplo anterior, las funciones se agregan al Call Stack en el orden en que se llaman y se eliminan una vez que han terminado de ejecutarse.

### Event Loop y Cola de Eventos:

El Event Loop es un mecanismo en JavaScript que permite manejar la asincronía. Cuando una operación asíncrona, como una solicitud de red o una temporización, se inicia, se coloca en la cola de eventos. El Event Loop se encarga de verificar constantemente si el Call Stack está vacío. Si el Call Stack está vacío, toma el próximo evento de la cola y lo coloca en el Call Stack para que se ejecute.

``` javascript
console.log("Inicio");

setTimeout(function() {
  console.log("Operación asíncrona");
}, 2000);

console.log("Fin");
```

En este ejemplo, el mensaje "Inicio" y "Fin" se imprimirán de inmediato en el Call Stack, ya que son operaciones sincrónicas. Sin embargo, la función de temporización setTimeout se coloca en la cola de eventos y se ejecutará después de un retraso de 2000 milisegundos. Esto demuestra cómo JavaScript puede continuar con la ejecución de otras tareas mientras espera que las operaciones asíncronas se completen.

##  Cómo funciona el Heap de memoria en JavaScript
El Heap de memoria en JavaScript es una parte fundamental de cómo se gestiona y utiliza la memoria en este lenguaje de programación. En esta seccion, exploraremos qué es el Heap de memoria, cómo se organiza y cómo se manejan los objetos en él, con ejemplos de código para ilustrar su funcionamiento.

### ¿Qué es el Heap de memoria en JavaScript?
El Heap de memoria en JavaScript es una región de la memoria utilizada para almacenar objetos y estructuras de datos dinámicas. A diferencia de la Pila de memoria, que se utiliza para gestionar el flujo de ejecución de las funciones y mantener las variables locales, el Heap se encarga de almacenar objetos y datos que se asignan y desasignan dinámicamente durante la ejecución del programa.

### Organización del Heap de memoria
El Heap de memoria en JavaScript está organizado en forma de montón (heap en inglés), que es una estructura de datos en la que los objetos se almacenan de manera no secuencial. A medida que se crean y se asignan objetos en el Heap, se utilizan algoritmos de administración de memoria para encontrar espacios disponibles y asignar la memoria necesaria.

Ejemplo de asignación de objetos en el Heap
Veamos un ejemplo de cómo se asignan objetos en el Heap de memoria en JavaScript:

``` javascript
// Creación de un objeto en el Heap
const obj = { nombre: 'John', edad: 30 };
```

En este ejemplo, creamos un objeto utilizando la sintaxis de notación de objetos. El objeto { nombre: 'John', edad: 30 } se almacena en el Heap de memoria y la variable obj contiene una referencia a ese objeto en el Heap.

### Gestión de la memoria en el Heap
JavaScript utiliza un algoritmo de recopilación de basura (garbage collector) para administrar la memoria en el Heap. Este algoritmo es responsable de identificar los objetos que ya no están siendo utilizados por el programa y liberar la memoria que ocupan, lo que se conoce como recolección de basura.

Ejemplo de recolección de basura
Veamos un ejemplo de cómo funciona la recolección de basura en JavaScript:

``` javascript
let obj1 = { nombre: 'John', edad: 30 };
let obj2 = { nombre: 'Jane', edad: 28 };

obj1 = obj2; // obj1 ahora apunta al mismo objeto que obj2

// El objeto { nombre: 'John', edad: 30 } ya no tiene referencias y será eliminado en la próxima recolección de basura
```

En este ejemplo, inicialmente creamos dos objetos obj1 y obj2. Luego, asignamos obj2 a obj1, lo que significa que ambas variables hacen referencia al mismo objeto en el Heap. El objeto { nombre: 'John', edad: 30 } ya no tiene referencias y se considera inaccesible, por lo que será identificado y eliminado en la próxima recolección de basura.

