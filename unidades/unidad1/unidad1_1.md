---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

## 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

# 1.1. Distribuciones Linux
- [¿Qué es Linux?](#definicion)
    - [Linux en la industria](#industria)
    - [Linux es un kernel](#nucleo)
    - [Linux es open source](#open_source) 
    - [Linux usa CLI](#cli)
    - [Linux tiene distribuciones](#distribuciones)
        - [Red Hat](#redhat)
        - [SUSE](#suse)
        - [Debian](#debian)
        - [Android](#android)
        - [Otras distribuciones de Linux](#otras)
- [Referencias](#referencias)

<a name="objetivo_aprendizaje"> </a>



<a name="definicion"> </a>
## 💻 ¿Qué es Linux?
<p align="center">
  <img src="../imagenes/terminal-linux.png" style="width: 30%; height: 180px; float: left; padding: 15px;" alt="linux">
</p>


En 1983, *Richard Stallman* inició el Proyecto GNU, con el propósito de crear un sistema operativo similar y compatible con UNIX. 

En 1991, en Helsinki, *Linus Torvalds* comenzó un proyecto que más tarde llegaría a ser el núcleo Linux.

Las características que componen Linux incluyen lo siguiente:

- Detección y preparación del hardware
- Gestión de procesos
- Administración de memoria
- Proporcionar interfaces de usuario
- Control de sistemas de archivos
- Proporcionar acceso y autenticación de usuarios
- Ofreciendo utilidades administrativas
- Servicios de puesta en marcha
- Herramientas de programación

<a name="industria"> </a>
### 🕸️ **Linux en la industria**
<p align="center">
  <img src="../imagenes/industria-linux.png" alt="industria" width="70%">
</p>

Los trabajos de Linux están en todas partes, las habilidades de Linux están en demanda en casi todas las industrias y categorías de trabajo en el planeta.

VIDEO

<a name="nucleo"> </a>
### 🕸️ **Linux es un kernel**
Linux significa el *núcleo del sistema*, que es el controlador central de todo lo que sucede en la computadora.
Linux es una combinación de software llamado GNU/Linux, que define el sistema operativo.
- GNU es el software gratuito que proporciona equivalentes de código abierto de muchos comandos comunes de UNIX.
- La parte de Linux de esta combinación es el kernel de Linux, que es el núcleo del sistema operativo.

<a name="open_source"> </a>
### 🕸️ **Linux es open-source**
Históricamente, la mayoría del software se ha emitido bajo una licencia de código cerrado.

Esto significa que tiene derecho a usar el programa ejecutable o el código de máquina, pero no puede ver el código fuente.

El desarrollo de Linux es muy similar al aumento del software de código abierto.

La filosofía de código abierto es que tiene derecho a obtener el código fuente del software y modificarlo para su propio uso.

<a name="cli"> </a>
### 🕸️ **Linux usa CLI**
Hay dos tipos básicos de interfaces disponibles que le permiten interactuar con el sistema operativo.

- El usuario típico de la computadora hoy está más familiarizado con una interfaz gráfica de usuario (GUI).
En una GUI, las aplicaciones se presentan en ventanas que pueden redimensionarse y moverse. Hay menús y herramientas para ayudar a los usuarios a navegar.

- El segundo tipo de interfaz es la interfaz de línea de comando (CLI), una interfaz basada en texto para la computadora.
La CLI se basa principalmente en la entrada del teclado.

    - La interfaz de línea de comando (CLI) es un sistema de entrada de texto simple para ingresar comandos de una sola palabra hasta scripts complicados.
    - En los sistemas que se inician en una GUI, hay dos formas comunes de acceder a la línea de comandos, un terminal basado en GUI y un terminal virtual:
        - Navegue a la aplicación Terminal desde el menú de aplicaciones.
        - Se puede ejecutar un terminal virtual al mismo tiempo que una GUI, pero puede requerir que el usuario inicie sesión a través del terminal virtual antes de poder ejecutar commandos.

<a name="distribuciones"> </a>
### 🕸️ **Linux tiene distribuciones**
<p align="center">
  <img src="../imagenes/distribuciones.png" alt="distribuciones" width="80%">
</p>
Una distribución se refiere al kernel de Linux, las herramientas y el conjunto de aplicaciones que se agrupan.

Tome Linux y las herramientas GNU, agregue algunas aplicaciones orientadas al usuario, como un navegador web y un cliente de correo electrónico, y tendrá un sistema Linux completo.

Casi todos los programas que son necesarios en un sistema GNU/Linux son de libre distribución y están disponibles en algún sitio de la red para su descarga, normalmente en forma de código fuente.

Hay distribuciones que se centran en la ejecución de servidores, equipos de escritorio o incluso herramientas específicas de la industria, como el diseño electrónico o la informática estadística.

Existen organizaciones comerciales que se dedican a empaquetar juntos los programas, incluirlos en algún medio como un CD, añadir un manual de instrucciones y proporcionar soporte técnico.

También existen distribuciones realizadas por voluntarios y que no tienen ánimo de lucro.

Las distribuciones modernas cuentan con:

- Un programa de instalación que guíe al usuario desde el principio e instale los paquetes básicos.
- Un gestor de paquetes que se encargue de proporcionar el interfaz necesario para que el administrador pueda instalar y desinstalar programas de una manera fácil.
- Un entorno gráfico (normalmente KDE o GNOME), con el que se integren el resto de los programas.
- Manuales de instalación y uso y documentación adicional sobre los programas. 
- Un sistema de seguimiento de errores (bugs) y fallos de seguridad que proporcione al usuario versiones corregidas de los programas lo más rápido posible cuando se detecte un fallo.

<a name="redhat"> </a>
### 🕸️ **Red Hat**
<p align="center">
  <img src="../imagenes/redhat.png" style="width: 30%; height: 150px; float: right; padding: 15px;" alt="redhat">
</p>

- Se enfoca en aplicaciones de servidor como web y servicio de archivos.
- [Red Hat Enterprise Linux (RHEL)](https://www.redhat.com/), una distribución estable con largos ciclos de lanzamiento.
- Su gestor de paquetes (RPM) se ha convertido en un estándar en el mundo GNU/Linux.
- Patrocina el Proyecto Fedora, un escritorio personal con el último software.
- CentOS es una versión gratuita del software RHEL que no ofrece soporte.
- Scientific Linux es una distribución de uso específica basada en Red Hat.


<a name="suse"> </a>
### 🕸️ **SUSE**
<p align="center">
  <img src="../imagenes/suse.png" style="width: 20%; height: 80px; float: right; padding: 15px;" alt="debian">
</p>

- [SUSE](https://www.suse.com/) Una de las primeras distribuciones.
- Originalmente derivado de Slackware.
- Contiene código propietario y se vende como un producto de servidor. Algunos módulos o complementos pueden contener código propietario.
- Se vende como un producto de servidor aunque existe una versión de estación de trabajo. 
- Se preocupa especialmente por la seguridad del sistema.
- [OpenSUSE](https://www.opensuse.org/) es una versión completamente abierta y gratuita con múltiples paquetes de escritorio.


<a name="debian"> </a>
### 🕸️ **Debian**
<p align="center">
  <img src="../imagenes/debian.png" style="width: 15%; height: 70px; float: right; padding: 15px;" alt="debian">
</p>

- Esfuerzo comunitario que promueve el uso de software de código abierto.
- [Debian](https://www.debian.org/) inventó su propio sistema de administración de paquetes (apt) basado en el formato de archivo .deb.
- Ubuntu es su distribución derivada más popular, que tiene variantes para escritorio, servidor y aplicaciones. Ubuntu también ofrece una versión LTS.
- Linux Mint es un derivado de Ubuntu con varias versiones gratuitas, algunas tienen restricciones de licencia.

<a name="android"> </a>
### 🕸️ **Android**
<p align="center">
  <img src="../imagenes/android.png" style="width: 20%; height: 80px; float: right; padding: 15px;" alt="android">
</p>

- Proporciona una plataforma para usuarios móviles.
- Carece de los paquetes tradicionales de GNU / Linux para que sea compatible con el escritorio.
- Patrocinado por Google.
- [Android](https://www.android.com/) ofrece continuamente actualizaciones para ayudarte a hacer las cosas más rápido, más fácilmente y de forma personalizada.


<a name="otras"> </a>
### 🕸️ **Otras distribuciones de Linux**
<p align="center">
  <img src="../imagenes/raspberryPi.jpg" style="width: 30%; height: 100px; float: right; padding: 15px;" alt="debian">
</p>

- [Raspberry Pi](https://www.raspberrypi.org/) es una distribución de Linux diseñada para ejecutarse en hardware "Raspberry Pi”.

- [Linux From Scratch (LFS)](https://www.linuxfromscratch.org/) consiste en un libro en línea, código fuente e instrucciones para construir una distribución Linux personalizada.



<a name="referencias"> </a>
## 📚 Referencias
* Linux: The Complete Reference, Sixth Edition by Richard Petersen
* Red Hat Enterprise Linux (RHEL), from https://www.redhat.com/
* SUSE, from https://www.suse.com/
* Debian, from https://www.debian.org/
* Android, from https://www.android.com/
* Raspberry Pi, from https://www.raspberrypi.org/
* Linux From Scratch (LFS), from https://www.linuxfromscratch.org