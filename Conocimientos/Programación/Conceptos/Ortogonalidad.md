El concepto es heredado de la matemática, en la que dos líneas ortogonales siempre se encuentran en un ángulo de 90º. 

Podemos comprender la ortogonalidad de dos maneras distintas:
- La capacidad de hacer uso de distintas características de un lenguaje en una combinación arbitraria logrando resultados consistentes.
- **El desacoplamiento e independencia entre componentes y módulos de manera que al modificar una parte el resto no sean afectadas.**

Un **sistema ortogonal es uno que dispone de componentes autocontenidos, asilados unos de otros**. Esto **disminuye la complejidad de modificación** (ya que desciende riesgo de afectar a otros sistemas) y **aumenta la facilidad de mantenimiento** (ya que secciones que fallen están aisladas y es más sencillo someterlas a pruebas). Un sistema ortogonal es un sistema con **bajo acoplamiento**. 

#### CÓMO APLICAR ORTOGONALIDAD
El primer paso es pensar en un sistema como una serie de módulos que cooperan entre ellos, como si se tratase de [[Microservicios]]. Los organizamos en capas, asignándoles un nivel de abstracción, siempre teniendo en cuenta...

- ... que el código debe de estar desacoplado. Debe de ser **código "tímido"**: no expone a otros módulos nada que no sea estrictamente necesario, y no se basa en implementaciones provenientes de otros módulos (*Principio del Menor Conocimiento / Ley de Demeter*).

- ... que debemos de **evitar datos globales**, ya que estos están compartidos con otros módulos: es mejor **recibir un contexto explícito**, como, por ejemplo, una instancia de una clase que siga el patrón Singleton que funcione a manera de "global disfrazado"; un global algo más controlado, "elegante" según algunos. **Mejor, ninguno.**

- ... evitar funciones similares. Si cuentas con varios métodos que cumplen una tarea distinta pero que comparten secciones de código, refactorizar su estructura siguiendo *DRY (Don't Repeat Yourself)* resultaría en un sistema con mayor ortogonalidad.

#### TESTEO UNITARIO
Realizar testing unitario es una buena manera de poner a prueba el nivel de ortogonalidad de tu sistema: a más importaciones de otros modelos requieras para preparar y ejecutar una prueba unitaria, mayor acoplamiento tendrá; por ende, menor ortogonalidad. 