---
layout: blog
title: AOS (Animate On Scroll) Libreria
date: 2021-05-29T16:59:17.298Z
tags:
  - Javascript
  - Libraries
  - html
  - css
  - Animations
---
![Potions Class](./img/aos.jpg)

Una libreria Javascript simple para añadir efectos al hacer scroll.

Lo primero que tenemos que hacer es descargarnos la librería y añadirla a nuestro proyecto, o tambien podemos añadirla con algun cdn (Content Delivery Network). [Desde el sitio oficial](https://michalsnik.github.io/aos/) podemos descargar los archivos *aos.css* y *aos.js* para incluirlos en nuestro sitio.

Si descargamos la libreria, la vamos a añadir a nuestro proyecto de la siguiente manera. Supongamos que la estructura de nuestro html es la siguiente:

```
├── css
└── aos.css
├── js
└── aos.js
├── index.html
├── style.css
```

```html
<html>
<head>
  <link href="css/aos.css" rel="stylesheet">  
</head>
<body>
<script src="js/aos.js"></script>
</body>
</html>
```

### ¿Carga mediante CDN?



```html
<html>
<head>
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">  
</head>
<body>
<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
</body>
</html>
```

Una vez que cargemos estos dos archivos vamos a inicializar el plugin. Este código puede estar dentro de la etiqueta body o en un archivo .js externo.

```javascript
<script>
  AOS.init();
</script>
</body>
```

De esta forma ya tenemos preparado nuestro entorno web para añadir animaciones AOS. Más adelante te explicaré que opciones o parámetros podemos modificar cuando inicializamos el plugin.

### ¿Cómo añado una animación a cualquier elemento de mi web?

Muy facil!. Imagínate que quieres añadir una animación a una etiqueta h1 y otra con algo más de retardo al párrafo. Este sería el código. El h1 aparecería desde abajo mientras que el párrafo de arriba a abajo porque tiene la animación fade-down.

```html
<div>
<h1 data-aos="fade-up">Animación al hacer scroll</h1>
<p data-aos="fade-down" data-aos-delay="1200">Creando animaciones al hacer scroll...<p>
</div>
```

Cómo ves la dinámica es la siguiente añadimos el atributo y valor *data-aos=»fade-up»* para especificar el tipo de animación ( de arriba a abajo). Y el atributo data-aos-delay=»1200″ para el retraso o delay. Este valor se escribe en milisegundos y en teste caso corresponde a 1.2 segundos.

Podemos añadir algunos atributos más para personalizar nuestras animaciones  y efectos.

### ¿Qué atributos podemos utilizar con AOS?

*data-aos="fade-up"*. Tipo de animación a aplicar\
*data-aos-offset="200″.* Delay o retardo de la animación.\
*data-aos-delay="50″*. Cuando  se dispara la animación. En este caso serían 50px antes de la parte superior del elemento\
*data-aos-duration="1000″*. Duración de  la animación.\
*data-aos-easing="ease-in-out"*. Tipo  de transición.\
*data-aos-once="true": Indicamos que la animación sólo se aplica una vez y no cada vez que nos desplazamos*\
*data-aos-anchor-placement="top-center". La posición desde la cual se aplica o se contabiliza el offset.*

### ¿Qué tipo de animaciones podemos añadir?

#### Fade animations:

* fade
* fade-up
* fade-down
* fade-left
* fade-right
* fade-up-right
* fade-up-left
* fade-down-right
* fade-down-left

<!--StartFragment-->

#### Flip animations:

* flip-up
* flip-down
* flip-left
* flip-right

#### Slide animations:

* slide-up
* slide-down
* slide-left
* slide-right

#### Zoom animations:

* zoom-in
* zoom-in-up
* zoom-in-down
* zoom-in-left
* zoom-in-right
* zoom-out
* zoom-out-up
* zoom-out-down
* zoom-out-left
* zoom-out-right
