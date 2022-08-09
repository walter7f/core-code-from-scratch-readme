# Desafio Lunes 
## Ejercicio ¿A quien le gusta?
Probablemente conozcas el sistema de "me gusta" de Facebook y otras páginas. Las personas pueden "gustar" publicaciones de blog, imágenes u otros elementos. Queremos crear el texto que debe mostrarse junto a dicho elemento.

Implemente la función que toma una matriz que contiene los nombres de las personas a las que les gusta un 
artículo.

[]                                -->  "no one likes this"

["Peter"]                         -->  "Peter likes this"

["Jacob", "Alex"]                 -->  "Jacob and Alex like this"

["Max", "John", "Mark"]           -->  "Max, John and Mark like this"

["Alex", "Jacob", "Mark", "Max"]  -->  "Alex, Jacob and 2 others like this"

## Ejercicio de conteo de bits

## Soluccion
```js
function likes(names) {
  if (names.length == 0) return 'no one likes this';
  if (names.length == 1) return names[0] + ' likes this';
  if (names.length == 2) return names[0] + ' and ' + names[1] + ' like this';
  if (names.length == 3) return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
  return (names[0] +', ' +names[1] +' and ' +(names.length - 2) +' others like this');
}
```

## Ejerccio 
Escriba una función que tome un número entero como entrada y devuelva el número de bits que son iguales a uno en la representación binaria de ese número. Puede garantizar que la entrada no sea negativa.

Ejemplo : la representación binaria de 1234es 10011010010, por lo que la función debería regresar 5en este caso

Solucion



```js
var countBits = function(n) {
    // combertimos en binario 
  let binario = n.toString(2);
  let contador =0;
  // recorromos
  for(let i = 0; i < binario.length; i++){
    // si encontramos algo igual a i sumamos 1 al contador 
    if ( binario[i]==="1"){
      contador++;
    }
  }
  return contador;

}
```
## Su pedido, por favor 
## Ejercicio 

Su tarea es ordenar una cadena dada. Cada palabra en la cadena contendrá un solo número. Este número es la posición que debe tener la palabra en el resultado.

Nota: Los números pueden ser del 1 al 9. Por lo tanto, 1 será la primera palabra (no 0).

Si la cadena de entrada está vacía, devuelve una cadena vacía. Las palabras en la cadena de entrada solo contendrán números consecutivos válidos.

Solucion:
``` js 
function order(words){
  words = words.split(' ');
  
  return words.sort((a,b) => {
    if(orden(a) > orden(b)){
      return 1;
    }
    if (orden(a)< orden(b)){
      return -1;
    }
    return 0;
  }).join(' ');
}
  
 function orden(word){
  for (let i = 0; i< word.length; i++ ){
    if(Number.isNaN(parseInt(word[i]))== true){
      continue;
    }else{
      return parseInt(word[i])
    }
  }

}
```
# Desafio Martes 
## Latín de cerdo simple 

Ejercicio:

Mueva la primera letra de cada palabra al final de la misma, luego agregue "ay" al final de la palabra. Deje los signos de puntuación intactos.

pigIt('Pig latin is cool'); // igPay atinlay siay oolcay

pigIt('Hello world !');     // elloHay orldway !

## Solucion
```js 
function pigIt(str) {
  // definimos los signos que no queremos alterar 
  let signos = ['!', '¡', '?', '¿', '.', ',', ':', ';'];
  str = str.split(' ');
  //separamos el string por espacios 
  for (let i = 0; i < str.length; i++) {
    // recorremos nuesta cadena  omitiendo la primera letra de la mismas 
    if (signos.indexOf(str[i]) >= 0) continue;
    str[i] = str[i].slice(1) + str[i].slice(0, 1) + 'ay';
  }
  return str.join(' ');
}

```
## Contador de  duplicados 
Cuente el número de duplicados

Escriba una función que devuelva el recuento de caracteres alfabéticos y dígitos numéricos distintos que no distinguen entre mayúsculas y minúsculas que aparecen más de una vez en la cadena de entrada. Se puede suponer que la cadena de entrada contiene solo letras (tanto mayúsculas como minúsculas) y dígitos numéricos.

```js

function duplicateCount(text) {
  // convertimos todos los carracteres a minuscula,separamaos y ordenamos 
  let textArray = text.toLowerCase().split('').sort();
  let i = 0,
    result = 0,
    lastIndexOfChar = 0;
  while (textArray.length) {
    lastIndexOfChar = textArray.lastIndexOf(textArray[i]);
    if (lastIndexOfChar !== i) {
      i = lastIndexOfChar;
      result++;
    }
    textArray = textArray.slice(++i);
    i = 0;
  }
  return result;

```