
Es un principio fundamental en el diseño de sistemas distribuidos, como las bases de datos NoSQL, este establece que es imposible para un sistema de datos distribuido proporcionar simultáneamente más de dos de las siguientes  garantías:

1. **Consistencia:** Todos los nodos ven los mismos datos al mismo tiempo. Si realizas una escritura en un nodo, cualquier lectura posterior en cualquier otro nodo debe devolver ese dato actualizado.

2. **Disponibilidad :** Cada petición recibe una respuesta (éxito o fallo), sin garantía de que contenga la versión más reciente de la información. El sistema siempre está "operativo".

3. **Tolerancia al Particionado:** El sistema sigue funcionando a pesar de que la red se rompa o se pierdan mensajes entre los nodos (una "partición" de red).