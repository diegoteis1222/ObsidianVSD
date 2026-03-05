Introducidos en Java 8, un Stream es una secuencia de objetos sobre la que se pueden aplicar múltiples métodos en formato pipeline para lograr el resultado deseado. 

- Los Streams **NO son estructuras de datos**: hacen uso de colecciones, arrays o canales de input/output para procesar sus datos.
- Los Streams **NO modifican los datos originales**: sólo producen resultados tras aplicar sus métodos.
- Los operadores de los Streams son [*lazy*](Funcional), por lo que pueden concatenarse.
- Requieren de un **operador terminal** para adquirir su resultado. 