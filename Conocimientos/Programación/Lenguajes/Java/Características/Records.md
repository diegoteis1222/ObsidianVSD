Los records, implementados en el JDK 17, son una **implementación del patrón DTO capaces de almacenar valores de forma inmutable en unos objetos tipo Record** de fácil creación, a los que sólo debemos de asignar atributos, y dejar que el compilador genere su constructor, getters, equals, hashcode y toString.

A parte de estos métodos generados por el compilador, **podemos implementar métodos personalizados definiéndolos en su interior**. Naturalmente, debido a que los Records son inmutables (final), estos métodos no podrán modificar la información que contienen. También podemos implementar constructores explícitos, pero estos siempre deben de iniciar todos los atributos.

- **Se declaran con la palabra reservada Record**.
- No pueden extender otras clases (más allá de Object) y no pueden actuar de superclase.
- Pueden implementar interfaces.
- Sus instancias se generan a través de sus constructores con *new.*

```java
public record Drone(String uuid, String ref, boolean isActive) extends Aircraft{
	
	public Drone(String uuid, String ref){
		this(name, email, false);
	}
	
	public String getFullReference(){
		return uuid + "/" + ref;
	}
	
	@override
	public void isInAir(){
		if (isActive){
			System.out.println("El dron se encuentra en el aire.")
		} else {
			System.out.println("El dron se encuentra en tierra.")
		}
	}
}
```

```java
[...]

Aircraft aircraftInUse = new Drone("1a85sd", "87da5f4da8");

System.out.println(aircraftInUse.getName())
// 1a85sd

System.out.println(aircraftInUse.isInAir())
// El dron se encuentra en tierra.
```