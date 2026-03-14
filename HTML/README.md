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
---
- Formas de optimizar: Usar WEBP o AVIF en vez de PNG o JPG.
- propiedad intelectual: Estan protegidas por derechos de autor. 
- No puedes usarlas a menos que hagas esto: obtener permiso por escrito del titular de los derechos de autor, comprar una licencia del titular de los derechos de autor, o incorporar la imagen de manera que se clasifique como uso legítimo.
Ese tercer punto es complicado. El uso legítimo requiere que tu uso de la imagen sea tanto limitado como transformador. Algunos ejemplos de uso legítimo serían comentar o revisar el arte o crear una parodia de la imagen.
- Algunas imágenes pueden estar bajo una licencia permisiva, como una licencia Creative Commons, o la licencia BSD que usa freeCodeCamp. Estas imágenes están disponibles para su uso en tu sitio web, pero deberás leer la licencia para comprender las reglas que debes seguir al usar estas imágenes.
- Finalmente, algunas imágenes pueden estar liberadas al dominio público. No tiene derechos de autor y es libre de ser usada sin restricciones. Las imágenes específicamente licenciadas bajo la licencia Creative Commons 0 se consideran de dominio público.
- La mayoría de los motores de búsqueda te permitirán filtrar los resultados de imágenes por licencia. También existen sitios como Pixabay y Unsplash, que ofrecen imágenes de libre uso. Siempre ten en cuenta los derechos de autor y la licencia cuando uses una imagen en tu sitio web.
---
- PNG Y JPG: formatos de imagen rasterizados, osea, se basan en píxeles, con los datos rastreando el valor de color en cada píxel.
- SVG: gráfico vectorial escalable, rastrea datos basados en trazos y ecuaciones para trazar puntos, líneas y curvas. Se puede escalar a cualquier tamaño sin afectar la calidad, almacena datos en XML, es programable en HTML.
```html
<svg width="100" height="100" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
  <circle cx="50" cy="50" r="45" stroke="yellow" stroke-width="3" fill="blue" />
  <circle cx="35" cy="40" r="5" fill="black" />
  <circle cx="65" cy="40" r="5" fill="black" />
  <path d="M35 65 Q50 80 65 65" stroke="black" stroke-width="4" fill="transparent" />
</svg>
```
- svg: contiene todo el dibujo, circulos, lineas, etc.
- circle: crea cara y ojos.
- path: dibuja la sonrisa, crea una linea curva.
- Font awesome: tiene muchos íconos de este estilo.
- viewbox: ontrola qué parte de la imagen es visible dentro del SVG.
```html
<svg viewBox="0 0 50 50">
</svg>
```
- Los dos primeros números (0 0) establecen la posición inicial del viewBox: la esquina superior izquierda (x e y).
Los siguientes dos números (50 50) definen el ancho y alto del viewBox.
---
- elemento reemplazado: Su contenido es determinado por un recurso externo en lugar de por el CSS mismo, puede controlar la posición o el diseño de un elemento. Pero su CSS no puede modificar directamente el contenido de ese elemento.
- Incluyen los elementos de imagen, iframe y video.
- iframe: embeds an external site on your web page, youtube, mapas:
```html
<iframe
  title="Map of the Royal Observatory, Greenwich, London"
  width="300"
  height="200"
  src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&amp;layer=mapnik">
</iframe>
```
- El elemento en sí es reemplazado por el objeto externo: el sitio. Su CSS puede cambiar la posición del sitio incrustado, pero no puede modificar el contenido del sitio.
- Hay otros elementos reemplazados, como video y embed. Y algunos elementos se comportan como elementos reemplazados en circunstancias específicas:
```html
<input type="image" alt="Descriptive text goes here" src="example-img-url">
```
- Este tipo de input se considera un elemento reemplazado, pero otros tipos de input como text o email no son elementos reemplazados.
---
- iframe: Este elemento representa un marco en línea. Se usa para incrustar otro contenido HTML directamente dentro de la página HTML. Ese contenido HTML podría ser un video, un mapa, otro elemento HTML o incluso otras páginas web.
```html
<iframe
  width="400"
  height="400"
  src="https://www.youtube.com/embed/PkZNo7MFNFg?si=-UBVIUNM3csdeiWF"
  title="Learn JavaScript - Full Course for Beginners (YouTube video)"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  referrerpolicy="strict-origin-when-cross-origin"
  allowfullscreen
></iframe>
```
- allowfullscreen: permite al usuario mostrar en modo de pantalla completa.
- es una buena práctica especificar un atributo title para el iframe, ya que es importante para la accesibilidad.
- allow: Permite definir lo que un iframe puede o no puede hacer. Esto se llama una lista de permisos. Los elementos en una lista de permisos pueden separarse por puntos y comas o espacios, y ambos pueden usarse juntos.
- Si desea incrustar HTML directo dentro del elemento iframe, debe usar el atributo srcdoc.
- accelerometer: permite que el iframe use sensores de movimiento para que pueda detectar cosas como la inclinación y rotación del dispositivo. 
- autoplay: permite que el video comience a reproducirse automáticamente.
- clipboard-write: permite que el iframe escriba datos en el portapapeles del usuario.
- encrypted-media, gyroscope y web-share: Estos tres permitirán el uso de extensiones de medios cifrados para proteger el video, otorgar acceso a los sensores de movimiento y orientación del dispositivo, y permitir compartir el contenido del iframe a través de los diálogos nativos de compartir del dispositivo.
- referrerpolicy: Es la regla que determina cuánta información compartes cuando tu página se conecta a otra página.
- strict-origin-when-cross-origin: Esto comparte la dirección completa en el mismo sitio, solo el nombre del sitio en otros sitios, y nada en sitios inseguros.

