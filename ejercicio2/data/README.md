[TOC]

# Ejercicio 2 - Docker Compose

## Explorar la imagen de la aplicación FileBrowser

![captura1](./README.assets/captura1.png)





![captura2](./README.assets/captura2.png)

![captura3](./README.assets/captura3.png)

![captura4](./README.assets/captura4.png)

Esto son los datos de los que vamos a sacar la información para realizar

De aquí debemos sacar la información:

- nombre de la imagen: hurlenko/filebrowser
- puerto : 8080
- volumenes: /data y /config

## Captura de pantalla y documento donde se vea el fichero dockercompose yaml que has creado.

![captura5](./README.assets/captura5.png)

A continuación creamos en un editor de texto el archivo .yaml con el que utilizaremos para lanzar el contenedor

Descripción: 

- versión  - Indica la versión del esquema Docker Compose
- filebrowser - Nombre del servicio
- image - es la imagen de Docker que usamos
- container_name - nombre que le damos al contenedor

- ports- indicas que puerto del contenedor se debe conectar a que puerto de la máquina
- volumes - Creas el vínculo entre carpetas locales y rutas dentro del contenedor con esto estamos realizando **bind-mount**
- restart: unless-stopped - reinicia este contenedor automáticamente si se apaga, a no ser que lo apague yo

A continuación en Git-Bash escrbimos el comando `docker compose up -d` para lanzar el contenedor por comandos



![captura6](./README.assets/captura6.png)

## Captura de pantalla donde se vean los volúmenes/carpetas donde se han almacenado los datos


Comprobamos que realmente se ven las carpetas donde se almacenan los datos

![captura7](./README.assets/captura7.png)

![captura8](./README.assets/captura8.png)

Podemos comprobar que efectivamente tenemos **data y config**

A continuación en el navegador escribimos localhost:8080 y entraremos en el panel de login de **FileBrowser** 

## Captura de pantalla donde se vea la aplicación funcionando, sube algún fichero, cambia el lenguaje a español...


![captura9](./README.assets/captura9.png)

Cambiamos el idioma a español

![captura10](./README.assets/captura10.png)

Creo un archivo en mi ordenador y a continuación en la flecha de subir de la aplicación exploro por mi ordenador hacia la ubicación del archivo y la subo



![Captura de pantalla 2025-04-07 094114](./README.assets/captura11.png)

![captura12](./README.assets/captura12.png)



Por último desde mi ordenador nos dirigimos a data para comprobar que efectivamente el archivo se ha guardado en data.

![captura14](./README.assets/captura14.png)

## Explicar brevemente cómo funciona esta aplicación y qué hace. 

Esta aplicación que esta creada con docker lo que permite no tenerla instalada en nuestro equipo sino acceder a ella desde el navegador, nos permite manejar archivos de nuestro equipo desde el navegador, lo que nos da muchas posibilidades,, ya que esto nos permite añadir , borrar o editar archivos desde cualquier otro dispositivo que este conectado a internet.

Con la configuración adecuada podríamos acceder a archivos subidos a FileBrowser desde nuestro móvil, en esta práctica los archivos se almacenan en carpeta local gracias al uso de bind-mounts.
