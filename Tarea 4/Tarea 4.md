# Docker

Instalamos docker-compose para poder realizar dicha acción.

```bash
apt install docker-compose
```

![](assets/captura1.png)

Subimos la imagen a nuestro propio repositorio en [hub.docker.com]()

![](assets/captura2.png)

Estructura del documento docker-compose.yml

![](assets/captura3.png)

Ejecutamos el comando cmatrix (En mi caso, me funciono de dos maneras diferentes)

```bash
docker compose run cmatrix cmatrix
```

```bash
docker-compose run cmatrix cmatrix
```

![](assets/captura4.png)

Ejecutamos el comando greenrain

```bash
docker compose run cmatrix greenrain
```

![](assets/captura5.png)

Lo que hace, es simular el efecto Matrix en la terminal