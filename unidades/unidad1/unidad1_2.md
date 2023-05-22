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
### 🕸️ **Aplicaciones de servidor**
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
### 🕸️ **Aplicaciones de escritorio**
- El ecosistema de Linux tiene una amplia variedad de aplicaciones de escritorio.
- ***Correo electrónico:***
    - La Fundación Mozilla lanzó Thunderbird, un cliente de correo electrónico de escritorio con todas las funciones que se conecta a un servidor POP o IMAP.
    - Otros clientes de correo electrónico notables son Evolution y KMail, que son los clientes de correo electrónico del proyecto GNOME y KDE.

- ***Creativo:***
    - Para los tipos creativos, hay Blender, GIMP (Programa de manipulación de imágenes Gnu) y Audacity, que manejan la creación de películas en 3D, la manipulación de imágenes en 2D y la edición de audio, respectivamente.
    
- ***Productividad:***
<p align="center">
  <img src="../gifs/libreoffice.gif" style="width: 25%; height: 100px; float: left; padding: 10px;" alt="libreoffice">
</p>

LibreOffice es una bifurcación de la suite de aplicaciones OpenOffice (a veces llamada OpenOffice.org).

- ***Navegadores web:***
<p align="center">
  <img src="../imagenes/firefoxgoogle.png" style="width: 25%; height: 80px; float: left; padding: 10px;" alt="firefoxgoogle">
</p>

Los navegadores Mozilla Firefox y Google Chrome son navegadores web de código abierto que son rápidos, ricos en funciones y tienen un excelente soporte para desarrolladores web.


<a name="herramientas_consola"> </a>

## 💻 Herramientas de consola


<a name="paquetes"> </a>
<a name="lenguajes"> </a>
<a name="referencias"> </a>

