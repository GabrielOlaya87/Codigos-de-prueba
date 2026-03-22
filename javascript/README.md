# Curso JavaScript
- Acá tendré toda la información importante para repaso sobre JavaScript.
## Códigos javascript
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
- 