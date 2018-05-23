# Apuntes React

## JSX

#### Que es?
JSX es un preprocesador y transforma el codigo a javascript, que tiene como proposito, poder tener una facil lectura por parte del desarrollador.
#### Sintaxis
JSX usa una sintaxis muy similar a HTML, existen algunas diferencias, un ejemplo seria escribir el nombre de una clase en una etiqueta.
#### Ejemplo
##### HTML
```html
<h1 class="miClaseChida">Tag en html</h1>
```
##### JSX
```javascript
<h1 className="miClaseChida">Tag en JSX</h1>
```
### Condiciones

Se pueden agregar condiciones siempre y cuando no se encuentren dentro del codigo jsx.

La sintaxis es la de js.

#### If / Else condition

```javascript
if (true) {
	//Some condition
} else {
	//else condition
}
```

#### Ternary Operator

Sintaxis del operador ternario

```javascript
x == true ? 'es true' : 'es false';
```

Ejemplo para usar dentro de jsx code
```javascript
<p className={x == true ? 'nameClass' : 'noNameClass'} >Algun Texto</p>
```
#### &&

No es exclusivo de React, se ejecuta una accion en caso de ser true.

##### Ejemplo

```javascript
{beearAge > 18 && <p>Get a beer now!</p>}
```

## Componentes

Para que react funcione, se necesita importar el objeto react. Con esto se podra accesar a las propiedades del objeto, tales como `React.createElement()`.

```JavaScript
import React from 'react'
```

Para obtener metodos que ayuden con la interaccion del DOM, se necesita importar el objeto react-dom.
```JavaScript
import reactDOM from 'react-dom';
```
los componentes son creados por medio de clases, haciendo una subclase de `Component`.
El siguiente codigo muestra la estructura de una clase para crear un cokponente
```JavaScript
class miComponente extends React.Component {
	//Algo de codigo
}
```
Se necesita el metodo render para cuando sea instanciado, se cree el componente.
```javascript
class miComponente extends React.component {
	render() {
		return <p>Soy un componente</p>
	}
}
```
Los componentes heredan sus metodos, en este caso, se hereda el metodo render. Cuando el componente es instanciado dentro de `reactDOM.render()`, este manda a llamar el metodo render de la clase instanciada, en este caso, el metodo render de la clase miComponente.

## Props
`props` son las propiedades que tiene el componente.

## States

Es un atributo.

### setStates

El setStates tiene como funcion principal buscar en el DOM virtual, algun cambio que se haya realizado. En caso de que detecta un cambio, ejecuta el metodo render del nodo, en este caso, de la clase.
