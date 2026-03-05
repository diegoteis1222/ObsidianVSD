Las proxies dinámicas de Java permiten a los programas generar objetos durante runtime que se comportarán como si implementasen distintas interfaces, pero que, en vez de tener sus propios cuerpos de métodos, hacen uso de un *handler*.

En otras palabras: **estos objetos NO existen en tiempo de compilación, pero son generados como instancias proxy cuando la JVM interactúa con sus clases.** Las clases en las que se basan no saben que serán utilizadas a través de un proxy:

```java
import java.lang.reflect.*;
// la librería donde se encuentran la CLASE .Proxy y la INTERFAZ .InvocationHandler

Service proxy = (Service) Proxy.newProxyInstance(
	Service.class.getClassLoader(),
	new Class<?>[] {Service.class},
	new MyHandler()
);
```

- Como las proxies no se generan en tiempo de compilación si no en ejecución, **su comportamiento no es fijo; puede ser modificado en runtime con**, por ejemplo, una flag en un ternario que apunte a un objetivo u otro. 
- Los usos de las proxies dinámicas están limitados por las interfaces que implementa la clase base: **no podrá hacer uso de métodos que no aparezcan definidos en ella.** 
- Como no cuentan con cuerpo, no pueden ser debuggeadas a través de breakpoints. 
##### FUNCIONALIDAD
Al lanzar el método Proxy.newProxyInstance, se inicia una cadena de eventos:

1. Generación de la clase proxy: el JVM crea una nueva clase que implementa las interfaces que le asignes, y le da un nombre sintético `com.sun.proxy.$Proxy0`.
2. Enrutación de métodos: Por cada método en cada interfaz, el proxy añade una implementación en el que delega control sobre el `InvocationHandler.invoke()`. **La referencia del método a usar y su array de argumentos se generan en el momento de uso.**
3. Inyección de constructor: La clase proxy generada toma, a través de su constructor, un **InvocationHandler, que guarda en un argumento privado que utiliza en cada llamada de método para enrutar**. 
4. Cargado de clase: Una vez generada, se carga en memoria usando el cargador de la clase que pasaste inicialmente al `Proxy.newProxyInstance`, permitiéndola vivir en el mismo contexto que la clase normal. 

##### EJEMPLO
Una clase proxy que audita llamadas antes de delegarlas a un servicio real:
```java
import java.lang.reflect.*;

class LoggingHandler implements InvocationHandler {
	private final Service realService;
	
	public LoggingHandler(Service realService){
		this.realService = realService;
	}
	
	@Override
	public Object invoke(Object proxy, Method method, Object[] args) throws Throwable{
		System.out.println("Llamando método: " + method.getName());
		return method.invoke(realService, args);
	}
}
```