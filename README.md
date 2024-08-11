# Taller-Clean-Code
# Como el codigo limpio ayuda a mejorar nuestros proyectos

A la hora de programar es extremadamente importante que todas las personas involucradas en un proyecto puedan facilmente comprender las funciones que el codigo esta ejecutando, por lo general los programadores dejan comentarios describiendo las funciones que sus metodos cumplen en el programa, pero esto muchas veces no es sufienciente, codigo que solo puede ser comprendido por su autor es perjudicial tanto para la estabilidad y mantenimiento a largo plazo de un proyecto, en estas instancias y en general es muy importante implementar el **codigo limpio**.

El codigo limpio a grandes rasgos se basa en crear metodos pequeños que solo cumplan una funcion en lugar de un metodo que innecesariamente realize muchas pequeñas tareas.

Si por ejemplo tenemos un metodo para crear un usuario en una plataforma, este a la hora de ejecutarse realiza las siguientes funciones:
1. Recibir el correo, usuario y contraseña de la cuenta a crear.
2. Realiza una peticion a la base de datos para verificar si no existe una cuenta con el usuario y/o correo ingresado.
- De no encontrar ninguna coincidencia
3. Realizar una peticion a la base de datos para registrar la cuenta con los datos ingresados.
4. Por ultimo, enviar al cliente una alerta de que su cuenta ha sido registrada exitosamente.

Como podemos ver cada una de las funciones ejecutadas por este metodo son bastante extensas y que todas estas sean realizadas en un mismo lugar puede ser perjudicial para nuestro programa.

Siguiendo los principios del codigo limpio, para realizar esta misma tendriamos que crear un metodo para cada funcion diferente, a su vez, tambien tendriamos que crear un metodo general que contenga los 4 metodos anteriores y la informacion ingresada por el usuario, este pasara dicha informacion a los metodos segun estos la necesiten.

Estos cambios no solo nos ayudaran con la cohesion del codigo. si no que tambien hace que estos metodos puedan ser usados en otras situaciones en las que sus funciones necesiten ser usadas sin tener que reescribirlos una y otra vez, creando una base solida que puede ser reutilizada la cantidad de veces que sea necesaria. 
