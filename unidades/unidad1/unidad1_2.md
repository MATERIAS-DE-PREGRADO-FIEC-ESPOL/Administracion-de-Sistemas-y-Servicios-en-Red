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
  <img src="../imagenes/owncloud.png" style="width: 20%; height: 80px; float: left; padding: 20px;" alt="owncloud">
</p>

El proyecto ownCloud proporciona software para almacenar, sincronizar y compartir datos de servidores privados en la nube.


<p align="center">
  <img src="../imagenes/nextcloud.png" style="width: 20%; height: 70px; float: left; padding: 20px;" alt="nextcloud">
</p>

El proyecto Nextcloud también proporciona software de nube privada.


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
  <img src="../gifs/libreoffice.gif" style="width: 25%; height: 100px; float: left; padding: 5px;" alt="libreoffice">
</p>

LibreOffice es una bifurcación de la suite de aplicaciones OpenOffice (a veces llamada OpenOffice.org).



- ***Navegadores web:***
<p align="center">
  <img src="../imagenes/firefoxgoogle.png" style="width: 25%; height: 80px; float: left; padding: 10px;" alt="firefoxgoogle">
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
