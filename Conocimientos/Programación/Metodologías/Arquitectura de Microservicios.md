El tratar aplicaciones como microservicios es un enfoque arquitectónico que divide aplicaciones en funciones específicas de menor complejidad, bajo acoplamiento y alta cohesión que se pueden comunicar entre ellas a través de APIs o servicios web. **Esta estructura contrapone la estructura monolítica.**

### Características principales
- Descentralización de datos, ya que cada uno contiene su base de datos, evitando una capa de datos centralizada.
- Resiliencia, ya que si un servicio falla, el sistema no se detiene por completo.
- Aumento de agilidad, ya que permiten a varios equipos desarrollar independientemente diferentes servicios.
- Escalabilidad flexible, ya que sólo se deben de escalar las partes específicas de la aplicación que se encuentren bajo demanda.
- Desacoplamiento de tecnologías, ya que distintos microservicios que operan de forma independiente no tienen por qué hacer uso del mismo stack.

### Desafíos
- Alta complejidad operativa, ya que requiere de una infraestructura de conexión y workflow avanzada.
- Improbable consistencia de los datos, que pueden sufrir modificaciones indeseadas a través de distintas transacciones.
- Latencia, ya que la comunicación entre sistemas puede aumentar el tiempo de procesamiento. 

### Ejemplos reales
#### Amazon
En el año 2000, la web de Amazon era monolítica, diseñada en distintas capas con alto acoplamiento que causaban que el lifecycle de desarrollo se ralentizase notablemente, hasta el punto en el que se detectó la necesidad/problema ([[ADKAR]]).

Para resolver este cuello de botella, fragmentaron las capas del monolito en distintos servicios a los que asignaron distintos equipos de desarrolladores. Tras hallar esta solución, desarrollaron AWS, de la que no hay mucho más que decir. 

#### Spotify
Cuando su cuota de usuarios aumentó entorno a los 170 millones, Spotify decidió liberar a desarrolladores de capas de mantenimiento comenzando a migrar sus servicios a la nube de Google. 

Este cambio no fue sencillo ya que con una simple migración cada microservicio acabaría con 10 o más dependencias, en un total de 1200 microservicios donde la latencia se convertiría en un grave problema. Tras migrar el tráfico de usuarios directamente a la web, copiaron todos sus datos existentes a la nube, donde opera en BigQuery con más de 10 millones de queries al mes.



