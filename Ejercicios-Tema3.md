### Ejercicio 1: Buscar alguna demo interesante de Docker y ejecutarla localmente, o en su defecto, ejecutar la imagen anterior y ver cómo funciona y los procesos que se llevan a cabo la primera vez que se ejecuta y las siguientes ocasiones.

Primero se ha instalado Docker, cuyo proceso de instalación se encuentra en [este enlace](https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/instalacion_docker.md).

Se ha utilizado [el contenedor de ejemplo en el tema](https://hub.docker.com/r/jjmerelo/docker-daleksay/). En la primera ejecución, busca una imagen local que se llame **docker-daleksay**. Al no encontrarla, se descarga del *Hub* de Docker.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/tema3-image1.png" width="60%" height="60%">

En las siguientes ejecuciones, como la imagen ya se ha almacenado localmente no necesita descargársela de nuevo del *Hub* de Docker:

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/tema3-image2.png" width="60%" height="60%">

### Ejercicio 2: Tomar algún programa simple, “Hola mundo” impreso desde el intérprete de línea de órdenes, y comparar el tamaño de las imágenes de diferentes sistemas operativos base, Fedora, CentOS y Alpine, por ejemplo.

Se han ejecutado un simple ``echo Hello World!`` en cada uno de los sistemas operativos con las siguientes órdenes:

```docker run --rm alpine echo Hello World!```
```docker run --rm fedora echo Hello World!```
```docker run --rm centos echo Hello World!```

El tamaño de cada imagen es el siguiente:

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/tema3-image3.png" width="60%" height="60%">

**Centos** es la imagen que más pesa con 215MB, seguida de **Fedora** con un tamaño de 175MB. **Alpine** es, con diferencia, la imagen que menos pesa con solamente 5.57MB.

### Ejercicio 3: Crear a partir del contenedor anterior una imagen persistente con commit.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/tema3-image4.png" width="60%" height="60%">

### Ejercicio 4: Examinar la estructura de capas que se forma al crear imágenes nuevas a partir de contenedores que se hayan estado ejecutando.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/tema3-image5.png" width="75%" height="75%">