[TOC]

#  Ejercicio1 - Contenedores en red y Docker Desktop

               ## 1. Crea una red bridge redej1

Tal y como se indica en la tarea para facilitar la tarea hemos descargado la extensión "PortNavigator", en ella vamos a crear la red  **redej1**



![Captura de pantalla 2025-04-05 204926](./README.assets/Captura%20de%20pantalla%202025-04-05%20204926.png)

## 2. Crea un contenedor con una imagen de mariaDB que estará en la red redej1

En la imagen mariadb, le damos a Run para crear el contenedor añadiendo el nombre del contenedor, las variables el puerto tal y como se indica en la tarea

![Captura de pantalla 2025-04-05 205811](./README.assets/Captura%20de%20pantalla%202025-04-05%20205811.png)

Aquí podemos comprobar que efectivamente se esta ejecutando el contenedor creado

![Captura de pantalla 2025-04-05 221739](./README.assets/Captura%20de%20pantalla%202025-04-05%20221739.png)

Ahora lo conéctatenos con la extensión **PortNavigator** haciendo clic en la red **redej1** añadir contenedor.

![Captura de pantalla 2025-04-05 222030](./README.assets/Captura%20de%20pantalla%202025-04-05%20222030.png)

A continuación creamos el script SQL con los nombres de los módulos que se están estudiando



![Captura de pantalla 2025-04-05 223558](./README.assets/Captura%20de%20pantalla%202025-04-05%20223558.png)

## 3. Crear un contenedor con Adminer o con phpMyAdmin que se pueda conectar al contenedor de la BD

Buscamos la imagen adminer



![Captura de pantalla 2025-04-05 223951](./README.assets/Captura%20de%20pantalla%202025-04-05%20223951.png)

hacemos el pull para descargarla y de nuevo le damos en la imagen a Run y desplegamos para rellenar el formulario

![Captura de pantalla 2025-04-05 224533](./README.assets/Captura%20de%20pantalla%202025-04-05%20224533.png)

De nuevo hacemos clic en **PortNavigator** y a la red redej1 le añadimos el contenedor que acabamos de crear

![Captura de pantalla 2025-04-05 224623](./README.assets/Captura%20de%20pantalla%202025-04-05%20224623.png)

## 4. Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal

A continuación entramos desde el navegador poniendo **localhost:8080**  y nos saldrá el panel de adminer

![Captura de pantalla 2025-04-05 224841](./README.assets/Captura%20de%20pantalla%202025-04-05%20224841.png)

Lo rellenamos con el nombre de las variables que asignamos, y servidor mariadb-ejercicio1 que es como lo hemos nombrado

![Captura de pantalla 2025-04-05 224932](./README.assets/Captura%20de%20pantalla%202025-04-05%20224932.png)

En la imagen siguiente pegamos el script que realizamos con las consultas para la base de datos que cree la tabla módulos e inserte el nombre de los módulos que estamos estudiando

![Captura de pantalla 2025-04-05 225059](./README.assets/Captura%20de%20pantalla%202025-04-05%20225059.png)

Ejecutamos

![Captura de pantalla 2025-04-05 225127](./README.assets/Captura%20de%20pantalla%202025-04-05%20225127.png)

Y podemos comprobar que se a ejecutado con éxito de esta manera comprobamos que hemos accedido a adminer con éxito , se ha creado la tabla módulos, e insertamos los registros solicitados.



## ![Captura de pantalla 2025-04-06 180737](./README.assets/Captura%20de%20pantalla%202025-04-06%20180737.png)



## 5. Instala la extensión Disk Usage , muestra el espacio ocupado, borra algo...

Entramos en Containers, y paramos uno de los contenedores, para a a continuación eliminarlo, seguidamente en Images hacemos los mismo con la imagen que se uso para crear el contenedor borrado.

En las dos siguientes capturas se puede apreciar el antes y después en Disk usage del borrado.



![Captura de pantalla 2025-04-06 181610](./README.assets/Captura%20de%20pantalla%202025-04-06%20181610.png)

![Captura de pantalla 2025-04-06 182114](./README.assets/Captura%20de%20pantalla%202025-04-06%20182114.png)

![Captura de pantalla 2025-04-06 182128](./README.assets/Captura%20de%20pantalla%202025-04-06%20182128.png)

![Captura de pantalla 2025-04-06 182210](./README.assets/Captura%20de%20pantalla%202025-04-06%20182210.png)

A continuación se eliminara los contenedores, la red y los volúmenes utilizados

![Captura de pantalla 2025-04-06 190533](./README.assets/Captura%20de%20pantalla%202025-04-06%20190533.png)

![Captura de pantalla 2025-04-06 190431](./README.assets/Captura%20de%20pantalla%202025-04-06%20190431.png)

![Captura de pantalla 2025-04-06 190541](./README.assets/Captura%20de%20pantalla%202025-04-06%20190541.png)

![Captura de pantalla 2025-04-06 190552](./README.assets/Captura%20de%20pantalla%202025-04-06%20190552.png)