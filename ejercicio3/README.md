[TOC]

# Ejercicio 3 - imagen con Dockerfile - Aplicación web
## Usa un contenedor que ejecute una instancia de la imagen

## Coloca en el directorio raíz del servicio web ( /var/www/html ) un "sitio web" donde figure tu nombre el sitio deberá tener al menos un
archivo index.html sencillo y un archivo .css

![Captura de pantalla 2025-04-07 112247](./README.assets/Captura%20de%20pantalla%202025-04-07%20112247.png)

## 



![Captura de pantalla 2025-04-07 111938](./README.assets/Captura%20de%20pantalla%202025-04-07%20111938.png)

![Captura de pantalla 2025-04-07 111951](./README.assets/Captura%20de%20pantalla%202025-04-07%20111951.png)



## Coloca en ese mismo directorio raíz el siguiente script php , llámalo fecha.php
![Captura de pantalla 2025-04-07 111958](./README.assets/Captura%20de%20pantalla%202025-04-07%20111958-1744018050707-15.png)

## Ver la salida del script fecha.php y de la página index.html en el navegador

Construimos la imagen con el comando 

```docker build -t ejercicio3```

Ejecutamos el contenedor y aquí es donde voy a exponer el puerto 8000 como se indica en la tarea

```docker run -d --name ejercicio3 -p 8000:80 ejercicio3```



![Captura de pantalla 2025-04-07 113853](./README.assets/Captura%20de%20pantalla%202025-04-07%20113853.png)

En el navegador ponemos localhost:8000 y comprobamos que funciona correctamente

![Captura de pantalla 2025-04-07 113942](./README.assets/Captura%20de%20pantalla%202025-04-07%20113942.png)

![Captura de pantalla 2025-04-07 113949](./README.assets/Captura%20de%20pantalla%202025-04-07%20113949.png)

## Una vez creada la imagen, súbela a tu cuenta de Docker Hub

Debemos etiquetar la imagen ejercicio3 con mi nombre de usuario de docker hub más el nombre de la imagen

`docker tag ejercicio3 jalbertolv16/ejercicio3`

Realizamos el push

`docker push jalbertolv16/ejercicio3`

![Captura de pantalla 2025-04-07 114834](./README.assets/Captura%20de%20pantalla%202025-04-07%20114834.png)

## Borra la imagen de tu Docker local

`docker rmi jalbertolv16/ejercicio3`

![Captura de pantalla 2025-04-07 115647](./README.assets/Captura%20de%20pantalla%202025-04-07%20115647.png)

## Ejecuta un contenedor usando esa imagen

`docker run -d --name ejercicio3 -p 8000:80 jalbertolv16/ejercicio3`

para ello antes he parado el contenedor ejercicio3, lo he borrado también y por último he lanzado el contenedor de nuevo usando esa imagen con ese comando.

![Captura de pantalla 2025-04-07 121639](./README.assets/Captura%20de%20pantalla%202025-04-07%20121639.png)

Y comprobamos que efectivamente vuelve a funcionar

![Captura de pantalla 2025-04-07 121518](./README.assets/Captura%20de%20pantalla%202025-04-07%20121518.png)

![Captura de pantalla 2025-04-07 121527](./README.assets/Captura%20de%20pantalla%202025-04-07%20121527.png)

## creación de un nuevo contenedor con esa imagen y su ejecución. Cambia el puerto del contenedor, por ejemplo, - p 1234:80

``` Eliminar y detener contenedor en marcha
docker stop ejercicio3
docker rm ejercicio3

```

Lanzar el contenedor 

`docker run -d --name ejercicio3 -p 1234:80 jalbertolv16/ejercicio3`



![Captura de pantalla 2025-04-07 122339](./README.assets/Captura%20de%20pantalla%202025-04-07%20122339.png)

![Captura de pantalla 2025-04-07 122404](./README.assets/Captura%20de%20pantalla%202025-04-07%20122404.png)

![Captura de pantalla 2025-04-07 122410](./README.assets/Captura%20de%20pantalla%202025-04-07%20122410.png)

