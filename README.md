# JS desde cero en el navegador... antes que REACT.

El objetivo de esta práctica es crear un formulario básico en HTML y JavaScript que permita saludar a un usuario. Publicarlo en un repositorio de GitHub con GitHub Pages. Todo debes documentarlo con un pantallazo en este mismo archivo y personalizarlo con tu tus datos personales.

## Por qué REACT

- REACT es una biblioteca de JavaScript para construir interfaces de usuario.
- Es mantenida por Meta y una comunidad de desarrolladores.
- Permite construir componentes reutilizables.
- Es ampliamente utilizada en la industria, lo que la hace relevante para desarrolladores web.
- Aprender REACT abre oportunidades laborales y mejora las habilidades en desarrollo frontend.
- Cuenta con un ecosistema robusto, incluyendo herramientas como Redux para la gestión del estado y React Router para la navegación.
- Tiene un rendimiento optimizado gracias a su uso del Virtual DOM.
- Se sitúa como uno de los frameworks más populares en la actualidad. [State of JS 2023](https://2023.stateofjs.com/en-US/libraries/front-end-frameworks/)

## Por qué JavaScript antes de REACT
- REACT está construido sobre JavaScript, por lo que es esencial tener una buena comprensión de este lenguaje antes de aprender REACT.
- JavaScript es el lenguaje de programación principal para el desarrollo web frontend.

# ¿Qué es JavaScript?

JavaScript (JS) es un lenguaje de programación interpretado, ligero y multiplataforma, creado inicialmente para dotar de interactividad a las páginas web. Hoy en día, se utiliza tanto en el desarrollo frontend (navegadores) como en el backend (servidores, gracias a Node.js), aplicaciones móviles, de escritorio y más.

## Versiones
- **ECMAScript** es el estándar que define el lenguaje. Las versiones más importantes son:
  - **ES5 (2009):** Amplió la compatibilidad y funcionalidades.
  - **ES6/ES2015:** Introdujo let/const, arrow functions, clases, módulos, promesas, etc.
  - Desde 2015, cada año se publica una nueva versión con mejoras y nuevas características.

## Potencia
- Permite crear desde páginas web dinámicas hasta aplicaciones complejas, videojuegos, servidores, inteligencia artificial y más.
- Es asíncrono, flexible y tiene una enorme cantidad de librerías y frameworks (React, Angular, Vue, etc.).
- Es esencial para el desarrollo web y uno de los lenguajes más demandados en el mercado laboral.

---
## Parte 1: Instalación y configuración

1. **Instala Visual Studio Code**  
   Descarga e instala VS Code desde [code.visualstudio.com](https://code.visualstudio.com/).

## Parte 2: Primeros pasos con la consola del navegador

1. Abre tu navegador web (Chrome, Firefox, Edge, etc.).
2. Accede a cualquier página web y pulsa `F12` o `Ctrl+Shift+I` para abrir las herramientas de desarrollo.
3. Haz clic en la pestaña "Consola".
4. Prueba los siguientes comandos uno por uno y observa el resultado:
   ```js
   2 + 2
   console.log("¡Hola, mundo!")
   let nombre = "Anita"
   nombre
   ```

## Parte 3: Tu primer archivo HTML + JavaScript

1. Crea una carpeta llamada `00JSyEntorno` dentro de tu espacio de trabajo.
2. Dentro de esa carpeta, crea un archivo llamado `hola.html`.
3. Escribe el siguiente código en `hola.html`:
   ```html
   <!DOCTYPE html>
   <html lang="es">
   <head>
     <meta charset="UTF-8">
     <title>Hola JS</title>
   </head>
   <body>
     <script>
       console.log("¡Hola, mundo!");
       let nombre = "Ana";
       console.log("Bienvenida, " + nombre);
     </script>
   </body>
   </html>
   ```
4. Desde VSCode abre el archivo `hola.html` en tu navegador.
5. Observa el resultado en la consola del navegador.
[hola.html](AdrianLinares41.github.io/00JSyEntorno/hola.html)
## Parte 4: Experimenta

- Cambia el valor de la variable `nombre` por el tuyo y recarga la página.
   <!DOCTYPE html>
   <html lang="es">
   <head>
     <meta charset="UTF-8">
     <title>Hola JS</title>
   </head>
   <body>
     <script>
       console.log("¡Hola, mundo!");
       let nombre = "Adrian";
       console.log("Bienvenida, " + nombre);
     </script>
   </body>
   </html>
- Añade una línea que sume dos números y muestre el resultado con `console.log`.
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Hola JS</title>
</head>
<body>
  <script>
    console.log("¡Hola, mundo!");
        let nombre = "Adrian";
        console.log("Bienvenida, " + nombre);
        console.log(5 + 3);
  </script>
</body>
</html> 
- Añade otra variable con tu apellido y muestra un saludo completo.

let apellido = "Linares";
console.log("¡Hola, " + nombre + " " + apellido + "!");

- Modifica el saludo para que incluya el apellido en mayúsculas. Busca en la consola cómo convertir una cadena a mayúsculas. Para ello usa un literal de cadena (con tu nombre) seguido del operador punto (`.`) 

console.log("¡Hola, " + nombre + " " + apellido.toUpperCase() + "!");

- Modifica el archivo para que el saludo se muestre en la página web en lugar de la consola. Usa `document.body.innerHTML` para esto:
   ```js
   document.body.innerHTML = "<h1>¡Hola, " + nombre + "!</h1>";
   ```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Hola JS</title>
</head>
<body>
  <script>
     console.log("¡Hola, mundo!");
        let nombre = "Adrian";
        console.log("Bienvenida, " + nombre);
        console.log(5 + 3);
        let apellido = "Linares";
        document.body.innerHTML = "<h1>¡Hola, " + nombre + " " + apellido.toUpperCase() + "!</h1>";
  </script>
</body>
</html> 
  
- Publica tu proyecto en el repositorio de GitHub y usa GitHub Pages para alojarlo. Sigue [esta guía](https://docs.github.com/es/pages/getting-started-with-github-pages/creating-a-github-pages-site) para hacerlo.


## parte 5: formulario HTML + JavaScript
1. Crea un archivo llamado `formulario.html` en la misma carpeta `00JSyEntorno`.
2. Crea un archivo llamado `formulario.js` en la misma carpeta `00JSyEntorno`.
3. Escribe el siguiente código en `formulario.html`:
4. ```html
   <!DOCTYPE html>
   <html lang="es">
   <head>
     <meta charset="UTF-8">
     <title>Formulario de Saludo</title>
   </head>
   <body>
     <h1>Formulario de Saludo</h1>
     <form id="formulario">
       <label for="nombreInput">Nombre:</label>
       <input type="text" id="nombreInput" required>
       <button type="submit">Saludar</button>
     </form>
     <p id="salida"></p>
     
     <script src="formulario.js"></script>
   </body>
   </html>
   ```
5. Escribe el siguiente código en `formulario.js`:
   ```js
   document.addEventListener('DOMContentLoaded', function() {
     document.getElementById('formulario').addEventListener('submit', function(event) {
       event.preventDefault();
       const nombre = document.getElementById('nombreInput').value;
       document.getElementById('salida').textContent = '¡Hola, ' + nombre + '!';
     });
   });
   ```
6. Desde VSCode abre `formulario.html` en tu navegador y prueba el formulario.
[formulario](AdrianLinares41.github.io/00JSyEntorno/formulario.html)

   
## Parte 6: Preguntas de reflexión

1. ¿Qué hace `console.log`?
Es una función de JavaScript que sirve para imprimir mensajes o valores en la consola de desarrollador del navegador. Se utiliza principalmente para depurar código (debug), verificar valores de variables y rastrear el flujo de ejecución durante el desarrollo.
2. ¿Qué ocurre si cambias el valor de la variable desde la consola? ¿Se puede?
Sí, se puede.
Si abres la consola de las herramientas de desarrollo e interactúas con ella:

* En el segundo ejemplo, la variable nombre fue declarada con let nombre = "Ana"; en el ámbito global del script.

* Si en la consola escribes nombre = "Adrian";, la variable cambiará su valor en memoria a "Adrian".

* Si después ejecutas console.log(nombre);, la consola devolverá "Carlos".

3. ¿Para qué sirve la consola del navegador en este contexto?

Sirve como entorno de inspección y prueba en tiempo real. Permite:

* Ver las salidas de console.log("¡Hola, mundo!").

* Inspeccionar posibles errores de sintaxis o ejecución.

* Interactuar dinámicamente con las variables y funciones creadas en el código.

4. Para qué sirve el archivo HTML en este contexto?

El archivo HTML provee la estructura y el contenido estático de la página web. Define los elementos de la interfaz de usuario (el título <h1>, el formulario <form>, el cuadro de texto <input>, el botón <button> y el párrafo <p id="salida">) sobre los cuales JavaScript va a interactuar y modificar visualmente.

5. ¿Por qué es una buena práctica separar el código JavaScript del HTML?

* Mantenibilidad y Limpieza: El código HTML se enfoca exclusivamente en la estructura (marcado) y el JavaScript en el comportamiento/lógica.

* Reutilización: Permite vincular el mismo archivo .js a diferentes páginas HTML.

* Caché del Navegador: Los archivos .js externos se guardan en la memoria caché del navegador, lo que acelera la carga de la página en subsecuentes visitas.

* Trabajo en equipo: Facilita que un diseñador/desarrollador trabaje en la maquetación HTML mientras otro trabaja en la lógica de scripts.

6. Por qué se llama Vanilla JavaScript?

Se le denomina Vanilla JS al uso de JavaScript nativo o puro, sin la ayuda de librerías externas (como jQuery) o frameworks (como React, Angular o Vue). El término "Vanilla" hace referencia a lo básico o "sabor tradicional" del lenguaje.

7. Cuándo se usa JavaScript puro y cuándo se usan frameworks o librerías como REACT?

JavaScript Puro: Se utiliza para proyectos pequeños o medianos, scripts sencillos (como el formulario del ejemplo), sitios estáticos o cuando se busca un rendimiento máximo sin la carga de peso extra que añaden las dependencias externas.

Frameworks/Librerías (React, Vue, etc.): Se utilizan para aplicaciones web complejas (SPAs - Single Page Applications), donde el estado de la interfaz cambia constantemente, hay múltiples componentes reutilizables y se requiere una arquitectura más escalable para equipos de desarrollo grandes.

8. Cómo se define una función en JS

function(nombre) {
  // código
}

9. Sobre el código demuestra la diferencia entre let y const

* let (Variable reasignable): En el segundo ejemplo se declara let nombre = "Ana";. Al usar let, se le permite a la variable cambiar su valor más adelante (ej. nombre = "Pedro";).

* const (Constante de solo lectura): En formulario.js se declara const nombre = document.getElementById('nombreInput').value;. Al usar const, ese identificador no puede ser reasignado a otro valor en ese mismo ámbito; si intentas hacer nombre = "Otro", JavaScript arrojará un error.

10. Indica en el código:
   1. Si puede evitarse el uso de let. Qué hace

  Sí, puede evitarse.

  En el segundo ejemplo:

  JavaScript
  let nombre = "Ana";

  Dado que el valor "Ana" nunca se vuelve a reasignar en el script, es mejor práctica declarar esa variable usando const:

  const nombre = "Ana";

  * Instancia una variable en memoria con el texto "Ana", la cual posteriormente es concatenada dentro del parámetro que recibe console.log para mostrar "Bienvenida, Ana".

   2. Cuántos eventos hay en el código, cuáles son y para qué sirven

   Hay 2 eventos en el archivo formulario.js:

  * DOMContentLoaded

  ¿Para qué sirve?: Garantiza que la función se ejecute únicamente cuando todo el documento HTML haya sido completamente cargado y parseado por el navegador, evitando intentar acceder al DOM antes de que los elementos existan.

  * submit

  ¿Para qué sirve?: Captura la acción del usuario al enviar el formulario. Dentro de su manejador se llama a event.preventDefault() para evitar que la página se recargue por defecto.





