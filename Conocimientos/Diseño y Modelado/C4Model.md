Marco de trabajo  diseñado para documentar la arquitectura de sistemas de software de una manera sencilla y visual. 
Se basa en la idea de que la arquitectura de software se puede entender mejor si se "hace zoom" en diferentes niveles, tal como lo harías con un mapa (de un continente a una calle específica).

C4Model tiene obviamente 4 niveles y su nombre proviene de las cuatro capas de abstracción que propone: **Contexto, Contenedores, Componentes y Código.**

#### Contexto:
Muestra cómo el sistema interactúa con los usuarios y con otros sistemas externos.

#### Contenedores
Un "contenedor" en C4 no es como uno en  Docker, es mas bien cualquier unidad ejecutable o que almacena datos.

#### Componentes
Hacemos zoom dentro de un contenedor específico para ver sus piezas internas.

#### Código 
Es el nivel de máximo detalle, mostrando cómo se implementa un componente.