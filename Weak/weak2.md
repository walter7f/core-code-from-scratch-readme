# <b>Desafio Lunes </b>
## <b>Funcion  if , if else </b>

IF es una estructura de control utilizada para tomar decisiones. Es un condicional que sirve para realizar unas u otras operaciones en función de una expresión. Funciona de la siguiente manera, primero se evalúa una expresión, si da resultado positivo se realizan las acciones relacionadas con el caso positivo, de caso contrario se opera la siguiente condicion de falso.

<img src="https://miro.medium.com/max/906/1*WFDgMcVTqQ4JmZQdsbs7lQ.png" alt="drawing" width="370"/>

## <b>Ciclo   for  </b>
El bucle FOR se utiliza para repetir una o más instrucciones un determinado número de veces. De entre todos los bucles, el FOR se suele utilizar cuando sabemos seguro el número de veces que queremos que se ejecute. La sintaxis del bucle for se muestra a continuación.
El bucle FOR tiene tres partes incluidas entre los paréntesis, que nos sirven para definir cómo deseamos que se realicen las repeticiones. La primera parte es la inicialización, que se ejecuta solamente al comenzar la primera iteración del bucle. En esta parte se suele colocar la variable que utilizaremos para llevar la cuenta de las veces que se ejecuta el bucle.

La segunda parte es la condición, que se evaluará cada vez que comience una iteración del bucle. Contiene una expresión para decidir cuándo se ha de detener el bucle, o mejor dicho, la condición que se debe cumplir para que continúe la ejecución del bucle.

Por último tenemos la actualización, que sirve para indicar los cambios que queramos ejecutar en las variables cada vez que termina la iteración del bucle, antes de comprobar si se debe seguir ejecutando.

Después del for se colocan las sentencias que queremos que se ejecuten en cada iteración, acotadas entre llaves.

<img src="http://estilow3b.com/wp-content/uploads/2021/05/10-JavaScript-Bucles-Declaracion-continue.png"  alt="drawing" width="320"/> 

## <b>Ciclo  While   </b>
El bucle while es muy similar al bucle for. While es la palabra inglesa para ‘mientras’ y cuando la incluimos en nuestro código la podríamos traducir al castellano por: “mientras se cumpla una condición, ejecuta las siguientes instrucciones". 

<img src="https://www.aulafacil.com/uploads/cursos/451/editor/15-1.png" alt="drawing" width="370"/>

## <b>  Funciones  </b>

Una función en JavaScript es similar a un procedimiento — un conjunto de instrucciones que realiza una tarea o calcula un valor, pero para que un procedimiento califique como función, debe tomar alguna entrada y devolver una salida donde hay alguna relación obvia entre la entrada y la salida.

<img src="https://miro.medium.com/max/1400/1*Pf-f06mfFnteJeSk9a5cqA.png" alt="drawing" width="400"/>

<br>

# <b> Desafio Martes<b>
## Ejercicio de Multiplicacion

Ejercicio:

Resuelve la multiplicacion

```js
function multiply(a, b){
  a * b
}
```
Solucion

```js
function multiply(a, b){
  let multiplicacion= a * b;
  return multiplicacion;
}
```

## Ejercicio ASCII Total 
Ejercicio:

Se le dará una cadena y tendrá que devolver la suma de todos los caracteres como un int. La función debería poder manejar todos los caracteres ASCII.
```js
function uniTotal (string) {
// total up dem unicodes!
}
```
Solucion
```js
function uniTotal (string) {
  let sumaCaracter=0;  // Contador iniciado a 0
  // iniciamos un for 
  // con la variable cadena contamos los string 
  for( let i = 0, cadena= string.length; i < cadena; i++ ){
    // i cuenta cada letra del string hasta que sea menor que la cadena 
    // recordar que contamos desde 0 cada posicion (i= i-1)
    sumaCaracter += string[i].charCodeAt(); // en lista donde i guarda los valores del caracter 
    // char code  convierte todos los valores en codigo asii
  }
  return sumaCaracter;
  // retorna la suma de los caractes 
}
```

# <b>Desafio Miercoles</b>
## Char From ASCII Value

Ejercicio:

Escriba una función get_char()/ getChar()que tome un número y devuelva el carácter ASCII correspondiente a ese valor.
```js
function getChar(c){
  // ...
}
```
```js
function getChar(c){
  // solo tomamos el valor de la variable la y la retornamos  con String.fromCharcode()
  return String.fromCharCode(c)
}
```
## Adicion en binario 

Ejercicio

Debe de presentar la suma de dos numeros decimales y presetar la suma en decimal y binario 

```js
function addBinary(a,b) {
  //return retorna la suna de a+b 
  return (a + b).toString(2);
  //  (a + b).toString(2) retorna la convercion en binario de la suma  

}
```

## Calificación final del estudiante

Ejercicio 
Cree una función notaFinal, que calcule la nota final de un estudiante en función de dos parámetros: una nota para el examen y una cantidad de proyectos completados.

Esta función debe tomar dos argumentos: examen - calificación del examen (de 0 a 100); proyectos - número de proyectos completados (de 0 en adelante);

Esta función debería devolver un número (calificación final). Hay cuatro tipos de calificaciones finales:

```js
function finalGrade (exam, projects) {
  let resultado = 0;
  if (exam > 90 || projects > 10) {
    resultado  = 100;
  } else if (exam > 75 && projects >= 5) {
    resultado  = 90;
  } else if (exam > 50 && projects >= 2) {
    resultado  = 75;
  } else {
    resultado =0;
  }
  return resultado ;
}

```



# <b>Desafio Jueves </b>
## <b>Eliminar todos los signos de exclamación del final de la oración</b>

Ejercicio 

Elimina todos los signos de exclamación del final de la oración.

Ejemplos
remove("Hi!") === "Hi"
remove("Hi!!!") === "Hi"

Solucion

```js

function remove (string) {  
  
  let cadena= "";
  // declaraamos cadena como variable vacia 
  let posicion= string.length - 1;
  // contamos las posciciones de string menos 1 por que iniciamos desde 0
  for (i=posicion; i>0; i--){
    //rrecoremos desde la posicon final hasta 0
    if (string[i] !== "!"){
      // condicionamos que en la lista de i los strings sean diferentes de "!"
      cadena = string.substring(0, i +1);
      // substring debuelve la cadena desde 0 hasta la posicion -1 por eso le colocamaos +1
      //para que lea correctamente el recorrido 
    break;
      // rompe el ciclp una vez compretado el ciclo 
    
  }
}
return cadena;
}

```

## Eliminacion de Vocales 

<br>
Ejercicio

Cree una función llamada shortcutpara eliminar las vocales minúsculasa ( , e, i, o, u) en una cadena determinada.

Solucion 


```js

function shortcut (string) {
  // declaramos una cadena vacia 
  let texto = "";
  for (i=0; i< string.length; i++){
    //recorremos el string 
    if ( string[i]== "a" || string [i]=="e" || string[i]=="i" ||string [i]=="o" || string[i]=="u"){
      //con las condicones finalizamos las vocales y dejamos continuar 
      continue;
    }
    texto= texto+ string[i];
    // contactemanos la cadeana vaica pas el resultado de las listas
    }
    return texto;
}
```

<br>

## ¡Piedra Papel tijeras!

Ejercicio

Piedra Papel tijeras

¡Vamos a jugar! ¡Tienes que devolver qué jugador ganó! En caso de empate devolución Draw!.

Solucion 

```js 
const rps = (p1, p2) => {
  if (p1===p2)
    return "Draw!";
  
  if (p1 === "rock" && p2 === "scissors")
    return "Player 1 won!";
  
  if (p1 === "scissors" && p2 ==="paper")
    return"Player 1 won!";
  
  if (p1 === "paper" && p2 === "rock")
    return "Player 1 won!";
  
    else 
    return "Player 2 won!";
  
};
```

## Ejercicio de Bugger persistente
