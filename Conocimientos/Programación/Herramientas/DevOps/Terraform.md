Terraform es una herramienta de **infraestructura como código** (IaaS) que permite definir, aprovisionar y gestionar infraestructura en la nube o local (AWS, Azure, Google Cloud, etc...) utilizando archivos de configuración declarativos, generalmente escritos en **HashiCorp Configuration Language** (HCL).
Automatiza el ciclo de recursos de TI de manera segura y eficiente.

Características clave:

- **Declarativo**: Defines el estado de la infraestructura en lugar de los pasos necesario para llegar a él.

- **Agnóstico a la nube** (Multi-cloud): Utiliza un solo lenguaje para gestionar múltiples proveedores de servicios.

- **Idempotencia**: Al igual que [[Ansible]], Terraform garantiza que el estado real de la infraestructura coincida con la configuración definida independientemente de cuantas veces se ejecute.

- **Gestión de estado** (State file): Mantiene un archivo que rastrea la infraestructura actual para gestionar  el ciclo de vida de los recursos.


Flujo de trabajo:

1. **Write** (Escribir): Se definen los recursos en archivos de configuración (`.tf`)
2. **Plan** (Planificar): `terraform plan` genera un plan de ejecución para previsualizar los cambios.
3. **Apply** (Aplicar): `terraform apply` lleva a cabo los cambios propuestos en el orden correcto.