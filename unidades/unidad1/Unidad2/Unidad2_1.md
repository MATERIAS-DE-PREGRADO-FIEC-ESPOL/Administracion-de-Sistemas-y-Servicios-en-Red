---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

# Unidad 2: Internet y servicios en red
1. ADMINISTRACIÓN DE SERVICIOS EN RED
2. ENRUTAMIENTO EN LINUX
3. LINUX EN SISTEMAS EMBEBIDOS
4. SERVICIOS PARA ANÁLISIS DE DATOS


## 🎯 Objetivo de Aprendizaje

Al finalizar la clase el estudiante será capaz de:

Experimentar la gestión de servicios en red incluyendo servicios de Internet más usados  para el análisis de utilización de recursos computacionales que cumplan con  requerimientos específicos.

## 🕸️  💻 📚Conceptos Básicos de Servicios de Red

- Un único sistema Linux puede proporcionar varios tipos diferentes de servicios, que van desde seguridad a la  administración e incluyen servicios de Internet como: sitios web y sitios FTP, correo electrónico e impresión,  herramientas de seguridad como SSH y kerberos, herramientas de red administrativas como DHCP y LDAP.

- La interfaz de conexión de red es en sí un servicio que se puede reiniciar a voluntad. Cada servicio opera como un  “daemon” continuamente en ejecución que busca peticiones para sus servicios particulares. En el caso de un  servicio web, las solicitudes provendrán de usuarios remotos. Puede activar o desactivar los servicios iniciando  o apagando sus demonios.

- El proceso de iniciar o cerrar un servicio es manejado por scripts de servicio.

## 🕸️ Conceptos de Servicios de Red
### Servicios iniciales: **STANDALONE Y XINETD**

<p align="center">
  <img src="../imagenes/.png" style="width: 20%; height: 80px; float: right; padding: 15px;" alt=>
</p>


Un servicio es un demonio que se ejecuta simultáneamente con los demás  programas, buscando continuamente una solicitud para sus servicios, ya sea de  otros usuarios de su sistema o de usuarios remotos que se conectan a su sistema  a través de una red. Cuando un servidor recibe una solicitud de un usuario, inicia  una sesión para proporcionar sus servicios.

Por ejemplo, si los usuarios quieren descargar un archivo desde su sistema,  pueden usar su propio cliente FTP para conectarse a su servidor FTP e iniciar una  sesión. En la sesión, pueden acceder y descargar archivos desde su sistema. Su  servidor debe estar funcionando para que un usuario acceda a sus servicios. Por  ejemplo, si configura un sitio web en su sistema con archivos HTML, debe tener el  programa de servidor web httpd ejecutándose antes de que los usuarios puedan  acceder a su sitio web y mostrar esos archivos.


```
Directorio /etc/xinet.d:
root@ workstation acollaguazo]# cd /etc/xinet.d
[root@workstation xinetd.d]# ll
total 0
Estado del servicio xinetd:
[root@workstation xinetd.d]# service xinetd status  Redirecting to /bin/systemctl status xinetd.service  xinetd.service
Loaded: not-found (Reason: No such file or directory)  Active: inactive (dead)
Instalación del servicio xinetd usando el repositorio YUM:
[root@workstation acollaguazo]# yum install xinetd
Loaded plugins: fastestmirror, langpacks
Loading mirror speeds from cached hostfile
base: mirror.cedia.org.ec
extras: mirror.cedia.org.ec
updates: mirror.cedia.org.ec  Resolving Dependencies
--> Running transaction check
---> Package xinetd.x86_64 2:2.3.15-13.el7 will be installed
--> Finished Dependency Resolution  Dependencies Resolved
================================================================================
Package	Arch	Version	Repository	Size
================================================================================
Installing:
xinetd	x86_64	2:2.3.15-13.el7	base	128 k  Transaction Summary
================================================================================
Install 1 Package
Total download size: 128 k  Installed size: 261 k
Is this ok [y/d/N]: y
Downloading packages:

warning: /etc/xinetd.conf created as /etc/xinetd.conf.rpmnew  Verifying : 2:xinetd-2.3.15-13.el7.x86_64
Installed:
xinetd.x86_64 2:2.3.15-13.el7  Complete!

```

```
4. Estado del servicio xinetd posterior a la instalación: 

 [root@workstation acollaguazo]# service xinetd status  Redirecting to /bin/systemctl status xinetd.service  xinetd.service - Xinetd A Powerful Replacement For Inetd
Loaded: loaded (/usr/lib/systemd/system/xinetd.service; enabled)  Active: active (running) since Thu 2017-05-04 22:05:10 ECT; 16s ago  Process: 8768 ExecStart=/usr/sbin/xinetd -stayalive -pidfile
/var/run/xinetd.pid $EXTRAOPTIONS (code=exited, status=0/SUCCESS)  Main PID: 8769 (xinetd)
CGroup: /system.slice/xinetd.service
└─8769 /usr/sbin/xinetd -stayalive -pidfile /var/run/xinetd.pid  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing daytime  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing discard  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing discard  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing echo  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing echo  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing tcpmux  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing time  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: removing time
May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: xinetd Version 2....  May 04 22:05:10 workstation.fiec.espol.edu.ec xinetd[8769]: Started working: ...  Hint: Some lines were ellipsized, use -l to show in full.

````


## Protocolo FTP (File Transfer Protocol)

<p align="center">
  <img src="../imagenes/.png" style="width: 20%; height: 80px; float: right; padding: 15px;" alt=>
</p>

**FTP (File Transfer Protocol)**
El software del servidor FTP consiste en un daemon FTP y archivos de configuración. El daemon es un programa que comprueba continuamente las solicitudes de FTP de usuarios remotos. Cuando se recibe una solicitud, gestiona un inicio de sesión, establece la conexión a la cuenta de usuario solicitada y ejecuta los comandos FTP enviados por el usuario remoto. Utiliza el protocolo TCP, y el puerto 20, 21.

Existen varios servidores FTP disponibles para su uso en sistemas  operativos Linux:

**Paso 1. Instalar el paquete vsftpd**

```

[root@srv1-linux vsftpd]# yum -y install vsftpd  Dependencies Resolved
=========================================================================
Package	Arch	Version	Repository
=========================================================================
Updating:
vsftpd	x86_64	3.0.2-21.el7	base

Transaction Summary
=========================================================================
Running transaction

Updating:  vsftpd-3.0.2-21.el7.x86_64    1/2
Cleanup:  : vsftpd-3.0.2-9.el7.x86_64    1/2
Verifying:  vsftpd-3.0.2-21.el7.x86_64   1/2
Verifying: vsftpd-3.0.2-9.el7.x86_64     1/2

Updated:
vsftpd.x86_64 0:3.0.2-21.el7  Complete!

```

**Paso 2. Configurar el archivo /etc/vsftpd/vsftpd.conf**

```
[root@srv1-linux adita]# vi /etc/vsftpd/vsftpd.conf
# Allow anonymous FTP? (Beware - allowed by default if you comment this out).  anonymous_enable=YES	#Cambiar por anonymous_enable=NO
#
# Uncomment this to allow local users to log in.
# When SELinux is enforcing check for SE bool ftp_home_dir
local_enable=YES  #
# Uncomment this to enable any form of FTP write command.  write_enable=YES
#
# You may specify an explicit list of local users to chroot() to their home  # directory. If chroot_local_user is YES, then this list becomes a list of  # users to NOT chroot().
# (Warning! chroot'ing can be very dangerous. If using chroot, make sure that  # the user does not have write access to the top level directory within the
# chroot)
#chroot_local_user=YES	#Descomentar está línea quitandole el símbolo numeral

````
**Paso 3. Reiniciar el servicio**
´
````
[root@srv1-linux adita]#service vsftpd restart
````

# PROTOCOLO DNS (DOMAIN NAME SERVICE)

**DNS (Domain Name Service)**

Convierte nombres de máquinas a direcciones IP, es decir, mapea de una  nombre a una dirección y viceversa. Hay varios servicios que puede  utilizar para resolver direcciones IP. El más utilizado es Berkeley Internet  Name Domain service (BIND). Al configurar la biblioteca de resolución  para utilizar el servicio de nombres DNS para las búsquedas de host,  también tiene que indicar qué servidores de nombres utilizar. Hay un  archivo separado para esto llamado /etc/resolv.conf. Utiliza el  protocolo TCP/UDP con el puerto 53.
La configuración DNS más importante son las zonas de dominios que se  encuentran en el archivo /etc/named.conf. Entre los registros de  configuración de zonas se encuentran:
A: Este registro asocia una dirección IP con un nombre de host.  MX: Un intercambiador de correo para un dominio.
CNAME: Este registro asocia un alias con el nombre de host canónico de  un host.
PTR: Este tipo de registro se utiliza para asociar nombres en el dominio  in-addr.arpa con nombres de host.

+ Paquete del servicio dns: bind, bind-chroot, bind-utils

+ Archivo de configuración de zona de dominio 

````
vbrew: /etc/named.conf
zone "vbrew.com" {
type master;  allow-transfer { 10.10.0.5;
172.16.90.4;
1.2.3.4;
};
file "/etc/bind/db.vbrew.com";
};
zone "0.168.192.in-addr.arpa" {  type master;
file "/etc/bind/db.192.168.0";
````

## **PROTOCOLOS SMTP/POP/IMAP**

**Correo**.-
El servidor de correo proporcionan a los usuarios servicios de correo electrónico. Ellos  tienen sus propios protocolos TCP/IP tales como el Simple Mail Transfer Protocol (SMTP),  Post Office Protocol (POP), Internet Mail Access Protocol (IMAP). Muchas distribuciones  de Linux instalarán y configurarán automáticamente sendmail o postfix. También puede  configurar su sistema Linux para ejecutar un servidor POP. Dichos servidores de correo  están asociados con diferentes hosts mediante registros de intercambio de correo,  conocidos como registros MX, en la configuración DNS de una red. Utiliza el protocolo  SMTP para el correo saliente con el puerto 25 y el protocolo POP para el correo  entrante con el puerto 110.

**Por ejemplo:**
name  espol.edu.ec
class
MX
type
0	espol-edu-ec.mail.protection.outlook.com

+ Servicio de correo saliente: sendmail

+ Servicio de correo entrante: dovecot

+ Servicio de administración vía web para el cliente de correo: SquirrelMail  https://squirrelmail.org/

+ Servicio de Anti-spam: SpamAssassin  http://spamassassin.apache.org/


## PROTOCOLO DE NAVEGACIÓN
**Proxy**

Los servidores proxy operan como un  intermediario entre una red local y los  servicios disponibles en uno más grande  como Internet. Los servidores proxy  mantienen copias actuales de las páginas  web de acceso común. Squid es un servidor  gratuito, de código abierto y de caché  proxy para clientes web, diseñado para  acelerar el acceso a Internet y proporcionar  controles de seguridad para servidores web.  Utiliza el protocolo TCP, y el puerto 3128.

Los protocolos soportados por squid son

+ Paquete: squid

+ Paquete para generación de reporte del squid: SARG

## PROTOCOLOS DE SERVICIOS DE RED

