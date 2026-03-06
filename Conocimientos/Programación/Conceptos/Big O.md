La notación Big O es un estándar utilizado en programación para medir la eficiencia y el escalado de un algoritmo, describiendo cómo aumenta su tiempo de ejecución o espacio en memoria a medida que crecen los datos de entrada (*n*).

Se enfoca en el "peor de los casos" para garantizar en el rendimiento máximo.

Detalles clave: 

- **Finalidad**: Compara la eficiencia entre algoritmos (por ejemplo, de búsqueda u ordenamiento).

- **Tipos comunes de complejidad**:

	- ***O1*****- Constante**: El tiempo es el mismo, sin importar el tamaño de los datos (ej. acceder a un elemento  de un array).

	- ***0(log n)*** **- Logarítmica**: Muy eficiente, reduce el problema a la mitad en cada paso (ej. búsqueda binaria).

	- ***0(n)*** **- Lineal**: El tiempo crece proporcionalmente a la entrada (ej. recorrer un bucle simple).

	- ***0(n log n)*** **- Linealítmica**: Común en algoritmos de ordenamiento eficientes como Merge Sort.

	- ***0(n²)*** **- Cuadrática:** Común en bucles anidados, el tiempo crece al cuadrado de la entrada.

	- ***0(2ⁿ)*** **- Exponencial**: Extremadamente lento, ineficiente para datos grandes.

 - **Simplificación**: La notación ignora constantes y términos de menor orden, enfocándose solo en la tasa e crecimiento principal.

En resumen, Big O ayuda a los desarrolladores a elegir el enfoque más rápido y escalable para sus soluciones, siendo un concepto crucial en entrevistas técnicas.