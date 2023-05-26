---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

# 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

<<<<<<< Updated upstream
## 1.3. Administración del sistema
- [Recursos computacionales para Linux](#recursos)
- [Tipos de Instalación](#instalacion)
- [Particiones en un disco duro](#particiones)
- [Herramientas de virtualización](#herramientas_virtualizacion)
- [Referencias](#referencias)

<a name="recursos"> </a>
## 💻 Recursos computacionales para Linux
Previo a la instalación de una distribución de Linux para un servidor es necesario considerar los recursos básicos de hardware como sigue:

- CPU: Intel Celeron de 2.4 Ghz
 -Procesador: Pentium IV
- Disco duro: 40 GB
- Memoria: 4 GB
- Tarjetas de Red: 2 NICs PCI Realtek/basadas en chip Realtek o Via

<a name="instalacion"> </a>
## 💻 Tipos de Instalación
- Estación de trabajo: Más adecuada si es nuevo en el mundo de Linux y quiere probarlo. 
- Servidor: Si desea que su sistema funcione como un servidor basado en Linux utilizando servicios específicos.
- Portátil: Instalación sencilla en ordenadores portátiles. 
- Personalizada: Mayor flexibilidad en el proceso de instalación. Podrá elegir su esquema de particionamiento, los paquetes que desea instalar y mucho más. 
- Actualización: Para actualizar rápidamente a los últimos paquetes y versiones del kernel. 

<a name="particiones"> </a>
## 💻 Particiones en un disco duro
- Hay tres clases de particiones: primarias, extendidas y lógicas.
- Muchas distribuciones necesitan que se creen a mano las particiones de Linux utilizando el programa fdisk. Otras pueden crearlas automáticamente.
- En el primer sector del disco está el registro de arranque maestro “MBR” junto a la tabla de particiones.

<p align="center">
  <img src="../imagenes/particion.png" alt="industria" width="100%">
</p>

En Linux los manejadores, que se encuentran en el directorio /dev, se usan para comunicarse con los dispositivos de su sistema como discos duros. Los discos duros SSD se nombran con /dev/disksn.

<p align="center">
  <img src="../imagenes/df.png" alt="industria" width="100%">
</p>

Por lo general se crean dos particiones para Linux, una para ser usada como sistema de ficheros raíz y la otra como espacio de intercambio “swap”.
La partición swap, es un espacio de intercambio de ayuda a la memoria RAM a pasar datos temporalmente al disco duro.

<p align="center">
  <img src="../imagenes/particiones_servidor.png" alt="industria" width="100%">
</p>

<a name="herramientas_virtualizacion"> </a>
## 💻 Herramientas de virtualización
- [VirtualBox](https://www.virtualbox.org)
- [Vmware](https://www.vmware.com)
- [Microsoft Azure](https://azure.microsoft.com/)
<p align="center">
  <img src="../imagenes/virtualization_tools.png" alt="industria" width="70%">
</p>

<a name="referencias"> </a>
## 📚 Referencias
- VirtualBox from https://www.virtualbox.org
- Vmware from https://www.vmware.com
- Microsoft Azure from https://azure.microsoft.com/
=======






Administración del sistema

Cada vez que inicia su sistema, lee una serie de comandos de inicio de los archivos de inicialización del sistema ubicados en su directorio /etc/rc.d. Algunos se encuentran en el propio directorio /etc/rc.d, mientras que otros se encuentran en un subdirectorio llamado init.d. A continuación se detalla la tabla de archivos del sistema y directorios:

Linux tiene la capacidad de cargar diferentes versiones del kernel de Linux.
La tarea de seleccionar e iniciar un sistema operativo o kernel es administrada por una utilidad de administración de inicio, el Grand Unified Bootloader (GRUB) o Linux Loader (LILO).
La fecha y hora del sistema puede ser configurada con el comando date o usando NTP.
Cuando inicia el sistema, usa el nivel de ejecución especificado en el archivo /etc/inittab.
id:5:initdefault: 

Sysbench: Permite obtener rápidamente una impresión del rendimiento del sistema.

## Webmin

Webmin es un programa que simplifica el proceso de gestión de un sistema Linux o Unix. Webmin permite editar manualmente los archivos de configuración y ejecutar comandos para crear cuentas, configurar un servidor web y administrar el reenvío de correo electrónico a través de una interfaz web fácil de usar y actualiza automáticamente todos los archivos de configuración necesarios.

## Administración de usuarios

El usuario root puede leer, modificar o borrar cualquier archivo en el sistema. Este usuario es utilizado para ejecutar tareas específicas que no pueden ser ejecutadas usando un usuario normal.
El archivo /etc/passwd contiene las cuentas de usuarios, cada línea de este archivo denota un usuario, el formato de cada línea es:

**/etc/passwd**


**/etc/shadow**

## Grupos de Usuarios

La entidad grupo permite asignar permisos a los archivos de manera más eficiente, ya que podremos agrupar usuarios que compartan similares carácterísticas con respecto al acceso a ciertos directorios y/o archivos.
La definición de grupos de usuarios se encuentra en el archivo /etc/group, como en el archivo /etc/passwd. El formato del archivo /etc/group se define así:


## Linux en la Nube

Linux juega un papel fundamental en la computación en la nube. ¿Qué hace que Linux sea único para habilitar la computación en la nube? 
Flexibilidad: la computación en la nube brinda la capacidad de aprovisionar recursos de TI rápidamente y en cualquier momento.
Accesibilidad: las aplicaciones y los datos residen centralmente y se accede desde cualquier lugar a través de una red desde cualquier dispositivo.
Este proceso libera a los administradores para supervisar las operaciones informáticas en lugar de configurar y actualizar los sistemas manualmente.
Seguridad: Linux puede ayudar a compensar los problemas de seguridad porque es uno de los sistemas operativos más seguros y confiables disponibles.
Linux es de código abierto, lo que significa que su código fuente puede ser inspeccionado por vulnerabilidades y problemas de compatibilidad. 

## La Nube (The Cloud)

Cloud computing permite que los recursos informáticos se muevan a ubicaciones remotas donde se puede acceder al contenido, manipularlo y compartirlo por todo el mundo.

Cloud adoption es la migración de las aplicaciones y procesos de una organización TI a servicios en la nube.

Cloud se puede describir como recursos informáticos de uno o varios centros de datos externos a los cuales se puede acceder a través de Internet.

Los datos y recursos que las organizaciones almacenan en la nube pueden incluir datos, servidores, almacenamiento, alojamiento de aplicaciones, análisis y una gran cantidad de otros servicios.

Existen cuatro modelos principales de implementación en la nube:

**Public Cloud:** es infraestructura de nube implementada por un proveedor para ofrecer servicios en la nube al público en general y a las organizaciones a través de Internet.
**Private Cloud:** es una infraestructura de nube configurada para el uso exclusivo de una organización en particular. Estas plataformas son conocidas como “Infrastructure-as-a-Service (IaaS)”.

Existen cuatro modelos principales de implementación en la nube:

**Hybrid Cloud:** Una nube híbrida se compone de dos o más nubes individuales, cada una de las cuales puede ser privada, comunitaria o pública.

**Edge Cloud:** Debido al crecimiento de Internet de las cosas (IoT), está ganando popularidad . Estos dispositivos conectados, como cámaras conectadas, vehículos autónomos e incluso teléfonos inteligentes, se benefician cada vez más de la potencia informática que existe más cerca de ellos en la red.


## Virtualización

- Virtualización es uno de los avances más significativos que ha contribuido a la habilitación de la computación en la nube.
- Virtualización es el proceso en el que una computadora física, llamada host, ejecuta múltiples copias de un sistema operativo, donde cada copia es llamada guest  (invitado).
- Cada invitado obtiene sus propios recursos virtuales y se comunica con la red por su cuenta.
- El sistema host ejecuta un software llamado hypervisor que cambia los recursos entre los distintos invitados.
- Con el software de compañías como VMWare y Openbox, puede tomar una CPU potente y usarla para ejecutar múltiples máquinas virtuales.
- Esto optimiza el uso de los recursos físicos y reduce drásticamente los costos con respecto a la máquina anterior, un modelo de sistema operativo.

## Infraestructura basada en contenedores

Un contenedor generalmente representa solo una aplicación o un grupo de aplicaciones.
El valor de usar contenedores es que se incluyen todas las bibliotecas y binarios que necesita para ejecutar la aplicación, por lo que el usuario no tiene que realizar ese paso de instalación adicional.
El software para crear y administrar u orquestar contenedores está disponible en Docker, AWS (Elasticized Container Service), Microsoft (Azure Container Service) y otros.
Los programadores están creando software que realiza una única función de un sistema (como el procesamiento o almacenamiento de la base de datos) que se ejecuta en un contenedor.
Estos contenedores están organizados en "pods" que se ejecutan dentro de un "nodo" y pueden comunicarse entre sí y con el mundo exterior si es necesario.
Linux es la tecnología subyacente que hace que la tecnología de contenedores funcione.
Bare-Metal Deployment, es un sistema informático o una red en la que una máquina virtual se instala directamente en el hardware en lugar de dentro del sistema operativo (SO) del host.




>>>>>>> Stashed changes
