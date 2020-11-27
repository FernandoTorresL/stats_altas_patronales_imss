# stats_altas_patronales_imss

Automatic ETL process about 'Alta Patronal' procedure on 'Instituto Mexicano del Seguro Social (IMSS)' offices in México

## Results, test and work in progress published on my [Tableau profile](https://public.tableau.com/profile/fertorresmx)

### Description

We want stats about 'Alta Patronal' procedure that is managed on IMSS's offices on México. The data available is not public and its reserved to internal use.

The exercise in this repository only show off dummy data and will be a practice of several technologies on DataScience.

## Data origins

The data came from several PDF's reports that gather the following fields:

- Registro Patronal (unique ID of each employer)
- Modalidad
- Centro Informático de Zona (One of 3 datacenters)
- Delegación IMSS (State office)
- Subdelegación IMSS (Sub-state office)
- Fecha y hora de inicio del trámite (Timestamp when procedure starts)
- Fecha y hora de fin del trámite (Timestamp when procedure finish)

## Goals

The main objetive is show stats that allow us to improve the flow of the procedure and answer the following questions:

- Which is the average time on minutes to finish this procedure?
- How many procedures are presented by year, hour, weekday, or in each state office and sub-state office?
- Which are the rush hours on this offices?

(I'll add more questions later)

## Requirements and problems founded

Some issues and problems are:

- The preliminary reports are internal and came from a website, searching for a date range very short. So, to get all the data since 2009 and quickly requires several amount of time and check 300+ PDF's files.
- There are some reports with missing data or corrupted values, most of them on the timestamps.
- It's important to clean the data and avoid duplicates.
- On some cases, not all the fields or data are available.

We need:


- [ ] Implement an fast, automatic and repetitive ETL process.
- [ ] Clean data and complete missing information.
- [ ] Create a database with the data.
- [ ] Create an API REST to query the information and share it with another programs
- [ ] Possibility of custom reports
- [ ] Get valuable data, insights and data for improve the bussiness (lower time on procedures, identify rush hours, high demand...)

### To do list

- [x] Keep the data safe and confidential.
- [x] Create a automatic process to download PDF documents and generate .csv files (WIP).
- [x] Clean and complete the missing data.
- [ ] Load the info on a database
- [x] Create graphs and customs reports with the data.
- [ ] Create an API REST
- [ ] Publish the data and reports on a dashboard and website


## WIP (Work in progress)

So far, the Jupyter Notebook on this repo is semi-automatic. Has been published and test graph on Tableau with only 500K records of dummy data; the real data is about 1.2M of records (with more fields) since 2009. 
Just now, I'm coding on a develop branch a python program pipeline about the entire ETL process.

---

## Follow me

### [fertorresmx.dev](https://www.fertorresmx.dev/)

#### :globe_with_meridians: Twitter, Instagram: [@fertorresmx](http://www.twitter/fertorresmx)



---

# stats_altas_patronales_imss

Proceso ETL sobre trámites de Alta Patronal en subdelegaciones IMSS
## Resultados publicados en mi [perfil de Tableau](https://public.tableau.com/profile/fertorresmx)

### Descripción

Se desea obtener información estadística acerca del trámite Alta Patronal, el cual se realiza en oficinas de afiliación en las subdelegaciones del Instituto Mexicano del Seguro Social (IMSS). Si bien parte de esta información es de caracter confidencial y no es información pública, de forma interna se puede obtener directamente por otros medios. 

El ejercicio que se realizará en este repositorio sólo expondrá información de prueba y ficticia y será una práctica de diversas tecnologías.

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
- [ ] Implementar un proceso de ETL rápido, automatizado y recurrente.
- [ ] Que se limpie y complete la información faltante.
- [ ] Que la información se encuentre disponible en una base de datos.
- [ ] Que se puede consultar mediante una API para consumo interno.
- [ ] Que se puedan generar reportes personalizados.
- [ ] Generar información valiosa para el negocio (para mejorar tiempos de atención, identificar y preveer alta demanda, etc).

### Solución propuesta

- [x] Mantener la confidencial de la información.
- [ ] Automatizar el acceso y generación de documentos PDF. (WIP)
- [x] Automatizar la extracción de información a archivos CSV. (WIP)
- [x] Limpiar y completar la data faltante.
- [ ] Cargar la información a una base de datos.
- [x] Crear gráficos con la información generada.
- [ ] Generar una API para consulta.
- [ ] Crear un sitio web con un dashboard y un generador de reportes personalizados.

## WIP (Work in progress)

Por ahora el proceso en el notebook en éste repositorio es semi-automático. Se publicó una gráfica de ejemplo en Tableau con 500,000 registros de prueba; los datos reales superan 1.2 millones de registros y muchos más campos. Se inicia la etapa de automatizar totalmente un proceso de ETL usando Python

---

## Follow me

### [fertorresmx.dev](https://www.fertorresmx.dev/)

#### :globe_with_meridians: Twitter, Instagram: [@fertorresmx](http://www.twitter/fertorresmx)
