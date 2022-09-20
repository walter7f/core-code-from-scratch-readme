# <b>Desafio Lunes </b>
## <b> Programacion orientada a objetos 
## Los cuatro pilares de POO</b>

La POO permite modelar entidades para despues trabajar con ellas.

1. Pilar 1: Encapsulación

El concepto de encapsulación es el más evidente de todos. Pero, precisamente por su sencillez, a veces pasa inadvertido.

La encapsulación es la característica de un lenguaje POO que permite que todo lo referente a un objeto quede aislado dentro de éste. Es decir, que todos los datos referentes a un objeto queden "encerrados" dentro de éste y sólo se puede acceder a ellos a través de los miembros que la clase proporcione (propiedades y métodos).

2. Pilar 2: Abstracción

Como la propia palabra indica, el principio de abstracción lo que implica es que la clase debe representar las características de la entidad hacia el mundo exterior, pero ocultando la complejidad que llevan aparejada. O sea, nos abstrae de la complejidad que haya dentro dándonos una serie de atributos y comportamientos (propiedades y funciones) que podemos usar sin preocuparnos de qué pasa por dentro cuando lo hagamos.

Así, una clase (y por lo tanto todos los objetos que se crean a partir de ella) debe exponer para su uso solo lo que sea necesario. Cómo se haga "por dentro" es irrelevante para los programas que hagan uso de los objetos de esa clase.

3. Pilar 3: Herencia

Desde el punto de vista de la genética, cuando una persona obtiene de sus padres ciertos rasgos (el color de los ojos o de la piel, una enfermedad genética, etc...) se dice que los hereda. Del mismo modo en POO cuando una clase hereda de otra obtiene todos los rasgos que tuviese la primera.

Dado que una clase es un patrón que define cómo es y cómo se comporta una cierta entidad, una clase que hereda de otra obtiene todos los rasgos de la primera y añade otros nuevos y además también puede modificar algunos de los que ha heredado.

A la clase de la que se hereda se le llama clase base, y a la clase que hereda de ésta se le llama clase derivada.

4. Pilar 4: Polimorfismo

En POO, el concepto de polimorfismo se refiere al hecho de que varios objetos de diferentes clases, pero con una base común, se pueden usar de manera indistinta, sin tener que saber de qué clase exacta son para poder hacerlo.

El polimorfismo nos permite utilizar a los objetos de manera genérica, aunque internamente se comporten según su variedad específica.

#
## <b> Programacion orientada a objetos 
##  Glosario</b>
1. Abstracción

La abstraccion es la partde de la POO donde solo se muestra al usuario el contenido esencial del programa, por ejemplos botones y un area de texto. Todo el contenido complejo, no se muestra.

2. Herencia

Las clases hijo, heredan los atributos y caracteristicas de la clase padre y pueden hacer uso de ellas. 

3. Polimorfismo

El Polimorfismo hacer referencia que tanto la clase padre y la clase hijo, pueden funcionar con sus propias caracteristicas y metodos, cada clase se puede manejar de forma distinta.

4. Encapsulación

Permite que todo lo referente a un objeto quede aislado dentro de éste. Es decir, que todos los datos referentes a un objeto queden "encerrados" dentro de éste y sólo se puede acceder a ellos a través de los miembros que la clase proporcione.

5. Clase
Una clase es una plantilla. Define de manera genérica cómo van a ser los objetos de determinado tipo, definen sus atributos y acciones.

6. Objeto

 Un objeto es ya una entidad concreta que se crea a partir de la plantilla que es la clase. Este nuevo objeto tiene ya "existencia" real, puesto que ocupa memoria y se puede utilizar en el programa.

7. Instancia

Crea un objeto apartir de una Clase. Instanciar una clase consiste en crear un nuevo objeto concreto de la misma.

8. Interfaz

Las Interfaces son usadas para indicar qué métodos debe obligatoriamente implementar (contener) una Clase (aunque no tienen por qué comportarse del mismo modo).

9. Modificadores de acceso

Los modificadores de acceso nos permiten cambiar la "visibilidad" y los "privilegios de acceso" de un miembro de la clase (o módulo).

- Private : solo se puede acceder desde la clase o módulo que fue declarado

- Public : no tiene restricciones de acceso e incluso se puede acceder desde fuera de la clase

- Protected : solo pueden ser aceder a el los hijos de la aclase padre. 

10. Constructores

Un constructor es una subrutina cuya misión es inicializar un objeto de una clase. En el constructor se asignan los valores iniciales del nuevo objeto.

##  <b>Example </b>
Funcionamiento de:
 - [clases](https://www.tutorialesprogramacionya.com/angularya/detalleconcepto.php?punto=23&codigo=23&inicio=20)
 - [objetos](https://apuntes.de/typescript/object-types/#gsc.tab=0)
 - [encapsulación](https://blog.jetbrains.com/webstorm/2019/03/write-object-oriented-typescript-encapsulation/)
 - [modificadores de acceso](https://programmerclick.com/article/53241462366/)
 - [instancias](https://gustavodohara.com/blogangular/clases-en-typescript/)
 - [interfaces](https://www.tutorialsteacher.com/typescript/typescript-interface)

#
# <b>Desafio Martes </b>

--- estudio 

---------

# <b>Desafio Miercoles </b>
## Ejercicio Build Tower
```ts
export const towerBuilder = (nFloors: number): string[] => {
    if (nFloors === 1) return ['*'];
    const torre: string[] = [];
    for (let i = 1; i <= nFloors; i++) {
      torre.push(
        `${' '.repeat(nFloors - i)}${'*'.repeat(2 * i - 1)}${' '.repeat(
          nFloors - i)}`
      );
    }
  
    return torre;
  }
  ```

  ---
  ## Ejercicio  Meeting 
  ```ts

  export function meeting(s: string): string {
    let order=s.toUpperCase().split(';')
      .sort((a: string, b: string) => {
        const [aNombre, aApellido] = a.split(':');
        const [bNombre, bApellido] = b.split(':');
        if (aApellido === bApellido) {
          return aNombre > bNombre ? 1 : bNombre > aNombre ? -1 : 0;
        }
        return aApellido > bApellido ? 1 : bApellido > aApellido ? -1 : 0;
      })
      .map((NombreCompleto: string) => {
        const [Nombre, Apellido] = NombreCompleto.split(':');
        return `(${Apellido}, ${Nombre})`;
      })
      .join('');
    return order;
  }
```
---
# <b>Desafio Jueves  </b>
##  Interfaces 
---
Ejercicio TypeScript Guiado 

```ts
/* Module 3: Implement interfaces in TypeScript
   Lab Start  */

/*  EXERCISE 1
    TODO: Declare the Loan interface. */
    interface Loan{
        principal:number,
        interestRate:number
    }


/*  TODO: Declare the ConventionalLoan interface. */
interface ConventionalLoan extends Loan{
    months: number
}



/*  TODO: Update the calculateInterestOnlyLoanPayment function. */

function calculateInterestOnlyLoanPayment(loanTerms:Loan):string {
    // Calculates the monthly payment of an interest only loan
    let interest = loanTerms.interestRate / 1200; // Calculates the Monthly Interest Rate of the loan
    let payment;
    payment = loanTerms.principal * interest;
    return 'The interest only loan payment is ' + payment.toFixed(2);
}

/*  TODO: Update the calculateConventionalLoanPayment function. */

function calculateConventionalLoanPayment(loanTerms:ConventionalLoan):string {
    // Calculates the monthly payment of a conventional loan
    let interest =loanTerms.interestRate / 1200; // Calculates the Monthly Interest Rate of the loan
    let payment;
    payment = loanTerms.principal * interest / (1 - (Math.pow(1 / (1 + interest),loanTerms.months)));
    return 'The conventional loan payment is ' + payment.toFixed(2);
}

let interestOnlyPayment = calculateInterestOnlyLoanPayment({principal: 30000,interestRate: 5});
let conventionalPayment = calculateConventionalLoanPayment({principal: 30000,interestRate: 5,months: 180});

console.log(interestOnlyPayment);     //* Returns "The interest only loan payment is 125.00" 
console.log(conventionalPayment);     //* Returns "The conventional loan payment is 237.24" 

```