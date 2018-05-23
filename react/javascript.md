# JavaScript

## Funciones

### Definiciones

#### Declaracion de funcion

#### Expresion de funcion

#### Metodo
Un metodo, es una funcion que es propiedad de un objeto.
#### Funcion izada
Es cuando la funcion es declarada despues de la llamada. Solo funciona con una declaracion de funcion y no con una expresion de funcion.


## Array.prototype.map()

Se usa para el mapeo de un array.

### Sintaxis

```javascript
var nuevo_array = arr.map(function callback(currentValue, index, array) {
    // Elemento devuelto de nuevo_array
}[, thisArg])
```
* Callback
  * currentValue

   currentValue lala
  * index

   indice del elemento actual de la iteracion
  * array

   el array que se esta utilizando.
* thisArg

   Opcional, valor que se usa para llamar a this.

#### Referencia
[Mozilla](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Array/map)

## Sentencias

### let

La instruccion ``let`` al igual que ``var``, declara una variable, con la diferencia que let solo estara disponible de manera local, es decir en el mismo bloque.

```JavaScript
var x = 4;

if (1 === 1 ) {
	let x;
	x = 1;
	y = x + 1;
}

console.log(y);
//Se imprime 2
console.log(x);
//Se imprime 4

```

### scope and context

#### context
``context`` de manera simple, es el valor que tiene ``this``, que es la referencia al objeto dentro del que se esta ejecutando.

#### scopes
``scopes`` sirve para determinar el nivel de acceso de alguna variable, funcion, objeto.
##### local scopes
cuando una variable es declarada dentro de una funcion, solo esa funcion y las funciones invocadas en esa funcion tendran acceso a la variable, pero no de manera inversa.
```JavaScript

function first () {
	var variableFirst = 'variable first';
	second();
	function second() {
		var variableSecond = 'variable second';
		// Se muestra variable first
		alert(variableFirst);
		// Se muestra variable second
		alert(variableSecond);
	}
	//Se muestra error
	alert(variableSecond);
}

```

##### global scopes
un ``scope`` se puede volver global en los siguientes casos:
* Cuando una variable, funcion, objeto es declarada fuera de una funcion.
* Cunado a una variable se le asigna un valor sin ser declarado. (En modo estricto, genera un error)

```javascript


```


### this

this es un keyword que se usa para referirse dependiendo el contexto en donde se esta ejecutando.

```javascript
function testFunction () {
	alert(this);
}
//El this hace referencia al objeto window, ya que la funcion al no estar directamente en un objeto, pertenece al objeto global window.
testFunction()

//Cuando se hace una instancia a la funcion, se convierte en un objeto, por eso, this hace referencia al objeto testFunction y no al objeto global window
new testFunction();
```
Nota: en modo estricto ``use strict``, cuando una funcion es invocada fuera d eun objeto, el keyword ``this``, en lugar de tomar el objeto global window, nos arrojara un error.
