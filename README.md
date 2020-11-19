# stats_altas_patronales_imss

Proceso ETL sobre trámites de Alta Patronal en subdelegaciones IMSS

### Description
## WIP (Work in progress)

Se desea obtener información estadística acerca del trámite Alta Patronal, el cual se realiza en oficinas de afiliación en todas las subdelegaciones del Instituto Mexicano del Seguro Social (IMSS). Si bien parte de esta información es de caracter confidencial, no es información pública y de forma interna se puede obtener directamente por otros medios, el ejercicio que se realizará en este repositorio sólo expondrá información de prueba y ficticia y será una práctica de diversas tecnologías.

## Origen de la información
La información se obtiene principalmente de unos reportes en formato PDF que contienen la siguiente información:

- Registro Patronal (identificador único del empleador)
- Modalidad
- Centro Informático de Zona (CIZ)
- Delegación IMSS
- Subdelegación IMSS
- Fecha y hora de inicio del trámite
- Fecha y hora de fin del trámite

## Objetivo

El objetivo es generar estadísticas con esta información y obtener respuesta a las siguientes y otras interrogantes, por ejemplo:

- ¿Cuál es el tiempo promedio de atención del trámite?
- ¿Cuántos trámites se realizan por año, hora, día, delegación, subdelegación?
- ¿Cuál es el día/horario con mayor demanda?

## Requerimientos y problemas encontrados

Algunos problemas e inconvenientes a resolver:

- Los reportes preliminares se obtienen de forma interna ingresando a una aplicación web, indicando un periodo de fecha, sin embargo, sólo se puede usar un periodo de fecha muy corto, por lo que obtener la información que existe desde al menos 2009,  supone generar y analizar 300+ archivos individuales.
- Se han detectado documentos PDF con información corrupta o con un formato de fecha/hora no estandarizado.
- Se debe limpiar la información y evitar duplicidades.
- En algunos casos no se tiene la información completa.

Se requiere:
- Implementar un proceso de ETL rápido, automatizado y recurrente.
- Que se limpie y complete la información faltante.
- Que la información se encuentre disponible en una base de datos.
- Que se puede consultar mediante una API para consumo interno.
- Que se puedan generar reportes personalizados.
- Generar información valiosa para el negocio (para mejorar tiempos de atención, identificar y preveer alta demanda, etc).
 
### Solución propuesta

- Mantener la confidencial de la información.
- Automatizar el acceso y generación de documentos PDF.
- Automatizar la extracción de información a archivos CSV.
- Limpiar y completar la data faltante.
- Cargar la información a una base de datos.
- Generar una API para consulta.
- Crear un sitio web con un dashboard y un generador de reportes personalizados.

## WIP (Work in progress)

---

## Follow me

### [fertorresmx.dev](https://www.fertorresmx.dev/)

#### :globe_with_meridians: Twitter, Instagram: [@fertorresmx](http://www.twitter/fertorresmx)
