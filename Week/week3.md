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

## Decodificador de Codigo Morse 
Ejercicio

```js
decodeMorse = function (morseCode) {
  morseCode = morseCode.replace(/   /g, '#');
  let decodedCode = '';
  let tempWordToDecode = '';
  for (let i = 0, lenght = morseCode.length; i < lenght; i++) {
    if (morseCode[i] === ' ') {
      decodedCode += MORSE_CODE[tempWordToDecode] || '';
      tempWordToDecode = '';
    } else if (morseCode[i] === '#') {
      decodedCode += `${MORSE_CODE[tempWordToDecode] || ''} `;
      tempWordToDecode = '';
    } else {
      tempWordToDecode += morseCode[i];
    }
  }
  decodedCode += MORSE_CODE[tempWordToDecode] || '';
  return decodedCode.trim();
};
```

## Parentesis Validos 
Ejercicio 

Escribe una función que tome una cadena de paréntesis y determine si el orden de los paréntesis es válido. La función debería regresar truesi la cadena es válida y falsesi no es válida.

## Solucion
```js
function validParentheses(parens) {
  let resp = 0;
  for (let i = 0; i < parens.length; i++) {
    if (parens[i] === ')') 
      resp--;
    if (parens[i] === '(') 
      resp++;
    if (resp < 0) 
      return false;
  }
  return resp== 0;
}
```
## Convertir cadena a caja de camello
Ejercicio

Complete el método/función para que convierta las palabras delimitadas por guiones/guiones bajos en mayúsculas y minúsculas. La primera palabra dentro de la salida debe estar en mayúsculas solo si la palabra original estaba en mayúsculas (conocido como Upper Camel Case, también conocido como caso Pascal).
## Solucion 

```js
function toCamelCase(str) {
  let resultado= '';
  for (let i = 0; i < str.length; i++) {
    if (i != 0 && (str[i-1] === '-' || str[i-1] === '_') ){
        
        //continue;
        resultado += str[i].toUpperCase();
    } else if (str[i] != '-' && str[i] != '_'){
      resultado += str[i];
    }
  }
  return resultado;
}
```
## Único en orden

Ejercicio

mplemente la función unique_in_order que toma como argumento una secuencia y devuelve una lista de elementos sin ningún elemento con el mismo valor uno al lado del otro y conservando el orden original de los elementos.

Por ejemplo:

uniqueInOrder('AAAABBBCCDAABBB') == ['A', 'B', 'C', 'D', 'A', 'B']
uniqueInOrder('ABBCcAD')         == ['A', 'B', 'C', 'c', 'A', 'D']
uniqueInOrder([1,2,2,3,3])       == [1,2,3]

## Solucion 
```js
var uniqueInOrder=function(iterable){
  let array=[];
  let indice ='';
  for (let i=0; i<iterable.length; i++){
    if(iterable[i] !== indice){
      indice = iterable[i];
      array.push(indice);
    }
  }
  return array;
}
```

# Desafio Jueves


## Doblar una Matriz


Ejercicio

En este kata, debe escribir un método que doble una matriz determinada de números enteros por el medio x veces.

```js
function foldArray(array, runs) {
  if (array.length === 1) return array;
  let output = [...array];
  let aheadPosition = 0;
  while (runs) {
    if (output.length === 1) return output;
    output = Array.from(
      { length: Math.round(output.length / 2) },
      (v) => 0
    ).map((v, i) => {
      aheadPosition = output.length - (i + 1);
      if (aheadPosition === i) return output[i];
      return output[i] + output[aheadPosition];
    });
    runs--;
  }
  return output;
}


```
##  ¡Cifra Esto¡

Ejercicio

¡Cifra esto!

¡Quieres crear mensajes secretos que puedan ser descifrados por Descifrar esto! kata. Aquí están las condiciones:

Su mensaje es una cadena que contiene palabras separadas por espacios.
Debe encriptar cada palabra en el mensaje usando las siguientes reglas:
La primera letra debe convertirse a su código ASCII.
La segunda letra debe ser intercambiada con la última letra
Manteniéndolo simple: no hay caracteres especiales en la entrada.

## Solucion
```js
function encryptedWord(word) {
  if (word.length == 1) return word.charCodeAt();
  if (word.length == 2) return `${word.charCodeAt(0)}${word[1]}`;
  return `${word.charCodeAt(0)}${word[word.length - 1]}${word.slice(
    2,
    word.length - 1
  )}${word[1]}`;
}

var encryptThis = function (text) {
  return text.split(' ').map(encryptedWord).join(' ');
}

```

## Desafio Principal 


1. ¿Quién eres?

2. ¿Qué antecedentes tienes?

3. ¿Quién quieres ser?

4. ¿Qué quieres hacer?

5. ¿Cuáles son los valores y principios fundamentales que rigen su carácter y contribuciones?

Soy Walter Diaz, me desarrolle en C++ de forma basica, quiero convetirme en uno de los mejores progamadores y desarroladores, no solo en programamacion si no tambien en la sistemas tecnologicos como robotica, me gusta trabajar en Amanzon y NASA. Soy alguien muy decidido y curioso con ganas de aprender para poder lograr mis objetivos.

1. Who are you?
2. What background do you have?
3. Who do you want to be?
4. What do you want to do?
5. What are the core values and principles that govern your character and contributions?

I am Walter Diaz, I developed in C++ in a basic way, I want to become one of the best programmers and developers, not only in programming but also in technological systems such as robotics, I like to work at Amazon and NASA. I am someone very determined and curious with a desire to learn in order to achieve my goals.

