Mecanismo de la Programación Orientada a Objetos (POO) que permite que una clase herede atributos y métodos de otra clase.

Se heredan los métodos públicos y protegidos pero no los constructores. 

Se utiliza la palabra super para llamar al constructor, a métodos del padre o para sobrescribir métodos del padre.

```
class Vehiculo {
    void arrancar() {
        System.out.println("El vehículo arranca");
    }
}

class Coche extends Vehiculo {
    void tocarBocina() {
        System.out.println("Beep beep");
    }
}

public class Main {
    public static void main(String[] args) {
        Coche miCoche = new Coche();
        miCoche.arrancar();      // heredado
        miCoche.tocarBocina();   // propio
    }
}
```