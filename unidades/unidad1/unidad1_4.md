---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 1: Internet y servicios en red

# 🎯 Objetivo de Aprendizaje
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

## 1.4. Mantenimiento y respaldo del sistema
- [Comprimir archivos](#comprimir)
- [Almacenar archivos](#almacenar)
- [Archivos ZIP](#zip)
- [Automatización de tareas programadas](#automatizacion)

<a name="comprimir"> </a>
## 💻 Comprimir archivos

Linux proporciona varias herramientas para comprimir archivos, el más común es gzip. Aquí mostramos un archivo antes y después de la compresión:


El tamaño original del archivo llamado longfile.txt es 66540 bytes.
El archivo se comprime invocando el comando gzip con el nombre del archivo como argumento.
Una vez que se completa ese comando, el archivo original desaparece y se deja en su lugar una versión comprimida con una extensión de archivo .gz.
El tamaño del archivo ahora es de 341 bytes.

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
  



``` function cambioip()
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

``` [root@localhost scripting]# ./menuadmin.sh

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

## Script en Perl para la configuración de enrutadores Cisco






