Framework para desarrollar aplicaciones en Java de forma más simple, modular y desacoplada.
Se creo para reducir la complejidad de java en el ámbito empresarial, facilitar inyectar dependencias y mejorar los testeos y mantenimientos de aplicaciones. 

Sus características son:
- **Tecnologías**: como la inyección de dependencias, eventos, recursos, i18n, validación, enlace de datos, conversión de tipo, **SpEL**.
- **Acceso a datos**: soporte **DAO, JDBC, ORM, Marshalling XML**.
- **Gestión de transacciones**.
- **Integración**: comunicación remota, JMS, JCA, JMX, correo electrónico, tareas, programación, caché.
- **Pruebas (Testing)**: simulacro de objetos, el framework TestContext, Spring MVC prueba, WebTestClient.
- **Programación orientada a aspectos (AOP)**: permite la implementación de rutinas transversales.
- MVC (**Modelo Vista Controlador**).
- **Seguridad**.
- **Frameworks web**: Spring WebFlux y Spring MVC.
- **Procesamiento de datos por lotes**.
- **Administración Remota**: a través de este módulo se puede configurar la visibilidad y gestión de los objetos Java para la configuración local o remota vía JMX.
- Es un framework liviano debido a su implementación **POJO (Plain Old Java Object)**, Spring Framework no obliga al programador a heredar ninguna clase ni a implementar ninguna interfaz.

A destacar:
- La **Inyección de Dependencias (Dependency Injection)**: Al momento de escribir una aplicación Java compleja, las clases de la aplicación deben ser lo más independientes posible de otras clases Java, para aumentar la posibilidad de reutilizarlas y probarlas independientemente de otras clases, mientras se prueban las unidades. Básicamente la inyección de dependencias (**DI**) ayuda a unir estas clases y al mismo tiempo mantenerlas