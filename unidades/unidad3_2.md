---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)


# Unidad 3: Tecnologías Web

# 🎯 **Objetivo de Aprendizaje**
Al finalizar la clase el estudiante será capaz de:
- Diseñar sitios web dinámicos y sus funciones para la administración de la información usando gestores de base de datos.

# 3.2 RESTful API
- [API](#api)
    - [¿Por qué se usan las APIs?](#uso_api)
    - [APIs sincrónicas](#sincronicas)
    - [APIs asincrónica](#asincronicas)
    - [Estilos de Arquitectura de la API](#estilos)

<a name="api"> </a>

## 💻 API

- Una interfaz de programación de aplicaciones (API) permite una conversación de software con otra.
- Utiliza interacciones basadas en la web o protocolos de comunicación comunes y sus propios estándares patentados.
- Una API determina qué tipo de datos, servicios y funcionalidad expone la aplicación a terceros.
- Al proporcionar API, las aplicaciones pueden controlar lo que exponen de forma segura.


<p align="center">
  <img src="imagenes/assr_unidad3_1_api.png" alt="observador" width="80%">
</p>

<a name="uso_api"> </a>

### 🕸️ ¿Por qué se usan las APIs?

Las API están diseñadas para ser consumidas mediante programación por otras aplicaciones y también pueden ser usadas por humanos que desean interactuar con la aplicación manualmente.
Los casos de uso de las API son los siguientes:

- **Tareas de automatización:** cree un script que realice tareas manuales de forma automática y programática.
- **Integración de datos:** una aplicación puede consumir o reaccionar a los datos proporcionados por otra aplicación.
- **Funcionalidad:** una aplicación puede integrar la funcionalidad de otra aplicación en su producto.

<a name="sincronicas"> </a>

### 🕸️ APIs sincrónicas

- Las API sincrónicas responden directamente a una solicitud proporcionando datos inmediatamente.

**¿Cuándo las API son sincrónicas?**
- Las API son sincrónicas cuando los datos de la solicitud están disponibles fácilmente.

**Ventajas de un diseño de API sincrónico**
- Las API sincrónicas permiten que la aplicación reciba datos inmediatamente. Si la API está diseñada correctamente, el rendimiento de la aplicación será mejor.

**Procesamiento del lado del cliente**
- La aplicación que realiza la solicitud de API debe esperar la respuesta antes de realizar tareas adicionales de ejecución de código.

<p align="center">
  <img src="imagenes/assr_unidad3_1_sincronicas.png" alt="observador" width="60%">
</p>

***Las entradas se venden en orden por orden de llegada. Este es un proceso sincrónico.***


<a name="asincronicas"> </a>

### 🕸️ APIs asincrónica
- Las API asincrónicas proporcionan una respuesta (sin datos) para indicar que se ha recibido la solicitud.

**¿Cuándo son asincrónicas las API?**
- Las API son asincrónicas cuando la solicitud tarda algún tiempo en procesarse el servidor o si los datos no están disponibles fácilmente.

**Beneficio del diseño de API asincrónico**
- Las API asincrónicas permiten que la aplicación continúe su ejecución sin ser bloqueada hasta que el servidor procese la solicitud, lo que resulta en un mejor rendimiento.

**Procesamiento del lado del cliente**
- Con el procesamiento asincrónico, el diseño de la API en el lado del servidor define el requisito en el lado del cliente.

<p align="center">
  <img src="imagenes/assr_unidad3_1_asincronicas.png" alt="observador" width="60%">
</p>


<a name="estilos"> </a>

### 🕸️ Estilos de Arquitectura de la API

**Cliente-Servidor**
- El cliente y el servidor deben ser independientes entre sí.
- Esto permitirá que el cliente se construya para múltiples plataformas, lo que simplificará los componentes del lado del servidor.

<p align="center">
  <img src="imagenes/assr_unidad3_1_cliente_servidor.png" alt="observador" width="60%">
</p>

**Sin estado**
- Las solicitudes del cliente al servidor deben contener el modelo cliente-servidor REST y toda la información que el servidor necesita para realizar la solicitud.
- El servidor no puede contener estados de sesión.

<p align="center">
  <img src="imagenes/assr_unidad3_1_sin_estado.png" alt="observador" width="60%">
</p>

**Modelo de caché**
• Las respuestas del servidor deben indicar si la respuesta se puede almacenar en caché o no en caché.
• Si se puede almacenar en caché, el cliente puede utilizar los datos de la respuesta para solicitudes posteriores.

<p align="center">
  <img src="imagenes/assr_unidad3_1_cache.png" alt="observador" width="60%">
</p>

**Interfaz uniforme**
La interfaz entre el cliente y el servidor se adhiere a los cuatro principios:
- Identificación de recursos
- Manipulación de recursos a través de representaciones • Mensajes autodescriptivos
- Hypermedia como motor del estado de la aplicación.

**Sistema de capas**
El sistema en capas consta de diferentes capas jerárquicas en las que cada capa proporciona servicios sólo a la capa que está encima.
Como resultado, consume servicios de la capa siguiente.

<p align="center">
  <img src="imagenes/assr_unidad3_1_capas.png" alt="observador" width="60%">
</p>

**Código bajo demanda**
Modelo de sistema en capas REST
- La información devuelta por un servicio REST puede incluir código ejecutable (por ejemplo, javascript) o enlaces destinados a extender de manera útil la funcionalidad del cliente.
- La restricción es opcional porque la ejecución de códigos de terceros introduce posibles riesgos de seguridad.