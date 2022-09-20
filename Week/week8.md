# <b>Desafio Lunes </b>
## Programacion Orientada a Objetos
---
La programación Orientada a objetos es una manera de programar específica, donde se organiza el código en unidades denominadas clases, de las cuales se crean objetos que se relacionan entre sí para conseguir los objetivos de las aplicaciones.
Podemos entender la programación Orientada a objetos como una forma especial de programar, más cercana a como expresaríamos las cosas en la vida real que otros tipos de programación, que permite diseñar mejor las aplicaciones, llegando a mayores cotas de complejidad, sin que el código se vuelva inmanejable.

---
# <b> Desafio Martes</b>

## Funciones
## Ejercicio guiado de Typescript 

```ts
/* Module 4: Develop typed functions using TypeScript
   Lab Start  */

/*  EXERCISE 1
    TODO: Declare a new function type for the sortDescending and sortAscending functions. */
    type copareFunctionType = (a:number, b:number)=> number;

/*  TODO: Convert the sortDescending and sortAscending functions to arrow 
    functions. */

/*  sortDescending is a comparison function that tells the sort method how to sort 
    numbers in descending order */
let  sortDescending:copareFunctionType=(a, b) => {
if (a > b) {
    return -1;
} else if (b > a) {
    return 1;
} else {
    return 0;
}
}

/*  sortDescending is a comparison function that tells the sort method how to sort 
    numbers in ascending order. */
let  sortAscending:copareFunctionType = (a, b)  =>{
if (a > b) {
    return 1;
} else if (b > a) {
    return -1;
} else {
    return 0;
}
}

/*  The buildArray function builds an array of unique random numbers containing the number 
    of items based on the number passed to it. The sortOrder parameter determines 
    whether to sort the array in ascending or descending order. */

/*  TODO: Update the BuildArray function. */

function buildArray(items:number, sortOrder:'ascending'|'descending'):number[] {
    let randomNumbers = [];
    let nextNumber;
    for (let counter = 0; counter < items; counter++) {
        nextNumber = Math.ceil(Math.random() * (100 - 1));
        if (randomNumbers.indexOf(nextNumber) === -1) {
          randomNumbers.push(nextNumber);
        } else {
          counter--;
        }
    }
    if (sortOrder === 'ascending') {
      return randomNumbers.sort(sortAscending);
    } else {
      return randomNumbers.sort(sortDescending);
    }
}

let myArray1 = buildArray(12, 'ascending');
let myArray2 = buildArray(8, 'descending');

/*  EXERCISE 2
    TODO: Update the LoanCalculator function. */

function loanCalculator (principle:number, interestRate:number, months=12) {
    let interest = interestRate / 1200;   // Calculates the monthly interest rate
    let payment;
    payment = principle * interest / (1 - (Math.pow(1/(1 + interest), months)));
    return payment.toFixed(2);
}
```
---
## Clases Abstractas

Las clases abstractas se pueden definir como clases que no se pueden instanciar, es decir, cuya referencia de objeto no se puede crear y contiene dentro de ella, uno o más métodos abstractos.
Un método abstracto es un método que solo puede declararse pero no tiene implementación. Las clases abstractas deben heredarse y requieren subclases para proporcionar implementaciones para el método declarado en la clase abstracta.

----
## Clases Abstractas vs Interfases 

|Clase Abstracta|Interfaz|
|-|-|
|Una clase abstracta puede proporcionar la implementación de una interfaz. Las variables no son definitivas por defecto. Puede contener variables no finales.  |Una interfaz no puede proporcionar la implementación de una clase abstracta. |

La mayor diferencia entre ambos es el proposit. La clase abstracta se usa cuando se quiere generalizar el comportamiento. y la interfaz cuando se quiere estandarizar el comportamiento. 

Cuando una clase hereda de otra clase (abstracta o no), estás definiendo qué es, pasar de una idea abstracta a una concreción. Además, estás definiendo una relación entre clases pero cuando implementas una interfaz, estás definiendo cómo se comporta. Es algo como definir y cumplir un contrato.
 
---
# <b>Desafio Miercoles </b>

## Ejercicio Deadfish Swim (TypeScript)

 Escriba un analizador simple que analice y ejecute Deadfish.

Deadfish tiene 4 comandos, cada uno de 1 carácter:

1. i= incrementa el valor (inicialmente 0)
2. d= disminuye el valor
3. s= eleva al cuadrado el valor
4. o= genera el valor en la matriz de retorno
Los caracteres no válidos deben ignorarse.

parse("iiisdoso") => [8, 64]

```ts
export function parse(data: string): number[] {
  let n = 0;
  let result: number[] = [];
  data.split('').forEach((index: string) => {
    switch (index) {
      case 'i':
        n++;
        break;
      case 'd':
        n--;
        break;
      case 's':
        n= Math.pow(n, 2);
        break;
      case 'o':
        result.push(n);
        break;
    }
  });
  return result;
}
```
---
## Ejercicio decodificador de duplicados 

El objetivo de este ejercicio es convertir una cadena en una nueva cadena donde cada carácter de la nueva cadena es "("si ese carácter aparece solo una vez en la cadena original, o ")"si ese carácter aparece más de una vez en la cadena original. Ignore las mayúsculas al determinar si un carácter es un duplicado.

Ejemplos
- "din"      =>  "((("
- "recede"   =>  "()()()"
- "Success"  =>  ")())())"
- "(( @"     =>  "))((" 
```ts
 export function duplicateEncode(word: string){ // Success
    // lower case
    word = word.toLowerCase(); // 'success'
    // (string) | (string[]) ***
    const characters: string[] = word.split(''); // ['s','u','c','c','e','s','s']
    // iterar 
    const encoded: string[] = characters.map((character) => {
      character = character.replace(/\(/g, '\\(');
      character = character.replace(/\)/g, '\\)');
      const regex = new RegExp(character, 'g');
      const found = word.match(regex) || [];
      if(found.length === 1) {
        return '(';
      } 
      return ')';  
    }); // [')','(',')',')','(',')',')']
    return encoded.join('');  
  }
  ```
---
## Ejercicio  Odd Int
Dada una matriz de números enteros, encuentre el que aparece un número impar de veces.

Siempre habrá un solo número entero que aparecerá un número impar de veces.
```ts
export function findOdd(xs: number[]): number {
   let inpar= xs.find((x: number, index: number, a: number[]) =>
        a.filter((y: number) => y === x).length % 2 === 1
    ) || -1;
    return inpar;
}
```
---
## Ejercicio Quien esta adentro 

Dadas dos matrices de cadenas a1y a2devolver una matriz ordenada ren orden lexicográfico de las cadenas de las a1cuales son subcadenas de cadenas de a2.

```ts
export function inArray(a1: string[], a2: string[]): string[] {
  
  // 0. Quitar repetidos de a1
  // 1. Recorrer a1
  // 1.1 Mientras recorro a1, filtro los elementos de a1
  // 1.1.1 Filtrar:
  // 1.1.1.1 Se quedan los elementos que son un substring de un string en a2
  // 1.1.2 sort sobre arreglo filtrado
  // 1.1.3 return de arreglo filtrado
  
  return [... new Set(a1)].filter((subStr:string) => {
    let result = a2.find((str:string) => str.includes(subStr));
    return result !== undefined;
  }).sort();
  
}
```
---
# <b>Desafio Jueves </b>
