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
---
### precedencia de operadores:
- Determina el orden en el que se evalúan las operaciones en una expresión. Los operadores con mayor precedencia se evalúan antes que los de menor precedencia. Piensa en la precedencia de operadores como en las matemáticas, donde la división y multiplicación suceden antes que la suma y resta.
- JavaScript tiene sus propias reglas sobre qué operadores van primero, segundo, y así sucesivamente.
```js
const result = 2 + 3 * 4;
console.log(result); // 14
```
- Si JavaScript evaluara esta expresión de izquierda a derecha, esperarías 2 + 3 = 5, luego 5 * 4 = 20. Pero debido a que la multiplicación tiene una precedencia mayor que la suma, JavaScript evalúa primero la parte 3 * 4, resultando en 2 + 12 = 14.
- Puedes usar paréntesis, (), ya que cualquier cosa dentro de los paréntesis se evalúa primero, sin importar qué. los paréntesis obligan a JavaScript a evaluar 2 + 3 primero, y luego multiplicar el resultado por 4. Esto te da 20 en lugar de 14.
```js
const result = (2 + 3) * 4;
console.log(result); // 20
```
- El operador de división tiene más precedencia que la suma o resta también, como la división tiene una precedencia mayor que la suma, JavaScript evalúa primero la división: 6 / 3 = 2, y luego suma 2 + 2, dando el resultado 4:
```js
const result = 2 + 6 / 3;
console.log(result); // 4
```
- Entonces, en multiplicación y división, esas operaciones siempre se llevan a cabo antes que la suma y la resta, a menos que se usen paréntesis para cambiar el orden. ¿Qué pasa si los operadores tienen la misma precedencia? JavaScript utiliza asociatividad para determinar el orden de evaluación. La asociatividad es lo que le dice a JavaScript si debe evaluar operadores de izquierda a derecha o de derecha a izquierda. Para la mayoría de los operadores como suma y multiplicación, la asociatividad es de izquierda a derecha.
```js
const result = 10 - 2 + 3;
console.log(result); // 11
```
- Primero, 10 - 2 = 8, luego 8 + 3 = 11. JavaScript avanza de izquierda a derecha en este caso. 
- Algunos operadores, como el de asignación (=), son asociativos de derecha a izquierda. Esto significa que el lado derecho de la expresión se evalúa primero, JavaScript asigna 5 a b primero, luego asigna b (que ahora es 5) a a.
```js
let a, b;
a = b = 5;

console.log(a); // 5
console.log(b); // 5
console.log(a + b); // 10
```
- El operador de exponente también es asociativo de derecha a izquierda.
---
###  operadores de incremento y decremento:
- Los operadores de incremento y decremento están representados por ++ y --, respectivamente. Ambos te permiten ajustar el valor de una variable en 1.
- En lugar de escribir algo como x = x + 1 o x = x - 1, puedes simplemente usar x++ para sumar 1, o x-- para restar 1. Es más rápido, limpio y fácil de leer.
- Hay un giro en la forma en que funcionan los operadores de incremento y decremento: vienen en dos formas, prefijo y postfijo, con la diferencia siendo cuándo se actualiza el valor. Para el operador de incremento, el prefijo (++x) incrementa el valor de la variable primero, luego devuelve un nuevo valor. El postfijo (x++) devuelve primero el valor actual de la variable, luego lo incrementa:
```js
let x = 5;
console.log(++x); // 6
console.log(x); // 6
```
- En el código anterior, ++x significa "incrementa x primero, luego úsalo". Así que cuando registras ++x, obtienes inmediatamente el valor incrementado, que es 6.
```js
let y = 5;
console.log(y++); // 5
console.log(y); // 6
```
- En este ejemplo, y++ significa "usa y primero, luego increméntalo". Cuando registras y++, obtienes 5, pero y se convierte en 6 después de esa línea de código.
- El operador de decremento hace lo mismo que incrementar, excepto que disminuye el valor en 1. De nuevo, hay dos formas: prefijo (--x) disminuye primero el valor de la variable, luego devuelve el nuevo valor. Y el postfijo (x--) devuelve primero el valor actual, luego lo reduce:
```js
let x = 5;
console.log(--x); // 4
console.log(x); // 4

let y = 5;
console.log(y--); // 5
console.log(y); // 4
```
- Entonces, ¿cuál deberías usar: prefijo o postfijo? En muchos casos, no importa cuál uses. Ambos hacen el trabajo. Sin embargo, si estás usando el valor inmediatamente en una expresión, la diferencia se vuelve importante.
```js
let a = 5;
let b = ++a;
console.log(b); // 6 (a was incremented before assignment)

let c = 5;
let d = c++;
console.log(d); // 5 (c was incremented after assignment)
```
- Entonces, si necesitas el valor actualizado de inmediato, usa prefijo. Si quieres el valor actual primero y no te importa el incremento hasta más tarde, utiliza postfijo.
---
### ¿Qué son los operadores de asignación compuesta en JavaScript y cómo funcionan?:
- todos los operadores aritméticos tienen una forma de asignación compuesta. provide a concise shorthand for an operation on a variable followed by storing the result in that same variable. They combine the operation and assignment into a shorter form like x += y, which is equivalent to writing x = x + y but without repeating the variable name.
```js
//En vez de:
let num = 5;
num = num + 2;
console.log(num); // 7
//Mejor:
let num = 5;
num += 2;
console.log(num); // 7
```
- El operador += te permite agregar un valor a una variable existente. Se conoce como el operador de asignación de suma, toma el valor actual de la variable, agrega el número especificado a él, y luego asigna el resultado de nuevo a la variable.
```js
let total = 10;
total += 5;
console.log(total); // 15
```
-  existe un operador de asignación de resta denotado por -=. El operador de asignación de resta resta el valor especificado del valor actual de la variable y asigna el nuevo valor de nuevo a la variable.
```js
let score = 20;
score -= 7;
console.log(score); // 13
```
- El operador de asignación de multiplicación está representado por *=. Multiplica el valor actual de la variable por el número especificado y lo reasigna de nuevo a la variable. (igual a los anteriores pero con *).
- existe un operador de asignación de división denotado por /=. Te permite dividir el valor actual de una variable por un número que especifiques y luego asignar el resultado de nuevo a la variable. (igual que los anteriores pero con /).
- Operador de asignación de residuo (%=), que divide una variable por el número especificado y asigna el residuo a la variable.
- Operador de asignación de exponente (**=), que eleva una variable a la potencia del número especificado y reasigna el resultado a la variable.
- Operador de asignación AND a nivel de bits (&=), que realiza una operación AND a nivel de bits con el número especificado y reasigna el resultado a la variable.
- Operador de asignación bit a bit OR (|=), que realiza una operación OR bit a bit con el número especificado y reasigna el resultado a la variable.
---
## ¿Qué son los booleanos, y cómo funcionan con los operadores de igualdad y desigualdad?:
- Los booleanos son un tipo de datos con solo valores de true y false. Son útiles porque permiten realizar acciones en función de ciertas condiciones. Son esenciales para evaluar si algo debe ocurrir o no, como por ejemplo, decidir si alguien puede acceder a una función específica de la aplicación. Aquí hay un ejemplo de establecer el valor true a una variable llamada isOldEnoughToDrive:
```js
let isOldEnoughToDrive = true;
console.log(isOldEnoughToDrive); // true
//Puedes usar esta variable dentro de una condicional así:
let isOldEnoughToDrive = true;
if (isOldEnoughToDrive) {
 console.log("You're old enough to drive"); // You're old enough to drive
} else {
 console.log("Sorry, you are not old enough to drive");
}
```
- Una condicional te ayuda a tomar decisiones en tu código basado en una condición. Este ejemplo utiliza lo que se llama una sentencia if/else. Si isOldEnoughToDrive es true, entonces la oración Estás lo suficientemente viejo para conducir se registrará en la consola. De lo contrario, si isOldEnoughToDrive es false, entonces la oración Lo siento, no eres lo suficientemente viejo para conducir se registrará en la consola. Dado que la variable isOldEnoughToDrive está configurada como true, la primera oración se registrará en la consola.
- Para comparar dos valores, puedes usar el operador de igualdad o de estricta igualdad. El resultado de la comparación será un booleano de true o false. El operador de igualdad se representa con un símbolo de doble igual (==).
```js
console.log(5 == "5"); // true
console.loh(6 == "5"); //false
```
- El operador de igualdad utiliza coerción de tipo antes de verificar si cada valor es igual. Esto difiere del operador de igualdad estricta, que no realiza coerción de tipo.
- El operador de igualdad estricta verificará si los tipos son los mismos y si los valores son los mismos. Este operador se representa con un símbolo de triple igual (===).
```js
console.log(5 === '5'); // false
console.log(5 === 5); //true
```
- La siguiente comparación será false, porque un tipo de dato cadena no es igual a un tipo de dato número. Si necesitas verificar si algo no es igual a otro valor, puedes usar los operadores de desigualdad o estricta desigualdad.
- Operador de desigualdad (!=) para comparar un número con una cadena.
- El resultado sería false porque el operador de desigualdad primero convierte el valor de cadena a un número y luego compara los valores. Dado que los valores serían los mismos, devolverá false.
- Si intentaras usar el operador de desigualdad estricta, obtendrías un resultado diferente. El operador de desigualdad estricta se representa con un signo de exclamación seguido de dos signos de igual (!==).
```js
console.log(5 !== "5"); // true
console.log(5 !== 5); //false
```
- El resultado sería true porque el operador de desigualdad estricta no realiza ninguna coerción de tipo. Dado que el número 5 no es igual a la cadena "5", entonces el resultado es true.
- Se considera una buena práctica usar operadores de desigualdad y igualdad estricta siempre que sea posible, ya que no realizan coerción de tipo. La mayoría de las veces en proyectos profesionales, verás bases de código que usualmente prefieren estos dos operadores sobre los operadores de desigualdad y igualdad.
---
### ¿Cuáles son los operadores de comparación y cómo funcionan?:
- Los operadores de comparación te permiten comparar dos valores y devolver un resultado true o false. Luego puedes usar el resultado para tomar una decisión o controlar el flujo de tu programa. Las comparaciones se utilizan en sentencias if, loops y muchas otras situaciones donde se necesita tomar decisiones en función de ciertas condiciones. Analicemos los operadores de comparación más comunes y veamos cómo funcionan.
- El operador mayor que, representado por un corchete angular derecho (>), verifica si el valor a la izquierda es mayor que el de la derecha:
```js
let a = 6;
let b = 9;
console.log(a > b); // false
console.log(b > a); // true
```
- El operador mayor o igual, representado por un corchete angular derecho y el signo igual (>=), verifica si el valor a la izquierda es mayor o igual que el de la derecha. (igual que el anterior pero con >=).
- El operador menor que, representado por un corchete angular izquierdo (<), verifica si el valor a la izquierda es menor que el de la derecha. (igual que los anteriores pero con <).
- El operador menor o igual, representado por un corchete angular izquierdo y el signo igual (<=), verifica si el valor a la izquierda es menor o igual que el de la derecha. (igual que los anteriores pero con <=).
- Un valor truthy es un valor que se evalúa como true en un contexto booleano. Ejemplos de valores truthy son: Cadenas no vacías, números distintos de cero, el booleano true.
- Boolean(): Para verificar la veracidad de un valor. Por ejemplo, Booleanks("Hello World!") devolverá true porque "Hello World!" es verdadero.
- Los valores falsy son valores que se evalúan como false en un contexto booleano. Ejemplos de valores falsy son: "" (cadena vacía), 0, false, null, undefined, NaN.
- Una estructura condicional puede tener una cláusula else, que ejecuta código cuando la condición if es falsa.
---
### ¿Qué son los operadores unarios y cómo funcionan?:
- actúan sobre un solo operando para realizar operaciones como conversión de tipo, manipulación de valores o verificación de ciertas condiciones. 
- El operador unario de suma convierte su operando en un número. Si el operando ya es un número, permanece sin cambios. Es útil cuando deseas asegurarte de trabajar con un valor numérico.
```js
const str = '42';
const strToNum = +str;
console.log(strToNum); // 42
console.log(typeof str); // string
console.log(typeof strToNum); // number
```
- existe un operador de negación unario. Niega el valor del operando. Funciona de manera similar al unario de suma, excepto que invierte el signo.
```js
const str = '42';
const strToNegativeNum = -str;
console.log(strToNegativeNum); // -42
console.log(typeof str); // string
console.log(typeof strToNegativeNum); // number
```
- El operador lógico NOT, representado por un signo de exclamación (!), es otro operador unario. Invierte el valor booleano de su operando. Por lo tanto, si el operando es true, se convierte en false, y si es false, se convierte en true. 
```js
let isOnline = true;
console.log(!isOnline); // false
let isOffline = false;
console.log(!isOffline); // true
```
- El operador bitwise NOT es un operador unario menos común. Representado por una tilde, ~, invierte la representación binaria de un número. Las computadoras almacenan números en formato binario (1s y 0s). El operador ~ invierte cada bit, es decir, cambia todos los 1s a 0s y todos los 0s a 1s. 
```js
const num = 5; // The binary for 5 is 00000101
console.log(~num); // -6
```
- En este ejemplo, 5 se convirtió en -6 porque al aplicar el operador ~ a 5, obtienes - (5 + 1), que equivale a -6 debido a la representación en complemento a dos, que es una forma en que las computadoras representan números negativos en binario. Probablemente no uses el bitwise NOT a menudo a menos que trabajes en tareas de programación de bajo nivel como manipulación directa de bits.
- void es un operador unario que evalúa una expresión y devuelve undefined.
```js
const result = void (2 + 2);
console.log(result); // undefined
```
- void también se utiliza comúnmente en hipervínculos para evitar la navegación.
```js
<a href="javascript:void(0);">Click Me</a>
```
- el operador typeof devuelve el tipo de su operando como una cadena.
---
### ¿Qué son los operadores a nivel de bits y cómo funcionan?:
- Son operadores especiales que operan sobre las representaciones binarias de los números. Un bit es la unidad de información más básica. Solo puede tener dos valores: 0 o 1. Binario es un sistema de numeración que utiliza solo estos dos dígitos para representar todos los números.
- Por ejemplo, la representación binaria del número decimal 10 es 1010. En este sistema, cada dígito representa una potencia de 2, comenzando por el dígito más a la derecha e incrementando a medida que nos movemos hacia la izquierda.
<table>
  <th>1</th>
  <th>0</th>
  <th>1</th>
  <th>0</th>
</table>
<table>
  <th>1·2<sup>3</sup></th>
  <th>0·2<sup>2</sup></th>
  <th>1·2<sup>1</sup></th>
  <th>0·2<sup>0</sup></th>
</table>
<table>
  <th>8</th>
  <th>0</th>
  <th>2</th>
  <th>0</th>
</table>

- En la tabla anterior, la primera fila muestra el número binario 1010, la segunda fila muestra la potencia de 2 representada por cada posición binaria, y la tercera fila muestra el resultado de cada multiplicación. Si sumas todos los valores en la tercera fila, totalizan 10.
- operadores a nivel de bits. Estos operadores realizan operaciones sobre las representaciones binarias de los números. JavaScript provides several bitwise operators, including AND (&), OR (|), XOR (^), NOT (~), left shift (<<), and right shift (>>).
- El operador AND a nivel de bits (&) devuelve un 1 en cada posición de bit para la cual los bits correspondientes de ambos operandos son 1.
```js
let a = 5;  // Binary: 101
let b = 3;  // Binary: 011
console.log(a & b);  // 1 (Binary: 001)
```
- En este ejemplo, realizamos una operación AND a nivel de bits en 5 (101 en binario) y 3 (011 en binario). El resultado es 1 (001 en binario) porque solo el bit más a la derecha es 1 en ambos números.
- El operador a nivel de bits OR (|) devuelve un 1 en cada posición de bit para la cual los bits correspondientes de cualquiera de los operandos son 1.
```js
let a = 5;  // Binary: 101
let b = 3;  // Binary: 011
console.log(a | b);  // 7 (Binary: 111)
```
- Aquí, el resultado es 7 (111 en binario) porque al menos uno de los bits es 1 en cada posición.
- El operador a nivel de bits XOR (^) devuelve un 1 en cada posición de bit para la cual los bits correspondientes de uno, pero no de ambos operandos son 1. 
```js
let a = 5;  // Binary: 101
let b = 3;  // Binary: 011
console.log(a ^ b);  // 6 (Binary: 110)
```
- El resultado es 6 (110 en binario) porque el primer y el segundo bit desde la derecha son diferentes en los dos números.
- El operador NOT a nivel de bits (~) invierte todos los bits de su operando.
```js
let a = 5;  // Binary: 101
console.log(~a);  // -6
let b = -5;
console.log(~b); // 6
```
- El operador de desplazamiento a la izquierda (<<) mueve todos los bits hacia la izquierda un número especificado de posiciones.
```js
let a = 5;  // Binary: 101
console.log(a << 1);  // 10 (Binary: 1010)
```
- Aquí, todos los bits se desplazan una posición hacia la izquierda, multiplicando efectivamente el número por 2.
- El operador de desplazamiento a la derecha (>>) mueve todos los bits hacia la derecha.
```js
let a = 5;  // Binary: 101
console.log(a >> 1);  // 2 (Binary: 10)
```
- Aquí, todos los bits se desplazan una posición hacia la derecha, dividiendo efectivamente el número por 2 y redondeando hacia abajo.
- Los operadores a nivel de bits se utilizan a menudo en programación de bajo nivel y criptografía. Aunque pueden no ser tan comúnmente utilizados en la programación diaria de JavaScript, entenderlos puede ser beneficioso para ciertas tareas especializadas y puede profundizar tu comprensión de cómo funcionan las computadoras a un nivel fundamental.
---
### ¿Cuáles son las declaraciones condicionales y cómo funcionan las sentencias if/else?:
- Las declaraciones condicionales te permiten tomar decisiones en tu código JavaScript. Permiten que tu programa fluya de una manera particular basada en ciertas condiciones.
- if toma una condición y ejecuta un bloque de código si esa condición es verdadera. Los valores verdaderos son aquellos que resultan en true cuando se evalúan en un contexto booleano. ejemplos de valores verdaderos: Cadenas de texto no vacías, por ejemplo, hello, cualquier número diferente de 0 y -0, por ejemplo, 4, -5 y otros, arrays, objetos, el booleano true.
-  los valores falsos son aquellos que se evalúan como false en un contexto booleano. JavaScript tiene pocos valores falsos, lo que los hace fáciles de recordar. Aquí hay unos pocos valores falsos: Booleano false, 0 (cero), "" (cadena vacía), null, undefined, NaN (No es un Número).
```js
if (null) {
  console.log("This will not run.");
}

if ("freeCodeCamp") {
  console.log("This will run.");
}
```
- Dado que null es un valor falso, el mensaje dentro del bloque nunca se registrará en la consola. Pero para la segunda declaración if, la cadena freeCodeCamp es un valor verdadero y se considerará true en este contexto booleano de la declaración if. Como resultado, el mensaje se registrará.
- Aquí hay un ejemplo de usar una declaración if para verificar si el usuario es elegible para votar:
```js
const age = 22;
if (age >= 18) {
 console.log("You're eligible to vote"); // You're eligible to vote
}
else {
 console.log("You're not eligible to vote"); // You're not eligible to vote
}
```
- Cuando una condición es false, entonces puedes usar una cláusula else.
- Si deseas verificar múltiples condiciones, puedes usar un bloque else if. Esto le permite a tu programa elegir entre más de dos caminos.
```js
const score = 87;

if (score >= 90) {
 console.log('You got an A'); 
} else if (score >= 80) {
 console.log('You got a B'); // You got a B
} else if (score >= 70) {
 console.log('You got a C');
} else {
 console.log('You failed! You need to study more!');
}
```
- El operador ternario es una forma compacta de escribir sentencias simples de if/else. Tiene tres partes: una condición, un resultado si la condición es verdadera y un resultado si es falsa. Aquí está la sintaxis básica: condition ? expressionIfTrue : expressionIfFalse;
- Aquí hay un ejemplo que trata con temperaturas del clima en Celsius:
```js
const temperature = 30;
const weather = temperature > 25 ? 'sunny' : 'cool';
console.log(`It's a ${weather} day!`);
```
- Entonces, ¿cuál deberías usar entre una declaración if y un operador ternario? Usa un operador ternario al tratar con una sola condición o expresión, o cuando deseas una sintaxis compacta para lógica simple. Usa declaraciones if/else cuando estás tratando con condiciones complejas y múltiples sentencias, ya que las cosas se vuelven ilegibles si anidas ternarios. 
---
### ¿Cuáles son los operadores lógicos binarios, y cómo funcionan?:
- ayudan a evaluar dos expresiones y devuelven un resultado basado en su veracidad.
- The logical AND operator is represented by a double ampersand (&&). Verifica si ambos operandos son verdaderos y devuelve un resultado. Si ambos operandos son truthy, devuelve el segundo valor, es decir, el de la derecha:
```js
const result = true && 'hello';
console.log(result); // hello
```
- En el ejemplo anterior, el texto hello se registra en la consola porque ambos operandos son true. Si cualquiera de los operandos es falsy, devuelve el valor falsy:
```js
const result = 0 && 3;
console.log(result); // 0
```
- Dado que 0 es un valor falsy, el número 0 se registra en la consola. Y si ambos operandos son falsy, devuelve el primer valor falsy, Dado que false es un valor falsy, entonces false se registra en la consola
```js
const result = false && 0;
console.log(result); // false
```
- El operador AND lógico es útil cuando deseas verificar múltiples condiciones y asegurarte de que todas sean verdaderas antes de continuar.
```js
if (2 < 3 && 3 < 4) {
 console.log('The if block runs'); 
} else {
 console.log('The else block runs');
}
```
- El operador lógico OR verifica si al menos uno de los operandos es verdadero. Si el primer operando es verdadero, devuelve ese valor:
```js
const result = 'This is truthy' || false;
console.log(result); // This is truthy
```
- Si el primer operando es falsy pero el segundo es truthy, el segundo valor se registrará en la consola:
```js
const result = 0 || 'This is truthy';
console.log(result); // This is truthy
```
- Es común usar el operador OR lógico dentro de sentencias if/else como esta:
```js
let userInput;
if (userInput || 'guest') {
 console.log('A user is present');
} else {
 console.log('No user detected');
}
```
- Como no asignamos un valor a la variable userInput, actualmente es undefined. La condición en la sentencia if revisa si la variable userInput o la cadena Guest son truthy. Dado que la cadena Guest es verdadera en un contexto booleano como este, la cadena se registrará en la consola.
- El operador de fusión nula es más sofisticado que el OR lógico y el AND lógico. Representado por un doble signo de interrogación (??), ayuda en escenarios donde quieres devolver un valor solo si el primero es null o undefined.
```js
const result = null ?? 'default';
console.log(result); // default
```
-  El operador de fusión nula es increíblemente útil en situaciones donde null o undefined son los únicos valores que deben activar un valor de reserva o por defecto.
- Aquí hay un ejemplo de cómo manejar las configuraciones de preferencias de un usuario:
```js
const userSettings = {
 theme: null,
 volume: 0,
 notifications: false,
};
let theme = userSettings.theme ?? 'light';
console.log(theme); // light
```
- En el ejemplo anterior, tenemos un objeto llamado userSettings que contiene las propiedades theme, volume y notifications. Estamos accediendo al theme utilizando la notación de punto como userSettings.theme. Como el theme del usuario actualmente se establece en null, entonces la cadena light se registrará en la consola.
---
### ¿Qué es el objeto Math en JavaScript y cuáles son algunos métodos comunes?:
- Esta herramienta útil proporciona una variedad de métodos que facilitan realizar cálculos avanzados y manipular números.
- El método Math.random() genera un número flotante aleatorio entre 0 (incluido) y 1 (excluido). Esto significa que el resultado posible puede ser 0, pero nunca llegará a 1.
```js
const randomNum = Math.random();
console.log(randomNum); // any number between 0 and 1 – 0 inclusive and 1 exclusive
```
- Math.min() y Math.max() toman un conjunto de números y devuelven el valor mínimo y máximo, respectivamente.
```js
const smallest = Math.min(1, 5, 3, 9);
console.log(smallest); // 1
const largest = Math.max(1, 5, 3, 9);
console.log(largest); // 9
```
- La primera console.log() registrará el número 1, ya que 1 es el menor en esa lista de números. Y el segundo console.log() registrará el número 9, ya que 9 es el mayor número en esa lista.
- Si quieres redondear números hacia arriba o hacia abajo al entero más cercano, puedes usar los métodos Math.ceil() y Math.floor(). 
```js
console.log(Math.ceil(4.3)); // 5
```
- Math.ceil() redondeará 4.3 hacia arriba al entero más cercano, que es 5 en este caso.
- Math.floor() redondeará 4.7 hacia abajo al entero más cercano, que en este caso es 4.
 ```js
console.log(Math.floor(4.7)); // 4
```
- Math.round() es la estructura híbrida de Math.ceil() y Math.floor(). Redondea un número a su entero más cercano, tomando en cuenta el punto decimal:
```js
console.log(Math.round(2.3)); // 2
console.log(Math.round(4.5)); // 5
console.log(Math.round(4.8)); // 5
```
- Entonces, si el punto decimal es menor que 5, el número se redondea hacia abajo. Y si el punto decimal es 5 o mayor, el número se redondea hacia arriba. Un uso práctico de Math.floor() y Math.random() es generar un número aleatorio entre dos números enteros.
```js
const max = 10;
const min = 5;
const randomNum = Math.floor(Math.random() * (max - min + 1)) + min;
console.log(randomNum);
```
```js
const randomNumBtw1And20 = Math.floor(Math.random() * 20) + 1;
console.log(randomNumBtw1And20); //Generar un número aleatorio entre 20 y 1 se vería así:
```
- Otro método útil de Math sería el método Math.trunc(). Math.trunc() elimina la parte decimal de un número, devolviendo solo la porción entera, sin redondear:
```js
console.log(Math.trunc(2.9)); // 2
console.log(Math.trunc(9.1)); // 9
```
- Si necesitas obtener la raíz cuadrada o cúbica de un número, puedes usar los métodos Math.sqrt() y Math.cbrt(), respectivamente.
```js
console.log(Math.sqrt(81)); // 9 // raíz cuadrada
console.log(Math.cbrt(27)); // 3 // raíz cubica
```
- La primera declaración de registro mostrará 9 porque la raíz cuadrada de 81 es 9, mientras que la segunda declaración de registro mostrará 3 porque la raíz cúbica de 27 es 3. 
- Si necesitas obtener el valor absoluto de un número, puedes usar el método Math.abs():
```js
console.log(Math.abs(-5)); // 5
console.log(Math.abs(5)); // 5 //Math.abs() devuelve el valor absoluto de un número, convirtiendo negativos en positivos. 
```
- Math.pow() toma dos números y eleva el primero a la potencia del segundo. Hay muchos más métodos que pertenecen al objeto Math que puedes explorar por tu cuenta.
```js
console.log(Math.pow(2, 3)); // 8
console.log(Math.pow(8, 2)); // 64
```
- La fórmula para generar un número aleatorio entre dos valores es la siguiente:
```js
Math.random() * (maximum - minimum) + minimum;
```
- La fórmula para generar un entero aleatorio entre dos valores es la siguiente:
```js
Math.floor(Math.random() * (maximum - minimum) + minimum);
```
---
#### MathBot:
```js
const botName = "MathBot";
const greeting = `Hi there! My name is ${botName} and I am here to teach you about the Math object!`;
console.log(greeting);
console.log("The Math.random() method returns a pseudo random number greater than or equal to 0 and less than 1.");
const randomNum = Math.random();
console.log(randomNum);
console.log("Now, generate a random number between two values.");
const min = 1;
const max = 100;
const randomNum2 = Math.random() * (max - min) + min;
console.log(randomNum2);
console.log("The Math.floor() method rounds the value down to the nearest whole integer.");
const numRoundedDown = Math.floor(6.7);
console.log(numRoundedDown);
console.log("Now, generate a random integer between two values.");
const randomInt = Math.floor(Math.random() * (max - min) + min);
console.log(randomInt);
console.log("The Math.ceil() method rounds the value up to the nearest whole integer.");
const numRoundedUp = Math.ceil(3.2);
console.log(numRoundedUp);
console.log("The Math.round() method rounds the value to the nearest whole integer.");
const numRounded = Math.round(2.7);
console.log(numRounded);
const numRounded2 = Math.round(11.2);
console.log(numRounded2);
console.log("The Math.max() and Math.min() methods are used to get the maximum and minimum number from a range.");
const maxNum = Math.max(3, 125, 55, 24);
console.log(maxNum);
const minNum = Math.min(6, 90, 14, 90, 2);
console.log(minNum);
console.log("It was fun learning about the different Math methods with you!");
```
---
### ¿Cómo funciona isNaN?
- NaN significa "Not a Number". Es un valor especial que representa un resultado numérico no representable o indefinido. NaN es una propiedad del objeto global, y también se considera un tipo de número en JavaScript, lo cual puede parecer contradictorio al principio. NaN es típicamente el resultado de operaciones que deberían retornar un número pero no pueden producir un valor numérico significativo.
- dividir cero por cero es matemáticamente indefinido, así que JavaScript devuelve NaN. Una propiedad peculiar de NaN es que no es igual a nada, incluyendo a sí mismo:
```js
console.log(NaN === NaN); // false
```
- Este comportamiento único dificulta verificar si un valor es NaN usando operadores de comparación estándar. Para abordar esto, JavaScript proporciona la función isNaN(). La propiedad de la función isNaN() se usa para determinar si un valor es NaN o no. A veces puede producir resultados inesperados.
```js
console.log(isNaN(NaN));       // true
console.log(isNaN(undefined)); // true
console.log(isNaN({}));        // true
console.log(isNaN(true));      // false
console.log(isNaN(null));      // false
console.log(isNaN(37));        // false
console.log(isNaN("37"));      // false: "37" is converted to 37
console.log(isNaN("37.37"));   // false: "37.37" is converted to 37.37
console.log(isNaN(""));        // false: empty string is converted to 0
console.log(isNaN(" "));       // false: string with a space is converted to 0
console.log(isNaN("blabla"));  // true: "blabla" is not a number
```
- isNaN() primero intenta convertir el parámetro a un número. Si no puede convertirse, devuelve true. Este comportamiento puede llevar a resultados sorprendentes, especialmente cuando se trabajan con cadenas que pueden coercionarse en números.
- Number.isNaN(). Este método no intenta convertir el parámetro a un número antes de probar. Sólo devuelve true si el valor es exactamente NaN:
```js
console.log(Number.isNaN(NaN));        // true
console.log(Number.isNaN(Number.NaN)); // true
console.log(Number.isNaN(0 / 0));      // true
console.log(Number.isNaN("NaN"));      // false
console.log(Number.isNaN(undefined));  // false
console.log(Number.isNaN({}));         // false
console.log(Number.isNaN("blabla"));   // false
```
- Number.isNaN() proporciona una manera más confiable de verificar valores NaN, especialmente en casos donde la coerción de tipos podría llevar a resultados inesperados con la función global isNaN(). En la práctica, cuando se trabaja con operaciones numéricas o entradas de usuario que deberían ser números, a menudo es necesario verificar NaN para manejar errores o entradas inesperadas de manera adecuada.
```js
let a = 0;
let b = 0;
let result = a / b;
if (Number.isNaN(result)) {
  result = "Error: Division resulted in NaN";
}
console.log(result); // "Error: Division resulted in NaN"
```
- estamos usando Number.isNaN() para detectar casos donde la operación de división resulta en NaN, permitiéndonos manejar este escenario de manera apropiada. Entender NaN y cómo verificarlo correctamente es crucial para escribir un código en JavaScript robusto, especialmente al tratar con operaciones matemáticas o analizar entradas de usuario.
---
###  ¿Cómo funcionan los métodos parseFloat() y parseInt()?
-  son dos métodos esenciales en JavaScript para convertir cadenas en números. Estos métodos son particularmente útiles al trabajar con entrada de usuario o procesar datos que llegan en formato de cadena pero necesitan ser tratados como valores numéricos.
- parseFloat(): Analiza un argumento de cadena y devuelve un número de punto flotante. Está diseñado para extraer un número del comienzo de una cadena, incluso si la cadena contiene caracteres no numéricos más adelante. Recuerda que los floats son números con puntos decimales. 
```js
console.log(parseFloat("3.14"));     // 3.14
console.log(parseFloat("3.14 abc")); // 3.14
console.log(parseFloat("3.14.5"));   // 3.14
console.log(parseFloat("abc 3.14")); // NaN
```
- parseFloat() comienza desde el principio de la cadena y continúa hasta que encuentra un carácter que no puede ser parte de un número de punto flotante. Si no puede encontrar un número válido al inicio de la cadena, devuelve NaN.
- parseInt(), por otro lado, analiza un argumento de cadena y devuelve un entero. Al igual que parseFloat(), comienza desde el principio de la cadena, pero se detiene en el primer carácter que no es un dígito. 
```js
console.log(parseInt("42"));       // 42
console.log(parseInt("42px"));     // 42
console.log(parseInt("3.14"));     // 3
console.log(parseInt("abc123"));   // NaN
```
- parseInt() se detiene en el primer carácter que no es un dígito. Para números de punto flotante, solo devuelve la parte entera. Si no puede encontrar un entero válido al inicio de la cadena, devuelve NaN.
- Ambos métodos tienen algunos comportamientos dignos de mención. Ignoran los espacios en blanco al inicio, manejan signos más y menos al principio de la cadena
```js
console.log(parseFloat("    +3.14"));  // 3.14
console.log(parseInt("    -42"));      // -42
```
- vale la pena señalar que, aunque estos métodos son poderosos, tienen algunas limitaciones. Por ejemplo, no manejan todos los formatos numéricos, como la notación científica, directamente. Para necesidades más complejas de análisis, es posible que necesites usar técnicas o bibliotecas adicionales. En conclusión, parseFloat() y parseInt() son herramientas valiosas para convertir cadenas en números en JavaScript. Entender cómo funcionan y sus comportamientos específicos te permite manejar datos numéricos más efectivamente en tus aplicaciones, especialmente cuando trabajas con entradas de usuario o fuentes externas de datos.
---
### ¿Qué es el método toFixed() y cómo funciona?
- .toFixed(): es una función incorporada de JavaScript que formatea un número usando notación de punto fijo. Es particularmente útil cuando se necesita controlar el número de decimales en un número, especialmente para mostrar valores de moneda o al trabajar con mediciones precisas.
- se llama en un número y toma un argumento opcional, que es el número de dígitos que aparecerán después del punto decimal. Devuelve una representación en cadena del número con el número especificado de decimales.
```js
let num = 3.14159;
console.log(num.toFixed(2)); // "3.14"
```
- En este caso, estamos limitando el número de decimales a dos. Por lo tanto, 3.14159 se convierte en 3.14. Es importante notar que .toFixed() devuelve una cadena, no un número. Esto se debe a que el método está principalmente destinado a formatear números para mostrar, no para cálculos posteriores. Redondea el número al valor más cercano que se pueda representar con el número especificado de decimales. Redondea hacia arriba cuando el siguiente dígito es 5 o mayor, y redondea hacia abajo de otro modo. Si llamas a .toFixed() sin argumentos, por defecto tiene 0 decimales.
- puede ser particularmente útil al trabajar con cálculos financieros o mostrar precios:
```js
let price = 19.99;
let taxRate = 0.08;
let total = price + (price * taxRate);
console.log("Total: $" + total.toFixed(2)); // "Total: $21.59"
```
- En este ejemplo, .toFixed(2) asegura que el total siempre se muestre con dos decimales, lo cual es estándar para moneda en muchos países.
- En conclusión, el método .toFixed() es una herramienta poderosa para formatear números en JavaScript, particularmente cuando necesitas controlar la visualización de decimales. Aunque principalmente se utiliza para formatear salida, recuerde su comportamiento, especialmente cuando se necesitan cálculos precisos.
---
### ¿Cómo funcionan las comparaciones con los tipos de datos nulos y no definidos?
- null y undefined son dos tipos de datos distintos que representan la ausencia de un valor, pero se comportan de manera diferente en las comparaciones.
- Una variable es undefined cuando ha sido declarada pero no ha sido asignada un valor. Es el valor por defecto de variables no inicializadas y parámetros de función a los que no se les proporcionó un argumento.
- null, por otro lado, es un valor de asignación que representa una no-valía deliberada. A menudo se usa para indicar que una variable intencionalmente no tiene valor.
- Al comparar null y undefined usando el operador de igualdad (==), JavaScript realiza una coerción de tipos. Esto significa que intenta convertir los operandos al mismo tipo antes de realizar la comparación. En este caso, null y undefined se consideran iguales.
```js
console.log(null == undefined); // true
```
- al usar el operador de igualdad estricta (===), que verifica tanto el valor como el tipo sin realizar coerción de tipos, null y undefined no son iguales.
```js
console.log(null === undefined); // false
```
- Esta diferencia es importante tenerla en cuenta al escribir declaraciones condicionales o realizar verificaciones de igualdad en el código. Al comparar null o undefined con otros valores usando el operador de igualdad (==), el comportamiento puede ser inesperado.
```js
console.log(null == 0);  // false
console.log(null == ''); // false
console.log(undefined == 0); // false
console.log(undefined == ''); // false
```
- Estas comparaciones devuelven false porque null y undefined sólo son iguales entre sí (y consigo mismos) al usar el operador de igualdad. El comportamiento de null en otras comparaciones es particularmente complicado.
```js
console.log(null > 0);  // false
console.log(null == 0); // false
console.log(null >= 0); // true
```
- undefined, por otro lado, siempre se convierte en NaN en contextos numéricos, lo que hace que todas las comparaciones numéricas con undefined devuelvan false:
```js
console.log(undefined > 0);  // false
console.log(undefined < 0);  // false
console.log(undefined == 0); // false
```
- Dadas estas diferencias, generalmente se recomienda usar el operador de igualdad estricta al comparar valores, especialmente al tratar con null y undefined. Este enfoque ayuda a evitar coerciones de tipo inesperadas y hace que el comportamiento de su código sea más predecible. En resumen, aunque null y undefined se utilizan para representar la ausencia de un valor, se comportan de manera diferente en las comparaciones.
---
### ¿Qué son las sentencias de `switch` y cómo difieren de las cadenas de `if/else`?
- son ambas estructuras de control de flujo en programación que nos permiten ejecutar diferentes bloques de código en base a ciertas condiciones.
- switch evalúa una expresión y compara su valor con una serie de cláusulas case. Cuando se encuentra una coincidencia, se ejecuta el bloque de código asociado con ese case. sintaxis:
```js
switch (expression) {
  case value1:
    // code to be executed if expression === value1
    break;
  case value2:
    // code to be executed if expression === value2
    break;
  default:
    // code to be executed if expression doesn't match any case
}
```
- break al final de cada case es crucial. Informa al programa que debe salir del bloque switch una vez que se haya ejecutado un case coincidente. Sin ella, el programa continuaría ejecutando los casos subsiguientes, un comportamiento conocido como "fall-through".
- switch se utilizan por lo general cuando se está comparando una sola variable con múltiples valores posibles. Son especialmente útiles cuando se tienen muchas condiciones potenciales para verificar contra una sola variable. 
```js
let dayOfWeek = 3; 

switch (dayOfWeek) {
    case 1:
        console.log("It's Monday! Time to start the week strong.");
        break;
    case 2:
        console.log("It's Tuesday! Keep the momentum going.");
        break;
    case 3:
        console.log("It's Wednesday! We're halfway there.");
        break;
    case 4:
        console.log("It's Thursday! Almost the weekend.");
        break;
    case 5:
        console.log("It's Friday! The weekend is near.");
        break;
    case 6:
        console.log("It's Saturday! Enjoy your weekend.");
        break;
    case 7:
        console.log("It's Sunday! Rest and recharge.");
        break;
    default:
        console.log("Invalid day! Please enter a number between 1 and 7.");
}
```
- switch pueden ser más legibles y concisas al manejar muchos valores posibles para una sola variable. Las sentencias if/else if, por otro lado, son más flexibles. Pueden evaluar condiciones complejas y diferentes variables en cada cláusula. Esto las hace adecuadas para un rango más amplio de escenarios.
```js
let creditScore = 720; 
let annualIncome = 60000; 
let loanAmount = 200000; 

let eligibilityStatus;

if (creditScore >= 750 && annualIncome >= 80000) {
    eligibilityStatus = "Eligible for premium loan rates.";
} else if (creditScore >= 700 && annualIncome >= 50000) {
    eligibilityStatus = "Eligible for standard loan rates.";
} else if (creditScore >= 650 && annualIncome >= 40000) {
    eligibilityStatus = "Eligible for subprime loan rates.";
} else if (creditScore < 650) {
    eligibilityStatus = "Not eligible due to low credit score.";
} else {
    eligibilityStatus = "Not eligible due to insufficient income.";
}

console.log(eligibilityStatus);
```
- switch en JavaScript utilizan comparación estricta (===), lo que significa que no realizan conversión de tipos. Esto puede ser una ventaja en términos de previsibilidad y evitar errores sutiles.
- En resumen, aunque tanto las sentencias switch como las cadenas de if/else if permiten lógica de múltiples ramas en tu código, tienen diferentes fortalezas. Las sentencias switch sobresalen en manejar múltiples valores posibles para una sola variable, mientras que las cadenas de if/else if ofrecen más flexibilidad para condiciones complejas. La elección entre ellas suele depender de los requisitos específicos de tu código y de las preferencias personales o del equipo en el estilo de programación.
---
### ¿Cuál es el propósito de las funciones y cómo funcionan?
- son piezas reutilizables de código que realizan una tarea específica o calculan un valor. Piensa en las funciones como una máquina que toma una entrada, realiza algunas operaciones y luego produce una salida. sintaxis:
```js
function greet() {
  console.log("Hello, Jessica!");
}
```
- In this example, we have declared a function called greet. Inside that function, we have a console.log that logs the message Hello, Jessica!. Si intentamos ejecutar este código, no veríamos aparecer el mensaje en la consola.
- na llamada a función, o invocación, es cuando realmente usamos o ejecutamos la función. Para llamar a una función, necesitarás referenciar el nombre de la función seguido de un conjunto de paréntesis:
```js
function greet() {
  console.log("Hello, Jessica!");
}
greet(); // "Hello, Jessica!"
```
- Ahora el mensaje de Hello, Jessica! estará registrado en la consola. ¿Pero qué si quisiéramos que el mensaje dijera Hello, Nick! o Hello, Anna!? No queremos escribir una nueva función cada vez que saludamos a un usuario diferente. En su lugar, podemos crear una función reutilizable que use parámetros de función y argumentos.
- Los parámetros actúan como marcadores de posición para los valores que se pasarán a la función cuando se llame. Permiten que las funciones acepten entradas y trabajen con esa entrada. Los argumentos son los valores reales que se pasan a la función cuando se llama.
```js
function greet(name) {
  console.log("Hello, " + name + "!");
}
greet("Alice"); // Hello, Alice!
greet("Nick"); // Hello, Nick!
```
- El name sirve como el parámetro mientras que las cadenas Alice y Nick sirven como los argumentos. Ahora tenemos una función reutilizable que puede usarse docenas de veces en nuestro código con diferentes argumentos.
- Cuando una función termina su ejecución, siempre devolverá un valor. Por defecto, el valor de regreso será undefined.
```js
function doSomething() {
  console.log("Doing something...");
}
let result = doSomething();
console.log(result); // undefined
```
- Si necesitas que tu función devuelva un valor específico, entonces deberás usar la declaración return. Aquí tienes un ejemplo de uso de una declaración return para devolver la suma de dos valores:
```js
function calculateSum(num1, num2) {
  return num1 + num2;
}
console.log(calculateSum(3, 4)); // 7
```
- también puedes crear lo que se llama una función anónima. Una función anónima es una función sin nombre que puede asignarse a una variable de esta manera:
```js
const sum = function (num1, num2) {
  return num1 + num2;
};
console.log(sum(3, 4)); // 7
```
- En este ejemplo, tenemos una variable const llamada sum y le estamos asignando una función anónima que devuelve la suma de num1 y num2. Luego podemos llamar a sum y pasar los números 3 y 4 para obtener el resultado de 7.
- Las funciones admiten parámetros predeterminados, lo que te permite establecer valores predeterminados para los parámetros. Estos valores predeterminados se usan si la función se llama sin un argumento para ese parámetro. 
```js
function greetings(name = "Guest") {
  console.log("Hello, " + name + "!");
}
greetings(); // Hello, Guest!
greetings("Anna"); // Hello, Anna!
```
- En este ejemplo, si no se proporciona un argumento para nombre, se establece por defecto como Guest. En resumen, las funciones te permiten escribir un código reutilizable y organizado. Pueden recibir entradas (parámetros), realizar acciones y devolver salidas.
---
### ¿Qué son las funciones flecha y cómo funcionan?
- Funciones, son fragmentos reutilizables de código que ayudan a que tu código sea más modular, fácil de mantener y más eficiente. Todos los ejemplos anteriores usaron la sintaxis regular de funciones, así:
```js
function greetings(name) {
  console.log("Hello, " + name + "!");
}
```
- Otra forma de escribir funciones en JavaScript es crear una expresión de función flecha. sintaxis de función flecha:
```js
const greetings = (name) => {
  console.log("Hello, " + name + "!");
};
```
- En este ejemplo revisado, estamos creando una variable const llamada greetings y asignándole una función anónima. Si tu lista de parámetros solo tiene un parámetro, entonces puedes eliminar los paréntesis así:
```js
const greetings = name => {
  console.log("Hello, " + name + "!");
};
```
- Si tu función flecha no tiene parámetros, entonces debes usar los paréntesis así:
```js
const greetings = () => {
  console.log("Hello");
};
```
- Al aprender por primera vez sobre funciones, tenías que envolver el cuerpo de la función en llaves. Pero si el cuerpo de tu función solo contiene una línea de código, puedes eliminar las llaves así:
```js
const greetings = name => console.log("Hello, " + name + "!");
```
- Es importante observar que eliminar los paréntesis y llaves para la sintaxis regular de función no funcionará. Obtendrás errores si intentas hacer algo como esto:
```js
// This will produce syntax errors 
function greetings name console.log("Hello, " + name + "!");
```
- Este tipo de funciones de una línea solo funcionan si estás usando la sintaxis de función flecha. Otro concepto clave es la sentencia return. Aquí tienes un ejemplo de uso de la sintaxis de función flecha para calcular el área:
```js
const calculateArea = (width, height) => {
  const area = width * height;
  return area;
};
console.log(calculateArea(5, 3)); // 15
```
- Estamos creando una variable dentro de la función llamada area y luego devolvemos esa variable. Pero podríamos hacer nuestro código un poco más limpio y devolver el cálculo en sí mismo:
```js
const calculateArea = (width, height) => {
  return width * height;
}; 
console.log(calculateArea(5, 3)); // 15
```
- Si intentaste eliminar las llaves y colocar el cálculo en la misma línea, recibirías un mensaje Uncaught SyntaxError: Unexpected token 'return'.
- La razón por la que obtienes este error es porque necesitas eliminar la sentenciareturn. Cuando eliminas esa sentencia return.
- Entonces, ¿cuándo deberías usar la sintaxis de función flecha? Bueno, depende. Muchos desarrolladores la usan consistentemente en sus proyectos personales. Sin embargo, al trabajar en equipo, la elección generalmente depende de si la base de código existente usa funciones regulares o funciones flecha.
---
### ¿Qué es el alcance en la programación y cómo funcionan los alcances global, local y de bloque?
- Alcance: En programación se refiere a la visibilidad y accesibilidad de las variables en diferentes partes de tu código. Determina dónde se pueden acceder o modificar las variables. En JavaScript, comprender el alcance es crucial para escribir código limpio, eficiente y libre de errores. Hay tres tipos principales de alcance: alcance global, alcance local y alcance de bloque.
- Global: Es el alcance más externo en un programa JavaScript. Las variables declaradas en el alcance global son accesibles desde cualquier parte de tu código, incluidos dentro de funciones y bloques. Pueden ser convenientes, deben usarse con moderación ya que pueden llevar a conflictos de nombres y dificultar el mantenimiento de tu código. Ejemplo de una variable global:
```js
let globalVar = "I'm a global variable";
function printGlobalVar() {
    console.log(globalVar);
}
printGlobalVar(); // "I'm a global variable"
```
- En este ejemplo, globalVar se declara en el alcance global y se puede acceder dentro de la función printGlobalVar.
- El alcance local, por otro lado, se refiere a variables que solo son accesibles dentro de una función. Aquí hay un ejemplo de alcance local:
```js
function greet() {
    let message = "Hello, local scope!";
    console.log(message);
}
greet(); // "Hello, local scope!"
//console.log(message); // This will throw an error
```
- En este código, message es una variable local dentro de la función greet. Se puede usar dentro de la función, pero intentar acceder a ella fuera de la función resultará en un error.
- El alcance de bloque es un concepto introducido con las palabras clave let y const en ES6. Un bloque es cualquier sección de código dentro de llaves, {}, como en sentencias if, bucles for o bucles while.
- Las variables declaradas con let o const dentro de un bloque solo son accesibles dentro de ese bloque. Aquí hay un ejemplo de alcance de bloque:
```js
if (true) {
    let blockVar = "I'm in a block";
    console.log(blockVar); // "I'm in a block"
}
console.log(blockVar); // This will throw an error
```
- En este ejemplo, blockVar solo es accesible dentro del bloque if. Intentar acceder a ella fuera del bloque resultará en un error. Entender estos diferentes tipos de alcance es esencial para gestionar la accesibilidad de variables y evitar efectos secundarios no deseados en su código.
- Las variables globales deben usarse con moderación, ya que pueden llevar a conflictos de nombres y dificultar el mantenimiento de su código. Las variables locales ayudan a mantener diferentes partes del código aisladas, lo cual es especialmente útil en programas más grandes. El alcance de bloque con let y const proporciona un control aún más fino sobre la accesibilidad de las variables, ayudando a prevenir errores y haciendo que su código sea más predecible.
---
### ¿Cuáles son las características clave de los arrays en JavaScript?
- Un array en JavaScript es una colección ordenada de valores, cada uno identificado por un índice numérico. Los valores en un array de JavaScript pueden ser de diferentes tipos de datos, incluidos números, cadenas, booleanos, objetos e incluso otros arrays. 
- Para crear un array en JavaScript, puedes usar corchetes, [], y separar los valores con comas. Aquí tienes un ejemplo:
- Una de las características clave de los arrays es que están indexados desde cero, lo que significa que el primer elemento en un array tiene un índice de 0, el segundo elemento tiene un índice de 1, y así sucesivamente. Puedes acceder a elementos individuales en un array utilizando su índice. 
```js
let fruits = ["apple", "banana", "orange"];
console.log(fruits[0]); // "apple"
console.log(fruits[2]); // "orange"
```
- Los arrays en JavaScript tienen una propiedad especial length que devuelve el número de elementos en el array. Puedes acceder a esta propiedad utilizando la palabra clave length.
```js
let fruits = ["apple", "banana", "orange"];
console.log(fruits.length); // 3
```
- Otra característica clave de los arrays en JavaScript es que son dinámicos, lo que significa que su tamaño puede cambiar después de haber sido creados. Puedes agregar o eliminar elementos de un array usando varios métodos de array. Los arrays en JavaScript son versátiles y útiles cuando se trata de almacenamiento de datos dentro de tus programas. A lo largo de este módulo, verás de primera mano cómo trabajar con arrays te ayudará a gestionar y manipular eficazmente colecciones de datos.
---
### ¿Cómo se accede y se actualizan elementos en un arreglo?
- Es importante notar que si intentas acceder a un índice que no existe en el arreglo, JavaScript devolverá undefined.
```js
let fruits = ["apple", "banana", "cherry"];
console.log(fruits[3]); // undefined
```
- Puedes actualizar un elemento asignando un nuevo valor a un índice específico.
```js
let fruits = ["apple", "banana", "cherry"];
fruits[1] = "blueberry";
console.log(fruits); // ["apple", "blueberry", "cherry"]
```
- En este ejemplo, hemos reemplazado banana con blueberry en el índice 1. Este método te permite cambiar cualquier elemento en el arreglo, siempre y cuando conozcas su índice. También puedes añadir nuevos elementos a un arreglo asignando un valor a un índice que aún no existe:
```js
let fruits = ["apple", "banana", "cherry"];
fruits[3] = "date";
console.log(fruits); // ["apple", "banana", "cherry", "date"]
```
- Sin embargo, ten cuidado al hacer esto. Si asignas un valor a un índice que es mucho más grande que la longitud actual del arreglo, crearás elementos indefinidos para los índices intermedios, lo que puede llevar a un comportamiento inesperado. A medida que continúes trabajando con JavaScript, encontrarás que estas formas de acceder y actualizar elementos de un arreglo son fundamentales para muchas tareas de programación. Ya sea que estés construyendo una lista de tareas simple o procesando estructuras de datos complejas, estas habilidades serán invaluables.
---
### ¿Cómo añades y eliminas elementos desde el principio y el final de un array?
- Hay cuatro métodos principales para añadir y eliminar elementos desde el principio y el final de un array: push(), pop(), shift() y unshift().
- push(): se utiliza para añadir uno o más elementos al final de un array. El valor de retorno para el método push() es la nueva longitud del array.
```js
const fruits = ["apple", "banana"];
const newLength = fruits.push("orange");
console.log(newLength); // 3
console.log(fruits); // ["apple", "banana", "orange"]
```
- comenzamos con un array llamado fruits que contiene dos elementos. Luego utilizamos el método push() para añadir la cadena orange al final del array.
- Quizás hayas notado que estamos utilizando const al declarar el array fruits. Pero, ¿por qué es posible añadir más elementos a este array fruits cuando fruits es una constante? Esto es posible porque declarar un array con la palabra clave const crea una referencia al array. Mientras que el array en sí es mutable y puede ser modificado, no puedes reasignar un nuevo valor a la constante fruits, así:
```js
const fruits = ["apple", "banana"];
fruits = ["This", "will", "not", "work"];
console.log(fruits); // Uncaught TypeError: Assignment to constant variable. 
```
- pop(): elimina el último elemento de un array y devuelve ese elemento. También modifica el array original.
```js
let fruits = ["apple", "banana", "orange"];
let lastFruit = fruits.pop();
console.log(fruits); // ["apple", "banana"]
console.log(lastFruit); // "orange"
```
- comenzamos con un array de tres frutas. El método pop() elimina el último elemento (orange) del array y lo devuelve. El array fruits original es modificado y contiene solamente dos elementos.
- unshift(): añade uno o más elementos al principio de un array y devuelve su nueva longitud. Funciona de manera similar a push(), pero modifica el inicio del array en lugar del final. 
```js
let numbers = [2, 3];
let newLength = numbers.unshift(1);
console.log(numbers); // [1, 2, 3]
console.log(newLength); // 3
```
- utilizamos unshift() para añadir el número 1 al principio del array numbers. El método devuelve la nueva longitud del array, que es 3.
- shift(): elimina el primer elemento de un array y devuelve ese elemento. Es similar a pop(), pero funciona al inicio del array en lugar del final.
```js
let colors = ["red", "green", "blue"];
let firstColor = colors.shift();
console.log(colors); // ["green", "blue"]
console.log(firstColor); // "red"
```
- comenzamos con un array de tres colores. El método shift() elimina el primer elemento (red) del array y lo devuelve. El array colors original se modifica para contener solamente dos elementos.
- Observa que mientras push() y unshift() pueden añadir múltiples elementos a la vez, pop() y shift() eliminan solo un elemento a la vez.
---
### ¿Cuál es la diferencia entre arreglos unidimensionales y bidimensionales?
- En programación, los arreglos son estructuras de datos fundamentales usadas para almacenar colecciones de elementos.
-  arreglo unidimensional, a menudo llamado simplemente arreglo, es como una sola fila de cajas. Imagina que tienes una fila de casilleros en una estación de tren. Cada casillero puede contener un elemento, y puedes acceder a cualquier casillero directamente si conoces su número.
-  cada elemento en un arreglo unidimensional se accede usando un solo índice. Por ejemplo, podrías crear y usar un arreglo unidimensional así:
```js
12
let fruits = ["apple", "banana", "cherry", "date"];
console.log(fruits[2]); // "cherry"
```
- arreglos bidimensionales: Si un arreglo unidimensional es como una sola fila de casilleros, un arreglo bidimensional es como una cuadrícula de casilleros: múltiples filas y columnas. En programación, un arreglo bidimensional es esencialmente un arreglo de arreglos. Se usa para representar datos que tienen una estructura natural en forma de cuadrícula, como un tablero de ajedrez, una hoja de cálculo o los píxeles de una imagen.
- Para acceder a un elemento en un arreglo bidimensional, necesitas dos índices: uno para la fila y otro para la columna. 
```js
let chessboard = [
    ["R", "N", "B", "Q", "K", "B", "N", "R"],
    ["P", "P", "P", "P", "P", "P", "P", "P"],
    [" ", " ", " ", " ", " ", " ", " ", " "],
    [" ", " ", " ", " ", " ", " ", " ", " "],
    [" ", " ", " ", " ", " ", " ", " ", " "],
    [" ", " ", " ", " ", " ", " ", " ", " "],
    ["p", "p", "p", "p", "p", "p", "p", "p"],
    ["r", "n", "b", "q", "k", "b", "n", "r"]
];
console.log(chessboard[0][3]); // "Q"
```
-  El primer índice, 0, selecciona la primera fila, y el segundo índice, 3, selecciona la cuarta columna de esa fila.
- La diferencia clave entre arreglos unidimensionales y bidimensionales radica en cómo accedes y organizas los datos. Los arreglos unidimensionales usan un solo índice y son adecuados para datos lineales como listas o secuencias. Los arreglos bidimensionales usan dos índices y son ideales para estructuras de datos en forma de cuadrícula.
- Vale la pena señalar que en JavaScript, los arreglos bidimensionales son en realidad arreglos de arreglos. Esto significa que cada elemento del arreglo externo es en sí mismo un arreglo. Esta estructura anidada permite una gran flexibilidad pero también requiere un manejo cuidadoso para evitar errores. A medida que avanzas en tu viaje de programación, descubrirás que elegir entre arreglos unidimensionales y bidimensionales depende de la naturaleza de tus datos y de cómo necesitas manipularlos.
- Los arreglos unidimensionales son más simples y suficientes para muchas tareas, mientras que los arreglos bidimensionales se vuelven invaluables cuando se trabaja con datos más complejos y estructurados.
---
### ¿Qué es la desestructuración de arreglos y cómo funciona?
- La desestructuración de arreglos es una característica en JavaScript que permite extraer valores de arreglos y asignarlos a variables de una manera más concisa y legible. Proporciona una sintaxis conveniente para desempaquetar elementos de un arreglo en variables distintas. Esta técnica es particularmente útil al trabajar con arreglos y funciones que devuelven múltiples valores. Desestructuración de arreglos:
```js
let fruits = ["apple", "banana", "orange"];
let [first, second, third] = fruits;
console.log(first);  // "apple"
console.log(second); // "banana"
console.log(third);  // "orange"
```
- En este ejemplo, tenemos un arreglo llamado frutas con tres elementos. Usando la desestructuración de arreglos, asignamos el primer elemento a la variable primero, el segundo elemento a segundo, y el tercer elemento a tercero. Esto nos permite acceder fácilmente a elementos individuales del arreglo sin usar notación de índice.
- La desestructuración de arreglos también te permite omitir elementos en los que no estás interesado usando comas.
```js
let colors = ["red", "green", "blue", "yellow"];
let [firstColor, , thirdColor] = colors;
console.log(firstColor); // "red"
console.log(thirdColor); // "blue"
```
- En este ejemplo, omitimos el segundo elemento del arreglo colores usando una coma extra. Esto asigna rojo a primerColor y azul a tercerColor, efectivamente ignorando verde.
- Otra poderosa característica de la desestructuración de arreglos es la capacidad de usar valores por defecto. Si el arreglo tiene menos elementos de los que intentas asignar a las variables, puedes proporcionar valores por defecto:
```js
let numbers = [1, 2];
let [a, b, c = 3] = numbers;
console.log(a); // 1
console.log(b); // 2
console.log(c); // 3 Aquí, asignamos el valor por defecto 3 a c porque el arreglo números no tiene un tercer elemento.
```
- Ahora vamos a discutir sobre la sintaxis de resto, denotada por tres puntos (...). Te permite capturar los elementos restantes de un arreglo que no han sido desestructurados en un nuevo arreglo.
```js
let fruits = ["apple", "banana", "orange", "mango", "kiwi"];
let [first, second, ...rest] = fruits;
console.log(first);  // "apple"
console.log(second); // "banana"
console.log(rest);   // ["orange", "mango", "kiwi"]
```
- primero y segundo capturan los primeros dos elementos del arreglo frutas, y resto captura todos los elementos restantes como un nuevo arreglo. La sintaxis de resto debe ser el último elemento en el patrón de desestructuración.
- La desestructuración de arreglos es una característica poderosa que puede hacer tu código más conciso y fácil de leer. Es especialmente útil al trabajar con arreglos, y cuando necesitas extraer elementos específicos de un arreglo.
---
### ¿Cómo puedes utilizar métodos de cadenas y matrices para invertir una cadena?
- Invertir una cadena es una tarea común de programación que se puede lograr en JavaScript usando una combinación de métodos de cadena y matriz. El proceso involucra tres pasos principales: Dividir la cadena en un arreglo de caracteres, Invertir el arreglo, Unir de nuevo los caracteres en una cadena. Exploremos cada uno de estos pasos usando los métodos split(), reverse(), y join().
- El primer paso para invertir una cadena es convertirla en un arreglo de caracteres individuales. Podemos hacerlo usando el método split() que divide una cadena en un arreglo de subcadenas y especifica dónde debe ocurrir cada división según un separador dado. Si no se proporciona un separador, el método devuelve un arreglo que contiene la cadena original como un único elemento. Ejemplos de separadores comunes incluyen: Una cadena vacía (""), que divide la cadena en caracteres individuales, Un espacio único (" "), que divide la cadena donde ocurren los espacios, Un guion ("-"), que divide la cadena en cada guion.
```js
//metodo split
let str = "hello";
let charArray = str.split("");
console.log(charArray); // ["h", "e", "l", "l", "o"]
```
- En este ejemplo, usamos split("") (con una cadena vacía) para convertir la cadena hello en un arreglo de sus caracteres individuales. Una vez que tenemos un arreglo de caracteres, podemos usar el método reverse() para invertir el orden de los elementos en el arreglo.
- reverse(): es un método de arreglo que invierte un arreglo en su lugar. Esto significa que modifica el arreglo original en lugar de crear uno nuevo. 
```js
let charArray = ["h", "e", "l", "l", "o"];
charArray.reverse();
console.log(charArray); // ["o", "l", "l", "e", "h"]
```
- reverse() cambia el orden de los elementos en charArray, invirtiéndolo de ["h", "e", "l", "l", "o"] a ["o", "l", "l", "e", "h"].
- El paso final es convertir el arreglo invertido de caracteres de nuevo en una cadena. Podemos lograr esto usando el método join(). El método join() crea y devuelve una nueva cadena al concatenar todos los elementos de un arreglo, separados por un separador de cadena especificado. Si deseas unir los caracteres sin ningún separador, puedes usar una cadena vacía como argumento.
```js
let reversedArray = ["o", "l", "l", "e", "h"];
let reversedString = reversedArray.join("");
console.log(reversedString); // "olleh"
```
- join("") (con una cadena vacía como argumento) combina todos los caracteres en el arreglo en una sola cadena sin ningún separador entre ellos.
- Recuerda que las cadenas en JavaScript son inmutables, lo que significa que no puedes invertir una cadena directamente modificándola. Es por eso que necesitamos convertirla en un arreglo, invertir el arreglo, y luego convertirla de nuevo en una cadena. Esta combinación de métodos de cadenas y matrices proporciona una manera potente y flexible de manipular cadenas en JavaScript.
- ejemplo de todo junto:
```js
let str = "coding";
let reversed = str.split("").reverse().join("");
console.log(reversed); //"gnidoc"
```
- 