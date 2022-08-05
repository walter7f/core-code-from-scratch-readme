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
```js
function contadorPalabras(arrayOfWords) {
  const wSort = arrayOfWords.sort();
  const result= [];
  let lastWordCheck = '';
  let lastResultPos = -1;
  for(let i = 0; i < wSort.length; i++) {
    if(wSort[i] !== lastWordCheck) {
      result.push([wSort[i], 1]);
      lastResultPos++;
    } else {
      result[lastResultPos][1] = result[lastResultPos][1] + 1;
    }
    lastWordCheck = wSort[i];
  }
  return result;
}
```