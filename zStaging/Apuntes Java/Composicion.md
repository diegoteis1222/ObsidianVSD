Relación entre clases donde **una clase contiene una instancia de otra clase** como parte de su estado.

```
class Direccion {
    String calle;
    String ciudad;

    Direccion(String calle, String ciudad) {
        this.calle = calle;
        this.ciudad = ciudad;
    }
}

class Usuario {
    String nombre;
    Direccion direccion;  // Composición

    Usuario(String nombre, Direccion direccion) {
        this.nombre = nombre;
        this.direccion = direccion;
    }
}
```

Para usar la composición debes instanciar el objeto en vez de extender de el.
Esto es mas modular que la herencia haciendo que no se creen jerarquías complejas