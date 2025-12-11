# LMSGI_PRUEBA_RA2

## 1.A ¿Por qué NO se centra el texto del h1  en este caso? Explícalo con tus palabras.(por qué visual y estructuralmente no aparece centrado entre el borde izquierdo y el menú)

En este caso, el texto no se centra debido a que se emplea un justify-content: space-between;, cuando lo que debemos emplear un justify-content: center, para centrarlo.
Por otro lado, el (text-align: center;) no hace efecto debido a que actúa sobre la caja del texto, la cual lo cubre por completo, sin dar margen a centrarlo.

## 1B Ejercicio - Soluciona de dos formas diferentes

FLEXBOX: Empleamos en el selector site-header un justify-content para centrar el texto.
```
.site-header {
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  text-align: center;
}
```
GRID: empleando el place-items logramos centrar el texto con grid.
```
.site-header {
  display: grid;
  place-items: center;
}

h1 {
  text-align: center;
}
```

## 1.C Ejercicio – Convertir la cabecera en dos filas
Mediante el empleo de ´´´flex-direction: column;´´´ logramos centrar los elementos de forma vertical.

```
.site-header {
  display: flex;
  justify-content: center;
  flex-direction: column;
}

h1 {
  text-align: center;
}
.main-nav {
  text-align: center;
}
```

## 1.D Ejercicio – Dar relieve y separación visual al header

Para lograr este efecto, eliminamos los márgenes del body para eliminar el espacio que hay entre el header y los bordes de la web, cambiamos el color del fondo a traves de ´´´background-color: black;´´´, para evitar poder ver el texto cambiamos el color de texto a blanco a traves de "color" y empleamos un borde inferior para diferenciar claramente el header del contenido que iría abajo.
Por último, logramos la separación del contenido del header hasta sus extremos mediante el empleo de "padding" que nos permite agregar una especie de margen interno.

```
body {
  margin: 0;
}
.site-header {
  display: flex;
  justify-content: center;
  flex-direction: column;
  background-color: black;
  color: white;
  border-bottom: 5px solid gray;
  padding: 20px;
}

h1 {
  text-align: center;
}
.main-nav {
  text-align: center;
}
```


# 2. Reorganización del header con tres elementos
## 2.A Cambia tu HTML para introducir el botón dentro de header.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title></title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <header class="site-header">
      <button>btn</button>
      <h1>Mi Sitio Web</h1>

      <nav class="main-nav">...</nav>
    </header>
  </body>
</html>

```

## 2.B Indica el CSS necesario para maquetar este diseño usando:
Para lograr lo siguiente:
1. El botón está alineado a la izquierda.
2. El h1 está centrado entre el botón y el menú.
3. El nav está alineado a la derecha.

Implementamos un "justify-content: space-between;"
```
body {
  margin: 0;
  padding: 0;
}
.site-header {
  display: flex;
  align-items: center;
  background-color: black;
  color: white;
  border-bottom: 5px solid gray;
  padding: 40px;
  justify-content: space-between;
}

h1 {
  text-align: center;
}
.main-nav {
  text-align: center;
}
```
# 3.  Miniaturas, zoom y enlace a la imagen original
## 3.A Crear miniaturas
Establecemos una miniatura para las imágenes.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b63993dd-dc5e-49f6-a1ee-3ad9a664bdae" />


## 3.B Efecto hover
1. Código css:
<img width="250" height="79" alt="image" src="https://github.com/user-attachments/assets/507199af-38dc-409b-964e-be5789cd5945" />


2. Resultado:
Apreciamos que en la primera imagen se agranda el estilo y se aplica un border a la imagen, es en la que se encuentra posicionado el ratón
<img width="627" height="241" alt="image" src="https://github.com/user-attachments/assets/6d5e11c9-d97c-419c-bc65-71a7febb9465" />



## 3C. Enlace a la imagen original
Lo logramos mediante ```<a href="img/barbero1.jpg" target="_blank">```
<img width="450" height="492" alt="image" src="https://github.com/user-attachments/assets/28643573-bb5b-4902-a30c-2cd37d444b06" />

# Ejercicio 4 — Informe de Evidencias del Proyecto (Barbería Elite)
## 4.1. Introducción
  
La temática de la web es la de un negocio dedicado a la barbería, con un estilo minimalista, que trasmita confianza y profesionalidad. Para ello he incluido una seccion de presentación de la barbería, la carta de servicios disponibles, una galería de cortes, una sección de reservas y por último una presentación del personal de la barbería. Para ello, me he inspirado en diversas webs de barberías de éxito, como Barba y Cabello.
<img width="1920" height="992" alt="image" src="https://github.com/user-attachments/assets/72e5f913-289e-4032-a668-bc7b9f390fe4" />

## 4.2 Evidencias de HTML5
  
Header-> empleamos un menú fijo que permita mejor navegación y fluidez, junto al botón hamburguesa. 
<img width="1919" height="74" alt="image" src="https://github.com/user-attachments/assets/26e58802-1f09-49dc-bb13-6effc473a347" />

Main-> incluimos la presentación de la barbería, siendo una de las partes principales de la web.  
<img width="1920" height="345" alt="image" src="https://github.com/user-attachments/assets/c60ca5d5-3bcb-4a28-9f35-835eb062de1f" />

Section -> incluyo varias, como el equipo, la galería, los servicios, etc.  
<img width="1238" height="391" alt="image" src="https://github.com/user-attachments/assets/9372ba3d-c7d2-4189-a911-a387e30364ff" />

Footer -> incluimos un pie de página reservando los derechos de autor.  
<img width="1920" height="90" alt="image" src="https://github.com/user-attachments/assets/066a4c49-ef7e-49e4-bae1-e11d5cef2c65" />

Menú superior-> empleo un `<nav>` y `<a>` para permitir una mejor navegación  
<img width="566" height="74" alt="image" src="https://github.com/user-attachments/assets/97623d4c-2913-4c1e-baa4-2bc4d64a9de7" />

Menú lateral -> empleo la configuración proporcionada por Diego, junto al script al final del código  
<img width="271" height="993" alt="image" src="https://github.com/user-attachments/assets/62e47b0a-202d-40a0-ac8f-c59c6e4dadd0" />

Sección Hero -> presentación de la web  
<img width="1920" height="367" alt="image" src="https://github.com/user-attachments/assets/cad4f452-76ff-49a9-8ef0-a4913495f565" />

Tabla -> servicios de la barbería en formato tabla  
<img width="1238" height="391" alt="image" src="https://github.com/user-attachments/assets/efd2e3f5-db65-4cbf-8c5c-dd343cc0c127" />

Formulario -> reserva de citas con la obligación de rellenar todos los campos a través de `required`  
<img width="702" height="494" alt="image" src="https://github.com/user-attachments/assets/d96b773d-4595-480f-b21f-77a29a9faf70" />

Galería -> completamos con una serie de fotos de los cortes realizados en la barbería  
<img width="1358" height="628" alt="image" src="https://github.com/user-attachments/assets/8d17ae5b-0fc4-49e2-90ae-7a8abc4c67a4" />

Enlaces internos y externos -> los internos los utilizamos para la navegación y los exteriores hacia barberías clásicas que comparten estilo  
<img width="360" height="211" alt="image" src="https://github.com/user-attachments/assets/c3ffd348-d0e2-430b-81f8-24bffa06d22c" />

  ## 4.3 Evidencias de CSS
Selectores utilizados  
Selector descendente para aplicar un estilo específico al encabezado de la tabla.  
<img width="1198" height="310" alt="image" src="https://github.com/user-attachments/assets/9010e703-9ce9-4d08-bcae-d78389947624" />


```
table thead {
background: #1a1a1a;
color: #fff;
}
```

  Pseudoclases   
  Utilizados para cambiar el color de los enlaces de navegación y el fondo de las filas de la tabla al pasar el ratón.  
  <img width="358" height="77" alt="image" src="https://github.com/user-attachments/assets/b8d6e942-ce46-49a9-a922-7bb67db702c1" />

  ``` 
.main-nav a:hover {
color: #d4a574;
}
```
Flexbox  
Lo he utilizado para distribuir el logo y el menú de navegación principal de forma horizontal, centrada verticalmente y con espacio entre ellos.  
  ```
.header-content {
display: flex;
justify-content: space-between;
align-items: center;
}
```

Grid  
Para crear el layout principal de la sección Hero y otras secciones como la galería, equipo o contacto).  
```
.hero-content {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 40px;
}
```

Sombras  
Con el objetivo de mantener la estética opté por emplear un border en lugarde un box shadow, manteniendo el estilo minimalista original, a pesar de haberlo podido implementar con ayuda de alguna web como https://www.w3schools.com/  

```
.card {
background: #fff;
text-align: center;
padding: 20px;
border-radius: 8px;
}
```
Estilos de Menús  
Para los menús utilizo el color blanco sobre el fondo oscuro, junto al color dorado para destacar el estilo de la web.  
<img width="1640" height="68" alt="image" src="https://github.com/user-attachments/assets/4e35d72f-6201-46a1-be26-56a44afe5ba3" />

```
.main-nav a {
color: #fff;
text-decoration: none;
}
```
## 4.4. Fuentes utilizadas
En este caso, como he mencionado anteriormente el objetivo de la web es inspirar confianza a la clientela, lo hemos hecho a traves de la presentación de los barberos, pero también empleando la clásica fuente Arial, sans-serif. La psicología que perseguimos es crear una sensación de familiriarización con el posible cliente.  
<img width="495" height="45" alt="image" src="https://github.com/user-attachments/assets/1fc68dca-fa10-43ad-bed4-28310193c391" />

Sin embargo, de haberlo necesitado, importaríamos las fuentes de la siguiente forma:   
Fuente local:  
```
@font-face {
    /* Nombre que usaremos en el resto del CSS */
    font-family: 'BarberiaStencil'; 
    /* Ruta al archivo WOFF2 (formato recomendado) */
    src: url('/ruta de la fuente'); 
    font-weight: normal;
    font-style: normal;
}
```
o, en el html con google fonts y css:  
```
<head>
    <link 
      href="https://fonts.googleapis.com/css2?family=Anton&family=Montserrat:wght@300;400;600&display=swap"
      rel="styles"
    />
</head>
```
```
body {
    font-family: "Montserrat", sans-serif;
}
```
## 4.5. Menú lateral: breve explicación
<img width="316" height="517" alt="image" src="https://github.com/user-attachments/assets/6462115d-1b9e-43f9-a608-9c196f91f850" />

Se ejecuta una función en JavaScript, esta función añade o elimina la clase active tanto del menú lateral como del botón. Además, el texto del botón cambia de ☰ a ✖ para indicar que el menú está abierto.  
La clase que se añade o elimina es active.  
Al comienzo, el `side-menu` se ubica fuera del punto de vista de la web, y al presionar el botón pasa a la posición `right:0`, apareciendo por pantalla.


