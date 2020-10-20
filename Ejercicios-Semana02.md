### Ejercicio 1: Instalar alguno de los entornos virtuales de node.js (o de cualquier otro lenguaje con el que se esté familiarizado) y, con ellos, instalar la última versión existente, la versión minor más actual de la 4.x y lo mismo para la 0.11 o alguna impar (de desarrollo).

Se ha elegido **nave** como entorno virtual. Se han instalado las versiones 0.11.16, 4.9.1 y 14.13.1.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image1.png" width="60%" height="60%">

### Ejercicio 2: Crear una descripción del módulo usando package.json. En caso de que se trate de otro lenguaje, usar el método correspondiente.

Para crear una descripción del módulo usando Nodejs se usa la orden `npm init`. Se siguen los pasos que aparecen en la terminal y se genera automáticamente el fichero **package.json**.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image2.png" width="60%" height="60%">

### Ejercicio 4: Para la aplicación que se está haciendo, escribir una serie de aserciones y probar que efectivamente no fallan. Añadir tests para una nueva funcionalidad, probar que falla y escribir el código para que no lo haga. A continuación, ejecutarlos desde mocha (u otro módulo de test de alto nivel), usando descripciones del test y del grupo de test de forma correcta. Si hasta ahora no has subido el código que has venido realizando a GitHub, es el momento de hacerlo, porque lo vamos a necesitar un poco más adelante.

Se han creado dos nuevas apuestas de igual contenido, con dos aserciones que verifican que se han creado correctamente y que la salida de la función `as_string` es correcta, respectivamente. También se han añadido dos nuevas aserciones que verifican que `apuesta2` y `apuesta3` tienen el mismo contenido, y que `nueva_apuesta` y `apuesta2` tienen un contenido diferente. En las dos siguientes imágenes se puede comprobar esto.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image3.png" width="60%" height="60%">

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image4.png" width="60%" height="60%">

A continuación, en `Apuesta.js` se ha creado una nueva función que devuelve los goles de la apuesta en formato string y con un espacio en blanco añadido, tal y como es muestra en la siguiente imagen.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image5.png" width="60%" height="60%">

Se ha añadido un nuevo test que testea la función `goles_string`. Se ha creado una nueva apuesta y, usando `assert`, se ha testeado que el resultado es el esperado.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image6.png" width="60%" height="60%">

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image8.png" width="60%" height="60%">

Se puede ver en las dos imágenes anteriores que el test ha fallado porque en el assert se ha indicado que se espera como salida un string "0-1", pero la función `goles_string` en realidad devuelve "0-1 " (un espacio adicional).

Al cambiar el assert, se ejecuta **Mocha** de nuevo y se puede ver que pasa los test perfectamente.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image7.png" width="60%" height="60%">

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image9.png" width="60%" height="60%">

### Ejercicio 5: Haced los dos primeros pasos antes de pasar al tercero (integración continua).

Los dos pasos a realizar son:

1. Darse de alta. Muchos están conectados con GitHub por lo que puedes usar directamente el usuario ahí. A través de un proceso de autorización, acceder al contenido e incluso informar del resultado de los tests.

2. Activar el repositorio en el que se vaya a aplicar la integración continua. Travis permite hacerlo directamente desde tu configuración; en otros se dan de alta desde la web de GitHub.

Se ha activado Travis en [este repositorio](https://github.com/Jumacasni/Gestion-porras-futbol). Se ha añadido un archivo **.travis.yml** con la configuración que se muestra en la siguiente imagen.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image10.png" width="60%" height="60%">

En la página de Travis se puede comprobar que se ha ejecutado el código del archivo **.travis.yml** con éxito, tal y como se muestra en la siguiente imagen.

<img src="https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/semana2-image11.png" width="80%" height="80%">
