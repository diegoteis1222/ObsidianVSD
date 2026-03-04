Para que una función sea considerada como pura, debe cumplir con dos reglas fundamentales:

1. **Dado el mismo conjunto de argumentos, la función siempre debe devolver el mismo resultado.** Esto significa que la función no debe depender de ninguna variable o estado externo.
2. La función **no debe tener efectos secundarios**. Esto significa que la función no debe cambiar ningún estado externo o interactuar con otras partes del sistema. La función solo debe realizar operaciones en los datos de entrada y devolver un resultado.

Una función es **no pura** si:

- Cambia algo fuera de ella
- Depende de algo fuera de ella
- Produce efectos secundarios
- No siempre devuelve el mismo resultado con los mismos argumentos