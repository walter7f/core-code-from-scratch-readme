# <b>Week Challenges "Tuesday"</b>
## <b>Ejercicios de Aprendizaje</b>
---
## Comprencion basica de Node.Js

|Preguntas|Descripcción|
|-|-|
|1. ¿Qué es Node.JS?|Node.js es un entorno de tiempo de ejecución de JavaScript quiere decir que incluye todo lo que necesita para ejecutar un programa escrito en JavaScript. Paso de solo ejecutarse en el navegador a ser ejecutardo como aplicacion independiente. Node.Js esta basado en el motor de JavaScript V8 de Chrome .|
|2. ¿Qué problema resuelve Node.JS?|Nos permite ejecutar en el servidor, de manera asíncrona, con una arquitectura orientada a eventos cambiando la manera de realizar las conexiones con el servidor. En vez de generar un nuevo hilo E/S para cada cliente, cada conexión dispara la ejecución de un evento dentro del proceso del motor de Node. De este modo, Node permite que un solo servidor que lo ejecute pueda soportar decenas de miles de conexiones.|
|3. ¿Qué es el motor Javascript V8?|Chrome V8 es un motor de JavaScript, lo que significa que ejecuta código JavaScript. Originalmente, se escribió JavaScript para ser ejecutado por los navegadores web. Chrome V8, puede ejecutar código JavaScript tanto dentro como fuera de un navegador| 
|4. ¿Es realmente necesario Node.JS en el ecosistema de Desarrollo?|Las funciones sin servidor necesitan una forma de ejecutarse cuando se activan. Varios proveedores de informática sin servidor ofrecen Node.js como tiempo de ejecución para funciones sin servidor de JavaScript. Pero otros lenguajes utilizan otros tiempos de ejecucion|
|5. ¿Cuál es la diferencia entre Node.JS y cualquier otro navegador?|En el navegador, la mayor parte del tiempo lo que está haciendo es interactuar con elDOM, u otroAPI de plataforma web. Y Node.JS es un entorno de tiempo de ejecución de JavaScript en Node.js controlas el entorno|
|6. ¿Qué es NVM y por qué es útil para los desarrolladores de Node.JS?| Node Version Manager es un script bash utilizado para administrar múltiples versiones lanzadas de Node. js. Permite realizar operaciones como instalar, desinstalar, cambiar de versión. El software nvm permite instalar y gestionar distintas versiones de NodeJS en un ordenador, lo que facilita el trabajo con proyectos que requieren versiones distintas,|

[Colegas de trabajo](https://github.com/edyrrg)

---

## Sistema de módulos Node.JS

|Preguntas|Descripcción|
|-|-|
|1. ¿Qué es un módulo Javascript?|Un módulo es solo un archivo. Un script es un módulo. Tan simple como eso. Los módulos pueden cargarse entre sí y usar directivas especiales export e import para intercambiar funcionalidades, llamar a funciones de un módulo desde otro:|
|2. ¿Por qué son necesarios los módulos de Javascript?|Sirve para intercambier funcionalidades y para reutilizar el codigo al usar los módulos de JS puedes evitar errores al incluir archivos en un orden diferente y además el código de ve más ordenado.|
|3. ¿Qué estándares de módulos están disponibles en Node.JS?| CommonJS (CJS), sistema por defecto de Node.js y ECMAScript Modules o (ESM), sistema oficial de JavaScript para la gestion de módulos|
|4. ¿Cuáles son las diferencias entre los módulos ESModules y CommonJS?|CommonJS sólo permite cargar módulos de forma síncrona, mientras que ESM permite carga síncrona y asíncrona. NodeJS permite hacer require() de bare imports utilizando npm mientras que ESM puede hacerlo mediante import maps, un fichero .json que incluye la URL de referencias a los nombres de los paquetes|
|5. ¿Qué tipos de módulos existen en Node.JS?|Node.js incluye tres tipos de módulos (Módulos centrales, Módulos locales, Módulos de terceros)|



[Colegas de trabajo](https://github.com/edyrrg)

[Video de Referncia](https://www.youtube.com/watch?v=29iYdru2KUg)


----

## Sistema de módulos Node.JS - Práctica

Descripcion 

1. Cree un nuevo proyecto Node.JS, asígnele el nombre modules.
2. Cree un nuevo módulo, asígnele el nombre:operations.js
En el interior operations.js implemente dos funciones, una para la operación de suma y otra para la operación de resta.
3. Cree un nuevo módulo, asígnele el nombre:main.js
Importe las funciones implementadas en operations.js y utilícelas de cualquier forma en main.js.

## [Solucion :)](https://github.com/walter7f/core-code-from-scratch-readme/tree/main/cod/EjercicioNode1)

----
## Modelo de cliente-servidor 
Descripcion 

La arquitectura cliente-servidor es un modelo de diseño de software. Acá, las tareas se reparten entre los proveedores de recursos o servicios, llamados servidores, y los demandantes, llamados clientes.
<img src="https://miro.medium.com/max/640/0*NcDESRONCPqRBSaW">

|Pregunta|Descripción |
|-|-|
|1. ¿Qué es un servidor?|Un servidor es una aplicación que recibe los datos utilizando los mismos protocolos que se usaron para enviarlos.|
|2. ¿Qué es un Cliente?|Cualquier dispositivo que puede recibir servicios|
|3. ¿Un servidor es solo otra computadora física?|Aun que si pueden operar como servidores, es preferible que sean computadoras de proposito espesifico que funcionen como servidor.|
|° ¿Por qué nos referimos a cierta clase de aplicaciones como Servidores?|Colabora con el servidor web para ofrecer una respuesta dinámica y personalizada a una solicitud de cliente.|
|° ¿Cuál es la diferencia?|Una de ellas solo emiten solicitudes y la otra almacena y manda una respuesta a esa solicitud.|
|4. ¿Existe alguna similitud entre la comunicación humana y el modelo cliente-servidor?|Si, es como el servicio al cliente, pides informacion y recibes una respuesta ya sea que exista o no lo que pidas.|
|5. ¿El modelo cliente-servidor es aplicable sólo a la Web?|No, se aplica a otros modelos |
| °¿Puedes mencionar algún otro ejemplo de este modelo fuera de la Web?|Telecomunicaciones |

---
# <b>Week Challenges "Wendnesday"</b>

## <b>Ejercicios de Apredendizaje</b>

----

## Comprensión básica de las API
|||
|-|-|
|1. ¿Qué es una API?|Es una interfaz de programacion que permite la comunicacion de entra las aplicaciones y bases de datos para ofrecer una respuesta a un servicio solicitado.|
|2. ¿Qué es un Protocolo?|Un protocolo son una serie de pasos o proceso que se siguen para determinada tarea|
|3. ¿El término API solo es aplicable a la comunicación de programas a través de Internet?|No, de hecho se utiliza en casi todos los aspectos de la vida diaria, hacemos uso de ella sin darnos cuenta.|
|4. ¿Por qué es importante la comunicación estructurada entre dos programas?|Para tener una perfecta organizacion de la informacion y tambien para tener una mayor seguriad en el momento de navegar en la web. |
|° ¿Los humanos usamos API cuando nos comunicamos sin tecnología?|Si, cuando hacemos alguna solicitud de algun servicio, interactuamos con un mediador que nos proporciona informacion referente a lo que solicitamos.|
|5. ¿Es una API solo otro programa o un estándar?||
|6. ¿Conoces alguna API? ¿Puede enumerar al menos 5 ejemplos de API?||