## Ejercicio 3 - Redes

> Tarea realizada por: Pelayo de la Fuente Díaz

1. Crea una red bridge `redbd`

`docker network create redbd`

![](file:///C:/Users/alumno/Documents/PelayodelaFuente/DAW/ProyectoDespliegue/Ejercicio3_redes/imagenesRedes/imagen1.png)


2. Crea un contenedor con una imagen de `mariaDB` que estará en la red redbd. Este
contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306. (Es
necesario definir la contraseña del usuario root y un volumen de datos persistente)

`docker run -d --name contenedor_bd --network redbd -v /opt/mysql_bd:/var/lib/mysql -e MYSQL_PASSWORD=laboral -e MYSQL_ROOT_PASSWORD=laboral mariadb`

![](file:///C:/Users/alumno/Documents/PelayodelaFuente/DAW/ProyectoDespliegue/Ejercicio3_redes/imagenesRedes/imagen2.png)


3. Crear un contenedor con `Adminer` que se pueda conectar al contenedor de la BD

`docker run --link contenedor_bd:bd --network redbd -p 8080:8080 adminer`

![](file:///C:/Users/alumno/Documents/PelayodelaFuente/DAW/ProyectoDespliegue/Ejercicio3_redes/imagenesRedes/imagen3.png)


4. Comprobar que el contenedor Adminer puede conectar con el contenedor mysql abriendo
un navegador web y accediendo a la URL: `http://localhost:8080`

![](file:///C:/Users/alumno/Documents/PelayodelaFuente/DAW/ProyectoDespliegue/Ejercicio3_redes/imagenesRedes/imagen4.png)
