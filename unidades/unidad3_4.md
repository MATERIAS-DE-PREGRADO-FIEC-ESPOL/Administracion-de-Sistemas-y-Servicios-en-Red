---
remote_theme: pages-themes/cayman@v0.2.0
---
[Regresar](/Administracion-de-Sistemas-y-Servicios-en-Red/)


# Unidad 3: Tecnologías Web

# 🎯 **Objetivo de Aprendizaje**
Al finalizar la clase el estudiante será capaz de:
- Diseñar sitios web dinámicos y sus funciones para la administración de la información usando gestores de base de datos.

# 3.4 Almacenamiento de datos
- [Formato de datos](#formato)
    - [XML](#xml)
    - [JSON](#json)
    - [YAML](#yaml)


<a name="formato"> </a>

## 💻 Formato de datos

• Las API Rest le permiten intercambiar información con servicios remotos y equipamiento.
• Los tres formatos estándar más populares para intercambiar información con API remotas son XML, JSON y
YAML.
• El análisis de XML, JSON o YAML es un requisito frecuente para interactuar con las API. Un patrón frecuente en las implementaciones de API REST es el siguiente:
• Autenticar, normalmente mediante la publicación de una combinación de usuario/contraseña y la recuperación de un token que caduca para su uso en la autenticación de solicitudes posteriores.
• Ejecutar una solicitud GET a un extremo determinado (autenticando según sea necesario) para recuperar el estado de un recurso, solicitando XML, JSON o YAML como formato de salida.
• ModificarelXML,JSONoYAMLdevuelto.
• Ejecute un POST (o PUT) en el mismo punto final (de nuevo, autenticando según sea necesario) para cambiar el estado del recurso, solicitando nuevamente XML, JSON o YAML como formato de salida e interpretándolo según sea necesario para determinar si la operación se realizó correctamente.

<a name="xml"> </a>

### 🕸️ XML

- Extensible Markup Language (XML) es una metodología genérica para envolver datos textuales en etiquetas simétricas para indicar semántica.
- Es un derivado de Structured Generalized Markup Language (SGML), y también el padre de HyperText Markup Language (HTML).Los nombres de archivo XML suelen terminar en ".xml"

***Un ejemplo de documento XML***
```
<data>
  <interface-configurations xmlns="http://cisco.com/ns/yang/Cisco-IOS-XR-ifmgr-cfg">
   <interface-configuration>
    <active>act</active>
    <interface-name>GigabitEthernet0/0/0/0</interface-name>
    <shutdown></shutdown>
   </interface-configuration>
   <interface-configuration>
    <active>act</active>
    <interface-name>GigabitEthernet0/0/0/1</interface-name>
    <shutdown></shutdown>
   </interface-configuration>
   <interface-configuration>
    <active>act</active>
    <interface-name>GigabitEthernet0/0/0/2</interface-name>
    <shutdown></shutdown>
   </interface-configuration>
  </interface-configurations>
  <interfaces xmlns="http://cisco.com/ns/yang/Cisco-IOS-XR-um-interface-cfg">
   <interface>
    <interface-name>GigabitEthernet0/0/0/0</interface-name>
    <shutdown/>
   </interface>
   <interface>
    <interface-name>GigabitEthernet0/0/0/1</interface-name>
    <shutdown/>
   </interface>
   <interface>
    <interface-name>GigabitEthernet0/0/0/2</interface-name>
    <shutdown/>
   </interface>
  </interfaces>
 </data>
```


**Descripción de los formatos de datos XML**
- **Cuerpo del documento XML:** Excepto las dos primeras líneas de un documento XML, el resto del documento se considera como el cuerpo.
- **Nombres de etiquetas definidos por el usuario:** Los nombres de etiquetas XML son definidos por el usuario. Si está redactando XML para su propia aplicación, elija nombres de etiquetas que expresen claramente el significado de los elementos de datos, sus relaciones y jerarquía.
- **Codificación especial de caracteres:** Los datos se transmiten en XML como texto legible.
- **PrólogoXML:** El prólogo XML es la primera línea de un archivo XML.
- **Comentarios en XML:** Los archivos XML pueden incluir comentarios, utilizando la misma convención de comentarios utilizada en los documentos HTML.
- **Atributos XML:** XML permite incrustar atributos dentro de etiquetas para transmitir información adicional.


<a name="json"> </a>

### 🕸️ JSON

- JSON, o JavaScript Object Notation, es un formato de datos derivado de la forma en que se escriben literales de objetos complejos en JavaScript.
- Los nombres de archivo JSON suelen terminar en ".json".
- A continuación, se muestra un archivo JSON de ejemplo, que contiene dos valores que son cadenas de texto, uno es un valor booleano y dos son matrices(Array):

```
{
  "data": {
    "Cisco-IOS-XR-ifmgr-cfg:interface-configurations": {
       "interface-configuration": [
	  {
	     "active": "act",
	     "interface-name": "GigabitEthernet0/0/0/0",
	     "shutdown": [
	         null
             ]
           },
           {
	     "active": "act",
	     "interface-name": "GigabitEthernet0/0/0/1",
	     "shutdown": [
	         null
	     ]
	    },
	    {
	     "active": "act",
	     "interface-name": "GigabitEthernet0/0/0/2",
	     "shutdown": [
	         null
	     ]
	    }
	  ],
	"Cisco-IOS-XR-man-netconf-cfg:netconf-yang": {
	   "agent": {
	     "ssh": true
	    }
	},
 }
```

**Comprendiendo los formatos de datos JSON**

- **Tipos de datos básicos JSON:** Los tipos de datos básicos JSON incluyen números, cadenas, booleanos o nulos.
- **Objetos JSON:** Al igual que en JavaScript, los objetos individuales en JSON comprenden pares clave/valor, que pueden estar rodeados por llaves, individualmente.
- **Mapas y listas JSON:** En este caso, cada par clave/valor individual no necesita su propio conjunto de corchetes, pero todo el objeto sí.puede expresar matrices ordenadas por JavaScript (o 'listas') de datos u objetos.
- **Sin comentarios en JSON:** A diferencia de XML y YAML, JSON no admite ningún tipo de método estándar para incluir comentarios el código.
- **Espacio en blanco insignificante:** Elespacio en blanco en JSON no es significativo, y en los archivos se puede emplear sangría utilizando tabs o espacios como se prefiera, o no en absoluto.


<a name="yaml"> </a>

### 🕸️ YAML
- YAML Ain't Markup Language (YAML) es un superconjunto de JSON diseñado para una legibilidad humana aún más fácil.
- Como superconjunto de JSON, los analizadores YAML generalmente pueden analizar documentos JSON (pero no viceversa).
- Por lo tanto, YAML es mejor que JSON en ciertas tareas, incluida la capacidad de incrustar JSON directamente (incluidas las comillas) en archivos YAML.

```
NETWORKING:
 domain_name: cisco.com
 domain_name_servers: [171.70.168.183]
 networks:
 - gateway: 192.168.50.1
   pool: [192.168.50.100 to 192.168.50.2504
   segments: [management, provision]
   subnet: 192.168.50.0/24
   vlan_id: 105
 - gateway: 10.86.67.1
   segments: [api]
   subnet: 10.86.67.0/24
   vlan_id: 3522
```

- **Estructura de Archivos (File Structure) YAML:** Los archivos YAML se abren convencionalmente con tres guiones (— solos en una línea) y terminan con tres puntos (... igualmente).
- **Tipos de Datos(Data Types) YAML:** Los tipos de datos básicos de YAML incluyen números, cadenas, booleanos o nulos.
- **Objetos básicos(Basic Objects):** En YAML, los tipos de datos básicos se equiparan a claves.
- **Sangría de YAML y estructura de archivos(Indentation and File Structure):** YAML indica su jerarquía mediante sangría.
- **Mapas y listas(Maps and Lists):** YAML representa fácilmente tipos de datos más complejos, como mapas que contienen varios pares clave/valor y listas ordenadas.
  - Los mapas generalmente se expresan en varias líneas, comenzando con una clave de etiqueta y dos puntos, seguidos de miembros, sangrados en las líneas siguientes:

```
mymap:
 myfirstkey: 5
 mysecondkey: The quick fox
 ```
