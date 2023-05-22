---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

# 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

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
