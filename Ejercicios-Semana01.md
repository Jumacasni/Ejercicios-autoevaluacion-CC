### Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?

Como aplicación he elegido ImagymBot, que fue mi TFG del Grado en Ingenieria Informática en el curso 2019-2020. ImagymBot es un bot de Telegram que puede ser utilizado por los usuarios de un gimnasio para anotar sus rutinas y entrenamientos, llevar un registro de su peso, y varias funciones más. Su documentación y código se encuentra en este link de Github: https://github.com/Jumacasni/TFG-ImagymBot-UGR

El patrón que usa es una arquitectura en capas. Consta de 3 capas: una capa de presentación (usuarios de Telegram), una capa de negocio (servidor donde se almacena el bot), y una capa de datos (servidor de la base de datos). En la siguiente imagen se muestra un esquema de cómo quedaría esta arquitectura.

![](https://github.com/Jumacasni/Ejercicios-autoevaluacion-CC/blob/main/images/image1.png)

Para evolucionar a un patrón tipo microservicio, deberíamos desplegar de forma independiente tanto el servidor del bot como el servidor de la base de datos. Tendríamos un núcleo principal que se encarga de recibir y enviar peticiones de los dos servicios y responder a los distintos eventos que realizan los usuarios.

### En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?

ImagymBot está programado en Python y su base de datos en MySQL.

En esta aplicación solo hay un servicio que almacena el bot de Telegram, con lo cual sólo se tiene un lenguaje de programación. En el caso de haber tenido más servicios, si se podrían haber usado diferentes lenguajes, como JavaScript.

En cuanto a los almacenes de datos, lo más conveniente sería usar NoSQL, como por ejemplo MongoDB. De esta forma se ahorraría mucho espacio en el almacenamiento de estos datos.
