Mecanismo automático de gestión de memoria que se dedica a liberar memoria reclamando objetos que ya no se encuentren en uso (que no sean alcanzables). 

**Todos los lenguajes modernos cuentan con un GC, aunque cada uno hace uso de él de maneras distintas.** Suplanta a la necesidad de definir la lógica del ciclo de vida de un objeto, aunque el GC también ocupa rendimiento: si puedes liberarlos a mano y evitar el GC, mejor.

Inventado por John McCarthy en 1959.