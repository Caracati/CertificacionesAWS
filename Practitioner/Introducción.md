## Apuntes para el Examen de Practitioner de AWS - Introducción

- [Video uno](https://www.youtube.com/watch?v=RsNh0Qbt4zY)
  
- **Servicios Iniciales de AWS**:
  - AWS comenzó ofreciendo servicios como SQS (Amazon Simple Queue Service) y S3 (Amazon Simple Storage Service), marcando el inicio de su oferta de servicios en la nube.

- **Definición de la Nube**:
  - La nube se refiere a la entrega de servicios de cómputo, como servidores, almacenamiento, bases de datos, redes, software, entre otros, todo a través de internet.
  - Facilitar el acceso y los costes para los servidores
  - Base de datos autoescalables 
  - Como funciona ? 
    - son data centers muy grandes va todo a traves de una api

- **Modelos de Servicios en la Nube**:
  - **SaaS (Software as a Service)**:
    - Ofrece aplicaciones completas a través de internet, como Gmail o YouTube.
  - **PaaS (Platform as a Service)**:
    - Facilita el entorno para que los desarrolladores creen, prueben y desplieguen aplicaciones.
  - **IaaS (Infrastructure as a Service)**:
    - Proporciona infraestructura virtualizada, como máquinas virtuales o almacenamiento, en la nube.


- **Arquitecturas de Implementación**:
  - **On-Premise**:
    - Uso de servidores físicos instalados y mantenidos localmente por la organización.
  - **Híbrido**:
    - Integración entre infraestructuras de nube y locales (on-premise) para crear un entorno combinado.
  - **Todo en la Nube**:
    - Todos los servicios y recursos de la empresa se alojan en la nube sin infraestructura local.

### Beneficios de la Nube

- **Escalabilidad**:
  - **Horizontal**:
    - Implica agregar más máquinas o instancias al entorno para distribuir la carga.
    - Se refiere a la capacidad de escalar agregando más instancias de hardware (por ejemplo, más servidores) o recursos a través de múltiples máquinas. Puede ser tanto a nivel de máquina (instancias) como a nivel de aplicación (dividir la carga en múltiples servidores o instancias).
    - En AWS, esto puede lograrse mediante servicios como EC2 Auto Scaling o la adición de más instancias EC2 para distribuir la carga.
  - **Vertical**:
    - Implica aumentar la capacidad de una máquina individual agregando más recursos a esa máquina existente.
    - Se refiere a la capacidad de mejorar el rendimiento de una única máquina agregando más recursos (por ejemplo, más RAM, CPU, almacenamiento) a esa máquina específica.
    - En AWS, esto podría lograrse cambiando el tamaño de una instancia EC2 (aumentar la cantidad de CPU, RAM, etc., en una sola instancia).
  
- **Pago por Uso**:
  - No se tiene que invertir en máquinas 
  - Solo se paga por los recursos que se consumen sin necesidad de realizar un pago inicial.
  
- **Economías de Escala**:
  - Optimización de recursos, permitiendo que la infraestructura sea compartida y utilizada eficientemente, esto quiere decir que si tu no estas usando un servidor, este se utiliza por otro lado, y esto es como esta rotando

- **Velocidad de Desarrollo**:
  - Mayor agilidad y rapidez en el desarrollo y despliegue de aplicaciones.

- **Facilidad de Escalamiento**:
  - Capacidad de aumentar o reducir los recursos según la demanda en tiempo real. Con esto se puede escalar en caso de saber que un fin de semana habrá mucha demanda subir ram y todo lo necesario

- **Seguridad**:
  - Garantía de seguridad proporcionada por AWS para la protección de los datos.

- **Disponibilidad Global**:
  - Despliegue de servicios en múltiples regiones globales de AWS para una mayor accesibilidad.

### Servicios más importantes de AWS
- **Analítica**
- **Interacción entre aplicaciones (API Gateway)**
- **Realidad virtual y realidad aumentada**
- **EC2**
- **Base de datos**
- **Desarrollo**
- **Videojuegos**
- **Machine learning**
- **Migración de data center a Cloud**
- **Para móvil**
- **Robótica**
- **Satélites**
- **Almacenamiento**
- **Seguridad**
- **Computación cuántica**
- *(Existen más de 200 servicios)*

### Infraestructura global de AWS 
  - [Infraestructura Global](https://aws.amazon.com/es/about-aws/global-infrastructure/)
  - Lo que se ven azul son la regiones donde hay servidores de AWS y en naranja son las que van a abrir en poco tiempo
  - Por el momento hay 33 regiones con 105 zonas de disponibilidad
  - **Zona de disponibilidad (AZ)**
    - Conjunto de data centers cercanos pero lo suficientemente separados para evitar afectaciones conjuntas.
  - **Como se seleciona la región**
    - Requerimiento legales.
      - Los datos personales de gente de europa debe de estar en europa
    - Proximidad a tus clientes
      - Si tus clientes estan en francia hay que elegir la zona mas cerca
    - Servicios que hay en la región 
      - No todos los servicios están en todas las regiones
      - Las regones principales son north virgiena y en europa es irlanda, aquí reciben las 1ras actualizaciones
    - Costo, ya que no todos los servicios cuestan los mismo en todas las regiones
  - **Edge Locations y CDN (Content Delivery Networks)**
    - Existen las edge location que son servidores en difernte lugares del mundo para que haya mas velocidad entre cada una de las regiones
    - Se utilizan los CDN(Content delivery networks) como cloudFront para poder mejorar la latencia esto es colocar la información en puntos de presencia (PoPs - Points of Presence) distribudos en todo el mundo para tener la mejor ruta agregando cache en los recurso mencionados
           
### Como se usa AWS
  - AWS se basa en Apis es una apis y tiene 3 formas, mediante
    - Consola de administración que es entrando a la página
    - CLI que es la lina de comandos
    - Usar los SDK (software development kit)
  - Todo se hace a travez de la misma API
  - LA consola de AWS
    - Tienes todos los servicios disponibles 
  - CLI 
    - Se puede instalar y ya solo se configura 
  - SDK
    - Se descarga el sdk y se utilzia

### Resumen
- Ahorro de costos.
- Computación escalable.
- Almacenamiento sencillo.
- Regiones con múltiples Zonas de Disponibilidad.
  - Las AZ están diseñadas para ser independientes para garantizar la disponibilidad y tolerancia a fallos.
- Diferentes formas de acceso a AWS: consola, CLI y SDKs.