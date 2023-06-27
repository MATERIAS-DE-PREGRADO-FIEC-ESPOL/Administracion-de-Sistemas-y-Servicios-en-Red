---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)

## Trabajo Autónomo 2
## Automatización de la administración de un servidor Linux

## 🎯 Objetivo de Aprendizaje 
Al finalizar la clase el estudiante será capaz de:
- Utilizar los sistemas operativos basados en Linux mediante una interfaz de administración que permita el manejo adecuado de los recursos y servicios.

**Introducción**
Uno de los sistemas operativos más usados para el desarrollo web es Linux, cuyo kernel se encarga fundamentalmente de gestionar los recursos del equipo, establecer comunicación con los diferentes dispositivos, gestionar programas en ejecución, administrar la memoria, así como también el acceso a los sistemas de almacenamiento y uso del microprocesador. Dado que se trata de un software libre, se ofrecen varias versiones bajo la licencia GLP, entre las principales distribuciones se encuentran: Ubuntu, Debian, CentOS, Raspberry OS, entre otras.

**Instrucciones**
El formato del trabajo tiene habilitado recuadros de color amarillo para que llenen las respuestas.
Los trabajos se reciben hasta la fecha planificada en el Aula Virtual.
Coloque el nombre del archivo así “ASSR_TAA_GrupoB_Apellido1_ApellidoN”, siendo A el número del trabajo, B el número del grupo, N el último apellido del integrante del grupo.
Una vez que haya desarrollado el trabajo, cada integrante del grupo contestará la encuesta de evaluación de los trabajos autónomos ingresando al enlace https://bit.ly/2UdUwrj

**Actividades**
La empresa Adita S.A. tiene un único servidor que contiene servicios de proxy. Debido a una falla eléctrica el servidor presente errores en el disco duro por lo cual el personal del área de infraestructura decide iniciar el proyecto de creación de una granja de servidores independientes para el servicio de proxy. Considerando lo mencionado, han contratado a un grupo de ingenieros especializados para que realicen las siguientes actividades:


Actividad 1: Instalación

Paso 1. Creación de Máquinas virtuales
Para este trabajo autónomo se hará uso de tres máquinas virtuales. Se usará una máquina virtual con Windows 10, una máquina virtual con CentOS, y finalmente, una máquina virtual 	que corra Ubuntu Server.
Este paso consta en replicar lo aprendido en el trabajo autónomo 1, creando así las máquinas virtuales pedidas en el párrafo anterior.

	
Paso 2. Instalación de GNS3

GNS3 es un software de simulación que permite crear y testear redes virtuales. Este software permite importar routers, switches, firewalls, servidores, etc. A diferencia de otros programas similares, como lo puede ser Cisco Packet Tracer, GNS3 permite importar imágenes reales de los dispositivos antes mencionados, haciendo así que el uso de este simulador sea mucho más parecido a la realidad al momento de trabajar con los equipos, de la misma manera, no presenta las limitaciones que otros presentan.

Instalación: Para la instalación del simulador, use la página oficial de descargas. Descargue el archivo de programa y siga la guía de instalación oficial de acuerdo a su sistema operativo.


Actividad 2: Configuración de proxy transparente

Paso 1. Creación de la topología

Paso 2. Instalación y configuración de Squid en CentOS

En este paso, se debe realizar la instalación del paquete de Squid en la máquina virtual de CentOS. Squid es un proxy de cacheo que reduce el ancho de banda y que mejora los tiempos de respuesta de las páginas web. 
Referencia: http://www.squid-cache.org/
En este trabajo autónomo se deberá instalar el paquete en la máquina virtual como se mencionó anteriormente. Una vez que el paquete se encuentre instalado, se deberá realizar la configuración del mismo para que este actúe como un proxy transparente que permita a las otras dos máquinas virtuales restantes conectarse a Internet.

