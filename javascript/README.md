# Curso JavaScript
- Acá tendré toda la información importante para repaso sobre JavaScript.
## Códigos javascript
- strings: es una secuencia de caracteres envuelta en comillas simples, dobles o acentos graves. Las cadenas son tipos de datos primitivos y son inmutables. La inmutabilidad significa que una vez creada una cadena, no se puede cambiar.
- Punto flotante: Un número de punto flotante es un número con punto decimal. Los ejemplos incluyen 3.14, 0.5 y 0.0001.
- Symbol: Crea etiquetas o identificadores únicos:
```js
const crypticKey1= Symbol("saltNpepper");
const crypticKey2= Symbol("saltNpepper");
console.log(crypticKey1 === crypticKey2); // false
```
- BigInt: Para números muy grandes, se agrega una n al final.
```javascript
8372174328783289382n; (creo)
```
- Let: Sirve para declarar variables. Se puede declarar mas de una variable con el mismo nombre y diferentes valores.
```javascript
let age= 3;
console.log(age);
```
- Const: Igual que Let, pero no permite crear mas de una variable con el mismo nombre. Sin valor bota error. Declara constantes que no se permiten cambiar a lo largo del código, como PI o MAX_SIZE.
---
## Concatenación:
- Es el proceso de unir múltiples cadenas o combinar cadenas con variables que contienen texto. El operador + es uno de los métodos más simples y frecuentemente utilizados para concatenar cadenas.:
```javascript
let firstName = "John";
let lastName = "Doe";

let fullName = firstName + " " + lastName; 
console.log(fullName); // John Doe
```
- ese espacio entre las comillas es importante, ya que sin el, sería JohnDoe.
- usando el += sería así:
```javascript
let greeting = 'Hello';
greeting += ', John!';

console.log(greeting); // "Hello, John!"
```
- Concat(): 
```javascript
let firstName = "John";
let lastName = "Doe";
let fullName = firstName.concat(" ", lastName);
console.log(fullName); // John Doe
```
---
## Console.log():
- Registra mensajes en la consola. sirve para la depuración y verificación de código, registra texto o variables.
```javascript
let name = "Alice";
let age = 25;
console.log("Name:", name, "Age:", age); // Name: Alice Age: 25
```
Mediante comas puedes separar multiples factores.
---
## info, interesante:
- Boolean: True o False
- undefined: significa que una variable ha sido declarada pero aún no se le ha asignado un valor.
- null: significa que la variable ha sido intencionalmente establecida en "nada" y no contiene ningún valor.
- Object: colección de pares clave-valor. ejemplo: age: 30
- //: Comentarios de una linea
- comentarios de mas de una linea:
```js
/*...*/
```
- Las variables no pueden comenzar con numeros deben iniciar con , _ , $ o letras.ni !, ni @, ni let, const, function o return.
- Cadenas: con Const = "hola"
- función: bloque de código reutilizable que realiza una tarea específica y puede ser llamado con varias entradas.
- Método: tipo de función que está asociado con un objeto, lo que significa que opera sobre los datos contenidos en ese objeto.
- Objeto: es una colección de pares clave-valor. La clave es el nombre de la propiedad y el valor es el valor de la propiedad.
---
## Bot de prueba
```javascript
console.log("Hi there!");
console.log("I am excited to talk to you.");
let bot;
bot = "teacherBot";

let botLocation = "the universe";

console.log("Allow me to introduce myself.");

const botIntroduction = "My name is " + bot + ".";
console.log(botIntroduction);

const botLocationSentence = "I live in " + botLocation + ".";
console.log(botLocationSentence);

bot = "professorBot";

const nicknameIntroduction = "My nickname is " + bot + ".";
console.log(nicknameIntroduction);

bot = "awesomeTeacherBot";

const newNicknameGreeting = "I love my nickname but I wish people would call me " + bot + ".";
console.log(newNicknameGreeting);

const favoriteSubject = "Computer Science";

const favoriteSubjectSentence = "My favorite subject is " + favoriteSubject + ".";
console.log(favoriteSubjectSentence);

console.log("Well, it was nice to talk to you. Have a nice day!");
```
---
## tipificación dinámica y estática
- JavaScript es un idioma de tipado dinámico, ósea que no hay que especificar el tipo de dato al declarar variables, pero, el tipo se determina según el valor asignado a la variable mientras el programa se ejecuta, esto permite cambiar el tipo de variables durante el programa.
- tipado estático: C# o C++.
- es dinámico y puedes hacer cambios de numero hacia un string.
- el dinámico puede traer más errores a largo plazo.
---
## typeof y typeof null:
- permite ver el tipo de dato de una variable o valor, siempre devuelve un string con el tipo.
```javascript
let isUserLoggedIn = true;
console.log(typeof isUserLoggedIn); // "boolean"
```
- esto devuelve: "boolean"
```javascript
let exampleVariable = null;
console.log(typeof exampleVariable); // "object"
```
- esto devuelve: "object", lo que es un error de javascript.
---
## corchetes ([])
- permite recuperar un carácter específico de una cadena basado en su posición, que se llama su índice.
- índice: es la posición de un carácter dentro de una cadena, y es basado en cero. Esto significa que el primer carácter de una cadena tiene un índice de 0, el segundo carácter tiene un índice de 1, y así sucesivamente. Por ejemplo, en la cadena hello, el carácter h está en el índice 0, e está en el índice 1, l está en el índice 2, y así sucesivamente.
```js
let greeting = "hello";
console.log(greeting[1]); // "e"
```
- Para obtener el último carácter de una cadena, puedes usar la longitud de la cadena menos uno. La propiedad length de una cadena te dice cuántos caracteres contiene, por lo que para acceder al último carácter, restarías uno de la longitud:
```js
let greeting = "hello";
console.log(greeting[greeting.length - 1]); // "o"
```
- En este caso, la longitud de hello es 5, y el último carácter (o) está en el índice 4 que es 5 - 1.
- multiples caracteres:
```js
let greeting = "hello";
let firstTwo = greeting[0] + greeting[1]; // "he"
console.log(firstTwo);
```
- estamos concatenando el primer y segundo caracteres usando notación de corchetes para formar la cadena he.
- La notación de corchetes es útil cuando necesitas acceder a caracteres específicos en una cadena, como extraer iniciales de un nombre o verificar una letra específica para validación.
- puedes crear una nueva línea en una cadena usando un carácter especial llamado secuencia de escape. La secuencia de escape más común para nuevas líneas es \n. le dice a JavaScript que inserte un salto de línea en ese punto, lo que da como resultado que la cadena se muestre en múltiples líneas.
```js
let poem = "Roses are red,\nViolets are blue,\nJavaScript is fun,\nAnd so are you.";
console.log(poem);
```
- Si simplemente usas comillas dentro de una cadena sin escaparlas, puede causar un error porque JavaScript pensará que estás tratando de terminar la cadena.
- Puedes escapar las comillas internas colocando una barra inclinada (\) antes de ellas:
```js
let statement = "She said, \"Hello!\"";
console.log(statement); // She said, "Hello!"
```
- La barra inclinada le dice a JavaScript que trate las comillas como caracteres literales, para que aparezcan correctamente en la salida. También puedes escapar otros caracteres especiales, como la barra inclinada en sí (\\), o comillas simples dentro de una cadena rodeada por comillas simples (\').
---
## literales de plantilla y la interpolación de strings
- los literales de plantilla son una forma poderosa y flexible de trabajar con cadenas. A diferencia de las cadenas normales, que usan comillas simples (') o dobles ("), los literales de plantilla se definen con comillas inversas (```). Facilitan la creación de cadenas que abarcan múltiples líneas o incluyen expresiones (como variables o incluso código JavaScript) directamente dentro de la cadena.
- Permiten una manipulación de cadenas más sencilla, incluido el incrustar variables directamente dentro de una cadena, una característica conocida como interpolación de strings.
```js
const name = "Alice";
const greeting = `Hello, ${name}!`;
console.log(greeting); // Hello, Alice!
```
- La sintaxis ${name} es un ejemplo de interpolación de strings, donde el valor de la variable name se inserta directamente en la cadena. (un poco mejor que la concatenación).
- Otra gran característica de los literales de plantilla es que soportan cadenas multilínea. Con las cadenas normales, necesitarías usar caracteres de escape (\n) para crear nuevas líneas. Con los literales de plantilla, simplemente puedes escribir la cadena en varias líneas, y el formato se preserva:
```js
let poem = `Roses are red,
Violets are blue,
JavaScript is fun,
And so are you.`;
console.log(poem);
```
- Otra característica de los template literals es que te permiten insertar expresiones de JavaScript directamente dentro de la cadena.
```js
const song = "Bohemian Rhapsody";
const score = 9.5;
const highestScore = 10;
const output = `One of my favorite songs is "${song}". I rated it ${
  (score / highestScore) * 100
}%.`;
console.log(output); 
```
---
### ¿Cómo puedes encontrar la posición de una subcadena en una cadena? (indexOf())
- Una subcadena es una secuencia de caracteres que aparece dentro de una cadena más grande. Por ejemplo, en la cadena hola mundo, hola y mundo son subcadenas.
- indexOf(): Permite buscar una subcadena dentro de una cadena. Devuelve el índice (o posición) de la primera ocurrencia de esa subcadena. Si la subcadena no se encuentra, devuelve -1, lo que indica que la búsqueda no tuvo éxito. Toma dos argumentos: el primero es la subcadena que deseas encontrar dentro de la cadena más grande, y el segundo es una posición de inicio opcional para la búsqueda. Si no proporcionas una posición de inicio, la búsqueda comenzará desde el inicio de la cadena.
- un argumento es un valor que le das a una función o método cuando lo llamas, permitiendo que esa función o método realice su tarea usando la información específica que proporcionas. Aprenderás más sobre argumentos en lecciones futuras.
- Aquí tienes un ejemplo de uso del método indexOf() para encontrar la posición de la cadena awesome:
```js
let sentence = "JavaScript is awesome!";
let position = sentence.indexOf("awesome!");
console.log(position); // 14
```
- En este ejemplo, la palabra awesome comienza en el índice 14 en la cadena JavaScript es awesome!, por lo que el método indexOf() devuelve 14, (cuenta espacios), es sensible a mayusculas y minusculas.
---
### prompt()
- Es una de las formas más simples de obtener entrada de un usuario a través de una pequeña ventana de diálogo emergente.
- A menudo se utiliza cuando la página web necesita una información del usuario, como un nombre u otra forma de entrada de texto. Abre un cuadro de diálogo que pide al usuario alguna entrada y luego devuelve el texto ingresado por el usuario como una cadena.
- Toma dos argumentos: el primero es el mensaje que aparecerá dentro del cuadro de diálogo, generalmente pidiendo al usuario que ingrese información. Y el segundo es un valor predeterminado que es opcional y llenará el campo de entrada inicialmente.
```html
<button id="prompt-btn">Show Prompt</button>
<p id="output"></p>
<script src="index.js"></script>
```
```js
//prompt(message, default);
const btn = document.getElementById("prompt-btn");
const output = document.getElementById("output");
btn.addEventListener("click", () => {
  const userName = prompt("What is your name?", "Guest");
  output.textContent = "Hello, " + userName + "!";
});
```
- si se canela el prompt saldra null.
---
### ¿Qué es ASCII y cómo funciona con `charCodeAt()` y `fromCharCode()`?:
- abreviatura de American Standard Code for Information Interchange, es un estándar de codificación de caracteres utilizado en computadoras para representar texto. Asigna un valor numérico a cada carácter, lo cual es reconocido universalmente por las máquinas. Aunque las cadenas de JavaScript usan Unicode (UTF-16) internamente, los valores ASCII coinciden con los primeros 128 caracteres Unicode. 
- ASCII: es un sistema para codificar caracteres como letras, dígitos y símbolos en valores numéricos. Cada carácter se asigna a un número específico. Por ejemplo, la letra mayúscula A está representada por el número 65 en ASCII, mientras que la minúscula a es representada por 97. Esta codificación permite a las computadoras almacenar y manipular texto. El estándar ASCII cubre 128 caracteres, incluyendo:
- Letras inglesas mayúsculas y minúsculas (A-Z, a-z).
- Números (0-9).
- Signos de puntuación y símbolos comunes (!, @, #, y así sucesivamente).
- Caracteres de control (como nueva línea y tabulación).
- En JavaScript, puedes acceder al código numérico de un carácter usando el método charCodeAt(). Este método devuelve la unidad de código UTF-16 del carácter en un índice especificado. Para los primeros 128 caracteres, este valor coincide con el código ASCII.
```js
let letter = "A";
console.log(letter.charCodeAt(0));  // 65

let symbol = "!";
console.log(symbol.charCodeAt(0));  // 33
```
- Mientras que charCodeAt() te ayuda a obtener el código numérico de un carácter, el método fromCharCode() te permite hacer lo contrario: convertir una unidad de código UTF-16 (que coincide con ASCII para caracteres básicos) en su carácter correspondiente.
```js
let char = String.fromCharCode(70);
console.log(char);  //  A
```
- Estos métodos son particularmente útiles cuando necesitas manipular o comparar caracteres basándote en sus valores numéricos de código. Por ejemplo, podrías usar charCodeAt() para verificar si un carácter es mayúscula, minúscula o un dígito comparando su valor ASCII. Por otro lado, fromCharCode() puede ser utilizado para generar dinámicamente caracteres a partir de sus códigos ASCII.
---
### ¿Cómo puedes probar si una cadena contiene una subcadena?
- Por ejemplo, podrías querer verificar si la entrada de un usuario incluye una palabra o carácter específico antes de realizar alguna acción. Una forma de lograrlo es utilizando el método includes().
- includes(): se utiliza para verificar si una cadena contiene una subcadena específica. Si se encuentra la subcadena dentro de la cadena, el método devuelve true, de lo contrario, devuelve false. (sensible a mayusculas).
```js
let phrase = "JavaScript is awesome!";
let result = phrase.includes("awesome");
console.log(result);  // true
```
- para verificar una subcadena comenzando en un índice específico de la cadena proporcionando un segundo parámetro:
```js
let text = "Hello, JavaScript world!";
let result = text.includes("JavaScript", 7);
console.log(result);  // true
```
- solo devuelve un resultado de true o false. No proporciona información sobre dónde se encuentra la subcadena en la cadena ni cuántas veces ocurre. Si necesitas ese nivel de detalle, otros métodos, como el método indexOf() podrían ser más adecuados.
---
### ¿Cómo puedes extraer un subcadena de una cadena?
- slice(): te permite extraer una porción de una cadena y devuelve una nueva cadena, sin modificar la cadena original. Toma dos parámetros: el índice de inicio y el índice de fin opcional.
```js
let message = "Hello, world!";
let greeting = message.slice(0, 5);
console.log(greeting);  // Hello
```
- En este ejemplo, slice(0, 5) extrae caracteres comenzando desde el índice 0 hasta pero sin incluir el índice 5. Como resultado, se extrae la palabra Hello.
- Cuando usas un número negativo, se cuenta hacia atrás desde el final de la cadena.
---
### ¿Cómo puedes cambiar el caso de una cadena?
- hay muchas situaciones en las que podrías necesitar ajustar el caso del texto, como transformar todas las letras a mayúsculas para un encabezado o convertir el texto a minúsculas para uniformidad.
- toUpperCase(): Convierte todos los caracteres a letras mayúsculas y devuelve una nueva cadena con todos los caracteres en mayúsculas. Esto es útil cuando quieres enfatizar texto o crear consistencia en el formato de las cadenas.
```js
let greeting = "Hello, World!";
let uppercaseGreeting = greeting.toUpperCase();
console.log(uppercaseGreeting);  // "HELLO, WORLD!"
```
- toLowerCase() convierte todos los caracteres en una cadena a minúsculas. Esto es útil cuando necesitas estandarizar la entrada, como cuando comparas texto proporcionado por el usuario o haces verificaciones sin distinción de mayúsculas.
```js
let shout = "I AM LEARNING JAVASCRIPT!";
let lowercaseShout = shout.toLowerCase();
console.log(lowercaseShout);  // "i am learning javascript!"
```
- Estos métodos son particularmente útiles para estandarizar entradas de texto, realizar comparaciones sin distinguir entre mayúsculas y minúsculas, y asegurar la consistencia del diseño.
---
### ¿Cómo puedes eliminar los espacios en blanco de una cadena de texto?
- es común encontrar espacios en blanco no deseados al principio o al final de una cadena. Los espacios en blanco pueden interferir con operaciones como comparación, almacenamiento o visualización, por lo que es importante saber cómo eliminarlos eficientemente.
- trim(): Es la forma más común de eliminar espacios en blanco tanto del principio como del final de una cadena de texto.
```js
let message = "   Hello!   ";
console.log(message); // "   Hello!   "
let trimmedMessage = message.trim();
console.log(trimmedMessage);  // "Hello!"
```
- trimStart(): elimina espacios en blanco del principio (o inicio) de la cadena.
- trimEnd(): elimina espacios en blanco del final de la cadena.
---
### reemplazar partes de una cadena con otra:
- podrías necesitar actualizar la información del usuario en una URL, cambiar el formato de las fechas o corregir errores en el contenido generado por el usuario.
- replace(): Permite encontrar un valor especificado (como una palabra o carácter) en una cadena y reemplazarlo con otro valor. El método devuelve una nueva cadena con el reemplazo y deja la original sin cambios porque las cadenas en JavaScript son inmutables. Si el valor aparece varias veces en la cadena, solo se reemplazará la primera.
- replaceAll(): lo mismo de arriba, pero cambia todos los valores en la cadena.
- Esta es la sintáxis básica. (Es sensible a mayusculas):
- searchValue es el valor que quieres buscar en la cadena. Puede ser una cadena o una expresión regular (regex), que describe patrones en el texto. Esto te permite buscar y manipular cadenas de una manera flexible y poderosa.
- newValue es el valor que reemplazará al searchValue.
```js
//string.replace(searchValue, newValue);
let text = "I love JavaScript!";
console.log(text); // "I love JavaScript!"
let newText = text.replace("JavaScript", "coding");
console.log(newText);  // "I love coding!"
```
---
### ¿Cómo puedes repetir una cadena x número de veces?:
- puedes encontrar situaciones donde necesitas repetir una cadena un número específico de veces. Ya sea generando patrones repetidos o simplemente duplicando texto, el método repeat() proporciona una forma simple y efectiva de lograr esto.
- repeat(): Es una función incorporada en JavaScript que te permite repetir una cadena un número especificado de veces. puede simplificar tareas que implican duplicación de cadenas, haciendo que tu código sea más conciso y legible. Ya sea que generes patrones de texto repetidos o llenes un espacio con caracteres, repeat() puede ahorrarte escribir bucles o código más complejo. No estás limitado a pasar un número directamente al método repeat(). También puedes pasar una variable que almacene un valor numérico.
- Esta es la sintáxis básica:
```js
//string.repeat(count);
let word = "Hello!";
let repeatedWord = word.repeat(3);
console.log(repeatedWord);  // "Hello!Hello!Hello!"
```
- string es la cadena que deseas repetir, y count es el número de veces que deseas que la cadena se repita. count no acepta numeros negativos. Si el count es un decimal como 2.5, el método repeat() lo redondeará hacia abajo al número entero más cercano. Si se pone cero el string estará vacio.
- Infinity: es un valor especial que representa una cantidad infinita. Se usa para denotar números que son mayores que cualquier número finito. (no funciona en Count).
```js
let count = 4;
let word = "Test";
let repeatedWord = word.repeat(count);
console.log(repeatedWord); // TestTestTestTest
```
- En este ejemplo, la variable count almacena el número de repeticiones. Esto puede ser útil cuando el número de repeticiones depende de la entrada del usuario u otros valores dinámicos en tu programa.
- RangeError: se lanza al usar negativos o infinity con repeat().
- Puedes encadenar métodos así:
```js
.firstMethod().secondMethod()
```
---
#### tipos de números:
- decimales, enteros y negativos. Todo bajo el mismo paraguas del tipo de datos Number. Tiene casos especiales como ∞ y NaN, o "Not a number".
- Los números de punto flotante son números con puntos decimales. A menudo se les refiere simplemente como "floats" por los desarrolladores de JavaScript.
- infinitos:
```js
const infiniteNumber = 1 / 0;
console.log(infiniteNumber); // Infinity
```
- Aparte del sistema decimal estándar (base 10), JavaScript también admite números en diferentes bases como binario, octal y hexadecimal. 
- Binario es un sistema de base 2 que sólo utiliza dígitos 1 y 0. 
- Octal es un sistema de base 8 que usa sólo dígitos del 0 al 7. 
- Hexadecimal es un sistema de base 16 que usa dígitos del 0 al 9 y las letras a a f, como se ve en los colores hex de CSS.
---
### ¿Cuáles son los diferentes operadores aritméticos en JavaScript?:
- El operador de suma es un signo más (+). El operador de suma le permite encontrar el total de dos o más números. En las operaciones de suma, el orden de los números no importa.
```js
const difference = 10 + 5;
console.log(difference); // 5
```
- El operador de resta es un signo menos (-). Le permite encontrar la diferencia entre dos números.
```js
const difference = 10 - 5;
console.log(difference); // 5
```
- También puede asignar los números a variables y hacer la resta con los nombres de las variables:
```js
const num1 = 10;
const num2 = 5;
const result = num1 - num2;
console.log(result); // 5
```
- el operador de multiplicación se representa con un asterisco (*) y se utiliza para encontrar el producto de dos o más números. El orden de los números que está multiplicando no importa (código igual que los anteriores).
- el operador de división es una barra (/), que difiere del símbolo de división utilizado en las matemáticas tradicionales (÷). Realiza operaciones de división con el operador de división. El orden de los números que está dividiendo importa en este caso. (código igual a los anteriores).
- Es importante tener en cuenta que si intenta dividir por cero, JavaScript devolverá Infinity.
- El operador de resto, representado por un signo de porcentaje (%), devuelve el resto de una división. El resto en matemáticas es el valor sobrante después de realizar la división. (código igual a los anteriores).
- El operador de exponenciación, representado por un doble asterisco (**), eleva un número a la potencia de otro. (código igual que los anteriores).
- Es posible mezclar operadores en una sola operación o expresión:
```js
const result = 10 + 5 * 2 - 8 / 4;
console.log(result); // 18
```
- Cuando mezclas diferentes operadores en una sola expresión, el motor de JavaScript sigue un sistema llamado precedencia de operadores para determinar el orden de las operaciones. La precedencia de operadores determina el orden en el que se ejecutan las operaciones en las expresiones.
---
### ¿Qué ocurre cuando intentas hacer cálculos con números y cadenas?:
- Cuando usas + con un número y una cadena, JavaScript decide tratarlos a ambos como cadenas y los une. Si revisas el tipo del resultado con el operador typeof, verás que es, de hecho, una cadena:
```js
const result = 5 + '10';
console.log(result); // 510
console.log(typeof result); // string
```
- Esto se conoce como coerción de tipos. La coerción de tipos es cuando un valor de un tipo de datos se convierte en otro.
- cuando intentas realizar otras operaciones aritméticas como resta, multiplicación o división con una cadena y un número. En estos casos, JavaScript intenta convertir la cadena en un número antes de hacer la operación –¡otra coerción de tipos!
```js
const subtractionResult = '10' - 5;
console.log(subtractionResult); // 5
console.log(typeof subtractionResult); // number
```
- así con multiplicación y división también. si la cadena no es un número sale NaN
- JavaScript trata los booleanos como números en operaciones matemáticas: true = 1, false = 0, null= 0 y undefined = NaN.
