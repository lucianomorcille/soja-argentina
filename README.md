Clasificación del rendimiento de soja en Argentina
==============================

## **Descripción del dominio y contexto del problema**

El dominio seleccionado corresponde al sector agropecuario, específicamente al 
cultivo de soja en Argentina. 

El dataset utilizado contiene información histórica de la serie 1941–2023, con registros 
por provincia y departamento. Este tema resulta de gran interés debido a la relevancia 
económica y ambiental de la soja en el país, siendo uno de los principales cultivos de 
exportación y un indicador del impacto de las condiciones climáticas sobre la 
producción agrícola. 

El problema se enmarca en el ámbito del Aprendizaje Automático aplicado al análisis de 
datos agrícolas, donde se busca utilizar técnicas de modelado predictivo para 
comprender los factores que influyen en el rendimiento y anticipar posibles escenarios 
productivos. 

La elección de este dominio surge del interés en integrar aspectos productivos y 
ambientales, explorando cómo las variables agronómicas y meteorológicas afectan la 
productividad del cultivo en distintas regiones y campañas. Además, me resultó 
interesante elegirlo debido a que aparte de esta carrera estoy estudiando Licenciatura 
en Ciencias Ambientales en la Facultad de Agronomía, por lo que busqué un tema en el 
que pueda combinar ambas carreras. 

## **Objetivos generales** 

-Clasificar el rendimiento de soja en categorías de productividad (“Bajo”, “Medio” y “Alto”) 
utilizando modelos de clasificación supervisada, con el fin de identificar las provincias y 
campañas agrícolas más productivas, y facilitar la toma de decisiones en la planificación 
del sector agropecuario. 

## **Objetivos específicos** 

-Analizar la evolución temporal y espacial de la producción de soja en Argentina.

-Identificar las variables más influyentes sobre el rendimiento promedio del cultivo. 

-Implementar un enfoque de clasificación para categorizar el rendimiento en niveles 
“Bajo”, “Medio” y “Alto”. 

-Incorporar variables climáticas (temperatura media, precipitaciones, humedad relativa) 
para mejorar la precisión del modelo predictivo. 

-Evaluar y comparar el desempeño de distintos modelos mediante métricas de error y 
precisión.

## **Descripción del dataset y origen**

El dataset principal se titula “soja-serie-1941-2023.csv”. El mismo fue obtenido de la pagina https://www.datos.gob.ar/dataset/agroindustria-soja---siembra-cosecha-produccion-rendimiento y contiene aproximadamente más de 80 años de registros a nivel provincial y departamental. Las variables incluidas son:


*cultivo_nombre*: nombre del cultivo, que en este caso corresponde a la soja

*anio*: año del registro

*campania*: campaña agrícola correspondiente

*provincia_nombre y provincia_id*: identifican la provincia donde se cultiva

*departamento_nombre y departamento_id*: indican la subdivisión administrativa dentro de la provincia

*superficie_sembrada_ha*: superficie sembrada, expresada en hectáreas

*superficie_cosechada_ha*: superficie cosechada, expresada en hectáreas

*produccion_tm*: producción total, medida en toneladas métricas

*rendimiento_kgxha*: rendimiento promedio, expresado en kilogramos por hectárea. 

El otro dataset "registro_climatico_por provincia_1981_2023" es de mi autoría con información que recopilé de la página NASA POWER (https://power.larc.nasa.gov/). El mismo contiene la siguientes variables:

*provincia*: se refiere a la provincia a la cual corresponden los datos.

*anio*: año en el que fueron recolectados esos datos.

*precipitacion_total*: precipitación total en el año por provincia.

*temperatura_media*: temperatura media medida por año y por provincia.

*humedad_relativa*: humedad relativa medida por año y por provincia.

Ya tengo todos los datos pero aún no terminé de completar este dataset. En estos días subiré el archivo actualizado y completo.

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
