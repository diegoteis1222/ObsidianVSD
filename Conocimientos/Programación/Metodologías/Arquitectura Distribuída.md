Bajo la arquitectura distribuida, encontramos software desplegado entre múltiples nodos interconectados. Estos nodos pueden ser servidores físicos, virtuales, contenedores o funciones sin servidor como AWS Lambda o Azure Functions. La carga de trabajo de la aplicación es distribuida entre estos nodos con los siguientes objetivos en mente:

- Aumento de la escalabilidad, ya que añadir nodos no requiere afectar a los existentes.
- Tolerancia a errores, ya que si uno de los nodos falla, el resto pueden continuar operando independientemente.
- Capacidad de gestionar alto tráfico de volumen sin comprometer velocidad.

La filosofía es equivalente a [[Microservicios]], y es usada de manera ubicua en aplicaciones modernas. [[Arquitectura Cliente-Servidor]] es un tipo de arquitectura distribída; su forma más básica. Otras conocidas son...
- P2P, en la que cada nodo actúa como cliente y servidor al mismo tiempo.
- N-Capas (ver [[Arquitectura Cliente-Servidor]])
- Arquitectura Orientada a Servicios (SOA), en la que varios servicios reutilizables se comunican entre ellos a través de interfaces estandarizadas.
- Arquitectura Dirigida por Eventos (EDA), en la que distintos componentes reaccionan a eventos de forma asíncrona. 

##### COMUNICACIÓN
Hace uso de protocolos como REST (Represetntational State Transfer) o gRPC (Google Remote Procedure Call) para que los servicios puedan hacerse peticiones entre ellos. Existen también frameworks como Kafka o Rabbit MQ que se pueden considerar al uso.

##### COORDINACIÓN Y SINCRONIZACIÓN
Se utilizan técnicas como *elección de líder* (una de las máquinas coordina a otras), *consenso distribuído* (distintos servicios concuerdan en un estado compartido) y *bloqueos distribuidos* (previniendo accesos concurrentes a recursos).

##### GESTIÓN DE DATOS
Mención honorífica a la *replicación de datos* (mantener múltiples copias en distintos nodos por redundancia), *fragmentación/particionamiento* (división de datos) y a *BBDD* optimizadas para manejar datos segregados en distintas localizaciones. 

##### CARGA DE TRABAJO
Las arquitecturas distribuidas cuentan con sistemas cuyo único objetivo es distribuir la carga de trabajo, actuando de forma autónoma para distribuir peticiones entre distintos servicios. 

