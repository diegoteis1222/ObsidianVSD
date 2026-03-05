Permiten definir clases, interfaces y métodos que funcionan con diferentes tipos de datos.

Ejemplos: 

```java
class Caja<T> {
    private T contenido;

    public void set(T contenido) {
        this.contenido = contenido;
    }

    public T get() {
        return contenido;
    }
}
```

``` java
Caja<String> cajaString = new Caja<>();
cajaString.set("Hola");
System.out.println(cajaString.get()); // Imprime: Hola

Caja<Integer> cajaEntero = new Caja<>();
cajaEntero.set(123);
System.out.println(cajaEntero.get()); // Imprime: 123
```

```java
public class Utilidades {
    public static <T> void imprimirArray(T[] array) {
        for (T elemento : array) {
            System.out.println(elemento);
        }
    }
}

// Uso:
Integer[] numeros = {1, 2, 3};
Utilidades.imprimirArray(numeros);

String[] palabras = {"Java", "Genéricos"};
Utilidades.imprimirArray(palabras);
```

Se puede limitar que tipos pueden usarse usando extends:

```java
class CajaNumerica<T extends Number> {
    private T numero;

    public void set(T numero) {
        this.numero = numero;
    }

    public T get() {
        return numero;
    }
}

CajaNumerica<Integer> cajaInt = new CajaNumerica<>();
CajaNumerica<Double> cajaDouble = new CajaNumerica<>();
// CajaNumerica<String> cajaStr = new CajaNumerica<>(); // ERROR
```

