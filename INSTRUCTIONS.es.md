# Web scraping

En este proyecto, vamos a obtener y analizar los datos sobre el beneficio de Tesla, que almacenaremos previamente en un DataFrame y en una base de datos de sqlite.

## Paso 1: Instalación de dependencias

Asegúrate de que tienes instalados los paquetes `pandas` y `requests` de Python para poder trabajar en el proyecto. En el caso de que no tengas las librerías instaladas, ejecuta en la consola:

```bash
pip install pandas requests
```

## Paso 2: Descargar HTML

La descarga del HTML de la página web se realizará con la librería `requests`, como vimos en la teoría del módulo.

La página web que queremos scrapear es la siguiente: [https://ycharts.com/companies/TSLA/revenues](https://ycharts.com/companies/TSLA/revenues). Recopila y almacena información sobre el crecimiento de la compañía cada tres meses, desde junio de 2009. Almacena el texto scrapeado de la web en alguna variable.


## Paso 3: Transforma el HTML

El siguiente paso para comenzar con la extracción de la información es transformarlo en un objeto estructurado. Hazlo utilizando `BeautifulSoup`. Una vez hayas interpretado el HTML correctamente, analízalo para:

1. Buscar todas las tablas.
2. Encontrar la tabla con la evolución trimestral.
3. Almacena los datos en un DataFrame.


## Paso 4: Procesa el DataFrame

A continuación, limpia las filas para obtener los valores limpios eliminando `$` y las comas. Elimina también aquellas que estén vacías o no tengan información.


## Paso 5: Almacena los datos en sqlite

Crea una instancia vacía de la base de datos e incluye en ella los datos limpios, como vimos en el módulo de bases de datos. Una vez tengas una base de datos vacía:

1. Crea la tabla.
2. Inserta los valores.
3. Almacena (`commit`) los cambios.


## Paso 6: Visualiza los datos

¿Qué tipos de visualizaciones podemos realizar? Propón al menos 3 y muéstralos.