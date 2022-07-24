# <b><Font color="red">Introduccion Programacion y JavaScript</font> </b>

<center  ><img src="https://www.adictosaltrabajo.com/wp-content/uploads/2018/05/el_remozado_javascript.imagen.jpg"  alt="drawing" width="370"/></center>

# <b> <font color="yellow">Desafio Lunes</font></b>
### <b>Teoria de la programacion 

| Temas      | Descripcion |
| ----------- | ----------- |
| Que es Programacion     | La programación es el proceso de crear un conjunto de instrucciones que le dicen a una computadora como realizar algún tipo de tarea.     |
| Lenguajes de programcion   | Un lenguaje de programación es un lenguaje formal, que le proporciona a una persona, en este caso el programador, la capacidad de escribir una serie de instrucciones o secuencias de órdenes en forma de algoritmos con el fin de controlar el comportamiento físico o lógico de un sistema informático    |

# <b> <font color="yellow">Desafio Martes</font> </b>
## <b><font color="orange"> 1. Interpreted And Compiled Programming Languages</font></b>

|Lenguaje Complilado|Lenguaje Interpretado |
|-                  |-                     |
|<img src="https://edteam-media.s3.amazonaws.com/blogs/original/3a814d55-14c2-4a93-8f91-28bf1af3efa5.jpg" alt="drawing" width="300"/>|<img src="https://edteam-media.s3.amazonaws.com/blogs/original/183459ae-5acd-456d-8c18-ab6f5eb63ffc.jpg" alt="drawing" width="200"/>|
|Los lenguajes compilados se convierten directamente en código de máquina que el procesador puede ejecutar. Tienden a ser más rápidos y eficientes de ejecutar|Un lenguaje interpretado es un lenguaje de programación para el que la mayoría de sus implementaciones ejecuta las instrucciones directamente a instrucciones en lenguaje máquina |

## <b><font color="orange"> 2. ¿Java está compilado o interpretado, o ambos?</font></b>

| <font size="32" color="magenta">Java </font> |
|-  |
|<img src="https://dev.java/assets/images/java-logo-vert-blk.png" alt="drawing" width="300"/>|
|El lenguaje Java es a la vez compilado e interpretado. Con el compilador se convierte el código fuente que reside en archivos cuya extensión es .java, a un conjunto de instrucciones que recibe el nombre de bytecodes que se guardan en un archivo cuya extensión es .class. Estas instrucciones son independientes del tipo de ordenador. El intérprete ejecuta cada una de estas instrucciones en un ordenador específico (Windows, Macintosh, etc). Solamente es necesario, por tanto, compilar una vez el programa, pero se interpreta cada vez que se ejecuta en un ordenador.|

## <b><font color="orange" size="6"> 3. Ejercicio</font></b>
## <b><font color="magenta">Conversión de moneda de pseudocódigo</font></b>
Convertir Dolares a Bitcoins 

bitcoin = $-xxxxx.xx-"


cantidad = Input="inserte cantidad total de dolares "

resultado= cantidad / 1BTC

print resultado 

## <b><font size="6"> 4. Lenguajes de alto y bajo nivel </font><b>
| |<img src="https://edteam-media.s3.amazonaws.com/blogs/original/0cc7e2f7-1821-4603-88d6-7d7f271707a5.png" alt="drawing" width="300"/> | |
|-|-|-|
|Cuando hablamos de un lenguaje de alto nivel nos referimos al tipo de lenguaje de programación que no expresa los algoritmos teniendo en cuenta la capacidad que tienen las máquinas para ejecutar órdenes, sino al que se utiliza teniendo en cuenta las capacidades cognitivas de los seres humanos.|Un lenguaje de programación de bajo nivel, es aquel en el que sus instrucciones ejercen un control directo sobre el hardware y por lo tanto están condicionados por la estructura física de las computadoras que lo soportan, tiene poca abstraccion al lenguaje humano, practicamente es lenguaje maquina. |


# <b> <font color="yellow">Desafio Miercoles </font> </b>
## <b><font color="orange">1. Convertir tu fecha de nacimiento en Binario </font></b>

Fecha 03/12/1998  (Decimal)

- 2^0=1        
- 2^1=2         
- 2^2=4
- 2^3=8
- 2^4=16
- 2^5=32
- 2^6=64
- 2^7=128
- 2^8=256
- 2^9=512
- 2^10=1024
- 2^11=2048

|3= 2+1  =  11|
|-|
|12=8+4 = 1100|
|(1998-1024 = 974) -- (974-512=462) -- (462-256=206) -- (206-128=78) -- (78-64=14 )-- (14-8=6) -- (6-4=2) -- (2-2 = 0) ="11111001110"|
|Fecha 11 / 1100 / 11111001110 (Binario)|


