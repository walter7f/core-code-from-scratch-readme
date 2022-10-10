# <b>Week Challenges "Thuesday"</b>
## [<b>Ejercicio React </b>](https://www.codewars.com/kata/5a95947f4a6b342636000173)

Solucion 
```jsx
import React from 'react';

export const EggList = ({eggs}) => {
return(
<ul>
  {eggs.map((eggs, index)=>{
  return <EasterEgg name={eggs} key={index}/>
})}
</ul>
)
};

export const EasterEgg = ({name}) => {
  return <li>{name}</li>
};

```




# <b>Week Challenges "Wendnesday"</b>
## <b>¿Qué es React (React js) y por qué es tan popular?</b>
Sirve para desarrollar aplicaciones web de una manera más ordenada y con menos código que si usas Javascript puro o librerías como jQuery centradas en la manipulación del DOM. Permite que las vistas se asocien con los datos, de modo que si cambian los datos, también cambian las vistas.

React es una biblioteca de JavaScript para crear interfaces de usuario rapidas e interactivas, fue desarrollada por facebook y actualmente es la biblioteca de JavaScript mas popular, particularmente las aplicaciones de React son componentes un componente es esencialmente una pieza de interfaz de usuario, entonces cuando creamos una aplicacion en React construimos un grupo de componentes aislados y reutilizables independientes, luego los usamos para crear interfaces de usuario complejas. Cada aplicacion de React tiene un compontente al que nos referimos como componente raiz.

<img src="https://reactiveprogramming.io/figures/react/web-components.png"/>
