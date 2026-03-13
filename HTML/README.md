# Curso HTML
- Acá tendré toda la información importante sobre el curso de HTML.
- HTML significa Hypertext Markup Language.
## Códigos HTML
- h1: son headings, van del h1 al h6.
- p: Parrafos.
```HTML
<h1>hola</h1>
<p>hola<p>
```
- para mostrar una imagen, necesitarás incluir un par de atributos dentro de tu elemento de imagen. Un atributo es un valor especial utilizado para ajustar el comportamiento de un elemento HTML.

```HTML
<img src="https://cdn.freecodecamp.org/curriculum/cat-photo-app/cats.jpg" />
```
- alt: sirve para proporcionar un texto descriptivo para las imágenes.
- atributos: va dentro de un elemento, dan información adicional.
- href: especifica la  URL de un enlace.
- target: especifica donde abrir el enlace.
```html
<a href="https://www.freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
```
- target="_blank": sirve para abrir el enlace en otra pestaña.
- checked: 
```html
<input type="checkbox" checked />
```
- con el checked marca la casilla, sin el checked no marca la casilla.
- input: sirve para recoger datos de los usuarios.
- type: especifica el tipo de input.
- disabled, readonly y reqquired son tipos de booleanos.
- disabled: deshabilita el input.
- link: sirve para enlazar hojas de estilo.
```html
<link rel="stylesheet" href="./styles.css" />
```
- rel: especifica la relación entre el recurso enlazado y el HTML.
- href: especifica la ubicación URL.
todo esto dentro de head.
---
- ejemplo Google Font:
```html 
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Playwrite+CU:wght@100..400&display=swap"
  rel="stylesheet"
/>
```
- preconnect: para atributo.
- rel: le dice al navegador que cree una conexion anticipada con el valor especificado en el atributo href.
acelera tiempos de carga de recursos externos.
---
```html

<link rel="icon" href="favicon.ico" />
```
- favicon: es la abreviatura de favorite icon, es un icono pequeño que se ve en a pestaña del navegador junto al título del sitio, muchos sitios lo usan para mostrar el icono de su marca.
---
- boilerplate: es una plantilla lista para la pagina web, incluye la estructura esencial del HTML.
DOCTYPE: le dice a los navegadores que versión de HTML se esta utilizando.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <!--Important metadata goes here-->
  </head>
  <body>
    <!--Headings, paragraphs, images, etc. go inside here-->
  </body>
</html>
```
- engloba todo el contenido y puede especificar el idioma de la pagina, dentro de HTML estará head y body.
head, tiene info importante detras

```html
 <head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Document Title Goes Here</title>
  <link rel="stylesheet" href="./styles.css" />
</head>
```
- meta: tiene detalles sobre la codificación de caracteres.
title: determina el texto en la pestaña o ventana del navegador.
- body: acá va todo el contenido.

```html

<body>
  <h1>I am a main title</h1>
  <p>Example paragraph text</p>
</body>

```
---
- UTF-8: almacena caracteres como datos, 1 byte = 8 bits, admite cada carácter en el conjunto cd caractares Unicode, incluye caracteres y símbolos.
```html
<meta charset="UTF-8" />
```
- admite tildes, "e"(é).
---
comentarios: 
```html
"<!-- Hola -->"
```
- Posicionamiento en buscadores (Search Engine Optimization - SEO).
---
- main: representa el contenido principal del cuerpo de un documento HTML, debe ser unico y no debe repetirse en el documento.
```html
<main></main>
```
---
- anidamiento: agregar dos espacios más a la derecha de donde estan anidados, como una sangría, que facilita la lectura del HTML.
- antes de 
```html
<a href=""></a>
```
puede haber texto para complementar el texto del link, además puede ir dentro de un parrafo (p).
---
- section: define las secciones en un documento.
- ul: unordered list, junto con "li" que es list(creo).
- ol: ordered list, junto con "li" acá muestra la lista en números.
- figure: representa contenido independiente y permite asociar una imagen a una descripción.
- figcaption: se utiliza para añadir una descripción para describir una imagen anidada en un elemento figure.
- em: enfásis en palabra especifica
- todos estos con: "<></>".
- strong: se utiliza para indicar una parte de un texto importante o urgente.
- footer: pie de pagina.
---
- div: es un contenedor para agrupar elementos, se usa para tener orden en el CSS.
- section: es semántico, el navegador captará su significado semántico y entenderá que debe tratarlo como una sección - en escritorios, móviles, lo que sea. Es parecido al div.
- id: proporciona una identificación única para poder usar en CSS O JavaScript, no puede tener espacios.
- En contraste con el atributo id, el valor del atributo class no necesita ser único y puede contener espacios.
- ¿cuándo debes usar un id en lugar de una clase? Las clases son mejores para usar cuando quieres aplicar un conjunto de estilos a muchos elementos. Si quieres un elemento específico, es mejor usar un id porque esos valores deben ser únicos.
---
- entidad html:es un conjunto de caracteres utilizados para representar un carácter reservado en HTML.

- Referencias de carácter nombradas:
```html
&lt;p&gt;learning is fun&lt;/p&gt; 
<p>learning is fun</p>
```
- si escribes esa primera linea de codigo, saldra ese texto.
- más simbolos numerico decimal:
&#60;
&#169;
&#174;
```html
&#60;
&#169;
&#174;
```
- más simbolos numerico hexadecimal: 
&#x3C;
&#x20AC;
&#x03A9;
```html
&#x3C;
&#x20AC;
&#x03A9;
```
---
- script: lee archivos de javascript externos, y permite programar javascript dentro de html
```html
<body>
  <script>
    alert("Welcome to README.md");
  </script>
</body>
```
- esto permite enlazar el html a un archivo javascript:
```html
<script src="path-to-javascript-file.js"></script>
```
- src: en este caso es para ubicar la ubicación del archvio.
---
- SEO:  Optimización para Motores de Búsqueda, hace que sea más visible y tenga mejor posición en motores de busqueda.
- Se usa meta para esto:
```html
<meta
  name="description"
  content="Discover expert tips and techniques for gardening in small spaces, choosing the right plants, and maintaining a thriving garden."
/>
```
- description: se asegura que los navegadores, motores de búsqueda y otras herramientas web interpreten correctamente este metadato.
- content: es donde colocarás tu descripción
---
- Opne graph: permite controlar cómo aparece el contenido de su sitio web en varias plataformas de redes sociales. Puede atraer usuarios a querer hacer clic e interactuar con su contenido. Puede establecer estas propiedades a través de una colección de elementos meta dentro de su sección head en HTML.

La primera propiedad de OG importante para incluir sería el title. Aquí hay un ejemplo de cómo establecer el OG titltle:
```html
<meta content="freeCodeCamp.org" property="og:title" />
```
- La siguiente propiedad de OG importante sería el type. Aquí hay un ejemplo de cómo usar el OG type 
```html
<meta property="og:type" content="website" />
```
- type: representa el tipo de contenido que se comparte en redes sociales.
- La tercera propiedad de OG importante sería el image. Aquí hay un ejemplo de cómo establecer el OG image:
```html
<meta
  content="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
  property="og:image"
/>
```
- La cuarta propiedad de OG importante sería el url. Aquí hay un ejemplo de cómo establecer el OG url:
```html
<meta property="og:url" content="https://www.freecodecamp.org" />
```
- Hay más propiedades de OG que puede establecer, como description, audio, video y locale. Sin embargo, el Open Graph url, image, type y title son las más importantes para incluir.
- audio: soporta formatos de audio populares como mp3, wav y ogg.
- video: soporta formatos mp4, ogg y webm.
```html
<audio src="https://cdn.freecodecamp.org/curriculum/js-music-player/cruising-for-a-musing.mp3"></audio>
```
- controls: atributo booleano que puede añadirse a un elemento para habilitar controles de reproducción integrados. Si se omite, no se mostrarán controles.
- loop: atributo booleano que hace que el audio se reproduzca continuamente.
- muted: Cuando está presente en el elemento audio, este atributo booleano iniciará el audio en un estado silenciado.
```html
<audio
  src="https://cdn.freecodecamp.org/curriculum/js-music-player/can't-stay-down.mp3"
  loop
  controls
  muted
></audio>
```
- Tipos de archivos de audio: hay diferencias en qué navegadores soportan qué tipo. Para acomodar esto, puedes usar elementos source dentro del elemento audio, y el navegador seleccionará la primera fuente que comprenda.
```html
  <source src="audio.ogg" type="audio/ogg" />
  <source src="audio.wav" type="audio/wav" />
  <source src="audio.mp3" type="audio/mpeg" />
</audio>
```
- El navegador empezará primero con el tipo ogg, y si no puede reproducir el audio, pasará al siguiente tipo en la lista.
- autoplay: hace que el video se reproduzca automáticamente. 
- Poster: Si deseas mostrar una imagen mientras el video se descarga.
- para diferentes navegadores:
```html
<video
  controls
  width="400"
  poster="https://peach.blender.org/wp-content/uploads/title_anouncement.jpg?x11217"
>
  <source
    src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.mp4"
    type="video/mp4"
  />
  <source
    src="https://archive.org/download/BigBuckBunny_124/Content/big_buck_bunny_720p_surround.webm"
    type="video/webm"
  />
  Your browser does not support the video tag.
</video>
```
