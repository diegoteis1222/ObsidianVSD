Un stream es una secuencia de elementos que se pueden procesar de forma funcional.
Un  record dentro de un stream es cada elemento individual que recorre el stream.

En el siguiente codigo cada *names* es un record.

```
import java.util.List;
import java.util.stream.Stream;

public class StreamExample {
    public static void main(String[] args) {
        List<String> names = List.of("Ana", "Juan", "Luis");

        // Creamos un Stream de los records (elementos)
        Stream<String> nameStream = names.stream();

        // Procesamos cada record
        nameStream.forEach(System.out::println);
    }
}
```


Operaciones que utilizan:

- .filter : filtra los records según la condición dada.
- .map: transforma cada record a otro tipo.
- .sorted: ordena los records.
- .forEach: procesa cada record.
- .collect: recoge records en una colección.
- .reduce: combina records en un único valor.

```
record Person(String name, int age) {}

public class StreamRecordsExample {
    public static void main(String[] args) {
        List<Person> people = List.of(
            new Person("Ana", 25),
            new Person("Juan", 30)
        );
        people.stream()
              .filter(p -> p.age() > 26)
              .forEach(p -> System.out.println(p.name()));
    }
}
```

