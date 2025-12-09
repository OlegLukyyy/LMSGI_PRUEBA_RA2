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


