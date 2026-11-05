# Proyecto Final:

## Análisis de carreras de Fórmula 1

Este repositorio contiene el código desarrollado para el proyecto final de la asignatura de Adquisición de Datos de 2º iMAT.

El objetivo es construir un dataset con los resultados de las carreras de Fórmula 1 entre 2019 y 2024 combinando dos fuentes de datos y analizar la influencia de los pit stops en el resultado final. El proyecto se divide en:

1. Web scraping con Scrapy de las tablas de clasificación de cada carrera en Wikipedia
2. Obtención de los pit stops de cada carrera a través de la API de Jolpica (antigua Ergast)
3. Unión de ambas fuentes en un único dataset
4. Análisis de los datos para responder a distintas preguntas sobre los pit stops, la posición de salida, los puntos y la evolución de los equipos


## Estructura del proyecto

- `main.py`: ejecuta el scraping, las llamadas a la API y genera el dataset final
- `apartado_scrapy/`: proyecto de Scrapy, con el spider en `spiders/f1_results.py`
- `jolpicaF1_api.py`: funciones para obtener los pit stops de la API, agregarlos por piloto y unirlos con los datos de Wikipedia
- `analisis_ap4.ipynb`: análisis y visualizaciones del dataset final
- `requirements.txt`: librerías necesarias

Al ejecutar `main.py` se crea la carpeta `data/` con un csv por carrera y el archivo `Merged_data.csv` con todos los datos unidos, que es el que se utiliza en el notebook.


## Ejecución

Es necesario tener conexión a internet, ya que los datos se descargan al ejecutar:

python main.py


## Requisitos

Para ejecutar el código es necesario tener instalado Python 3 y las siguientes librerías:

scrapy
pandas
lxml
requests
numpy
matplotlib
seabornv
