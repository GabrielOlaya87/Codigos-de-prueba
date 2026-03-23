# Códigos-de-prueba
Códigos de prueba.

#### css extra
```css
/* Ocultar checkbox */
#menu-toggle {
  display: none;
}

/* Imagen hamburguesa */
.menu-icon img {
  width: 30px;
  cursor: pointer;
}

/* Menú lateral oculto */
.menu {
  position: fixed;
  top: 0;
  left: -250px; /* escondido fuera de la pantalla */
  width: 250px;
  height: 100%;
  background: #444;
  list-style: none;
  padding: 20px;
  display: flex;
  flex-direction: column;
  gap: 15px;
  transition: left 0.3s ease; /* animación suave */
}

/* Mostrar menú cuando el checkbox está activo */
#menu-toggle:checked ~ .menu {
  left: 0; /* aparece desde la izquierda */
}

.menu li a {
  color: white;
  text-decoration: none;
}
```
#### JavaScript de prueba
```js
console.log("Hi there!");

const botName = "teacherBot";

const greeting = `My name is ${botName}.`;
console.log(greeting);

const subject = "JavaScript";
const topic = "strings";

const sentence = `Today, you will learn about ${topic} in ${subject}.`;
console.log(sentence);

const strLengthIntro = `Here is an example of using the length property on the word ${subject}.`;
console.log(strLengthIntro);

console.log(subject.length);

console.log(`Here is an example of using the length property on the word ${topic}.`);
console.log(topic.length);

console.log(`Here is an example of accessing the first letter in the word ${subject}.`);

console.log(subject[0]);

console.log(`Here is an example of accessing the second letter in the word ${subject}.`);
console.log(subject[1]);

console.log(`Here is an example of accessing the last letter in the word ${subject}.`);

const lastCharacter = subject[subject.length - 1];
console.log(lastCharacter);

const learningIsFunSentence = "Learning is fun.";

console.log("Here are examples of finding the positions of substrings in the sentence.");

console.log(learningIsFunSentence.indexOf("Learning"));

console.log(learningIsFunSentence.indexOf("fun"));
console.log(learningIsFunSentence.indexOf("learning"));

console.log("I hope you enjoyed learning today.");
```