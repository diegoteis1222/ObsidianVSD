Docker es una plataforma de código abierto que automatiza el despliegue de aplicaciones dentro de **contenedores** ligero y portátiles. Permite empaquetar el código, librerías y dependencias necesarias para que una aplicación funcione en cualquier entorno, garantizando consistencia desde el desarrollo hasta la producción.

Puntos clave:

- **contenedores vs VMs**: A diferencia de las máquinas virtuales, los contenedores no incluyen un sistema operativo completo, sino que comparten el núcleo del sistema anfitrión, lo que los hace mucho más ligeros y eficientes.

- **Portabilidad**: "Funciona en mi máquina" se convierte en "funciona en cualquier lugar", facilitando el movimiento entre portátiles, servidores físicos o la nube.

- **Componentes principales**: Utiliza **imágenes** (plantillas de solo lectura), **contenedores** (instancias en ejecución de una imagen) y el **Docker Hub** (repositorio para compartir imágenes).

- **Dockerfile**: Un archivo de texto con instrucciones para construir la imagen de Docker de forma automatizada.

- **Ventajas**: Mejora el desarrollo ágil (CI/CD), la escalabilidad de [[Microservicios]] y la eficiencia de recursos.

En resumen, Docker permite crear entornos aislados y estandarizados para que las aplicaciones se ejecuten sin conflictos.