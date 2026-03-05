Estructura de red en la que clientes hacen peticiones de recursos o servicios a servidores que las procesan, devolviendo las respuestas requeridas a través de ciclos de comunicación estructurados. Los datos y servicios entregados a los clientes son controlados desde servidores, incrementando su seguridad y consistencia.

- El cliente, un dispositivo o una aplicación, envía una petición de servicio.
- El servidor, un sistema, permanece a la escucha respondiendo a peticiones enviando datos o accionando operaciones.

Tanto servidores como clientes hacen uso de sockets y protocolos de comunicación (TCP/IP, UDP...). Dependiendo del número de capas con las que cuente esta estructura, podemos encontrar:

- **Estructura de 2 capas**, idónea para aplicaciones pequeñas pero complicada de escalar cuando se esperan múltiples conexiones de clientes.
	- Capa de cliente y capa de servidor.
	- Cliente se ocupa de interfaz y puede realizar procesos antes de enviar las peticiones.
	- Servidor procesa peticiones y gestiona la base de datos.

- Estructura de 3 capas.
	- Capa de presentación (UI Cliente), capa de aplicación (Business), capa de datos (DB servidor).
	- El cliente interactúa con la capa de aplicación, que procesa la petición, aplica lógica de negocio y se comunica con la base de datos.
	- La base de datos NO está expuesta, añadiendo seguridad.
	- La más usada.


| VENTAJAS                                                                                                                                                                                                                                                                                                                   | DESVENTAJAS                                                                                                                                                                                                                                                                                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| + Gestión sencilla gracias a datos y servicios centralizados<br>+ Aumento de seguridad gracias a gestión de acceso.<br>+ Soporte a múltiples clientes simultáneos.<br>+ Mejor distribución de datos, que provienen de una sola fuente.<br>+ Aumenta la facilidad de mantenimiento gracias al desacoplamiento de las capas. | — Genera una dependencia en el servidor (Teoría del bus).<br>— Genera un cuello de botella si múltiples clientes envían peticiones al mismo tiempo.<br>— Requiere un coste de mantenimiento de un servidor que pueda responder a todas las peticiones y estar continuamente disponible.<br>— Requiere de conectividad a red constante.<br>— Requiere de backups, replicación y balance de carga. |
