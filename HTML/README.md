# Curso HTML
- Acá tendré toda la información importante sobre el curso de HTML.
- HTML significa Hypertext Markup Language.
## Códigos y info HTML Básico:
- h1: son headings, van del h1 al h6.
- p: Parrafos.
- elementos: son los bloques de construcción de un documento HTML. Representan encabezados, párrafos, enlaces, imágenes y más. Most HTML elements consist of an opening tag 
```html
<elementName>
and a closing tag 
</elementName>
```
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
- entidad html: es un conjunto de caracteres utilizados para representar un carácter reservado en HTML, como < y &.

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
---
- target: indica al navegador dónde abrir la URL del elemento anchor.
- Hay cuatro valores, cada uno con "_".
- _self: es el valor predeterminado. Esto abre el enlace en el contexto de navegación actual. En la mayoría de los casos, esto será la pestaña o ventana actual.
- _blank: abre el enlace en un nuevo contexto de navegación. Normalmente, esto se abre en una nueva pestaña. Pero algunos usuarios pueden configurar sus navegadores para abrir en una nueva ventana en su lugar.
- _parent: abre el enlace en el padre del contexto actual. Por ejemplo, si tu sitio web tiene un iframe, un valor de _parent en ese iframe se abriría en la pestaña/ventana de tu sitio web, no en el marco incrustado.
- _top: abre el enlace en el contexto de navegación más alto, piensa en "el padre del padre". Esto es similar a _parent, pero el enlace siempre se abrirá en la pestaña/ventana completa del navegador, incluso para marcos incrustados anidados.
- rutas absolutas: muestra la ubicación completa de un archivo dentro de un sistema de archivos y se usa comúnmente para recursos en una máquina local.  Comienza desde el directorio raíz, incluye todos los demás directorios y finalmente el nombre del archivo y la extensión. El 'directorio raíz' se refiere al directorio o carpeta de nivel superior en una jerarquía.
"/public/styles.css"
```html
<p>
  Read more on the
  <a
    href="/Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html"
    >About Page</a
    >
</p>
```
- URL absoluta en la barra de direcciones del navegador: file:///Users/user/Desktop/fCC/script-code/absolute-vs-relative-paths/pages/about.html,
ncluye información de acceso, como el protocolo y, para recursos web, el nombre de dominio, que indica al navegador cómo y dónde recuperar el recurso.
- rutas relativas: especifica la ubicación de un archivo en relación con el directorio del archivo actual. No incluye el protocolo ni el nombre de dominio, haciéndolo más corto y más flexible para enlaces internos dentro del mismo sitio web. "./script.js"
- Camino: es una cadena que especifica la ubicación de un archivo o directorio en un sistema de archivos. 
---
- rutas de archivos: /public/logo.png, ./script.js, o ../styles.css.
- barra: puede ser una barra invertida (\) o una barra diagonal (/) dependiendo de tu sistema operativo, "separador de rutas".
- punto: señala el directorio actual.
- dos puntos: señalan el directorio padre.
- Ruta relativa al directorio padre: "../src/nav.html"
- Los links tienen 5 tipos diferentes para estar.
- :link: Representa un enlace que el usuario no ha visitado. Proporciona los estilos base para todos los enlaces de tu página. Los demás estados se construyen sobre él.
- :visited: se aplica cuando un usuario ya ha visitado la página a la que se enlaza. Por defecto, esto convierte el enlace en púrpura, pero puedes usar CSS para proporcionar una indicación visual diferente al usuario.
- :hover: Se aplica cuando un usuario está pasando el cursor sobre un enlace. Es útil para proporcionar atención extra a un enlace, para asegurar que un usuario realmente tiene la intención de hacer clic en él.
- :focus: Se aplica a enlaces que están siendo activados por el usuario. Esto típicamente significa hacer clic en el enlace con el botón principal del mouse haciendo clic izquierdo, en la mayoría de los casos. Este estado puede ser útil para mostrar a un usuario que el elemento en el que hicieron clic es interactivo.
- Cuando uses estos estados para estilizar tus enlaces, hay un orden específico en el que necesitas escribir tu CSS: link, visited, hover, focus, luego active.
- asi van:
```html
<head>
    <link href="styles.css" rel="stylesheet" />
</head>

<body>
    <a href="https://freecodecamp.org" target="_blank">Visit freeCodeCamp</a>
</body>
```
```css
a:active {
  color: black;
}
```
- &amp;: ampersand.
- &lt;: menor que.
- &mdash;: guión largo.
```html
&amp;
&lt;
&mdash;
```
---
- og:title: Establece el título que se muestra para las publicaciones en redes sociales.
- og:type: Representa el tipo de contenido que se comparte en redes sociales. Ejemplos de este contenido incluyen artículos, sitios web, videos o música.
- og:image: Establece la imagen que se muestra para las publicaciones en redes sociales.
- og:url: Establece la URL a la que los usuarios harán clic para las publicaciones en redes sociales.
---
## HTML Semántico:
- son el significado de las palabras o frases en un idioma. En HTML, que es un lenguaje, los elementos también tienen su propio significado semántico. De hecho, puedes pensar en tu documento HTML como lo harías con un documento de texto. Y al igual que un documento de texto, puedes tener encabezados, imágenes, texto en negrita y otro formato.
- El significado semántico de un elemento se refiere a qué información especial transmite ese elemento. El significado semántico de un elemento p, por ejemplo, es un párrafo de texto.
- div no tiene.
- usarlo garantizará la mejor experiencia para usuarios con tecnologías de asistencia como lectores de pantalla. Pero también, el HTML semántico puede mejorar tu posicionamiento en buscadores. Esto se refiere a la optimización para motores de búsqueda, o SEO, puede mejorar tu experiencia de desarrollo.
- jerarquía estructural: h1 a h6, en ese orden, mejora el SEO, mejora la navegación y el entendimiento.
- HTML presentacional: se centra en la apariencia y el estilo del contenido. 
- font: Elemento obsoleto que se usa para establecer el tamaño y el color de la fuente del texto.
- center: Otro elemento obsoleto que se usa para centrar el contenido horizontalmente dentro de su contenedor.
- big: Otro elemento obsoleto de HTML presentacional que hace que el texto incluido sea un nivel más grande que el texto circundante.
- El HTML semántico es ahora la práctica recomendada. Describe el contenido de los elementos, por lo que es mucho más fácil de leer, entender y mantener.
---
- Elementos HTML semánticos: 
- main: se usa para contener el contenido principal de la página web
- header: para definir el encabezado del documento o sección.
- sección de navegación, nav: para secciones con enlaces de navegación.
- section: para agrupar información relacionada.
- figure: para ilustraciones y diagramas.
- HTML semántico describe el contenido, mientras que HTML presentacional se enfoca en la apariencia.
- texto idiomático, i: originalmente se utilizaba para propósitos presentacionales para mostrar el texto en cursiva. Pero ahora, se usa frecuentemente para resaltar voz o estado de ánimo alternativos, términos idiomáticos de otro idioma, términos técnicos y pensamientos.
```html
<p>There is a certain <i lang="fr">je ne sais quoi</i> in the air.</p>
```
- elemento que llama la atención, b: resalta palabras clave en resúmenes, o nombres de productos en reseñas. Normalmente, los navegadores muestran este texto en negrita.
- Strong VS elemento que llama la atención: Si necesitas enfatizar la importancia del texto, debes usar el elemento strong en lugar del b. Mientras el "b" solo atrae atención al texto, sin indicar un alto nivel de importancia, el elemento strong hace más que eso. Conlleva un sentido de importancia o urgencia. Esta es su principal diferencia, para elegir entre ellos, considera el propósito del texto y su importancia dentro del contenido circundante.
- listas de descripción: son perfectas para presentar términos y definiciones en un formato organizado y fácil de leer, como en un glosario, o un diccionario real, donde puedes encontrar palabras con sus definiciones correspondientes.
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
  <dt>CSS</dt>
  <dd>Cascading Style Sheets</dd>
  <dt>JS</dt>
  <dd>JavaScript</dd>
</dl>
```
- dl: es el contenedor para toda la lista.
- dt: para cada término. En este caso, la lista de descripción tiene dos términos, HTML y CSS.
- dd: para la descripción, o detalles asociados con ese término.
- CSS: Cascading Style Sheets.
---
- citas en bloque: representa una sección citada de otra fuente. Se usa principalmente para citas extensas. Si la fuente de la cita tiene una dirección, puedes citarla con el atributo cite. El valor de este atributo debe ser una URL válida. 

```html
<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  "Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?"
</blockquote>
```
- Aunque este atributo no cambia la presentación de la cita en bloque, es muy útil para dar a los lectores de pantalla y motores de búsqueda más información sobre la cita.
```html
<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  <p>Build your projects. Show them to your friends. Build projects for your friends.</p>
  <p>Build your network. Help the people you meet along the way. What goes around comes around. You'll get what's coming to you.</p>   
  <p>It is not too late. Life is long.</p>
  <p>You will look back on this moment years from now and be glad you made a move.</p>
</blockquote>
```
- blockquote: hace que se vea la cita en bloque.
- q: pone comillas a la cita que deseas. Se usa para distinguir el texto citado del contenido circundante.
- ¿Cuál es la diferencia entre citas en bloque y en línea? Debes usar citas en bloque para citas extensas de otras fuentes y citas en línea para citas breves de otras fuentes que deberían formar parte de párrafos existentes.
---
- aberviaturas en html: acrónimos e inicialismos.
- abbr: para marcar aberviaturas.
```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.</p>
```
---
- direcciones html: es como un section o div, pero de contacto.
```html
<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```
- br: salto en linea.
- tel:+ dentro del atributo href crea un enlace clicable para iniciar una llamada telefónica en ciertos dispositivos que soportan eso.
- mailto se usan en documentos HTML para permitir que los usuarios abran un nuevo correo electrónico en su cliente de correo preferido.
- Uno de los inconvenientes de usar un enlace mailto es que los usuarios a menudo lo perciben como spam. Desafortunadamente, muchos spammers usarán esta opción para enviar correos electrónicos a los usuarios. Así tener en cuenta eso cuando se use.
---
- horas y fechas:
```html
<p>The reservations are for <time datetime="20:00">20:00 </time></p>
```
- time: representa las 20 horas
- datetime: traduce fechas y horas a un formato legible.
```html
<p>
  The graduation will be on <time datetime="2024-06-15T15:00">June 15</time>
</p>
```
- La primera parte de ese valor es el año, mes y día. La T mayúscula es un separador entre la fecha y la hora.
- ISO 8601: es un estándar internacional para representar fechas y horas.
---
- ecuaciones matemáticas y fórmulas químicas: 
- superíndice: es un símbolo o letra impresa por encima de la línea normal de texto.
```html
<p>2<sup>2</sup> (2 squared) is 4.</p>
```
- sup: el número 2 está envuelto en etiquetas sup para representar el superíndice dentro del párrafo.
- Los casos de uso comunes para el elemento superscript incluirían exponentes, letras superiores y números ordinales. 
- sub: para ilustrar que el carácter debe ser un subíndice, muestra una línea de base más baja usando texto más pequeño.
- casos de uso comunes para el elemento subíndice incluyen fórmulas químicas, notas al pie y subíndices de variables.
---
- representación de código de computadora en html: 
```html
<p>
  To set the text color to blue in CSS, use the following code:
  <code>color: blue;</code>
</p>
```
- code: muestra el código en la página, ejemplos cortos.
- elemento de texto preformateado:
```html
<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>
```
- pre: (texto preformateado) tener cuidado con espacios porque se mostrará exactamente como está escrito dentro del documento HTML, para fragmentos de código más largos.
---
- U, S y Ruby:
- elemento de anotación no articulada, u: Sólo debe utilizarse para indicar que se ha aplicado una anotación no textual al texto.
```html
<p>
  You can use the unarticulated annotation element to highlight
  <u>inccccort</u> <u>spling</u> <u>issses</u>.
</p>
```
- El elemento de tachado, s: Debería usarse para representar cuando un texto ya no es preciso ni relevante.
```html
<p><s>Tomorrow's hike will be meeting at noon.</s></p>

<p>Due to unforeseen weather conditions, the hike has been canceled.</p>
```
- ruby: epresenta texto pequeño que se muestra arriba o debajo del texto principal. Se utiliza principalmente para mostrar la pronunciación de caracteres del este asiático.
```html
<ruby> 明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp> </ruby>
```
- rp: elemento de paréntesis de respaldo de ruby, se utiliza como respaldo para navegadores que no tienen soporte para mostrar anotaciones ruby.
- rt: elemento de texto ruby, se utiliza para indicar texto para la anotación ruby. Este texto suele usarse para detalles de pronunciación o traducción en la tipografía del este asiático.
- Aunque el elemento ruby puede usarse para otros tipos de anotaciones, el caso de uso más común es para la tipografía del este asiático.
---
- nav: se utiliza para proporcionar enlaces de navegación a otras secciones en el documento u otras secciones en el sitio web. Muchas veces verás el elemento nav utilizado para menús o tablas de contenido.
```html
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```
- article: representa contenido autocontenido en una página web.
---
## Forms y tablas:
- form: recopila información del usuario, como nombres y correos electrónicos.
```html
<form method="POST" action="url-goes-here">
  <!-- input elements go here -->
   <input type="text" />
</form>
```
- action: Especifica dónde se enviarán los datos del formulario al enviarlo. 
- method: se utiliza para especificar el método HTTP a usar al enviar los datos del formulario. Los métodos más comunes son GET y POST.
- input: recopila información específica, como nombres y correos electrónicos.
- type: define el tipo de dato que se espera del usuario. En este caso, los datos serían texto plano.
- checkbox: tipo caja para seleccionar.
```html
<form action="">
  <label>
    Full Name:
    <input type="text" />
  </label>
</form>
```
- label: añade una etiqueta para la entrada.
- Al anidar un input dentro de un elemento label, se crea una asociación implícita entre la label y el campo de input. El término "implícito" se refiere a algo que se entiende o infiere sin necesidad de expresarlo o definirlo explícitamente con atributos o elementos adicionales. Para asociar explícitamente una label con un input, se puede usar el atributo for.
```html
<form action="">
  <label for="email"> Email Address: </label>
  <input type="email" id="email" placeholder="ejemplo@email.com"/>
</form>
```
- Al usar una asociación explícita, los valores para los atributos for e id deben ser los mismos. En este caso, los valores se establecen ambos en email. El tipo email en la entrada proporciona una validación básica para direcciones de correo electrónico correctamente formateadas.
- placeholder: Si deseas mostrar sugerencias adicionales a los usuarios sobre la entrada esperada.
---
- button se utiliza para realizar una acción particular cuando se activa. 
- type: Controla el comportamiento del botón cuando se activa. El primer valor posible para el atributo type sería el tipo button
```html
<button>Start Game</button>
<button type="button">Show Alert</button>
```
- submit: envia el form.
- reset: reinicia el form.
```html
<form action="">
  <label for="email">Email address:</label>
  <input type="email" id="email" name="email" />
  <button type="reset">Reset form</button>
  <button type="submit">Submit form</button>
</form>
```
- con javascript para interactividad:
```html
<button type="button">Show Alert</button>
<script src="index.js"></script>
```
```javascript
const btn = document.querySelector("button");
btn.addEventListener("click", () => alert("You clicked on the alert button"));
```
```html
<input class="start-btn" type="button" value="Start Game" />
<script src="index.js"></script>
```
```javascript
document.addEventListener("DOMContentLoaded", () => {
  const btn = document.querySelector(".start-btn");
  btn.addEventListener("click", () => {
    const paraEl = document.createElement("p");
    const bodyEl = document.querySelector("body");

    bodyEl.appendChild(paraEl);
    paraEl.textContent = "The game has started!!!";
  });
});
```
- value: muestra el texto del botón.
- input: elementos vacios, no pueden tener nodos hijos, como texto, y solo puede tener una etiqueta de inicio.
- button: ofrece más flexibilidad porque puedes anidar texto, imágenes e íconos dentro de él.
---
- ¿Qué es la validación de formularios del lado del cliente en formularios HTML, y cuáles son algunos ejemplos?:
- lado del cliente: se refiere a todo lo que ocurre en el servidor, la computadora, o sistema que aloja el sitio web o aplicación. Esto incluye el procesamiento de datos, la ejecución de aplicaciones y la gestión de requests que provienen del dispositivo del usuario.
- required: especifica que el usuario necesita completar esa parte del formulario antes de que se envíe.
```html
<form action="">
  <label for="email">Email Address (Required field):</label>
  <input required type="email" name="email" id="email" minlength="4" maxlength="64"/>
  <button type="submit">Submit Form</button>
</form>
```
- Otra ventaja de usar el input de correo electrónico es que los inputs de correo tienen una validación básica para asegurar que las direcciones de email estén correctamente formateadas. Por ejemplo, si escribes palabras al azar y haces clic en enviar, el navegador mostrará una alerta indicando que falta un signo @.
- minlength y maxlength: se utilizan para establecer la longitud mínima y máxima en caracteres para la entrada de correo electrónico. Si no incluyes la longitud mínima o superas la longitud máxima de caracteres, el navegador mostrará un mensaje de alerta.
---
- estados del form: 
- por defecto: en una entrada de dirección de correo electrónico es un campo en blanco.
- enfocado: Cuando el usuario hace clic en un control de formulario o lo selecciona con la tecla Tabulador del teclado. Cuando una entrada está en este estado, la mayoría de los navegadores mostrarán un borde azul resaltado alrededor de la entrada. Pero puedes optar por añadir estilos adicionales en CSS.
- desactivado: Este estado muestra a los usuarios que un campo de entrada no se puede enfocar ni activar.
- solo lectura: Es cuando un control de formulario, como una entrada, no es editable por el usuario. 
```html
<input disabled type="email" name="email" id="email" />
<input
  readonly
  type="email"
  name="email"
  id="email"
  value="example@email.com"
/>
```
- disabled: no deja escribir.
- value: se utiliza para establecer el valor que se muestra dentro del campo de entrada.
- readonly: solo deja leer.
- fieldset: hace el cuadro de afuera del form.
- legend: pone un texto en la linea de arriba del cuadro de afuera del form.
- size: ancho de texto.
- 
```html
<main>
  <form method="POST" action="https://hotel-feedback.freecodecamp.org">
    <fieldset>
      <legend>Personal Information</legend>
    </fieldset>
  </form>
</main>
```
- El atributo name se usa para identificar los datos del formulario después de que se han enviado al servidor.
- Los elementos input pueden tener un atributo size. Este atributo define el número de caracteres que deberían ser visibles mientras el usuario escribe en el input. El valor de size debe ser un entero no negativo mayor que cero. Si no se especifica size, o se especifica con un valor no válido, el input tendrá el ancho predeterminado establecido por el navegador.
- type="number": tipo numerico.
- los atributos min y max se usan para establecer los valores mínimo y máximo que se pueden ingresar en el campo de entrada. En tipo numerico.
- type="radio": Un control de formulario que permite al usuario seleccionar una sola opción de un grupo predefinido. 
- select: menú que abre con multiples opciones
- option: opciones de lo de arriba.
- selected: el predeterminado en un grupo predefinido.
- textarea: es un control de entrada de texto de varias líneas que permite a los usuarios ingresar texto que es más largo que una sola línea. Se puede usar para crear una caja de comentarios, una entrada de mensaje u otras entradas de texto que requieran múltiples líneas.
- rows: se usa para especificar la altura visible del textarea.
- cols: se usa para especificar el ancho visible del textarea
---
- tablas html:
```html
<table id="quickfacts">
  <thead>
    <tr>
      <th colspan="2">Quick Facts: Software Developers, Quality Assurance Analysts, and Testers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>First Row</th>
      <td>
        First Data Cell
      </td>
    </tr>
    <tr>
      <th>Second Row</th>
      <td>
        Second Data Cell
      </td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>The footer of this table, which might contain date of publication, author credits, or other meta information.</th>
    </tr>
  </tfoot>
</table>
```
- table con un id establecido como quickfacts.
- thead: elemento de encabezado.
- tbody: cuerpo de tabla.
- tfoot: pie de tabla.
- tr: filas de tabla. 
- th: encabezado de tabla, etiqueta datos en fila.
- td: cierta cantidad de celdas de datos individuales, llamadas datos de tabla.
- Hoy en día, los desarrolladores usan CSS flexbox y grid para estructurar sus diseños.
- caption: define el título o descripción de una tabla, mejorando la accesibilidad y semántica.
- colspan: especifica el número de columnas que debe abarcar una celda.
---
- HTML es un lenguaje muy indulgente; los elementos se renderizan incluso cuando cometes errores, como olvidar incluir una etiqueta de cierre. Esto ocurre porque los navegadores utilizan un algoritmo de análisis que maneja errores comunes e intenta renderizar el HTML lo más cercano posible a la intención del autor. Pero esto podría resultar contraproducente a veces. 
- validador de HTML: es una herramienta que verifica la validez de tu código HTML con respecto a las especificaciones estándar de HTML. Te ayuda a identificar errores y advertencias en tu código HTML, asegurando que tus páginas web estén estructuradas correctamente y cumplan con los estándares web. beneficia no solo a ti y tus futuras revisiones de código, sino también a cualquier otra persona que revise tu código, como tus compañeros de equipo y colaboradores de código abierto.
- Existen varios validadores de HTML que puedes utilizar. El más ampliamente aceptado es el servicio de validación de marcas w3.org. Cuando visites el sitio validator.w3.org, puedes hacer clic en el botón Validate by Direct Input y pegar tu código HTML.
- Al hacer clic en el botón Check, se mostrará una lista de resultados con los errores que deben corregirse. 
- Otro validador de HTML que puedes usar es jsonformatter.org. Puedes copiar y pegar tu código HTML dentro del primer editor, y al hacer clic en el botón Validate, te mostrará cualquier error que tengas en tu código.
- DOM y DevTools. depuración y construcción de proyectos:
- corregir estos errores se conoce como depuración. Para depurar tu código, necesitarás usar algunas herramientas proporcionadas por tu navegador. Dos herramientas importantes a utilizar serían el inspector de DOM y las herramientas de desarrollador.
- El inspector de DOM te permite inspeccionar la estructura HTML de la página en la que estás. DOM significa Modelo de Objeto del Documento. Es una estructura en forma de árbol que representa los elementos de una página. Aprenderás más sobre el DOM en módulos posteriores.
- Las herramientas de desarrollador te permiten inspeccionar el HTML, CSS y JavaScript de la página en la que estás.
- Para abrir las herramientas de desarrollador en tu navegador, puedes hacer clic derecho en la página y seleccionar Inspeccionar. También puedes usar Control Shift I en tu teclado PC.
- Cuando abres las herramientas de desarrollador en Google Chrome, verás una serie de pestañas. La primera pestaña se llama pestaña Elementos. Esta pestaña te muestra la estructura HTML de la página en la que estás. La segunda pestaña se llama pestaña Consola. Esta pestaña te muestra cualquier error que pueda estar ocurriendo en la página.
- En la situación donde tengas un enlace roto, puedes revisar la consola para ver los mensajes de error de ese enlace roto. El mensaje común que continúa mostrando para el enlace roto es el error 404. El error 404 indica que la página no se encuentra.
## accesibilidad:
- implica crear productos y servicios que todos puedan usar. En el contexto del desarrollo web, se trata de hacer sitios que todos puedan entender e interactuar con ellos, incluidas las personas con discapacidades visuales, auditivas, motoras y cognitivas. Algunos ejemplos de discapacidades que pueden afectar la experiencia en línea incluyen:
Ceguera, Baja visión, Daltonismo, Sordera, Dificultad para usar teclados, ratones o pantallas táctiles, Trastornos de atención, Problemas de memoria, Dificultad al hablar o comprender el lenguaje hablado, Sensibilidad a las luces intermitentes.
- Para ayudarte a crear sitios accesibles, el World Wide Web Consortium, conocido como W3C, desarrolló un conjunto de estándares internacionales que puedes seguir para hacer que tus páginas sean más accesibles y fáciles de usar para personas con discapacidades. Estos estándares se conocen como las "Pautas de Accesibilidad para el Contenido Web" (WCAG).
- Estas pautas están diseñadas teniendo en cuenta cuatro principios básicos, conocidos como POUR:
- P representa Perceptible. Los usuarios deben poder percibir la información que estás presentando. Por ejemplo, puedes proporcionar texto alternativo para las imágenes, de modo que los usuarios que acceden a tu sitio web con un lector de pantalla puedan entenderlas.
- O representa Operable. Los usuarios deben poder interactuar con la interfaz de usuario. Por ejemplo, puedes asegurarte de que toda la funcionalidad sea accesible a través del teclado también, no solo con el ratón.
U-  representa Comprensible. Los usuarios deben poder entender la información. Por ejemplo, puedes evitar oraciones complejas y usar un lenguaje simple tanto como sea posible.
- R representa Robusto. Una amplia gama de navegadores y otras herramientas, incluidas las tecnologías asistivas, deben poder interpretar el contenido.
---
- lectores de pantalla:  son herramientas tecnológicas de asistencia que ayudan a las personas ciegas y con discapacidad visual a utilizar ordenadores y dispositivos móviles. Aparte del texto a voz y la salida en braille, otras características notables de los lectores de pantalla son las ayudas de navegación y asistencia de navegación web.
- Los ordenadores con Windows tienen Narrador incorporado. Puedes activarlo presionando WIN + CTRL + ENTER. NonVisual Desktop Access (NVDA) y Job Access With Speech (JAWS) también están disponibles para ordenadores con Windows. NVDA es gratuito y de código abierto, mientras que JAWS es de pago.
- Los teléfonos Android tienen TalkBack incorporado. Puedes activarlo accediendo a Settings > Special Function > Accessibility > Talkback.
- texto braille y gran impresion: Están diseñados para usuarios con discapacidades visuales. En los teclados de texto grande, también llamados teclados de gran impresión, son más grandes en comparación con los teclados estándar. Este diseño es útil para personas que pueden encontrar difícil ver el texto pequeño en las teclas. La mayoría de ellos también tienen un contraste y brillo mejorados.
- Los teclados braille proporcionan una experiencia completamente táctil para personas con discapacidades visuales más severas, incluidas las personas ciegas.
- El braille es un sistema táctil de lectura y escritura. Consiste en puntos en relieve dispuestos en patrones específicos para representar letras, números y puntuación.
- Los teclados braille usan este sistema para ayudar a los usuarios a encontrar las teclas correctas en el teclado sintiendo estos patrones con sus dedos. Las teclas tienen puntos en relieve en patrones que representan letras, números y símbolos.
- Y algunos teclados combinan ambos enfoques: fuentes grandes y patrones braille en las teclas. Esto es útil para personas con discapacidades visuales y para quienes están aprendiendo braille.
- dispositivos de apuntado alternativos como trackballs, joysticks y touchpads:
- son buenas alternativas al ratón tradicional. Son esenciales para mejorar la accesibilidad informática para personas con discapacidades, problemas de antebrazo y movilidad limitada.
- magnificadores de pantalla: son herramientas que ayudan a las personas con baja visión y otras deficiencias visuales a acceder mejor al contenido digital y la web. Profundicemos en qué son estas herramientas y el papel que desempeñan en la accesibilidad del contenido digital. Los magnificadores de pantalla funcionan ampliando textos, gráficos y otros elementos en la pantalla de una computadora o dispositivo móvil. Muchos magnificadores de pantalla permiten a los usuarios ampliar la pantalla en más del 200%. Luego, los usuarios pueden navegar por la página utilizando su dispositivo apuntador o teclado. Además, la mayoría de los magnificadores ofrecen porcentajes de zoom personalizables y otras características en sus configuraciones. ayudan principalmente a las personas con baja visión a leer textos, ya que las fuentes pequeñas en documentos o aplicaciones pueden ser un desafío para ellos. 
- los desarrolladores de software deben hacer que sus productos digitales sean accesibles para personas con baja visión. Algunas consideraciones incluyen: Usar fuentes escalables para que el usuario pueda cambiar el tamaño de la página sin romper el diseño.
Garantizar que la interfaz de usuario se adapte a diferentes tamaños de pantalla a través del diseño receptivo. Usar esquemas de color de alto contraste y colores personalizables. Implementar una barra de navegación no pegajosa y pequeña para que los usuarios aún puedan ver contenido al usar magnificadores. Usar texto HTML regular en vez de imágenes de texto. Proporcionar comentarios directamente junto al elemento que lo activa, y más.
- software de reconocimiento de voz: ayuda a las personas con discapacidades a interactuar con computadoras y otros dispositivos digitales. permiten a las personas con discapacidades usar su voz para dar comandos para realizar diversas tareas en lugar de usar dispositivos de entrada tradicionales como teclados y ratones. Esto incluye escribir correos electrónicos y otros documentos, navegar por la web y controlar dispositivos inteligentes del hogar. 
- herramientas comunes para auditar la accesibilidad: es una aplicación que te ayuda a mejorar la accesibilidad de tu contenido digital al reportar problemas de accesibilidad que se pueden encontrar fácilmente mediante pruebas automatizadas. 
- Google Lighthouse: verificador de métricas web popular que puedes usar directamente en Chrome DevTools o en línea. Esto significa que no solo puedes verificar sitios web en vivo, sino también aquellos desarrollados localmente. Las métricas que puedes verificar incluyen accesibilidad, SEO, mejores prácticas y rendimiento. Para usar Lighthouse, abre tus DevTools presionando F12 y cambia a la pestaña Lighthouse. Selecciona las métricas que deseas verificar, elige el dispositivo en el que deseas probar y haz clic en el botón "Analyze page load". Aparecerá una puntuación de accesibilidad después de que termine la verificación, junto con una lista de problemas que necesitan ser corregidos. Si deseas métricas más fiables, considera usar la versión web. La desventaja es que no admite pruebas en sitios web locales. Puedes acceder a la versión web en pagespeed.web.dev.
- WAVE es otro verificador de accesibilidad confiable que puedes usar como extensión de Chrome o en la web. Todo lo que necesitas hacer es ingresar el URL de tu sitio web y se generará un informe de accesibilidad completo para ti. Este informe incluye características de accesibilidad implementadas, ARIA y contrastes.
- El IBM Equal Accessibility Checker es otra herramienta robusta para mejorar la accesibilidad de contenido digital. Con él, puedes escanear tus sitios web para detectar problemas de accesibilidad y generar un informe detallado.
- IBM Accessibility Checker como extensión de Chrome, descárgalo desde la tienda web de Chrome. Abre tus DevTools presionando F12 y selecciona la pestaña "Accessibility Checker" ubicada en el panel Elementos. Haz clic en el botón de escanear para iniciar la revisión y se generará un informe para ti. Puedes exportar el informe como una hoja de cálculo y un archivo HTML haciendo clic en el botón "Exportar XLS".
---
- ¿Cómo afecta la estructura adecuada de niveles de encabezado a la accesibilidad?: El uso adecuado de los encabezados crea una jerarquía visual para que los usuarios naveguen y comprendan tu página web. El uso de una jerarquía de encabezados lógica permite a los usuarios de lectores de pantalla comprender la estructura de tu contenido y navegar rápidamente por él. Crear un texto de encabezado adecuado que describa con precisión el contenido que sigue ayuda a todos a encontrar la información que necesitan en tu sitio. Como beneficio adicional, los encabezados bien formados también pueden mejorar el SEO de tu sitio.
---
- mejores prácticas para tablas y accesibilidad: Mientras que una persona vidente puede comprender las relaciones en esta tabla, asociar los valores con sus encabezados resulta mucho más difícil para las personas que usan lectores de pantalla para navegar por la tabla. La primera mejor práctica que cubriremos es el uso de leyendas (caption) para las tablas. Puedes escribir la leyenda (o título) de una tabla, para que los usuarios, especialmente aquellos que utilizan tecnologías de asistencia, puedan comprender rápidamente el propósito y contenido de la tabla. Debes colocar el elemento caption inmediatamente después de la etiqueta de apertura del elemento table. De esta manera, los lectores de pantalla y otras tecnologías de asistencia pueden ofrecer más contexto anunciando primero la leyenda antes de leer el contenido.
- Los encabezados son celdas especiales, que típicamente se encuentran al inicio de una fila o columna, que describen el tipo de datos almacenados en la fila o columna. Puedes definir un encabezado de fila o columna con el elemento de encabezado de tabla, th.
```html
<table>
  <caption>Our Pets</caption>
  <thead>
    <tr>
      <!-- Column Headers -->
      <th>Name</th>
      <th>Age</th>
      <th>Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Nora</th> <!-- Row Header -->
      <td>5</td>
      <td>Dog</td>
    </tr>
    <tr>
      <th>Gino</th> <!-- Row Header -->
      <td>2</td>
      <td>Cat</td>
    </tr>
  </tbody>
</table>
```
- Observa que el código anterior tiene un elemento caption inmediatamente después del elemento table. Luego, dentro del elemento thead del encabezado de la tabla, están los encabezados de columna (Nombre, Edad, y Tipo ). En la segunda y tercera filas, dentro del elemento tbody, encontramos los datos de cada una de nuestras mascotas. Los nombres de las mascotas son los encabezados de fila porque están dentro de los elementos de encabezado de tabla (th). Asociar las celdas de datos con sus correspondientes encabezados también es muy importante para los lectores de pantalla. 
- atributo scope: determina si un encabezado es un encabezado de fila o de columna. Los lectores de pantalla pueden adivinar esto correctamente a partir de la estructura de la tabla, pero generalmente se recomienda indicar explícitamente el scope para asegurar claridad. scope tiene cuatro valores posibles. Los dos valores que usarás más a menudo son:
- col: para columna.
- row: para fila. 
Los tres encabezados de columna (Nombre, Edad, y Tipo) tienen un scope de col, columna.
Los dos encabezados de fila (Nora y Gino) tienen un scope de row.
```html
<table>
  <caption>Our Pets</caption>
  <thead>
    <tr>
      <!-- Now they have scope -->
      <th scope="col">Name</th>
      <th scope="col">Age</th>
      <th scope="col">Type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Nora</th>
      <td>5</td>
      <td>Dog</td>
    </tr>
    <tr>
      <th scope="row">Gino</th>
      <td>2</td>
      <td>Cat</td>
    </tr>
  </tbody>
</table>
```
```html

```