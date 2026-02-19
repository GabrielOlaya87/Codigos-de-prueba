# Códigos javascript

- Symbol: Crea etiquetas o identificadores únicos:

Symbol('mysymbol');

- BigInt: Para números muy grandes, se agrega una n al final.
```javascript
8372174328783289382n; (creo)
```
- Let: Sirve para declarar variables. Se puede declarar mas de una variable con el mismo nombre y diferentes valores.
```javascript
let age= 3;
console.log(age);
```
- Const: Igual que Let, pero no permite crear mas de una variable con el mismo nombre. Sin valor bota error.

---

## Concatenación:
- con el + se unen cadenas y variables:
```javascript
let firstName = "John";
let lastName = "Doe";

let fullName = firstName + " " + lastName; 
console.log(fullName); // John Doe
```
ese espacio entre las comillas es importante, ya que sin el, sería JohnDoe.

- usando el += sería así:
```javascript
let greeting = 'Hello';
greeting += ', John!';

console.log(greeting); // "Hello, John!"
```
- Concat(): 
```javascript
let str1 = 'Hello';
let str2 = 'World';

let result = str1.concat(' ', str2); 
console.log(result); // Hello World
```

---

## Console.log():

- Sirve para la depuración y verificación de código, registra texto o variables.
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
- //: Comentarios.
- Las variables no pueden comenzar con numeros deben iniciar con , _ , $ o letras.ni !, ni @, ni let, const, function o return.
- Cadenas: con Const = "hola"
- función:bloque de código reutilizable que realiza una tarea específica y puede ser llamado con varias entradas.
- Método:  tipo de función que está asociado con un objeto, lo que significa que opera sobre los datos contenidos en ese objeto.
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