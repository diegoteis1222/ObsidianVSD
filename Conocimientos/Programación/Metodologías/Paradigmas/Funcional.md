> *Functional Programming*

La programación funcional es un paradigma declarativo de programación basado en la aplicación y composición de funciones, en las que **expresiones vinculan valores a otros valores**. Toman datos de entrada, que envían como argumentos y devuelven como futuros argumentos para otras funciones.

Dentro de la programación funcional, encontramos...
- Funciones de primera clase, que pueden **tomar otras funciones como argumento** o devolverlas como respuesta. 
- [[Funciones puras]], que no cuentan con dependencias entre ellas, **muestran resultados constantes** y que si no son utilizados pueden ser borrados sin afectar a otras expresiones.
- Recursión, a través de funciones recursivas que se invocan a si mismas creando bucles.
- Eager vs. Lazy, cómo se procesan los argumentos a la hora de evaluar una función. ¿Se procesan antes o después de sus subtérminos? 
```python
print(len([2+1, 3*2, 1/0, 5-4]))
```
	Eager devolvería un error ya que no puede realizar 1/0. Lazy devolvería 4, ya que no ha intentado procesar los argumentos antes de utilizar la función.