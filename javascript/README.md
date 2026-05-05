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
## ¿Cuál es el propósito de las funciones y cómo funcionan?
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
## ¿Cuáles son las características clave de los arrays en JavaScript?
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
---
### ¿Cómo obtener el índice de un elemento en un arreglo usando el método `indexOf`?
- indexOf() es útil para encontrar el primer índice de un elemento específico dentro de un arreglo. Si no se puede encontrar el elemento, entonces devolverá -1. Esta es la sintaxis básica:
```js
array.indexOf(element, fromIndex)
```
element representa el valor que quieres buscar dentro del arreglo, y el parámetro fromIndex es la posición desde la cual debe empezar la búsqueda. El parámetro fromIndex es opcional. Si no se proporciona fromIndex, la búsqueda comienza desde el inicio del arreglo. 
```js
let fruits = ["apple", "banana", "orange", "banana"];
let index = fruits.indexOf("banana");
console.log(index); // 1
```
- En este ejemplo, tenemos un arreglo fruits que contiene varios nombres de frutas. Usamos el método indexOf() para encontrar el índice de la cadena banana dentro del arreglo fruits. Dado que banana está presente en el índice 1, el método devuelve 1, que se almacena en la variable index y se registra en la consola. Si el elemento que buscas no se encuentra en el arreglo, indexOf() devuelve -1.
- Si deseas comenzar a buscar un elemento después de un número de índice específico, puedes pasar un segundo argumento como en este ejemplo:
```js
let colors = ["red", "green", "blue", "yellow", "green"];
let index = colors.indexOf("green", 3);
console.log(index); // 4
```
- En este ejemplo, la búsqueda no comienza desde el inicio de un arreglo, sino desde el número de índice 3, que es yellow y obtiene el resultado de 4.
---
###  ¿Cómo se agregan y eliminan elementos del medio de un arreglo?
- El método splice() en JavaScript es una forma poderosa de modificar arreglos. Permite agregar o eliminar elementos de cualquier posición en un arreglo, incluido el medio. El valor de retorno para el método splice() será un arreglo de los elementos eliminados del arreglo. Si no se eliminó nada, entonces se devolverá un arreglo vacío.
- Es importante notar que este método mutará el arreglo original, modificándolo en el lugar en lugar de crear un nuevo arreglo. Esto es algo que tener en cuenta al trabajar con splice(). Esta es la sintáxis básica:
```js
array.splice(startIndex, itemsToRemove, item1, item2)
```
- startIndex especifica el índice en el que comenzar a modificar el arreglo, mientras que itemsToRemove es un parámetro opcional que indica cuántos elementos eliminar. Si itemsToRemove se omite, splice() eliminará todos los elementos del startIndex hasta el final del arreglo. Los parámetros subsecuentes (item1, item2, etc.) son los elementos a añadir al arreglo, comenzando en el índice de inicio.
- Comencemos con un ejemplo de eliminación de elementos del medio de un arreglo:
``js
let fruits = ["apple", "banana", "orange", "mango", "kiwi"];
let removed = fruits.splice(2, 2);
console.log(fruits);  // ["apple", "banana", "kiwi"]
console.log(removed); // ["orange", "mango"]
```
- En este ejemplo, splice(2, 2) comienza en el índice 2 y elimina 2 elementos. El arreglo modificado ahora consistirá de solo manzana, plátano y kiwi. Ahora veamos cómo agregar elementos al medio de un arreglo:
```js
let colors = ["red", "green", "blue"];
colors.splice(1, 0, "yellow", "purple");
console.log(colors); // ["red", "yellow", "purple", "green", "blue"]
```
- Aquí, splice(1, 0, "amarillo", "morado") comienza en el índice 1, elimina 0 elementos e inserta amarillo y morado. El segundo parámetro (0) indica que no se eliminan elementos antes de la inserción. También puedes usar splice() para eliminar y agregar elementos simultáneamente:
```js
let numbers = [1, 2, 3, 4, 5];
numbers.splice(1, 2, 6, 7, 8);
console.log(numbers); // [1, 6, 7, 8, 4, 5]
```
- En este caso, splice(1, 2, 6, 7, 8) comienza en el índice 1, elimina 2 elementos (2 y 3) e inserta 6, 7 y 8. Si necesitas mantener el arreglo original sin cambios, debes crear una copia antes de usar splice():
```js
let original = [1, 2, 3, 4, 5];
let copy = [...original];
copy.splice(2, 1, 6);
console.log(original); // [1, 2, 3, 4, 5]
console.log(copy);     // [1, 2, 6, 4, 5]
```
- Cuando usamos copy.splice(2, 1, 6), modifica el arreglo copia eliminando el elemento en el índice 2 (que es 3) e insertando el nuevo elemento 6 en esa posición.
- Un caso de uso común para splice() es eliminar un solo elemento de un arreglo cuando conoces su índice:
```js
let fruits = ["apple", "banana", "orange", "mango"];
let indexToRemove = fruits.indexOf("orange");
if (indexToRemove !== -1) {
    fruits.splice(indexToRemove, 1);
}
console.log(fruits); // ["apple", "banana", "mango"]
```
- En este ejemplo, primero usamos el método indexOf() para encontrar el índice del elemento naranja en el arreglo frutas. El método indexOf() devuelve el índice de la primera aparición del elemento dado o -1 si el elemento no se encuentra en el arreglo.Luego comparamos indexToRemove con -1 para asegurarnos de que el elemento existe en el arreglo antes de intentar eliminarlo. Si indexToRemove no es igual a -1 (lo que significa que se encontró el elemento), usamos splice() para eliminar un elemento comenzando desde la posición indexToRemove.
- También puedes usar splice() para vaciar un arreglo eliminando todos los elementos:
```js
let array = [1, 2, 3, 4, 5];
array.splice(0);
console.log(array); // []
```
- Aunque splice() es poderoso, vale la pena señalar que para arreglos muy grandes, puede ser menos eficiente que otros métodos, especialmente al modificar el inicio del arreglo. Esto se debe a que splice() podría necesitar desplazar todos los elementos posteriores. En tales casos, si solo estás añadiendo o eliminando elementos al final del arreglo, métodos como push(), pop(), unshift() y shift() podrían ser más apropiados.
- En conclusión, el método splice() es una forma versátil de modificar arreglos en JavaScript. Permite un control preciso sobre la adición y eliminación de elementos de cualquier posición en un arreglo. Comprender cómo usar splice() eficazmente puede mejorar en gran medida tu capacidad para manipular arreglos en tu código JavaScript.
---
### ¿Cómo puedes verificar si un arreglo contiene un cierto valor?
- el método includes() es una forma simple y eficiente de verificar si un arreglo contiene un valor específico. Este método devuelve un valor booleano: true si el arreglo contiene el elemento especificado, y false en caso contrario.
- El método includes() es particularmente útil cuando necesitas verificar rápidamente la presencia de un elemento en un arreglo sin necesidad de conocer su posición exacta. Comencemos con un ejemplo de cómo usar el método includes():
```js
let fruits = ["apple", "banana", "orange", "mango"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("grape"));  // false
```
- includes() distingue entre mayúsculas y minúsculas cuando se trata de cadenas. Esto significa que Banana con una B mayúscula y banana con todas las letras en minúscula se consideran valores diferentes.
```js
let fruits = ["apple", "banana", "orange"];
console.log(fruits.includes("banana")); // true
console.log(fruits.includes("Banana")); // false
```
- includes() también puede aceptar un segundo parámetro opcional que especifica la posición en el arreglo para iniciar la búsqueda. Esto es útil si quieres verificar la presencia de un elemento en una parte específica del arreglo.
```js
let numbers = [10, 20, 30, 40, 50, 30, 60];
console.log(numbers.includes(30, 3)); // true
console.log(numbers.includes(30, 4)); // true
```
- Para el primer console.log, estamos buscando el número 30 comenzando en el índice 3. En este caso, hay un número 30 que aparece después del índice 3, por lo que el método includes() devuelve true.
- Lo mismo sucede con el segundo console.log. Estamos buscando el número 30 comenzando en el índice 4. Dado que el número 30 aparece después de ese índice, retornará true.
- Vale la pena señalar que includes() usa la comparación de igualdad estricta (===), lo que significa que puede distinguir entre diferentes tipos.
```js
let mixedArray = [1, "2", 3, "4", 5];
console.log(mixedArray.includes(2));  // false
console.log(mixedArray.includes("2")); // true
```
- En este caso, el número 2 y la cadena "2" se consideran diferentes tipos de datos. Por lo tanto, el primer console.log devolverá false, mientras que el segundo console.log devolverá true.
- El método includes() es una herramienta poderosa para verificar la presencia de elementos en arreglos. Es simple de usar, eficiente y puede ahorrarte de escribir bucles más complejos o condiciones para buscar en los arreglos. Ya sea que estés trabajando con cadenas, números o tipos de datos mixtos, includes() proporciona una manera directa de verificar si un valor existe en tu arreglo.
---
### ¿Qué es una copia superficial de un array, y cuáles son algunas formas de crear estas copias?
- Una copia superficial de un arreglo es un nuevo arreglo que tiene los mismos elementos que el original. Si el arreglo solo contiene valores primitivos como números o cadenas, el nuevo arreglo es completamente independiente. Pero si el arreglo contiene otros arreglos dentro, tanto el original como la copia tienen referencias a los mismos arreglos internos. Esto significa que si cambias algo dentro de un arreglo interno compartido, verás ese cambio en ambos arreglos. Las copias superficiales son útiles cuando necesitas modificar la estructura de nivel superior, como agregar, eliminar o reordenar elementos, sin modificar el arreglo original ni el arreglo interno. Hay varios métodos para crear copias superficiales de arrays, y exploraremos algunos de los más comunes: concat(), slice() y el operador de propagación.
- concat(). Este método crea un nuevo array al fusionar dos o más arrays. Cuando se utiliza con un solo array, efectivamente crea una copia superficial. Aquí tienes un ejemplo:
```js
const originalArray = [1, 2, 3];
const copyArray = [].concat(originalArray);
console.log(copyArray); // [1, 2, 3]
console.log(copyArray === originalArray); // false
```
- En este ejemplo, estamos utilizando el método concat() para concatenar un array vacío al originalArray. Esto creará un nuevo array que es una copia superficial de originalArray. El copyArray contiene los mismos elementos que originalArray, pero es un objeto array diferente, por lo que la verificación de igualdad estricta (===) devuelve false.
- Otro método para crear una copia superficial es el método slice(). Cuando se llama sin argumentos, slice() devuelve una copia superficial de todo el array. A continuación te mostramos como se hace:
```js
const originalArray = [1, 2, 3];
const copyArray = originalArray.slice();
console.log(copyArray); // [1, 2, 3]
console.log(copyArray === originalArray); // false
```
- En este caso, originalArray.slice() crea un nuevo array que es una copia superficial de originalArray. Nuevamente, el copyArray contiene los mismos elementos pero es un objeto array diferente.
- El operador de propagación (...), introducido en ES6, proporciona una forma concisa de crear copias superficiales de arrays.
```js
const originalArray = [1, 2, 3];
const copyArray = [...originalArray];
console.log(copyArray); // [1, 2, 3]
console.log(copyArray === originalArray); // false
```
- El operador de propagación (...) expande los elementos de originalArray en un nuevo array, creando efectivamente una copia superficial. Es importante observar que todos estos métodos crean nuevos objetos array, lo que significa que puedes modificar la copia sin afectar al array original.
```js
const originalArray = [1, 2, 3];
const copyArray = [...originalArray];
copyArray.push(4);
console.log(originalArray); // [1, 2, 3]
console.log(copyArray);     // [1, 2, 3, 4]
```
- En este ejemplo, añadir un elemento a copyArray no afecta a originalArray.
- En resumen, las copias superficiales de arrays pueden crearse fácilmente usando métodos como concat(), slice() o el operador de propagación. Estos métodos son útiles para crear nuevos arrays que pueden manipularse de manera independiente del array original.
---
## ¿Qué es un objeto en JavaScript y cómo puedes acceder a las propiedades de un objeto?
- En JavaScript, un objeto es una estructura de datos fundamental que te permite almacenar y organizar datos y funcionalidades relacionadas. Puedes pensar en un objeto como un contenedor que guarda varias piezas de información, al igual que un archivo almacena diferentes carpetas y documentos. Estas piezas de información se llaman propiedades y consisten en un nombre (o clave) y un valor.
```js
const exampleObject = {
  propertyName: value,
}
const animal = {}; // empty object
```
- Los objetos son increíblemente versátiles y forman la columna vertebral de JavaScript. De hecho, casi todo en JavaScript es un objeto o se puede tratar como uno. Esto incluye arreglos, funciones, e incluso tipos de datos primitivos como cadenas y números cuando se usan de cierta manera. Esta naturaleza centrada en objetos de JavaScript es una de las razones por las que es un lenguaje tan flexible y poderoso. Vamos a ver cómo puedes crear un objeto:
```js
const person = {
  name: "Alice",
  age: 30,
  city: "New York"
};
```
- En este ejemplo, hemos creado un objeto llamado persona con tres propiedades: nombre, edad, y ciudad. Cada propiedad tiene un nombre y un valor, separados por un colon. Ahora, exploremos cómo puedes acceder a estas propiedades. Hay dos formas principales de acceder a las propiedades del objeto en JavaScript: notación de punto y notación de corchetes.
- La notación de punto es la forma más común y directa de acceder a las propiedades del objeto. Aquí está la sintaxis básica para la notación de punto: `objectName.propertyName`
- Así es como usarías la notación de punto con nuestro objeto persona:
```js
const person = {
  name: "Alice",
  age: 30,
  city: "New York"
};
console.log(person.name);  // Alice
console.log(person.age);   // 30
```
- La notación de punto es concisa y fácil de leer, lo que la convierte en la opción preferida cuando conoces el nombre exacto del propiedad que quieres acceder y ese nombre es un identificador válido de JavaScript (lo que significa que no comienza con un número y no contiene caracteres especiales o espacios).
- La notación de corchetes, en cambio, te permite acceder a las propiedades del objeto usando una cadena dentro de corchetes cuadrados. Así es como usarías la notación de corchetes:
```js
const person = {
  name: "Alice",
  age: 30,
  city: "New York"
};
console.log(person["name"]); // Alice
console.log(person["age"]); //  30
```
- La notación de corchetes es más flexible que la notación de punto porque te permite usar nombres de propiedades que no son identificadores válidos de JavaScript. Por ejemplo, si tuvieras un nombre de propiedad con espacios o que comienza con un número, necesitas usar la notación de corchetes:
```js
const oddObject = {
  "1stProperty": "Hello",
  "property with spaces": "World"
};
console.log(oddObject["1stProperty"]);  // Hello
console.log(oddObject["property with spaces"]);  // World
```
- Otra ventaja de la notación de corchetes es que te permite usar variables para acceder a las propiedades dinámicamente:
```js
const person = {
  name: "Alice",
  age: 30,
  city: "Wonderland"
};
let propertyName = "city";
console.log(person[propertyName]); // Wonderland
```
- Esta flexibilidad hace que la notación de corchetes sea particularmente útil cuando no conoces el nombre exacto de la propiedad al momento de escribir el código, o cuando trabajas con nombres de propiedades que provienen de la entrada del usuario u otra fuente dinámica. Vale la pena señalar que los objetos en JavaScript son increíblemente poderosos y versátiles. Pueden contener no solo valores simples como cadenas y números, sino también arreglos, u otros objetos.
---
### ¿Cómo puedes remover propiedades de un objeto?
- Hay varias maneras de remover propiedades de un objeto, siendo el operador delete el método más directo y comúnmente usado. Cuando usas delete, remueve la propiedad seleccionada del objeto.
```js
 const person = {
  name: "Alice",
  age: 30,
  job: "Engineer"
};
delete person.job;
console.log(person.job); // undefined
```
- En este ejemplo, comenzamos con un objeto persona que tiene tres propiedades: nombre, edad y trabajo. Luego, usamos el operador delete para eliminar la propiedad trabajo. Después de la eliminación, el objeto persona ya no tiene la propiedad trabajo.
- Otra forma de eliminar propiedades es usando asignación declaratoria con parámetros rest. Este enfoque no elimina realmente la propiedad, pero crea un nuevo objeto sin las propiedades especificadas:
```js
const person = {
  name: "Bob",
  age: 25,
  job: "Designer",
  city: "New York"
};
const { job, city, ...remainingProperties } = person;
// { name: "Bob", age: 25 }
console.log(remainingProperties);
```
- En este ejemplo, usamos la asignación por desestructuración para extraer trabajo y ciudad del objeto persona, y recopilamos las propiedades restantes en un nuevo objeto llamado propiedadesRestantes. Esto crea un nuevo objeto sin las propiedades trabajo y ciudad.
---
### Cómo comprobar si un objeto tiene una propiedad?
- En JavaScript, hay varias maneras de comprobar si un objeto tiene una propiedad específica. Es util cuando estás manejando datos de fuentes externas o cuando necesitas asegurarte de que ciertas propiedades existen antes de usarlas.
- hasOwnProperty(): Este método devuelve un booleano que indica si el objeto tiene la propiedad especificada como su propia propiedad.
```js
const person = {
  name: "Alice",
  age: 30
};
console.log(person.hasOwnProperty("name")); // true
console.log(person.hasOwnProperty("job")); // false
console.log(person.hasOwnProperty("age")); // true
```
- En este ejemplo, tenemos un objeto llamado persona con dos propiedades: nombre y edad. Para comprobar si nombre es una propiedad en el objeto persona, usamos el método hasOwnProperty(). Dado que nombre es una propiedad, devolverá true. Pero cuando usamos el método hasOwnProperty() para comprobar si trabajo es una propiedad, devolverá false porque no existe en el objeto.
- Object.hasOwn(): es la forma moderna y recomendada de verificar si un objeto tiene una propiedad propia (no heredada). Piénsalo como una versión mejorada y más segura de hasOwnProperty(). La sintaxis es Object.hasOwn(object, propertyName) — pasas el objeto como primer argumento y el nombre de la propiedad como segundo.
```js
Object.hasOwn(object, propertyName);// La sintaxis
const person = {
  name: "Alice",
  age: 30
};
console.log(Object.hasOwn(person, "name")); // true
console.log(Object.hasOwn(person, "job")); // false // ejemplo
```
- En este ejemplo, Object.hasOwn(person, "name") devuelve true porque name existe directamente en el objeto person. Object.hasOwn(person, "job") devuelve false porque job nunca se añadió al objeto. Una cosa muy importante para entender es que Object.hasOwn() solo verifica si la propiedad existe — no le importa el valor de la propiedad. Esto significa que aún devuelve true incluso cuando el valor es 0, false, null o undefined.
```js
const user = {
  username: "coder123",
  score: 0,
  isActive: false,
  nickname: null
};
// Object.hasOwn() correctly reports these all exist
console.log(Object.hasOwn(user, "score"));    // true  (value is 0, but property exists)
console.log(Object.hasOwn(user, "isActive")); // true  (value is false, but property exists)
console.log(Object.hasOwn(user, "nickname")); // true  (value is null, but property exists)
console.log(Object.hasOwn(user, "email"));   // false (property was never added)
// Danger! Using if() directly gives wrong results for falsy values
if (user.score) {
  console.log("Has score"); // This will NOT print even though score exists!
}
// Safe! Object.hasOwn() gives correct result
if (Object.hasOwn(user, "score")) {
  console.log("Has score:", user.score); // Has score: 0
}
```
- Otra manera de comprobar la existencia de una propiedad en un objeto es usar el operador `in`. Al igual que hasOwnProperty(), el operador in devolverá true si la propiedad existe en el objeto.
```js
const person = {
  name: "Bob",
  age: 25
};
console.log("name" in person);  // true
```
- En este ejemplo, "nombre" in persona devuelve true porque nombre es una propiedad de persona.
- El tercer método implica verificar si una propiedad es undefined. Este enfoque puede ser útil, pero tiene algunas limitaciones. 
```js
const car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2020
};
console.log(car.brand !== undefined); // true
console.log(car.color !== undefined); // false
```
- En este código, comprobamos si auto.marca y auto.color no son undefined. Esto funciona porque acceder a una propiedad inexistente en un objeto devuelve undefined. Sin embargo, este método puede dar falsos negativos si una propiedad tiene explícitamente el valor undefined. En la práctica, la elección entre estos métodos a menudo depende de los requisitos específicos de tu código. Comprender las diferencias entre ellos te ayudará a tomar la decisión correcta en diferentes escenarios.
---
### ¿Cómo trabajas con el acceso a propiedades desde objetos y arreglos anidados en objetos?
- Al trabajar con JavaScript, a menudo te encontrarás con estructuras de datos complejas que involucran objetos anidados y arreglos dentro de objetos. Estas estructuras pueden representar datos ricos y jerárquicos, pero también requieren de un claro entendimiento de cómo acceder y manipular los datos dentro de ellas. Exploraremos cómo navegar por estas estructuras anidadas de manera efectiva.
- Acceder a propiedades desde objetos anidados implica usar la notación de puntos o la notación de corchetes, de manera similar a como se accede a propiedades de objetos simples. Sin embargo, necesitarás encadenar estos accesos para descender a la estructura anidada. Por ejemplo, consideremos un objeto anidado que representa a una persona con información de contacto:
```js
const person = {
  name: "Alice",
  age: 30,
  contact: {
    email: "alice@example.com",
    phone: {
      home: "123-456-7890",
      work: "098-765-4321"
    }
  }
};
// Para acceder al número de teléfono del trabajo de Alice, encadenarías los accesos a propiedades de esta manera:
console.log(person.contact.phone.work); // "098-765-4321"
// También puedes usar la notación de corchetes, que es particularmente útil cuando los nombres de propiedad incluyen espacios o caracteres especiales, o cuando estás usando variables para acceder a propiedades: 
console.log(person['contact']['phone']['work']); // "098-765-4321"
```
- Ahora, echemos un vistazo a cómo podemos acceder a datos donde una de las propiedades del objeto tiene el valor de un arreglo. Aquí hay un objeto persona modificado que incluye un arreglo de direcciones:
```js
const person = {
  name: "Alice",
  age: 30,
  addresses: [
    { type: "home", street: "123 Main St", city: "Anytown" },
    { type: "work", street: "456 Market St", city: "Workville" }
  ]
};
// Aquí tienes un ejemplo de cómo acceder a la ciudad de la dirección de trabajo de Alice:
console.log(person.addresses[1].city); // "Workville"
```
- En este ejemplo, persona.direcciones se refiere al arreglo de direcciones. Para acceder a la segunda dirección en ese arreglo, usamos la notación de corchetes e índice 1. Luego usamos la notación de puntos para acceder a la ciudad de ese objeto dirección.
---
### ¿Cuál es la diferencia entre tipos de datos primitivos y no primitivos?
- Los tipos de datos primitivos son la forma más simple de datos en JavaScript. They include number, bigint, string, boolean, null, undefined, and symbol. Estos tipos se llaman "primitivos" porque representan valores únicos y no son objetos.
- Cuando trabajas con tipos de datos primitivos, estás tratando directamente con sus valores. Por ejemplo, cuando creas una variable con un valor primitivo, ese valor se almacena directamente en la variable. 
- Los valores primitivos son inmutables, lo que significa que una vez creados, su valor no puede cambiarse. Sin embargo, puedes reasignar un nuevo valor a la variable. Aquí tienes un ejemplo de trabajo con tipos de datos primitivos:
```js
let num1 = 5;
let num2 = num1;
num1 = 10;
console.log(num2); // 5
console.log(num1); // 10
```
- En este ejemplo, estamos asignando un valor primitivo (5) de num1 a num2. Esto crea una copia independiente del valor. Como resultado, cualquier cambio realizado en la variable original (num1) no afecta la copia (num2).
- Los tipos de datos no primitivos, por otro lado, son más complejos. En JavaScript, estos son objetos, que incluyen objetos regulares, arreglos y funciones. A diferencia de los primitivos, los tipos no primitivos pueden contener múltiples valores como propiedades o elementos. Cuando creas una variable con un valor no primitivo, lo que se almacena en la variable es en realidad una referencia a la ubicación en memoria donde se almacena el objeto, no el objeto en sí. Esto lleva a algunas diferencias importantes en el comportamiento.
```js
const originalPerson = { name: "John", age: 30 };
const copiedPerson = originalPerson;
originalPerson.age = 31;
console.log(copiedPerson.age); // 31
```
- En este ejemplo tenemos un objeto llamado originalPerson con dos propiedades de nombre y edad. Luego asignamos el objeto originalPerson a una variable llamada copiedPerson. Luego actualizamos el valor de edad para el objeto originalPerson. Cuando registramos la propiedad edad del objeto copiedPerson muestra el valor actualizado. Pero, ¿por qué está sucediendo eso? Esto ocurre porque tanto originalPerson como copiedPerson están haciendo referencia al mismo objeto en memoria.
- En JavaScript, cuando asignas un objeto a otra variable, estás copiando la referencia al objeto, no el objeto en sí. Esto se conoce como copia superficial por referencia. Como resultado, cualquier cambio realizado en el objeto a través de una referencia se refleja en todas las referencias a ese objeto.
---
### ¿Cuál es la diferencia entre funciones y métodos objeto?
- En JavaScript, las funciones y los métodos de objeto son formas de encapsular código reutilizable, pero tienen algunas diferencias clave en cómo se definen, utilizan y el contexto en el que operan.
- Como aprendiste en módulos anteriores, las funciones son bloques de código reutilizables que realizan una tarea específica. Los métodos de objeto, por otro lado, son funciones asociadas a un objeto. Se definen como propiedades de un objeto y pueden acceder y manipular los datos del objeto.
```js
const person = {
    name: "Bob",
    age: 30,
    sayHello: function() {
        return "Hello, my name is " + this.name;
    }
};
console.log(person.sayHello()); // "Hello, my name is Bob"
```
- En este ejemplo, sayHello es un método del objeto person. La palabra clave this permite que el método sayHello acceda a las propiedades del objeto llamado person. 
- Una diferencia entre funciones y métodos es cómo se invocan. Las funciones se llaman por su nombre, mientras que los métodos se llaman usando la notación de punto en el objeto al que pertenecen. Por ejemplo, llamamos a la función greet como greet("Alice"), pero llamamos al método sayHello como person.sayHello().
- Otra diferencia importante es el contexto en el que operan. Las funciones regulares tienen su propio ámbito, pero no tienen una referencia integrada a ningún objeto en particular. Sin embargo, los métodos están vinculados a su objeto y pueden acceder a sus propiedades y otros métodos usando la palabra clave this. Un punto clave a destacar es que los métodos ayudan a organizar el código en objetos lógicos, mientras que las funciones se utilizan para un código más general y reutilizable.
---
### ¿Qué es el constructor Object() y cuándo debe usarlo?
- En JavaScript, un constructor es un tipo especial de función utilizada para crear e inicializar objetos. Se invoca con la palabra clave new y puede inicializar propiedades y métodos en el objeto recién creado. El constructor Object() crea un nuevo objeto vacío. Aquí hay un ejemplo: `new Object()`, cuando llamas a new Object(), retorna un nuevo objeto que puede utilizarse para almacenar valores. 
- El constructor Object() puede utilizarse con o sin la palabra clave new. Cuando se llama como función sin new, se comporta de manera diferente dependiendo del tipo de valor que se le pase. Aquí tienes un ejemplo de cómo usar el constructor Object() sin la palabra clave new:
```js
const num = 42;
const numObj = Object(num); // Creates an object wrapper for the number
console.log(numObj); // Number { constructor: { name: "Number" } }
console.log(typeof numObj); // "object"
```
- Como puedes ver en el segundo console.log, numObj es un objeto. Esto sucede porque usamos el constructor Object() para convertir esa entrada de número en un objeto. 
- ¿Qué pasa si intentamos pasar null o undefined al constructor Object()?
```js
const newObj = new Object(undefined);
console.log(newObj); // {}
```
- Bueno, el resultado será un objeto vacío. Otro caso de uso para el constructor Object() es cuando trabajas con un valor de tipo desconocido y necesitas asegurarte de que sea un objeto. 
```js
function toObject(value) {
  if (value === null || value === undefined) {
    return {};
  }
  if (typeof value === "object") {
    return value;
  }
  return Object(value);
}
console.log(toObject(null));
console.log(toObject(true));
console.log(toObject([1, 2, 3]));
```
- En este ejemplo, tenemos una función llamada toObject. La segunda condición verificará si el valor es de tipo objeto y retornará el valor si la condición es true. Esta condición verificará tanto objetos como matrices, ya que las matrices son tipos especiales de objetos. Si ninguna de las condiciones es verdadera, la función devuelve Object(value), que convierte la entrada en un objeto. Esto funciona para valores como números, cadenas y booleanos. La mayoría de las veces no estarás usando el constructor Object() para crear nuevos objetos porque usarás la sintaxis literal de objetos en su lugar (e.g., const objectLiteral = { name: "Beau" }).
---
### ¿Qué es JSON y cómo accedes a los valores usando notación de corchetes y notación de puntos?
- JSON significa Notación de Objetos de JavaScript. Es un formato de datos ligero, basado en texto, que se usa comúnmente para intercambiar datos entre un servidor y una aplicación web. Una de las razones por las cuales JSON es tan popular en el desarrollo web es porque es tanto parseable por máquina como legible por humanos. Dado que JSON es independiente del lenguaje, puedes enviar fácilmente datos JSON desde una aplicación Java a una aplicación Python, o desde una aplicación JavaScript a una aplicación C#. JSON soporta muchos tipos de datos incluyendo objetos, arreglos, cadenas, booleanos, nulo y números. Aquí hay un ejemplo de un objeto JSON:
```js
{
  "name": "Alice",
  "age": 30,
  "isStudent": false,
  "list of courses": ["Mathematics", "Physics", "Computer Science"]
}
```
- Como puedes ver, JSON usa pares de clave-valor para almacenar información y cada par está separado por una coma. Cada clave debe estar envuelta en comillas dobles, de lo contrario recibirás un error. Para acceder a los datos de un objeto JSON, puedes usar la notación de puntos o de corchetes. En este ejemplo, estamos usando la notación de puntos para acceder a la age del objeto JSON:
```js
import data from "./example.json" with { type: "json" };
console.log(data.age);
```
- Este ejemplo en particular está usando lo que se conoce como una sentencia import, que importa el objeto JSON en este archivo para que tengamos acceso a él. Aprenderás más sobre la sentencia import en una lección futura. También puedes usar la notación de corchetes para acceder a la información de los objetos JSON. Aquí hay un ejemplo de cómo acceder al arreglo list of courses:
```js
import data from "./example.json" with { type: "json" };
console.log(data["list of courses"]);
```
- Usar la notación de corchetes es especialmente útil aquí porque la clave contiene varias palabras separadas por espacios. Si intentáramos usar la notación de puntos, resultaría en un error. En resumen, JSON es un formato versátil que puede almacenar muchos tipos de datos, incluidos arreglos y objetos anidados. Usando la notación de puntos o de corchetes, puedes acceder fácilmente a los valores almacenados dentro de un objeto JSON.
---
### ¿Cómo funcionan JSON.parse() y JSON.stringify()?
- Hay dos métodos potentes en JavaScript para manejar datos JSON: JSON.parse() y JSON.stringify(). Estos métodos se utilizan comúnmente para convertir entre cadenas JSON y objetos de JavaScript.
- JSON.stringify(): se usa para convertir un objeto de JavaScript en una cadena JSON. Esto es útil cuando deseas almacenar o transmitir datos en un formato que pueda compartirse o transferirse fácilmente entre sistemas.
```js
const user = {
  name: "John",
  age: 30,
  isAdmin: true
};
const jsonString = JSON.stringify(user);
console.log(jsonString); // "{"name":"John","age":30,"isAdmin":true}"
console.log(user); // { name: "John", age: 30, isAdmin: true }
```
- El método JSON.stringify() también acepta un parámetro opcional llamado replacer, que puede ser una función o un arreglo. He aquí un ejemplo de uso de un arreglo para el parámetro opcional replacer:
```js
const developerObj = {
  firstName: "Jessica",
  isAwesome: true,
  isMusician: true,
  country: "USA",
};
console.log(JSON.stringify(developerObj, ["firstName", "country"]));// result: {"firstName":"Jessica","country":"USA"}
console.log(developerObj); // { firstName: "Jessica", isAwesome: true, isMusician: true, country: "USA" }
```
- En este ejemplo, tenemos un developerObj con cuatro propiedades. Cuando usamos el método JSON.stringify(), podemos pasar un arreglo como segundo parámetro y especificar qué propiedades queremos convertir en cadena. El resultado será un objeto en forma de cadena que contiene solo las propiedades firstName y country.
- Otro parámetro opcional para el método JSON.stringify() sería el parámetro spacer. Esto te permite controlar el espaciado del resultado convertido en cadena:
```js
const developerObj = {
  firstName: "Jessica",
  isAwesome: true,
  isMusician: true,
  country: "USA",
};
console.log(JSON.stringify(developerObj, null, 2));
/*
{
  "firstName": "Jessica",
  "isAwesome": true,
  "isMusician": true,
  "country": "USA"
}
*/
```
- La mayoría de las veces no usarás ninguno de estos parámetros opcionales para el método JSON.stringify(), pero sigue siendo útil estar al tanto de ellos. Otro método que usarás mucho en tu programación es el método JSON.parse() que convierte una cadena JSON de nuevo en un objeto JavaScript. Esto es útil cuando recuperas datos JSON de un servidor web o de localStorage y necesitas manipular los datos en tu aplicación. Aprenderás más sobre localStorage en una lección futura.
```js
const jsonString = '{"name":"John","age":30,"isAdmin":true}';
const userObject = JSON.parse(jsonString);
console.log(userObject); // { name: 'John', age: 30, isAdmin: true }
```
- Esto te permite trabajar con los datos en tu programa como un objeto de JavaScript normal, lo que facilita su manipulación y uso.
---
### ¿Qué es el Operador de Encadenamiento Opcional, y Cómo Funciona?
- El operador de encadenamiento opcional (?.) es una herramienta útil en JavaScript que te permite acceder de forma segura a propiedades de objetos o llamar métodos sin preocuparte de si existen. Es como una red de seguridad para trabajar con objetos que podrían tener partes faltantes.
```js
const person = {
  name: "Alice",
  age: 30
};
console.log(person.name); // "Alice"
console.log(person.job); // undefined
```
- En este ejemplo, person.name existe, así que muestra Alice. Pero person.job no existe, por lo que nos da undefined. Ahora, digamos que queremos acceder a una propiedad de un objeto que podría no existir:
```js
const person = {
  name: "Alice",
  age: 30
};
console.log(person.address.street); // This will throw an error!
```
- Este ejemplo generará un Uncaught TypeError. Dado que person.address es undefined, no podemos acceder a la propiedad street. Aquí es donde el operador de encadenamiento opcional resulta útil.
```js
const user = {
  name: "John",
  profile: {
    email: "john@example.com",
    address: {
      street: "123 Main St",
      city: "Somewhere"
    }
  }
};
console.log(user?.profile?.address?.street); // "123 Main St"
console.log(user?.profile?.phone?.number);   // undefined
```
- Al usar el operador de encadenamiento opcional, le indicamos a JavaScript que solo continúe con la operación si el objeto (o el valor antes de ?.) existe y no es null o undefined. Si el valor antes del ?. es null o undefined, JavaScript devuelve undefined en lugar de intentar continuar with la operación y generar un error. Recuerda, el operador de encadenamiento opcional es más útil cuando no estás seguro de si una propiedad o un método existe. Ayuda a prevenir errores y hace que tu código sea más robusto.
---
### ¿Qué es la desestructuración de objetos y cómo funciona?
-  La desestructuración de objetos es una característica poderosa en JavaScript que te permite extraer valores de objetos y asignarlos a variables de una manera más concisa y legible. Forma parte de la especificación ES6 (ECMAScript 2015) y se ha convertido en una herramienta esencial para muchos desarrolladores de JavaScript. La desestructuración puede simplificar tu código, especialmente al trabajar con objetos complejos o cuando necesitas extraer múltiples valores de una vez. En su núcleo, la desestructuración de objetos se trata de desempaquetar valores de objetos en variables distintas. En lugar de acceder a las propiedades del objeto una por una, puedes extraer múltiples propiedades en una sola declaración. Esto puede hacer que tu código sea más limpio y eficiente.
```js
const person = { name: "Alice", age: 30, city: "New York" };
const { name, age } = person;
console.log(name); // Alice
console.log(age);  // 30
```
- En este ejemplo, estamos extrayendo las propiedades name y age del objeto person y asignándolas a variables con los mismos nombres. Uno de los aspectos poderosos de la desestructuración de objetos es que puedes asignar los valores extraídos a variables con nombres diferentes. Esto es particularmente útil cuando trabajas con objetos cuyos nombres de propiedades pueden entrar en conflicto con variables existentes o cuando deseas usar un nombre diferente:
```js
let person = { name: "Alice", age: 30, city: "New York" };
let { name: personName, age: personAge } = person;
console.log(personName); // Alice
console.log(personAge); //  30
```
- En este caso, estamos extrayendo la propiedad name y asignándola a una variable llamada personName, y haciendo lo mismo con age y personAge.
- La desestructuración de objetos también te permite establecer valores predeterminados. Si una propiedad no existe en el objeto que estás desestructurando, puedes especificar un valor de respaldo:
```js
let person = { name: "Alice", age: 30, city: "New York" };
let { name, age, country = "Unknown" } = person;
console.log(country); // Unknown
```
- Aquí, dado que country no existe en nuestro objeto person, obtiene el valor predeterminado Unknown.
- Otro caso común es la desestructuración de objetos anidados. Puedes desestructurar propiedades anidadas dentro de otros objetos usando otro conjunto de llaves:
```js
const recipe = {
  name: "Chocolate Cake",
  ingredients: {
    flour: "2 cups",
    sugar: "1 cup"
  }
};
const { ingredients: { flour } } = recipe; // Extract `flour` from `ingredients`
console.log(flour); // "2 cups"
```
- Esto es equivalente a acceder a la propiedad directamente:
```js
const flour = recipe.ingredients.flour;
console.log(flour); // "2 cups"
```
- Ahora, hablemos sobre la notación abreviada en la desestructuración de objetos. Cuando estás creando objetos, especialmente cuando los nombres de propiedades coinciden con los nombres de variables, puedes usar una sintaxis abreviada:
```js
let name = "Bob";
let age = 25;
let person = { name, age };
console.log(person); // { name: "Bob", age: 25 }
```
- El código anterior toma las propiedades con el mismo nombre que nuestras variables y les asigna los valores de esas variables. Esta notación abreviada es particularmente útil cuando estás devolviendo objetos desde funciones o creando objetos con múltiples propiedades:
```js
function createPerson(name, age) {
  return { name, age };
}
let person = createPerson("Charlie", 35);
console.log(person); // { name: "Charlie", age: 35 }
```
- La desestructuración de objetos y la notación de objeto abreviada son características poderosas que pueden hacer que tu código sea más conciso y fácil de leer. Son especialmente útiles cuando trabajas con estructuras de datos complejas, o cuando necesitas pasar múltiples parámetros a funciones.
---
## ¿Cómo funcionan los bucles e iteraciones en JavaScript?
- Los bucles en programación se utilizan para repetir un bloque de código varias veces. Un ejemplo de un bucle sería cuando estás diseñando un programa que necesita imprimir una lista de elementos. Podrías usar un bucle para imprimir cada uno de los elementos de la lista. Otro ejemplo sería cuando estás diseñando un juego y quieres mover un personaje a través de la pantalla. Podrías usar un bucle para mover al personaje un cierto número de píxeles cada vez que se ejecuta el bucle.
- En JavaScript, hay varios tipos de bucles que puedes usar. In this lesson, we will cover the `for` loop. Aquí está la sintaxis básica para un bucle `for`:
```js
for (initialization; condition; increment or decrement) {
  // code block to be executed
}
```
- La declaración de inicialización se ejecuta antes de que comience el bucle. Se utiliza típicamente para inicializar una variable contador. Una variable contador es una variable que se utiliza para llevar el conteo de cuántas veces se ha ejecutado el bucle.
- La declaración de condición se evalúa antes de cada iteración del bucle. Una iteración es un único paso a través del bucle.
- Si la condición es verdadera, el bloque de código dentro del bucle se ejecuta. Si la condición es falsa, el bucle se detiene y pasas al siguiente bloque de código.
- La última parte del bucle es la declaración de incremento/decremento. Esta declaración se ejecuta después de cada iteración del bucle. Se utiliza típicamente para incrementar o decrementar la variable contador.
```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```
- En la primera parte del ejemplo anterior, inicializamos una variable contador i a 0. Es convención común usar i como la variable contador en un bucle for. La siguiente parte es verificar la condición. En este caso, la condición verifica si i es menor que 5. Dado que i es 0, la condición es verdadera y se ejecuta el bloque de código dentro del bucle. El bloque de código dentro del bucle es registrar el valor de i en la consola. El valor de i es 0, por lo que la consola mostrará el valor de 0. Luego se ejecuta la declaración de incremento. En este caso, estamos incrementando i en 1. Así que ahora i es 1. Luego verificamos la condición nuevamente, que es verificar si i es menor que 5. Dado que i es ahora 1, la condición sigue siendo verdadera y se ejecuta nuevamente el bloque de código dentro del bucle. Seguimos repitiendo este proceso hasta que la condición sea falsa. En este caso, cuando i es 5, la condición es falsa y el bucle se detiene.
- Cuando trabajes con bucles, debes tener cuidado de no crear una condición que sea siempre verdadera. Si lo haces, el bucle se ejecutará indefinidamente y tu programa se bloqueará. Esto se conoce como un bucle infinito.
- Es posible crear bucles for anidados. Un bucle anidado es cuando colocas un bucle dentro de otro.
- Los bucles pueden ser beneficiosos en la programación cuando necesitas repetir un bloque de código cierta cantidad de veces. Aunque trabajar con bucles for puede ser complicado al principio, con la práctica le cogerás el truco.
---
### ¿Cómo funciona el bucle For...of, y cuándo deberías usarlo?
- Se usa un bucle `for...of` cuando necesitas iterar sobre valores de un iterable. Ejemplos de iterables serían arreglos y cadenas de texto. Aquí está la sintaxis básica para un bucle `for...of`:
```js
for (variable of iterable) {
  // code block to be executed
}
```
- La variable en el ejemplo representa el valor actual del iterable que se está recorriendo. Si tienes un arreglo de números, la variable sería el número actual en el arreglo. Si tienes una cadena de texto, la variable sería el carácter actual en la cadena.
- En este primer ejemplo tenemos un arreglo de números y queremos recorrer cada número y registrarlo en la consola.
```js
const numbers = [1, 2, 3, 4, 5];
for (const num of numbers) {
  console.log(num);
}
```
- Hemos creado una variable llamada num que representará el número actual en el arreglo. Para la iteración 1, num será 1, para la iteración 2, num será 2, y así sucesivamente. Dentro del bucle, estamos registrando el número actual en la consola.
- Aquí hay otro ejemplo donde tenemos una cadena de texto y queremos recorrer cada carácter y registrarlo en la consola.
```js
const str = 'freeCodeCamp';
for (let char of str) {
  console.log(char);
}
```
- En este ejemplo, hemos creado una variable llamada char que representará el carácter actual en la cadena. Para cada iteración, el bucle registrará el carácter actual en la consola. Es importante notar que puedes usar let o const al declarar la variable en un bucle `for...of`, si vas a usar const, asegúrate de que el valor de la variable no cambie dentro del bucle. Si lo hace, obtendrás un error.
- Aquí hay un ejemplo de uso de const que resulta en un error:
```js
const numbers = [1, 2, 3, 4, 5];
for (const num of numbers) {
  console.log(num);
  num = num + 1; // This will cause an error
}
```
- En este ejemplo, estamos tratando de cambiar el valor de num dentro del bucle. Dado que declaramos num con const, obtendremos un error. Por eso, si necesitas cambiar el valor de la variable dentro del bucle, usa let en su lugar.
- Veamos un último ejemplo que trata con un arreglo de objetos.
```js
const people = [
  { name: 'John', age: 30 },
  { name: 'Jane', age: 25 },
  { name: 'Jim', age: 40 }
];
for (const person of people) {
  console.log(`${person.name} is ${person.age} years old`);
}
```
- En este ejemplo, tenemos un arreglo de objetos llamado people. Cada objeto tiene una propiedad name y una propiedad age. Cuando recorremos el arreglo, creamos una variable llamada person que representará el objeto actual en el arreglo. Dentro del bucle, estamos imprimiendo un mensaje en la consola.
- Los bucles `for...of` son realmente útiles cuando necesitas recorrer valores de un iterable como un arreglo o una cadena de texto. También son fáciles de leer y pueden hacer que tu código sea más conciso.
---
### ¿Qué es el bucle For...in y cuándo debes usarlo?
- Un bucle for...in se usa mejor cuando necesitas recorrer las propiedades de un objeto. Este bucle iterará sobre todas las propiedades enumerables de un objeto, incluidas las propiedades heredadas y no numéricas.
- Una propiedad heredada es una propiedad que se hereda de la cadena de prototipos del objeto. Una propiedad no numérica es una propiedad que no es un número o una cadena que se puede convertir en un número.
- Aquí está la sintaxis básica de un bucle `for...in`:
```js
for (variable in object) {
  // code block to be executed
}
```
- La variable en el ejemplo representa la propiedad actual del objeto que se está recorriendo.
- En este primer ejemplo, tenemos un objeto fruit y queremos recorrer cada propiedad y registrar el valor en la consola.
```js
const fruit = {
  name: 'apple',
  color: 'red',
  price: 0.99
};
for (const prop in fruit) {
  console.log(fruit[prop]);
}
```
- La variable prop representa la propiedad actual del objeto. Se usa fruit[prop] para acceder al valor de cada propiedad. Para la primera iteración, prop será name. Para la segunda iteración, prop será color, y así sucesivamente. Los resultados registrados en la consola serán apple, red, y 0.99.
- En este segundo ejemplo, tenemos un objeto anidado y queremos recorrer cada propiedad y registrar el valor en la consola.
```js
const person = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'Anytown',
    state: 'CA'
  }
};
for (const prop in person) {
  console.log(person[prop]);
}
```
- La propiedad address es un objeto en sí mismo. El bucle for...in también recorrerá las propiedades del objeto person y registrará el objeto address completo en la consola. Si deseas recorrer las propiedades del objeto address, puedes anidar otro bucle for...in dentro del primero.
```js
const person = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'Anytown',
    state: 'CA'
  }
};
function isObject(obj) {
  return typeof obj === 'object' && !Array.isArray(obj) && obj !== null;
}
for (const prop in person) {
  if (isObject(person[prop])) {
    for (const nestedProp in person[prop]) {
      console.log(person[prop][nestedProp]);
    }
  } else {
    console.log(person[prop]);
  }
}
```
- En este ejemplo, tenemos una función personalizada isObject que verifica si el valor es un objeto. Se usa el método Array.isArray para verificar si el valor es un arreglo. Colocando el operador lógico NO (!) delante del método, verificamos si el valor no es un arreglo. La razón por la que no podemos simplemente usar typeof igual a 'object' es porque las matrices también se consideran objetos en JavaScript. Queremos excluir arrays de la verificación. Además, debido a un error histórico en JavaScript, typeof null devuelve 'object'. Así que también queremos excluir valores null de la verificación. Si la condición es verdadera, anidamos otro bucle for...in que recorrerá las propiedades del objeto anidado y registrará el valor en la consola. La variable nestedProp representa la propiedad actual del objeto anidado.
- Un bucle for...in es útil cuando necesitas recorrer las propiedades de un objeto. No se recomienda usar un bucle for...in para recorrer los elementos de un arreglo. En su lugar, utiliza un bucle for...of u otros métodos.
---
### ¿Qué es un bucle While y cómo se diferencia del bucle Do...while?
- Un bucle while ejecutará un bloque de código mientras la condición sea verdadera. Aquí está la sintaxis básica de un bucle while:
```js
while (condition) {
  // code block to be executed
}
```
- La condición se verifica antes de ejecutar el bloque de código. Si la condición es falsa, el bloque de código no se ejecutará.
- Los bucles while son útiles cuando no sabes cuántas veces necesitas ejecutar el bloque de código. Aquí tienes un ejemplo de cómo usar un bucle while:
```js
let counter = 0;
while(counter < 5) {
  console.log(counter);
  counter++;
}
```
- En este ejemplo, tenemos una variable llamada counter que se inicializa en 0. El ciclo while continuará ejecutándose mientras el valor de counter sea menor que 5. Dentro del ciclo, registramos el valor de counter en la consola y luego incrementamos counter en 1.
- Otro bucle similar al bucle while sería el bucle `do...while`. Esta es la sintáxis básica:
```js
do {
  // code block to be executed
} while (condition);
```
- do...while ejecutará el bloque de código al menos una vez antes de verificar la condición. Si la condición es verdadera, el bloque de código continuará ejecutándose. Si la condición es falsa, el bloque de código dejará de ejecutarse.
```js
let counter = 0;
do {
  console.log(counter);
  counter++;
} while (counter < 5);  
```
- En este ejemplo, tenemos una variable llamada counter que se inicializa en 0. El ciclo do...while registrará el valor de counter en la consola y luego incrementará counter en 1. Después de ejecutar el bloque de código, verifica si el valor de counter es menor que 5. Si lo es, el ciclo continuará ejecutándose. Si no, el ciclo se detendrá.
- En la mayoría de los casos, probablemente usarás el bucle while más a menudo que el bucle do...while. Sin embargo, es bueno conocer ambos tipos de bucles y cuándo usarlos.
---
### ¿Para qué se utilizan las declaraciones Break y Continue en bucles?
- Una declaración break se usa para salir de un bucle temprano, mientras que una declaración continue se usa para saltar la iteración actual de un bucle y pasar a la siguiente.
- Aquí hay un ejemplo de usar una declaración break en un bucle for:
```js
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}
```
- En el ejemplo anterior, el ciclo comienza a contar en 0 y mientras i sea menor que 10, el ciclo continuará ejecutándose. Dentro del bucle, comprobamos si i es igual a 5. Si lo es, usamos la declaración break para salir del bucle antes. Si no, registramos el valor de i en la consola. Por lo tanto, la salida del código imprimirá los números 0, 1, 2, 3 y 4.
- La declaración break es útil cuando deseas salir de un bucle temprano en función de una condición determinada. Por ejemplo, si estás buscando un valor específico en una matriz, puedes usar una declaración break para salir del bucle una vez que encuentres el valor.
- A veces, puedes querer omitir una iteración particular de un bucle sin salir del bucle por completo. Aquí es donde entra la declaración continue. Aquí hay un ejemplo de usar una declaración continue en un bucle for:
```js
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    continue;
  }
  console.log(i);
}
```
- Al igual que antes, hemos inicializado i a 0 y tenemos una condición que ejecutará el bucle mientras i sea menor que 10. Dentro del bucle, cuando i es igual a 5, usamos la declaración continue para omitir la iteración actual y pasar a la siguiente. La salida de este código imprimirá los números 0, 1, 2, 3, 4, 6, 7, 8 y 9. El número 5 se omite debido a la declaración continue. Otra cosa que puedes hacer con las declaraciones break y continue es usar etiquetas para especificar qué bucle quieres terminar o continuar. Esto es útil cuando tienes bucles anidados y deseas controlar el flujo del bucle externo desde dentro del bucle interno. Aquí hay un ejemplo de usar etiquetas con la declaración break:
```js
outerLoop: for (let i = 0; i < 3; i++) {
  innerLoop: for (let j = 0; j < 3; j++) {
    if (i === 1 && j === 1) {
      break outerLoop;
    }
    console.log(`i: ${i}, j: ${j}`);
  }
}
```
- En este ejemplo, tenemos un bucle externo con la etiqueta outerLoop y un bucle interno con la etiqueta innerLoop. Cuando i es igual a 1 y j es igual a 1, usamos la declaración break con la etiqueta outerLoop para salir del bucle externo antes. Esto saldrá de ambos bucles, el interno y el externo.
- La mayoría de las veces no encontrarás la necesidad de utilizar etiquetas con las declaraciones break y continue, pero es bueno saber que tienes esa opción si alguna vez la necesitas.
---
## ¿Qué es un objeto de cadena y cómo se diferencia de un string primitivo?
- JavaScript también tiene objetos de cadena. Tanto los objetos de cadena como los string primitivos se utilizan para manejar texto, pero funcionan de manera diferente internamente. Un objeto de cadena se crea usando la función constructor de cadenas, que envuelve el valor primitivo en un objeto. Así es como crearías un objeto de cadena:
```js
const greetingObject = new String("Hello, World!");
console.log(typeof greetingObject); // "object"
```
- Una diferencia clave entre un objeto de cadena y un string primitivo es cómo se relaciona con la memoria y el rendimiento. Los string primitivos suelen ser más eficientes en términos de memoria y más rápidos en comparación con los objetos de cadena.
---
### ¿Qué es el método toString() y cómo funciona?
- toString() es una característica fundamental en JavaScript que convierte un valor en su representación en forma de cadena. Es un método que puedes usar para números, booleanos, arreglos y objetos. Uno de los usos más comunes de toString() es convertir un número en su representación en forma de cadena.
```js
const num = 10;
console.log(num.toString()); // "10"
```
- Este método acepta un radix opcional que es un número del 2 al 36. Este radix representa la base, como la base 2 para binario o base 8 para octal. Si el radix no se especifica, por defecto es la base 10, que es decimal. Aquí hay un ejemplo de pasar 2 como un argumento al método toString():
```js
const num = 10;
console.log(num.toString(2)); // "1010"
```
- El resultado será 1010, que es la representación binaria del número decimal 10.
- También puedes usar el método toString() para convertir arreglos y objetos en cadenas. Los arreglos tienen una implementación personalizada de toString() que convierte cada elemento en una cadena y los une con comas:
```js
const arr = [1, 2, 3];
console.log(arr.toString()); // "1,2,3"
```
- En este ejemplo todos los elementos del arreglo se unen para formar la cadena 1,2,3.
- Cuando se utiliza el método toString() con objetos, el resultado no será una versión en cadena de las propiedades del objeto.
```js
const person = {
  name: "John",
  age: 30,
  isStudent: true
};
console.log(person.toString()); // "[object Object]"
```
- En este ejemplo, el resultado será la representación en cadena predeterminada para el objeto que es [object Object]. Para obtener una versión en cadena de las propiedades del objeto person necesitarás usar JSON.stringify(), sobre lo cual aprenderás más en las lecciones futuras.
- En conclusión, el método toString() se usa para convertir valores en cadenas. Comprender cómo funciona con diferentes tipos de datos y cómo personalizarlo para tus propios objetos puede mejorar significativamente tu capacidad para manipular y mostrar datos en tus aplicaciones de JavaScript.
---
### ¿Qué es el constructor Number y cómo funciona para la coerción de tipos?
- Number() se utiliza para crear un objeto número. The number object contains a few helpful properties and methods like the isNaN and the toFixed method. Aquí tienes un ejemplo usando el constructor Number() con la palabra clave new:
```js
const myNum = new Number("34");
console.log(typeof myNum); // "object" 
```
- En este ejemplo, pasamos una cadena literal al constructor Number() y el tipo de retorno es de tipo objeto en lugar de una cadena.
- Cuando se llama al constructor Number() como una función sin la palabra clave new, entonces el valor de retorno será el tipo de número primitivo. La mayoría de las veces usarás el constructor Number() para convertir otros tipos de datos al tipo de dato número.
```js
const myNum = Number("100");
console.log(myNum); // 100
console.log(typeof myNum); // number
```
- Esto es útil cuando recibes entradas del usuario y necesitas convertir esa entrada de cadena a un número para realizar cálculos matemáticos.
- Si intentas llamar al constructor Number() a través de una cadena vacía, el resultado será el número 0: `const num = Number(""); console.log(num); // 0`
- Esto es porque JavaScript intentará analizar la cadena y como no contiene ningún dígito, el resultado será cero. Si intentas pasar una cadena con caracteres aleatorios, el resultado será NaN. `const num = Number("random"); console.log(num); // NaN`.
- Al trabajar con booleanos, true devuelve 1 porque true se convierte a uno y false devuelve 0 porque false se convierte a cero.
```js
const boolTrue = Number(true);
const boolFalse = Number(false);
console.log(boolTrue); // 1
console.log(boolFalse); // 0
```
- Si pasas null, el resultado será 0 y si pasas undefined, el resultado será NaN.
```js
const undefinedNum = Number(undefined);
const nullNum = Number(null);
console.log(undefinedNum); // NaN
console.log(nullNum); // 0
```
- Al trabajar con arreglos hay algunas cosas que considerar. Un arreglo vacío devolverá 0. Un arreglo con un solo número devolverá ese número. Un arreglo con múltiples números devuelve NaN. Y un arreglo con cadena(s) también devolverá NaN.
```js
const emptyArr = Number([]);
const arrOneNum = Number([7]);
const arrMultiNum = Number([7, 36, 12]);
const arrStr = Number(["str1"]);
const arrMultiStr = Number(["str1", "str2"]);
console.log(emptyArr); // 0
console.log(arrOneNum); // 7
console.log(arrMultiNum); // NaN
console.log(arrStr); // NaN
console.log(arrMultiStr); // NaN
```
- Al trabajar con objetos, el resultado es siempre NaN.
- En conclusión, usarás principalmente el constructor Number() para la conversión de tipos más que para crear un número o un objeto número.
---
### ¿Cuáles son algunas prácticas comunes para nombrar variables y funciones?
- Nombrar variables y funciones es un aspecto importante de escribir código limpio, legible y mantenible. Las buenas prácticas de nomenclatura hacen que tu código se autocomente, reduciendo la necesidad de comentarios extensos y facilitando que otros desarrolladores, incluido tu futuro yo, entiendan tu código.
- Comencemos con las convenciones generales de nomenclatura en JavaScript. In previous lessons you learned about using camel case for variable names. 
- Para las variables booleanas, es una práctica común usar prefijos como is, has o can. Esto le indica inmediatamente al lector que la variable es un booleano:
```js
let isLoading = true;
let hasPermission = false;
let canEdit = true;
```
-Para las funciones, el nombre debe indicar claramente lo que hace la función. A menudo es útil comenzar con un verbo:
```js
function getUserData(){}
function calculateTotal(){}
function validateInput(){}
```
- Para las funciones que devuelven un booleano, a menudo llamadas predicados, puedes usar los mismos prefijos is, has o can:
```js
function isValidEmail(email) {}
function hasRequiredFields(form) {}
```
- Cuando tienes funciones que obtienen datos, es común comenzar con la palabra get:
```js
function getProductDetails(productId) {}
function getUserProfile(userId) {}
```
- Cuando tienes funciones que asignan datos, es común comenzar con la palabra set:
```js
function setUserPreferences(preferences) {}
function setPageTitle(title) {}
```
- Para las funciones manejadoras de eventos, podrías utilizar el prefijo handle o el sufijo handler:
```js
function handleClick(){}
function onSubmit(){}
function keyPressHandler(){}
```
- Un manejador de eventos es una acción que ocurre después de que un evento ha sucedido, como un clic en un botón.
- Al nombrar variables iteradoras y bucles, es común usar letras individuales como i, j o k, pero para bucles anidados o iteraciones más complejas, nombres más descriptivos pueden ser útiles:
```js
for (let i = 0; i < array.length; i++) {}
for (let studentIndex = 0; studentIndex < students.length; studentIndex++) {}
```
- Para nombres de arreglos, considera usar sustantivos en plural para indicar que la variable contiene múltiples elementos:
```js
const colors = ['red', 'green', 'blue'];
const userNames = ['Alice', 'Bob', 'Charlie'];
```
- Recuerda que el objetivo es hacer que tu código sea lo más autoexplicativo posible. Una buena regla general es que si necesitas agregar un comentario para explicar qué hace una variable o función, podrías considerar renombrarla a algo más descriptivo. Por último, sé consistente con tu base de código o equipo. Si tu equipo ha establecido convenciones de nomenclatura, adhiérete a ellas. La consistencia hace que el código sea más legible y mantenible para todos los involucrados.
---
### ¿Cómo obtienes la longitud de una matriz y cómo puedes crear una matriz vacía de longitud fija?
- Es posible tener matrices con espacios vacíos. Los espacios vacíos se definen como espacios sin nada dentro. Esto es diferente de una matriz con el valor de undefined. Estos tipos de matrices se conocen como matrices dispersas. Aquí hay un ejemplo:
```js
const sparseArray = [1, , , 4];
console.log(sparseArray.length); // 4
```
- En este caso, aunque solo tenemos dos elementos definidos, 1 y 4, la longitud es 4 porque el índice más alto (3) más 1 nos da una longitud de 4.
- cómo crear una matriz vacía de longitud fija. Hay pocas formas de hacer esto en JavaScript, pero un método común es usar el constructor Array() con un argumento numérico. El constructor Array() se puede usar con la palabra clave new para crear una nueva matriz. 
```js
const emptyArray = new Array(5);
console.log(emptyArray.length); // 5
console.log(emptyArray); // [ , , , , ]
```
- En este ejemplo, creamos un nuevo arreglo usando Array(5). Esto crea un arreglo disperso con una longitud de 5 donde todos los espacios están vacíos.
- Otra forma de crear un arreglo vacío de longitud fija es usar el método Array.from() con un argumento de longitud. A diferencia de new Array(n), este método crea un arreglo de la longitud especificada donde todos los elementos existen y tienen un valor de undefined:
```js
const fixedLengthArray = Array.from({ length: 5 });
console.log(fixedLengthArray.length); // 5
console.log(fixedLengthArray); // [undefined, undefined, undefined, undefined, undefined]
```
- Si deseas crear un arreglo de longitud específica y llenarlo con un valor predeterminado, puedes usar el método Array.fill():
```js
const filledArray = new Array(3).fill(0);
console.log(filledArray); // [0, 0, 0]
```
- Esto crea un arreglo de longitud tres y llena todos los elementos con el valor 0. Nota: al llenar con objetos, todas las posiciones hacen referencia al mismo objeto; si necesitas copias independientes, usa una función de devolución de llamada o Array.from() en su lugar. Entender cómo obtener la longitud de una matriz y crear matrices de longitud fija es importante para muchas tareas de programación, especialmente cuando necesitas inicializar matrices para algoritmos o estructuras de datos específicos.
---
### ¿Qué son los linters y los formateadores, y cómo pueden ayudarte con la consistencia del código?
- En el mundo del desarrollo de software, mantener código limpio, consistente y libre de errores es importante. Aquí es donde entran en juego los linters y los formateadores. Estas herramientas son esenciales para los desarrolladores para asegurar la calidad y consistencia del código a lo largo de proyectos y equipos.
- linter: es una herramienta de análisis estático de código que señala errores de programación, bugs, errores de estilo y estructuras sospechosas. El término lint proviene de una utilidad Unix que examina el código fuente del lenguaje C. Ayudan de varias formas. Primero, detectan potenciales errores antes de la ejecución. Por ejemplo, un linter podría señalar el uso de una variable indefinida o una función llamando con un número incorrecto de argumentos. También imponen estándares de codificación y mejores prácticas. Esto podría incluir reglas sobre la indentación, el uso de punto y coma, o la longitud máxima permitida de línea. Por último, ayudan a mantener la consistencia a lo largo de un código base, especialmente cuando varios desarrolladores trabajan en el mismo proyecto.
- Un linter popular para JavaScript es `ESLint`.
- Formateadores: son herramientas que formatean automáticamente tu código para adherirse a una guía de estilo específica. Mientras que los linters a menudo pueden corregir automáticamente algunos problemas, los formateadores están diseñados específicamente para reescribir tu código para coincidir con un estilo predefinido.
- Los formateadores aseguran un estilo de código consistente en todo el proyecto o equipo, independientemente de las preferencias del desarrollador individual. También ahorran tiempo y energía mental que de otro modo se gastaría en formateo manual. Por último, pueden hacer que las revisiones de código sean más eficientes al eliminar discusiones sobre el estilo de código.
- Un formateador popular para JavaScript es `Prettier`.
- Pueden incluirse en tu proceso de construcción o añadirse como plugins a tu editor de texto o IDE, proporcionando retroalimentación en tiempo real a medida que codificas. Usar linters y formateadores juntos puede mejorar significativamente la calidad y consistencia del código. Por ejemplo, podrías utilizar ESLint para detectar potenciales errores e imponer ciertas prácticas de codificación, y luego usar Prettier para manejar todas las tareas de formateo.
- Muchos equipos de desarrollo configuran estas herramientas como parte de su configuración de proyecto, a menudo con ganchos pre-commit que ejecutan el linter y el formateador antes de permitir que el código sea comprometido. Esto asegura que todo el código en el repositorio cumpla con los estándares del equipo para calidad y estilo.
- En resumen, los linters y formateadores son herramientas poderosas que ayudan a mantener la calidad del código, detectar posibles errores tempranos y asegurar la consistencia a lo largo de los códigos base. Automatizando estos aspectos de la revisión de código, permiten a los desarrolladores enfocarse más en resolver problemas y menos en debatir sobre el estilo del código.
---
### 