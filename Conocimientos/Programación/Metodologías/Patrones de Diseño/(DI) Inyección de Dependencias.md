> *Dependency Injection*

Patrón de diseño [[(OOP) Orientado a Objetos]] en la que un **objeto o función recibe otros objetos y funciones** que requiera en vez de crearlos internamente, **segregando responsabilidades y desacoplando funcionalidades.**

Existen cuatro roles dentro de la *Inyección de Dependencias*...
- **Servicios y clientes**: Los servicios contienen funcionalidades útiles de los cuales las clases cliente hacen uso, convirtiéndolos en sus *dependencias.*
- **Interfaces**: ocultan el código, ya que los clientes no deberían de saber cómo sus dependencias están implementadas, sólo sus nombres y APIs. De esta manera, si las dependencias cambian, los clientes pueden mantenerse congelados.
- **Inyectores**: ensamblador, contenedor, proveedor, factoría... el encargado de introducir el servicio al cliente.

| VENTAJAS                                                                                                                                                                                                                                      | DESVENTAJAS                                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| + Disminución del acoplamiento.<br>+ Aumento de reusabilidad.<br>+ Aumento de flexibilidad.<br>+ Reducción de repetición (DRY)<br>+ Permite desarrollo síncrono.<br>+ Extracción de configuraciones.<br>+ Facilidad de testear unitariamente. | — Crea clientes que demandan objetos.<br>— Reduce la trazabilidad del código.<br>— Requiere más esfuerzo de desarrollo.<br>— Promueve la dependencia en frameworks. |
