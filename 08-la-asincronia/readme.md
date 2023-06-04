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


