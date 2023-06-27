---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

# 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

## 1.4 Mantenimiento y respaldo del sistema
- [Comprimir archivos](#comprimir)
- [Almacenar archivos](#almacenar)
- [Archivos ZIP](#zip)
- [Automatización de tareas programadas](#automatizacion)
- [Scripting](#scripting)
- [Linux en la Nube](#linux_nube)
- [La Nube (The Cloud)](#nube)
- [Virtualización](#virtualizacion)
- [Contenedores](#contenedores)


<a name="comprimir"> </a>
## 💻 Comprimir archivos

- Linux proporciona varias herramientas para comprimir archivos, el más común es gzip. Aquí mostramos un archivo antes y después de la compresión:

- El tamaño original del archivo llamado longfile.txt es 66540 bytes.

- El archivo se comprime invocando el comando gzip con el nombre del archivo como argumento.

- Una vez que se completa ese comando, el archivo original desaparece y se deja en su lugar una versión comprimida con una extensión de archivo .gz.

- El tamaño del archivo ahora es de 341 bytes.


<a name="almacenar"> </a>
## 💻 Almacenar archivos

Crear un archivo con el comando tar requiere dos opciones con nombre:

El siguiente ejemplo muestra un archivo tar, también llamado tarball, que se crea a partir de múltiples archivos:


## Almacenar archivos - Modo extraer

Puede extraer el archivo con la opción –x una vez que se haya copiado en un directorio diferente. El siguiente ejemplo utiliza un patrón similar al de los otros modos:

El siguiente ejemplo extrae el contenido del archivo folder.tbz:


<a name="zip"> </a>
## 💻 Archivos ZIP

- El archivo ZIP es la utilidad de almacenamiento predeterminada en Microsoft.
ZIP no es tan frecuente en Linux, pero es compatible con los comandos zip y descomprimir.

- El modo predeterminado de zip es agregar archivos a un archivo comprimido y comprimirlo.

- El siguiente ejemplo muestra un archivo comprimido llamado alpha_files.zip que se está creando:

- El comando zip no se repetirá en subdirectorios de forma predeterminada (tar lo hace), por lo que debe usar la opción –r para indicar que se va a utilizar la recursividad. El commando unzip descomprime un archivo.


<a name="automatizacion"> </a>
## 💻 Automatización de tareas programadas

La programación de tareas de mantenimiento regulares, como las copias de seguridad, es administrada por el servicio cron en Linux. El formato del archivo /etc/crontab es el siguiente:

# Un comentario inicia con el símbolo de # en cualquier parte del archivo.
```
  *      *       *         *        *          
minute  hour  day-month  month  day(s)-week   username   command to be executed
```

Ejercicio: Para realizar la tarea de reinicio del servidor, el domingo, miércoles y viernes a las 02h00 am.


<a name="scripting"> </a>
## 💻 Scripts en Bash

## Script de un menú de administración para el servidor con linux

``` #!/bin/bash
#################################################
# Script de menu de consola para administracion #
# Desarrollado por: Adriana Collaguazo          #
#################################################
 
echo -e "\n========================================="
echo -e "MENU DE ADMINISTRACION DEL SERVIDOR LINUX"
echo -e "                              Version 1.0                                       "
echo -e "=========================================\n"
 
echo "1. Interfaces            2. Cambio de IP WAN"
echo "3. Usuarios              4. Envio de correo"
echo "5. Sniffer               6. Logs del sistema"
echo -e "7. Reiniciar          8. Apagar\n"
echo -n "[$HOSTNAME]: "
read opcion
 
function interfaces()
{
ifconfig | less
sleep 4
}
  
function cambioip()
{
diriface="/etc/sysconfig/network-scripts/ifcfg-enp0s3"
 
echo -e "\nLa direccion IP WAN actual (enp0s3) es: $(ifconfig enp0s3 | sed -n '2p' |
 cut -c14-22)"
read -p "Ingrese la nueva direccion IP WAN (enp0s3): " dirip
read -p "Ingrese la nueva mascara de subred para la WAN: " ipnetmask
read -p "Ingrese la puerta de enlace predeterminada: " defgw
 
echo -e "IPADDR=$dirip \nNETMASK=$ipnetmask \nGATEWAY=$defgw" >> $diriface
 
echo -e "\nCambiando la direccion IP WAN en la interfaz enp0s3....\n"
service network restart
sleep 4
}
 
case $opcion in
 
1) interfaces;;
 
2) cambioip;;

5) Comando
tcpdump
 
esac

```

```
[root@localhost scripting]# ./menuadmin.sh

==========================================
MENU DE ADMINISTRACION DEL SERVIDOR LINUX
                              Version 1.0
==========================================

1. Interfaces            2. Cambio de IP WAN
3. Usuarios              4. Envio de correo
5. Sniffer               6. Logs del sistema
7. Reiniciar             8. Apagar

[localhost.localdomain]: 1
```

<a name="linux_nube"> </a>
## 💻 Linux en la Nube

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