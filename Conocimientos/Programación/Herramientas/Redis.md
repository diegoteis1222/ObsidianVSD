Redis (Remote Dictionary Server) es una base de datos NoSQL de código abierto, en memoria, de tipo clave-valor, reconocida por su extrema velocidad y baja latencia (microsegundos) al no depender de discos. Se utiliza principalmente como caché, gestor de sesiones y almacén de estructuras de datos en tiempo real.

Características clave:

- **En memoria** (in-Memory): Almacena datos en la RAM, lo que proporciona una rapidez superior a las bases de datos tradicionales que usan discos.

- **Estructuras Clave-Valor**: Almacena información con una clave única asociada a un valor (que puede ser cadenas, listas, conjuntos, hashes, etc.).

- **Persistencia**: Aunque trabaja en memoria, permite configuraciones para guardar datos en disco de forma periódica o secuencial, ofreciendo un equilibrio entre velocidad y durabilidad

- **Versatilidad:** Soporta estructuras de datos avanzadas, scripts Lua, y capacidades de publicación/suscripción (pub/sub).


¿Para qué sirve Redis?

1. **Caché de aplicaciones:** Reduce la latencia al almacenar datos frecuentes en memoria, aliviando la carga de bases de datos principales.

2. **Gestión de sesiones:** Almacena sesiones de usuario en aplicaciones web y móviles.

3. **Tiempo real:** Ideal para marcadores (rankings), sistemas de chat, contadores y analítica en tiempo real.

4. **Colas de mensajes:** Permite la gestión de colas de alto rendimiento.

En resumen, Redis funciona como un intermediario o complemento de alta velocidad para bases de datos convencionales (como MySQL o PostgreSQL) para optimizar el rendimiento de las aplicaciones