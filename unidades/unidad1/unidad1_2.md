---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

# 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

## 1.2. Software Linux
- [Categorías de aplicaciones](#aplicaciones)
    - [Aplicaciones de servidor](#servidor)
    - [Aplicaciones de escritorio](#escritorio)
    - [Herramientas](#herramientas)
- [Herramientas de consola](#herramientas_consola)
- [Gestión de paquetes](#paquetes)
- [Lenguajes de desarrollo](#lenguajes)
- [Referencias](#referencias)

<<<<<<< Updated upstream
<a name="aplicaciones"> </a>
## 💻 Categorías de aplicaciones
- El kernel decide qué programa obtiene qué bloques de memoria, inicia y elimina las aplicaciones, y maneja la visualización de texto o gráficos en un monitor.
- Las aplicaciones realizan solicitudes al núcleo y, a cambio, reciben recursos, como memoria, CPU y espacio en disco.
- El kernel también maneja el cambio de aplicaciones, un proceso conocido como multitarea.
- Hay una gran variedad de tipos de aplicaciones, como procesadores de texto, navegadores web y clientes de correo electrónico, y más.
- Un proceso es solo una tarea que el núcleo carga y rastrea.
- Una aplicación puede incluso necesitar múltiples procesos para funcionar, por lo que el núcleo se encarga de ejecutar los procesos, iniciarlos y detenerlos según lo solicitado, y distribuir los recursos del sistema.

El software de Linux generalmente cae en una de tres categorías:

1. *Aplicaciones de servidor*: El propósito de este software es proporcionar información a otras computadoras, llamadas clientes.
2. *Aplicaciones de escritorio*: Navegadores web, editores de texto, reproductores de música u otras aplicaciones con las que los usuarios interactúan directamente.
3. *Herramientas*: Una categoría suelta de software que existe para facilitar la administración de los sistemas informáticos.

<a name="servidor"> </a>
### </> **Aplicaciones de servidor**
- Linux sobresale en la ejecución de aplicaciones de servidor debido a su confiabilidad y eficiencia.
- Uno de los primeros usos de Linux fue para *servidores web*.
    - Un servidor web aloja contenido para páginas web, que son vistas por un navegador web utilizando el Protocolo de transferencia de hipertexto (HTTP) o cifrado con HTTPS.
- Existe una creciente demanda de software de servidor de nube privada que se pueda implementar y administrar internamente.

<p align="center">
  <img src="../imagenes/owncloud.png" style="width: 15%; height: 60px; float: left; padding: 5px;" alt="owncloud">
</p>
El proyecto ownCloud proporciona software para almacenar, sincronizar y compartir datos de servidores privados en la nube.  

<br><br>
<p align="center">
  <img src="../imagenes/nextcloud.png" style="width: 15%; height: 60px; float: left; padding: 5px;" alt="nextcloud">
</p>
El proyecto Nextcloud también proporciona software de nube privada.

<br><br>
<a name="escritorio"> </a>
### </> **Aplicaciones de escritorio**
- El ecosistema de Linux tiene una amplia variedad de aplicaciones de escritorio.
- ***Correo electrónico:***
    - La Fundación Mozilla lanzó Thunderbird, un cliente de correo electrónico de escritorio con todas las funciones que se conecta a un servidor POP o IMAP.
    - Otros clientes de correo electrónico notables son Evolution y KMail, que son los clientes de correo electrónico del proyecto GNOME y KDE.

- ***Creativo:***
    - Para los tipos creativos, hay Blender, GIMP (Programa de manipulación de imágenes Gnu) y Audacity, que manejan la creación de películas en 3D, la manipulación de imágenes en 2D y la edición de audio, respectivamente.

- ***Productividad:***
<p align="center">
  <img src="../gifs/libreoffice.gif" style="width: 20%; height: 100px; float: left; padding: 5px;" alt="libreoffice">
</p>

LibreOffice es una bifurcación de la suite de aplicaciones OpenOffice (a veces llamada OpenOffice.org).

<br><br>
<br><br>
- ***Navegadores web:***
<p align="center">
  <img src="../imagenes/firefoxgoogle.png" style="width: 20%; height: 80px; float: left; padding: 10px;" alt="firefoxgoogle">
</p>

Los navegadores Mozilla Firefox y Google Chrome son navegadores web de código abierto que son rápidos, ricos en funciones y tienen un excelente soporte para desarrolladores web.


<a name="herramientas_consola"> </a>
## 💻 Herramientas de consola
- UNIX tiene una superposición considerable entre las habilidades de desarrollo de software y administración de sistemas.
- Las herramientas para administrar sistemas tienen características de lenguajes de computadora, como bucles, y se usan ampliamente en la automatización de tareas de administración de sistemas.
- Por lo tanto, se requiere familiaridad básica con la programación para administradores de sistemas competentes.
- **Shells:**
    - Los usuarios interactúan con un sistema Linux a través de un shell, que acepta comandos para ejecutar.
    - Linux ofrece una variedad de shells para elegir tales como: ***shell Bourne, shell C, shell Bourne Again (Bash), tcsh, shell Korn (Ksh) y zsh.***

- **Editores de texto:**
    - La mayoría de los sistemas Linux ofrecen una selección de editores de texto que se usan comúnmente en la consola para editar archivos de configuración.
    - Los dos editores principales son **vi** (o el **vim** más moderno) y **Emacs**.
    - Pico y Nano están disponibles en la mayoría de los sistemas y proporcionan una edición de texto muy básica pero fácil de usar.


<a name="paquetes"> </a>
## 💻 Gestión de paquetes
- Todos los sistemas Linux necesitan agregar, eliminar y actualizar software.
- Las distribuciones modernas usan paquetes.
- Los paquetes son archivos comprimidos que agrupan una aplicación y sus dependencias (o archivos requeridos), lo que simplifica enormemente la instalación.
- Un administrador de paquetes se encarga de realizar un seguimiento de qué archivos pertenecen a cada paquete e incluso de descargar actualizaciones de los repositorios.
- En Linux, hay muchos sistemas de gestión de paquetes de software diferentes, pero los dos más populares son los de Debian y Red Hat.

- **Gestión de paquetes Debian:**
    - La distribución Debian y sus derivados, como Ubuntu y Mint, utilizan el sistema de gestión de paquetes de Debian.
    - La gestión de paquetes de Debian tiene paquetes de software que se distribuyen como archivos que terminan en la extensión `.deb.`
    - Las herramientas para administrar estos archivos incluyen `dpkg, apt-get, aptitude`, Synaptic y Software Center.

- **Gestión de paquetes RPM (Red Hat Package Manager):**
    - Según la base de estándares de Linux, el sistema de gestión de paquetes estándar es RPM.
    - RPM utiliza un archivo `.rpm` para cada paquete de software.
    - Las distribuciones derivadas de Red Hat, incluidos Centos y Fedora, usan RPM.
    - La herramienta de back-end más utilizada para RPM Package Management es el comando rpm.


<a name="lenguajes"> </a>
## 💻 Lenguajes de desarrollo
- Los lenguajes de programación de computadoras proporcionan una manera para que un programador ingrese instrucciones en un formato más legible para los humanos, y éstas instrucciones eventualmente se traduzcan en algo que la computadora entienda.
- Los lenguajes se dividen en dos: interpretados o compilados.
    - Un lenguaje interpretado traduce el código escrito en código de computadora a medida que se ejecuta el programa.
    - Un lenguaje compilado traduce todo el código de una vez.
- Linux fue escrito en un lenguaje compilado llamado **C.**
- C se ha extendido a lo largo de los años a **C ++, Objective C** y otras variantes.
- El lenguaje **Java** utiliza un CPU hipotético llamado **Java Virtual Machine (JVM)** y luego compila todo el código para ese.
- **JavaScript** es un lenguaje de programación interpretado de alto nivel que es una de las tecnologías principales en la red mundial.

- **Perl** es un lenguaje interpretado desarrollado originalmente para realizar la manipulación de texto, pero ha ganado relevancia con los administradores de sistemas y se utiliza en todo, desde la automatización hasta la creación de aplicaciones web.
- **PHP** es un lenguaje que se creó inicialmente para crear páginas web dinámicas.
- **Ruby** es otro lenguaje que fue influenciado por Perl y Shell que impulsa muchas de las herramientas líderes de automatización.
- **Python** es otro lenguaje de script que es de uso general.
    - Python tiene excelentes capacidades de procesamiento estadístico y es uno de los favoritos en la academia.
- **OpenSSL** es una biblioteca criptográfica que se utiliza en todo, desde servidores web hasta la línea de comandos.
- **C library:** Proporciona un conjunto básico de funciones para leer y escribir en archivos y pantallas, que utilizan las aplicaciones y otros idiomas por igual.


<a name="referencias"> </a>
## 📚 Referencias
* RPM Package Manager, from https://rpm.org/
=======
<a name="objetivo_aprendizaje"> </a>

El software de Linux generalmente cae en una de tres categorías:


+ **Aplicaciones de servidor:** El propósito de este software es proporcionar información a otras computadoras, llamadas clientes.
+ **Aplicaciones de escritorio:** navegadores web, editores de texto, reproductores de música u otras aplicaciones con las que los usuarios interactúan directamente.
+ **Herramientas:** una categoría suelta de software que existe para facilitar la administración de los sistemas informáticos.

## 🕸️ Aplicaciones del servidor

+ Linux sobresale en la ejecución de aplicaciones de servidor debido a su confiabilidad y eficiencia.
+ Uno de los primeros usos de Linux fue para servidores web.
Un servidor web aloja contenido para páginas web, que son vistas por un navegador web utilizando el Protocolo de transferencia de hipertexto (HTTP) o cifrado con HTTPS.
++ Existe una creciente demanda de software de servidor de nube privada que se pueda implementar y administrar internamente.
++ El proyecto ownCloud proporciona software para almacenar, sincronizar y compartir datos de servidores privados en la nube.
+ El proyecto Nextcloud también proporciona software de nube privada.

## Aplicaciones de escritorio

+ El ecosistema de Linux tiene una amplia variedad de aplicaciones de escritorio.
+ Correo electrónico:
La Fundación Mozilla lanzó Thunderbird, un cliente de correo electrónico de escritorio con todas las funciones que se conecta a un servidor POP o IMAP.
Otros clientes de correo electrónico notables son Evolution y KMail, que son los clientes de correo electrónico del proyecto GNOME y KDE.
+ Creativo:
Para los tipos creativos, hay Blender, GIMP (Programa de manipulación de imágenes Gnu) y Audacity, que manejan la creación de películas en 3D, la manipulación de imágenes en 2D y la edición de audio, respectivamente.
+ Productividad:
LibreOffice es una bifurcación de la suite de aplicaciones OpenOffice (a veces llamada OpenOffice.org).
+ Navegadores web:
Los navegadores Mozilla Firefox y Google Chrome son navegadores web de código abierto que son rápidos, ricos en funciones y tienen un excelente soporte para desarrolladores web.

## Herramientas de consola

+ UNIX tiene una superposición considerable entre las habilidades de desarrollo de software y administración de sistemas.
+ Las herramientas para administrar sistemas tienen características de lenguajes de computadora, como bucles, y se usan ampliamente en la automatización de tareas de administración de sistemas.
+ Por lo tanto, se requiere familiaridad básica con la programación para administradores de sistemas competentes.
+ Shells:
Los usuarios interactúan con un sistema Linux a través de un shell, que acepta comandos para ejecutar.
Linux ofrece una variedad de shells para elegir tales como: shell Bourne, shell C, shell Bourne Again (Bash), tcsh, shell Korn (Ksh) y zsh.

+ Editores de texto:
La mayoría de los sistemas Linux ofrecen una selección de editores de texto que se usan comúnmente en la consola para editar archivos de configuración.
Los dos editores principales son vi (o el vim más moderno) y Emacs.
Pico y Nano están disponibles en la mayoría de los sistemas y proporcionan una edición de texto muy básica pero fácil de usar.

## Gestión de paquetes

+ Todos los sistemas Linux necesitan agregar, eliminar y actualizar software.

+ Las distribuciones modernas usan paquetes.

+ Los paquetes son archivos comprimidos que agrupan una aplicación y sus dependencias (o archivos requeridos), lo que simplifica enormemente la instalación.

+ Un administrador de paquetes se encarga de realizar un seguimiento de qué archivos pertenecen a cada paquete e incluso de descargar actualizaciones de los repositorios.

+ En Linux, hay muchos sistemas de gestión de paquetes de software diferentes, pero los dos más populares son los de Debian y Red Hat.

+ Gestión de paquetes Debian:
La distribución Debian y sus derivados, como Ubuntu y Mint, utilizan el sistema de gestión de paquetes de Debian.
La gestión de paquetes de Debian tiene paquetes de software que se distribuyen como archivos que terminan en la extensión .deb.
Las herramientas para administrar estos archivos incluyen dpkg, apt-get, aptitude, Synaptic y Software Center.

+ Gestión de paquetes RPM (Red Hat Package Manager):
Según la base de estándares de Linux, el sistema de gestión de paquetes estándar es RPM.
RPM utiliza un archivo .rpm para cada paquete de software.
Las distribuciones derivadas de Red Hat, incluidos Centos y Fedora, usan RPM.
La herramienta de back-end más utilizada para RPM Package Management es el comando rpm.

## Lenguajes de desarrollo

Los lenguajes de programación de computadoras proporcionan una manera para que un programador ingrese instrucciones en un formato más legible para los humanos, y éstas instrucciones eventualmente se traduzcan en algo que la computadora entienda.

**Los lenguajes se dividen en dos: interpretados o compilados**
Un lenguaje interpretado traduce el código escrito en código de computadora a medida que se ejecuta el programa.
Un lenguaje compilado traduce todo el código de una vez.

Linux fue escrito en un lenguaje compilado llamado C.
C se ha extendido a lo largo de los años a C ++, Objective C y otras variantes.
El lenguaje Java utiliza un CPU hipotético llamado **Java Virtual Machine (JVM)** y luego compila todo el código para ese.
**JavaScript** es un lenguaje de programación interpretado de alto nivel que es una de las tecnologías principales en la red mundial.

+ **Perl** es un lenguaje interpretado desarrollado originalmente para realizar la manipulación de texto, pero ha ganado relevancia con los administradores de sistemas y se utiliza en todo, desde la automatización hasta la creación de aplicaciones web.
+ **PHP** es un lenguaje que se creó inicialmente para crear páginas web dinámicas.
+ **Ruby** es otro lenguaje que fue influenciado por Perl y Shell que impulsa muchas de las herramientas líderes de automatización.
+ **Python** es otro lenguaje de script que es de uso general.
Python tiene excelentes capacidades de procesamiento estadístico y es uno de los favoritos en la academia.
+ **OpenSSL** es una biblioteca criptográfica que se utiliza en todo, desde servidores web hasta la línea de comandos.
+ **C library**. Proporciona un conjunto básico de funciones para leer y escribir en archivos y pantallas, que utilizan las aplicaciones y otros idiomas por igual.

## Selección de recursos para Linux

Al seleccionar la distribución de Linux para un servidor es necesario considerar los recursos básicos de hardware como son:

1. Intel Celeron de 2.4 Ghz
2. Procesador Pentium IV
3. Tarjetas de Red: 2 NICs PCI Realtek/basadas en chip Realtek o Via
4. Disco duro: 40 GB
5. Memoria: 4 GB

## Tipos de Instalación

+ Estación de trabajo: Más adecuada si es nuevo en el mundo de Linux y quiere probarlo. 
+ Servidor: Si desea que su sistema funcione como un servidor basado en Linux utilizando servicios específicos.
+ Portátil: Instalación sencilla en ordenadores portátiles. 
+ Personalizada: Mayor flexibilidad en el proceso de instalación. Podrá elegir su esquema de particionamiento, los paquetes que desea instalar y mucho más. 
+ Actualización: Para actualizar rápidamente a los últimos paquetes y versiones del kernel. 

## Particiones en un disco duro para linux

+ Hay tres clases de particiones: primarias, extendidas y lógicas.
+ Muchas distribuciones necesitan que se creen a mano las particiones de Linux utilizando el programa fdisk. Otras pueden crearlas automáticamente.
+ En el primer sector del disco está el registro de arranque maestro “MBR” junto a la tabla de particiones.

## Particiones en un disco duro para Linux

En Linux los manejadores, que se encuentran en el directorio /dev, se usan para comunicarse con los dispositivos de su sistema como discos duros. Los discos duros SCSI se nombran con /dev/sda. Los discos duros IDE se nombran /dev/hda y las particiones son /dev/hda1, /dev/hda2, etc.

## Particiones en un disco duro para Linux 
Por lo general se crean dos particiones para Linux, una para ser usada como sistema de ficheros raíz y la otra como espacio de intercambio “swap”.
La partición swap, es un espacio de intercambio de ayuda a la memoria RAM a pasar datos temporalmente al disco duro.

## Herramientas de virtualización de sistemas operativos

1. VirtualBox: https://www.virtualbox.org
2. Vmware: https://www.vmware.com
3. Microsoft Azure: https://azure.microsoft.com/

## Instalación de Ubuntu
### Guía de trabajo autónomo

La instalación del sistema operativo a través de los CD's o DVD, solo se necesita tener este medio de instalación e insertarlo en la unidad lectora de CD-ROM / DVD-ROM y seguir las instrucciones.

### Configurando el idioma

Las versiones Linux basadas en Red Hat cuentan con un asistente gráfico llamado Anaconda.
Seleccione el idioma predeterminado que tendrá el sistema operativo como se muestra en la figura.
Como próximo paso presione el botón “Instalar Ubuntu”.

### Configurando el teclado

Seleccione el teclado como se muestra a continuación. Para el idioma Español existen diferentes distribuciones de teclado, las cuales varían por la ubicación de los signos de puntuación. Para conocer la distribución del teclado solo es necesario conocer la ubicación del carácter “@”, para la distribución español el “@” se encuentra en tecla “2”, para la distribución latinoamericana la “@” se encuentra en tecla “Q”.

### Configurando las particiones

Antes de comenzar la instalación, el asistente solicitará partición del disco duro en la cual se instalará el sistema operativo. Se muestran las siguientes opciones: 
Borrar disco e  instalar Ubuntu.- Borra todos sus programas, documentos, fotos, música y demás archivos en todos los sistemas operativos únicamente de la máquina virtual que está creando. 
Más opciones.- Permite particionar el disco duro de forma manual.

Al seleccionar la opción más opciones, se mostrará la siguiente ventana, que es una herramienta para particionar el disco duro. Para crear una partición, presione el botón “Nueva tabla de particiones”.

Después se mostrará una ventana de diálogo en la cual  deberá pulsar en “Continuar” para configurar las particiones, como se muestra en la segunda imagen.
Posteriormente presione el botón con el signo “+” que se encuentra en la esquina inferior izquierda.

A continuación se mostrará una ventana en donde se pueden cambiar las siguientes opciones:

Tamaño (MB).- Define el tamaño en Megabytes (MB) de la  partición.
Tipo de la nueva partición.- Se presentan dos opciones: lógica o primaria. Las particiones lógicas se recomiendan para el directorio raíz y para la memoria de intercambio (swap).
Punto de montaje.- Define el sistema de archivos que se instalará en ésta partición.

### Configurando la zona horaria

En esta parte se recomienda seleccionar la ubicación en la cual se encuentra el servidor para configurar la zona horaria, esto con el fin de tener sincronizada la fecha y hora del equipo.

### Configurando la contraseña de administrador

Definir la contraseña de “root” con privilegios de administrador, se recomienda que esta contraseña contenga caracteres alfanuméricos.

## Instalación de Ubuntu
### Bienvenido a Ubuntu

Finalmente, espere a que se realice la instalación de Ubuntu para poder hacer uso del sistema operativo.

## Shell

Cuando se ejecuta una aplicación de terminal y aparece un shell, que muestra una parte importante de la interfaz - el “prompt”. 
Normalmente, el mensaje contiene información sobre el usuario y el sistema. A continuación se muestra una estructura de aviso común:

El prompt que se muestra, contiene la siguiente información:
Username (sysadmin)
System name (localhost)
Current Directory (~)

## Comandos

Un comando es un programa de software que, cuando se ejecuta en la CLI, realiza una acción en la computadora.

Para ejecutar un comando, el primer paso es escribir el nombre del comando.

Si usted escribe ls y presiona Enter. El resultado debería parecerse al siguiente ejemplo:

Algunos comandos requieren una entrada adicional para ejecutarse correctamente.

Esta entrada adicional viene en dos formas: opciones y argumentos.
Las opciones se utilizan para modificar el comportamiento central de un comando.
Los argumentos se utilizan para proporcionar información adicional (como un nombre de archivo o un nombre de usuario).
El formato típico para un comando es el siguiente:

### Opciones

+ Las opciones se pueden usar con Comandos para expandir o modificar el comportamiento de un comando.
Por ejemplo, usando la opción -l del comando ls da como resultado una lista extensa, que proporciona información adicional sobre los archivos que se enumeran.

+ A menudo, el caracter se elige la letra l para mostrar más información o r por reversa.

+ Las opciones se pueden usar junto con otras opciones:   

+ Las opciones suelen ser letras simples; sin embargo, a veces también son palabras o frases.
+ Por lo general, los Comandos más antiguos usan letras simples, mientras que los comandos más nuevos usan palabras completas para las opciones.
+ Por lo general, los Comandos más antiguos usan letras simples, mientras que los comandos más nuevos usan palabras completas para las opciones. -h .
+ Las opciones de palabras completas están precedidas por dos guiones -- , caracteres como la forma de palabras completas de la opción  -h, la opción de --human-readable 

### Argumentos

Se puede usar un argumento para especificar algo sobre lo que el comando debe actuar.

Si el comando ls recibe el nombre de un directorio como argumento, enumera el contenido de ese directorio:

Algunos comandos (como ls) aceptan múltiples argumentos:

### Historial de comandos

+ Cuando se ejecuta un comando en el terminal, se almacena en una lista de historial.
+ Esto facilita la ejecución del mismo comando más tarde, eliminando la necesidad de volver a escribir todo el comando.
+ Al presionar la tecla de flecha hacia arriba  ↑ se muestra el comando anterior en la línea de solicitud.
+ Para ver la lista de historial completa de una terminal, use el comando  history.

### Historial de comandos

+ Si el comando deseado está en la lista que genera el comando de historial history , se puede ejecutar escribiendo un signo de exclamación ! y luego el número al lado del comando (es decir,! 3) (i.e., !3)

+ Si el comando de historial pasa un número como argumento, genera ese número de comandos anteriores de la lista de historial.

+ Para ejecutar el tipo de comando más reciente !! y presiona Enter: 
+ Para ejecutar la iteración más reciente de un comando específico, escriba !command y presione Enter.

### Visualización de páginas del manual

+ Para ver una página del comando man, use el comando man:

+ Por ejemplo, a continuación se muestra la página del comando man ls:

+ Navegue por el documento con las teclas de flecha:

+ Para salir de ver una página de manual, use la tecla Q.

## Visualización de páginas del manual

El comando man usa un localizador para mostrar documentos. Por lo general, este localizador es el comando less, pero en algunas distribuciones, puede ser el comando more. Ambos son muy similares en su desempeño.

## Encontrar comandos y documentación

Para buscar la ubicación de un comando o las páginas del comando man, use el comando whereis.

Este comando busca comandos, archivos de origen y páginas de manual en ubicaciones específicas donde estos archivos se almacenan normalmente:

Las páginas de manual se distinguen fácilmente de los comandos, ya que generalmente se comprimen con un programa llamado gzip, lo que da como resultado un nombre de archivo que termina en .gz.

## Encontrar cualquier archivo o directorio

+ Para buscar cualquier archivo o directorio, use el comando locate.

+ Este comando busca en una base de datos de todos los archivos y directorios que estaban en el sistema cuando se creó la base de datos.
Sin embargo, los archivos creados ese día no se podrán buscar con el comando de localizar porque la base de datos se actualiza todas las noches.
Es posible actualizar la base de datos de locate manualmente ejecutando el comando updatedb como root.

+ El resultado puede ser bastante grande, por lo que puede ser útil utilizar las siguientes opciones:
La opción -c del comando locate mostrará cuántos archivos coinciden:

+ La opción -b solo incluye listados que tienen el término de búsqueda en el nombre base del nombre del archivo. Para limitar aún más la salida, coloque un caracter \ delante del término de búsqueda:

## Documentación de información

+ Para mostrar la documentación de información de un comando, use el comando de información:

+ Para mostrar la documentación de información de un comando, use el comando de información:

+ Esta documentación se divide en nodos. En el ejemplo a continuación, la línea resaltada en blanco muestra que está actualmente en el nodo de invocación ls:

## Usar la opción de ayuda

Muchos comandos proporcionarán información básica, muy similar a la SINOPSIS que se encuentra en las páginas de manual, simplemente usando la opción --help para el comando.

## Estructura de directorios

En un sistema Windows, el nivel superior de la estructura de directorios se llama Mi PC.

La estructura de directorios de Linux, llamada sistema de archivos, también tiene un nivel superior llamado directorio raíz (simbolizado por la character slash /)

Para ver el contenido del directorio root, use el comando ls con el caracter / como argumento:


Observe que hay muchos directorios con nombres descriptivos que incluyen /boot, que contiene archivos para iniciar la computadora.

## Directorio Home

+ En la mayoría de las distribuciones de Linux hay un directorio llamado home debajo del directorio root /.

+ Debajo de este directorio /home hay un directorio para cada usuario en el sistema.

+ Cuando un usuario abre un shell, debe colocarse automáticamente en su directorio de inicio.
El usuario tiene el control total para crear y eliminar archivos y directorios adicionales en su directorio de inicio.
+ La mayoría de los otros directorios en un sistema de archivos Linux están protegidos con permisos de archivo.

+ El directorio home tiene un símbolo especial utilizado para representarlo, el caracter tilde ~.

+ El nombre del directorio es el mismo que el nombre del usuario.

+ Entonces, un usuario llamado sysadmin tendría un directorio de inicio llamado /home/sysadmin:

## Directorio actual

El comando pwd (directorio de trabajo de impresión) se puede utilizar para determinar dónde se encuentra actualmente el usuario dentro del sistema de archivos.

El comando pwd imprime el directorio de trabajo, que es la ubicación actual del usuario dentro del sistema de archivos.

## Cambiar directorios

+ Cuando un usuario abre un shell, generalmente comienza en su directorio home.

+ Para navegar por el sistema de archivos, use el comando cd (cambiar directorio).

+ Para pasar del directorio actual al directorio Documentos, use el nombre del directorio como argumento para el comando cd:

+ Después de cambiar los directorios, la nueva ubicación también se puede confirmar en el nuevo prompt, que se muestra nuevamente en azul en la imagen anterior.

## Cambiar directorios

+ Cuando se usa sin argumentos, el comando cd llevará al usuario a su directorio de inicio.
+ Si el usuario intenta cambiar a un directorio que no existe, el comando devuelve un mensaje de error:

## Rutas

Una ruta es una lista de directorios separados por el carácter /.

Hay dos tipos de rutas: absolutas y relativas.

Por ejemplo, /home/sysadmin es una ruta al directorio de inicio:

### Rutas absolutas


Las rutas absolutas permiten al usuario especificar la ubicación exacta de un directorio.

Las rutas absolutas siempre comienzan en el directorio root y, por lo tanto, siempre comienzan con el carácter /.

La ruta /home/sysadmin es una ruta absoluta; le dice al sistema que:
Comience en el directorio root / > muévase al directorio home > luego al directorio sysadmin.

Si la ruta /home/sysadmin se usa como argumento para el comando cd, mueve al usuario al directorio de inicio del usuario sysadmin.

### Rutas relativas

Una ruta relativa da instrucciones a un archivo en relación con la ubicación actual en el sistema de archivos.

El usuario debe estar actualmente en un directorio que contiene objetos en la ruta.

Las rutas relativas comienzan con el nombre de un directorio

### Rutas - Atajos: Los caracteres .

Los caracteres dos puntos ... siempre representan un directorio más alto en relación con el directorio actual, a veces denominado directorio padre.

Por ejemplo, para volver del directorio Art al directorio de la School:


El doble punto también se puede usar en rutas más largas:

### Rutas - Atajos: El caracter .

El caracter “.” representa el directorio actual.

Para el comando cd, este acceso directo no es muy útil, pero es útil para los comandos cubiertos en las secciones posteriores.

## Copiar archivos

El comando cp se usa para copiar archivos. Requiere una fuente y un destino.

La estructura del comando es la siguiente:


La fuente es el archivo que se copiará. El destino es donde se ubicará la copia.

El siguiente comando copiará el archivo /etc/hosts a su directorio de inicio:

## Mover archivos

Para mover un archivo, use el comando mv.

La sintaxis para el comando mv es muy similar al comando cp:



Cuando se mueve un archivo, el archivo se elimina de la ubicación original y se coloca en una nueva ubicación.

Nota: Si no tiene los permisos correctos, recibirá un mensaje de error "Permiso denegado".


## Crear directorios

Para crear un directorio, use el comando mkdir:

## Eliminar directorios

El comando rm se puede usar para eliminar directorios. Sin embargo, el uso predeterminado (sin opciones) del comando rm no podrá eliminar un directorio:

Para eliminar un directorio, use la opción -r (recursiva) para el comando rm:

Importante: cuando un usuario elimina un directorio, todos los archivos y subdirectorios se eliminan sin ninguna pregunta interactiva. Es mejor usar la opción   -i con el comando rm.

## Comprimir archivos

Linux proporciona varias herramientas para comprimir archivos, el más común es gzip. Aquí mostramos un archivo antes y después de la compresión:


El tamaño original del archivo llamado longfile.txt es 66540 bytes.
El archivo se comprime invocando el comando gzip con el nombre del archivo como argumento.
Una vez que se completa ese comando, el archivo original desaparece y se deja en su lugar una versión comprimida con una extensión de archivo .gz.
El tamaño del archivo ahora es de 341 bytes.

## Almacenar archivos - Modo crear

Crear un archivo con el comando tar requiere dos opciones con nombre:


El siguiente ejemplo muestra un archivo tar, también llamado tarball, que se crea a partir de múltiples archivos:

## Almacenar archivos - Modo extraer

Puede extraer el archivo con la opción –x una vez que se haya copiado en un directorio diferente. El siguiente ejemplo utiliza un patrón similar al de los otros modos:

El siguiente ejemplo extrae el contenido del archivo folder.tbz:

## Archivos ZIP

El archivo ZIP es la utilidad de almacenamiento predeterminada en Microsoft.
ZIP no es tan frecuente en Linux, pero es compatible con los comandos zip y descomprimir.
El modo predeterminado de zip es agregar archivos a un archivo comprimido y comprimirlo.

El siguiente ejemplo muestra un archivo comprimido llamado alpha_files.zip que se está creando:

El comando zip no se repetirá en subdirectorios de forma predeterminada (tar lo hace), por lo que debe usar la opción –r para indicar que se va a utilizar la recursividad. El commando unzip descomprime un archivo.





>>>>>>> Stashed changes
