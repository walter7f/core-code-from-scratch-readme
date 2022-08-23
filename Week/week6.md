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
