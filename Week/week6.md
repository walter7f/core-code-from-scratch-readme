# Desafio Lunes 

## <b> Declarar tipos de variables en TypeScrit </b>

En, TypeScript se utiliza la sintaxis variableName: type. Esta declaración let myVariable: numberdeclara la variable como un tipo de número sin inicializarla. Alternativamente, también puede inicializar la variable usando let myVariable: number = 10.

Para implicar el tipo de variable a través de la inferencia de tipo, simplemente use el mismo formato que usa en JavaScript. Por ejemplo, let myVariable = 10 infiere que la variable es de tipo numberporque se inicializa con el valor 10.

```ts
let x: number;   //* Explicitly declares x as a number type
let y = 1;       //* Implicitly declares y as a number type
let z;           //* Declares z without initializing it
```
La entrada  z = "one"_ Como era de esperar, esto genera el error El tipo 'String' no se puede asignar al tipo 'número' porque la verificación de tipo estático no permite que  string se asigne a la variable.



## <b> Tipos primitivos en TypeScript</b>


<b> Tipo booleano </b>

El tipo de dato más básico es el valor true o false, conocido como booleano.

Por ejemplo:
```ts
let flag: boolean;
let yes = true;
let no = false;
```
<b> Tipos numéricos y BigInteger </b>

Son valores de punto flotante o BigIntegers. Estos números obtienen el tipo number, mientras que BigIntegers obtienen el tipo bigint.

```TypeScript
let x: number;
let y = 0;
let z: number = 123.456;
let big: bigint = 100n;
```
<b> Tipo String </b>

Representa secuencias de caracteres almacenados como unidades de código Unicode UTF-16. Al igual que JavaScript, TypeScript también usa comillas dobles ( ") o comillas simples ( ') para rodear datos de cadena.
```TypeScript
let s: string;
let empty = "";
let abc = 'abc';
```
```Ts
let firstName: string = "Mateo";
let sentence: string = `My name is ${firstName}.
    I am new to TypeScript.`;
console.log(sentence);
// en consola devuelve ==
//My name is Mateo.
//    I am new to TypeScript.

```
###  <b> Los tipos void, null e indefinido </b>

JavaScript y TypeScript tienen dos valores primitivos que se usan para señalar un valor ausente o no inicializado: nully undefined.

### <b>Crear una enumeracion </b>
```ts
enum ContractStatus {
     Permanent,
     Temp,
     Apprentice
}
let employeeStatus: ContractStatus = ContractStatus.Temp;
console.log(employeeStatus);
// [Console]= 1       recorre las posiciones de las enumeraciones 


```
## Ejercicio 2
```ts
export type User ={name:string, age:number, occupation:string} ;

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user:User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);

```
## Ejercicio 3
```ts
interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}

persons.forEach(logPerson);
```

# Desafio Martes 
## Ejercicio 1
Suma de cuadrados

``` ts 
export function squareSum(numbers: number[]): number {
  let resultado:number;
  let initialValue=0;// valor de inicial o valor previo
  resultado = numbers.reduce(
    // valor previo 0 + valor actual al cuadrado 
    (previousValue, currentValue) => previousValue+ currentValue*currentValue,
    initialValue
  );


  
    return resultado;
}
```
## Ejercicio 2
Un lobo con piel de cordero 

```ts
export function warnTheSheep(queue: string[]): string | number {
    let ver;
    let contar = queue.length;
    //let alerta ;
    let posicion;
    ver= queue.indexOf("wolf")+1;
    posicion= contar-ver;
    if (ver == contar){
        return"Pls go away and stop eating my sheep" 
    }else{
        return "Oi! Sheep number "+ posicion+"!" +" You are about to be eaten by a wolf!"
    }
   
  }
```
#
# <b>Desafio Miercoles </b>
## Una regla de divisibilidad por 13
const rem = [1, 10, 9, 12, 3, 4];

```js
export function process(n: number): number {
  let reversedNumber: string[] = n.toString().split('').reverse();
  let index = 0;
  let result = reversedNumber.reduce((total: number, digit: string) => {
    if (index > 5) index = 0;
    return total + Number(digit) * rem[index++];
  }, 0);
  if (result === n) return result;
  return process(result);
}

export function thirt(n: number): number {
  return process(n);
}
```
## Jugando con Dígitos 
```js
xport class G964 {
  public static digPow = (n: number, p: number) => {
    let especialN = n.toString().split('').map(Number).reduce((prev: number, curr: number) => prev + Math.pow(curr, p++), 0);
    if (especialN % n === 0) return especialN / n;
    return -1;
  };
}

```
