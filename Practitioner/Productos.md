## Apuntes para el Examen de Practitioner de AWS - Productos

- [Video uno - 41:11](https://www.youtube.com/watch?v=RsNh0Qbt4zY)

- **Productos**
  - **Principales**
    - **EC2**
      - Servicio de máquinas virtuales de AWS. Permite crear instancias con diferentes sistemas operativos.
      - **Beneficios**
        - **Elasticidad**: Aumento fácil de RAM y almacenamiento.
        - **Flexibilidad**: Creación de varios tipos de máquinas.
        - **Integración con otros servicios de EC2** mediante roles específicos.
        - **Fiabilidad**: Baja probabilidad de caídas.
        - **Seguridad**: Utiliza security groups, entre otros.
        - **Costos reducidos**: Descuentos para periodos largos de uso.
        - **Facilidad de implementación**.
        - **Tipos de instancias**:
          - Clase C para computación y procesamiento.
          - Propósito general (M o T) más económicas.
          - Optimizadas para memoria (X y R) - más memoria que CPU.
          - Optimizadas para almacenamiento (H, I y D).
    - **EBS (Elastic Block Storage)**
      - Discos duros en red que se pueden desacoplar entre máquinas con distintas capacidades.
      - **Tipos de discos**:
        - Disco sólido SSD (gp2 y io1).
        - Disco duro mecánico HDD (st1).
      - **EBS Snapshot**: Copias de seguridad guardadas en S3.
      - Almacenamiento en bloques persistentes con replicación en caso de fallo.
      - Escalabilidad sencilla.
      - Pago por volumen utilizado.
      - Copias de seguridad rápidas y encriptación disponible.
    - **S3**
      - Es almacenamineto de datos en objetos
        - Difernecia de almacenamiento de datos en bloques y en objetos
          - bloques: cuando escribes en un log que tienes un fichero abierto y vas de linea por linea esto es por bloques
          - Obejtos: s3 subes n fichero y si queires añadir una linea tienes que subir ese fichero con una linea mas, no se puede evitar, se puede borrar pero no editar
        - Almacenamiento virtualmente infinito 
        - Se cobra por giga
        - Solo se almaenan solo fichero de 5 teras maximo
        - Durabilidad - son los 11 nueves o sea .99999999999%, o sea que la probablidad e que esto se pierda es la de os 11 nueves, ya que es un servicio global y no tiene regiones y los bucketes tiene un nombre unico para todo el mundo, es un sla
        - Se puede poner una acceso granular, o sea poner una regla donde pongas que un usuario solo puede tener acceso a los ficheros que empiecen con a, o sea dar permisos especificos 
        - Funcionliadad principal
          - Rapido
          - Duración
          - Alta disponibilidad de los datos
        - Es un almacenaiento de objetos para leer un archivo y subir archivos, no es posible escribir sobre un archivo para eso se usa EBS
        - No es un file system
        - Donde se usa
          - Backup
          - Almacenamitno de larga duración
          - Hosting de aplicaciones estaticas
          - Videos audio etc
        - Si se tine un bucket y una empresa queire algun archivo esto se cobra
          - El que pide paga
        - Versionados de objetos o sea que crea nueva versión sin borrar la versión pasada
          - si se activa y se borra un fihcero no se borra en automatico 
        - se pueden hacer borrados automáticos de la información 
        - S3 glacier -  permit meter obejtos en un almacenamint de larga duración con costos mas económicos pero si los quieres recuperar depende de l oque se pague
          - Se pueden archivar datos para temas legales por ejemplo dejar archivos sin borrar durante un tiempo determinado, el cual se puede consultar pero no se puede borrar
        - Hay otra opciones o tipo para almaencar objetos, por ejemplo guardas un backup en el cual no tendras que descargarlo se cobra menos por ese almacenamiento pero se cobra mas si lo descargas
          - S3 Standard: Es el estándar de almacenamiento de uso general. Proporciona alta durabilidad, disponibilidad y rendimiento. Adecuado para una amplia variedad de cargas de trabajo, como hosting de sitios web, almacenamiento de contenido multimedia, aplicaciones empresariales, etc.

          - S3 Standard-IA (Infrequent Access): Similar a S3 Standard, pero diseñado para datos que se acceden con menos frecuencia, con un costo más bajo que S3 Standard y una tarifa de recuperación de datos. Ideal para datos a los que se accede con menos frecuencia pero que necesitan estar disponibles rápidamente cuando sea necesario.

          - S3 One Zone-IA: Similar a S3 Standard-IA, pero los datos se almacenan en una sola zona de disponibilidad dentro de una región AWS. Apropiado para cargas de trabajo en las que la disponibilidad de los datos en una sola zona es suficiente y la redundancia en múltiples zonas no es esencial.

          - S3 Intelligent-Tiering: Clasifica automáticamente los datos entre niveles de acceso frecuente y acceso no frecuente, moviendo automáticamente los objetos entre los niveles según su patrón de acceso. Esto ayuda a optimizar costos al mantener automáticamente los datos menos accesibles en niveles de menor costo.

          - S3 Glacier: Ofrece almacenamiento de archivos a largo plazo y de respaldo con bajos costos, pero con tiempos de acceso más largos. Es útil para datos de archivo y copias de seguridad que rara vez se acceden pero se deben conservar durante mucho tiempo.

          - S3 Glacier Deep Archive: El nivel más económico de almacenamiento de Amazon S3 diseñado para datos que rara vez se acceden y que se conservarán durante mucho tiempo, con un tiempo de acceso largo.
    - **VPC** (Virtual Private Cloud)
        - **Descripción**: Es un servicio de red de AWS que te permite crear tu propia red virtual en la nube de Amazon. Funciona como una red de tu centro de datos en la nube de AWS. Permite tener un control granular sobre la configuración de la red, como las direcciones IP, subredes, tablas de ruteo, gateways, reglas de firewall y configuración de conexión a Internet.

        - **Funciones de VPC**:
            - **Red Privada Virtual**: Proporciona aislamiento lógico para tus recursos en la nube. Puedes crear subredes públicas y privadas para organizar y separar los recursos según tus necesidades.
            - **Control Total sobre la Red**: Te permite tener un control preciso sobre la configuración de la red, como la creación de subredes, la configuración de tablas de ruteo, la configuración de gateways de Internet y la asignación de direcciones IP.
            - **Conexiones Seguras**: Permite establecer conexiones seguras entre la infraestructura local y la nube mediante VPN (Virtual Private Network) o conexiones dedicadas mediante AWS Direct Connect.
            - **Escalabilidad y Flexibilidad**: VPC te ofrece la capacidad de escalar tu red en función de las necesidades de tu aplicación y negocio, ya que puedes modificar y ajustar los recursos de la red según sea necesario.

        - **Componentes Principales de VPC**:
            - **Subredes Públicas y Privadas**: Las subredes públicas tienen acceso a Internet, mientras que las subredes privadas no tienen acceso directo a Internet.
            - **Tablas de Ruteo**: Controlan el flujo del tráfico entre subredes y hacia y desde Internet.
            - **Internet Gateway (IGW)**: Permite la comunicación entre tu red VPC y Internet, siendo el punto de entrada y salida para el tráfico de Internet.
            - **Gateways y VPC Endpoints**: Permiten la conexión segura con otros servicios de AWS sin necesidad de una ruta a través de Internet.
            - **ACLs y Grupos de Seguridad**: Proporcionan capas adicionales de seguridad a nivel de red, filtrando el tráfico entrante y saliente.
            - **VPC Peering**: Permite conectar dos VPCs para que puedan comunicarse entre sí como si fueran una sola red.

        - **Límites de VPC**: Por defecto, se pueden crear hasta 5 VPC por región en una cuenta de AWS, pero este límite puede aumentarse mediante solicitudes especiales a AWS Support si es necesario.

        VPC es una característica esencial para la configuración y gestión de la red en la nube de AWS, permitiendo a los usuarios tener un control completo sobre su infraestructura de red y sus recursos en la nube de manera segura y personalizada.
      - **Security group**
        -  Es una forma de definir reglas de acceso a los distintos servicios 
        -  Como y desde donde se peude acceder
        -  Ej. a mi red privada solo puden entrar desde mi red publica y solo al puerto especifico
        -  Queirio que a mi servidor solo se pueda acceder por el puerto 80 
        -  si quiero que desde mi ip pueda acceder al puerto 22 para poder administrar
        -  Solo aceptan reglas de quien puede entrar, por defecto nadie puede entrar
        -  Por defecto un SG viene que todo el trafico entrata esta cerrado y todo el trafico saliente esta permitido
          -  para esto se debe de configurar
        - Son de tipo con estado, o sea cuando entras a una red y entras por el puerto 80 ese servidor no te responde por ese puerto 80, reponde por otro puerto aleatorio
        - Al ser sin estado cuando entras por el pourto 80 y te responde por otro puerto no hay que abrir otro puerto

- Resumen
  - Se tien el cloud de AWS, se tienen las regiones, dentro de cada una región se tiene las VPC y dentro de cada VPC se tienen las subredes, los bucketes se puden acceder desde las VPC desde intenre si esetán abiertos
  - Nombres de buckets de s3 son unicos
  - 


### Pendientes por ver
    - **Lightsail**
    - **SageMaker**
    - **Aurora**
    - **DynamoDB**
    - **RDS**
    - **Lambda**
