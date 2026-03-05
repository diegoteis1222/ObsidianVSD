> *Tiempo de ejecución y tiempo de compilación.*

Estos dos términos definen los dos estados del ciclo de vida por los que pasa un programa: compilación y ejecución (Si ignoramos a los lenguajes intepretados como Python, que añadirían un paso adicional previo a la compilación).

#### COMPILACIÓN
- Objetivo: Convertir código escrito en un lenguaje de alto nivel en código máquina. 
- Método: Traduce los archivos fuente a byte code (.java -> .class), importando dependencias, interfaces y librerías.
- Resultado...
	- Éxito: código compilado.
	- Errores: mensajes de error en tiempo de compilación causados por errores sintácticos o semánticos en los archivos fuente. 


#### EJECUCIÓN
- Objetivo: Que el programa desarrolle sus funcionalidades.
- Método: Otorgándole un espacio y contexto en CPU y memoria, y asignando procesadores a los hilos que deje en el gestor.
- Resultado...
	- Éxito: el programa cumple su función.
	- Errores: cualquier error que suceda durante la ejecución del programa causado por su estado.
		- De segmentación, cuando el programa intenta acceder a una memoria que no le ha sido asignada. Acceder variables sin inicializar, nullpointers, out of index...
		- De operaciones inválidas, si ocurre una división entre 0 o un overflow de integer (numero fuera del rango que puede representar).
		- De I/O, si el programa no cuenta con permisos de lectura o escritura sobre un archivo.