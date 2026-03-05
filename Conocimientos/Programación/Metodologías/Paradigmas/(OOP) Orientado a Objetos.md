> *Object-Oriented Programming*

Programación [imperativa](Imperativo) basada en **entidades, que encapsulan datos y funciones, y en cómo interactúan entre ellas**.

Sus características más notables son...
- **Cohesión, desacoplamiento y la ocultación.**
- **Herencia, a través de...**
	- Clases: Creadas a través de un constructor, diferenciando métodos y variables de clase e instancia. Heredan métodos de su superclase, y pueden sobrescribirlos.
	- Prototipos: Creados a través de enlaces de prototipo con un objeto *padre*.
- **Polimorfismo y enlace dinámico**
	- Si varios objetos implementan una interfaz, una función podrá hacer uso de cualquiera de ellos de manera uniforme. 
	- A través del enlace dinámico, el método correcto a usar (dentro de un objeto dado que implementa una interfaz) es seleccionado en tiempo de ejecución en vez de en tiempo de compilación.
- **Recursión abierta**
	- Los métodos del objeto pueden acceder a los datos y métodos del propio objeto. 
	- A través del enlazado tardío, en el que dos objetos se enlazan durante tiempo de ejecución, una clase podría llamar a un método definido más tarde en una subclase.