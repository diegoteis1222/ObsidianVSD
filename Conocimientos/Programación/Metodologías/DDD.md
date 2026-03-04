(Domain Driven Design)

Metodología de programación en la cual las reglas de negocio (dominio) son el centro del desarrollo del software y se debe usar un lenguaje común entre los desarrolladores y los expertos del negocio.

Conceptos: 
- Lenguaje ubicuo: Negocio y desarrolladores usan el mismo lenguaje (Si el negocio dice Pedido la lógica debe decirlo también).
- Entidades: Deben ser objetos con su identidad y poder evolucionar.
- Value Objects: Deben ser objetos sin identidad, inmutables y se deben comparar por valor.
- Agregados: Paquete coherente de objetos de dominio que se modifican juntos, su raiz es *Aggregate Root* que es la única puerta de entrada para cambios importantes.
- Repositorios: Interfaz moderna para cargar o guardar agregadores sin acoplarte a EF Core (Entity Framework Core).
- Domain Events: Son los echo del negocio: PedidoEcho. Sirven para desacoplar acciones secundarias como notificaciones.


Esta metodología es muy útil cuando el negocio es muy complejo y tiene muchas reglas, también si se sabe que el sistema va a crecer a largo plazo y se debe llevar una arquitectura clara.

