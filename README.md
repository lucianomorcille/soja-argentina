# Predicción del rendimiento de soja en Argentina

## Contexto del problema

La soja constituye uno de los cultivos más importantes de Argentina debido a su relevancia económica y su participación en las exportaciones agroindustriales del país. La producción de este cultivo se encuentra influenciada por diversos factores, entre ellos las condiciones climáticas, la superficie sembrada, la superficie cosechada y las características productivas de cada región.

Comprender cómo estos factores afectan el rendimiento resulta fundamental para mejorar la planificación agrícola, optimizar la utilización de recursos y anticipar posibles escenarios productivos. En este contexto, el análisis de datos históricos permite estudiar el comportamiento de la producción de soja a lo largo del tiempo y detectar patrones asociados a variaciones climáticas y productivas.

Para el desarrollo de este proyecto se utilizaron datos históricos de producción de soja en Argentina correspondientes al período 1941-2023, complementados con información climática provincial del período 1981-2023 obtenida a partir de la plataforma NASA POWER.

## Justificación

La elección de este tema se fundamenta en la importancia que posee la producción de soja para la economía argentina y en la creciente necesidad de comprender los efectos que las condiciones ambientales ejercen sobre la productividad agrícola.

Además, el proyecto permite integrar conocimientos provenientes de dos áreas de formación complementarias: la Ciencia de Datos y las Ciencias Ambientales. Esta combinación posibilita abordar un problema real mediante técnicas de análisis de datos y modelado predictivo, utilizando información climática y productiva para generar conocimiento útil para la toma de decisiones.

Asimismo, la disponibilidad de registros históricos extensos y de variables meteorológicas relevantes convierte a este problema en un caso adecuado para la aplicación de técnicas de aprendizaje automático.

## Aplicación del Aprendizaje Automático

El rendimiento de los cultivos depende de múltiples variables que interactúan de manera compleja y que no siempre presentan relaciones lineales. Debido a ello, los métodos tradicionales de análisis pueden resultar insuficientes para capturar completamente los patrones presentes en los datos.

El Aprendizaje Automático permite construir modelos capaces de identificar relaciones entre variables productivas y climáticas a partir de ejemplos históricos, generando predicciones sobre nuevos casos sin necesidad de definir explícitamente todas las reglas que intervienen en el proceso.

En este proyecto se aborda un problema de regresión supervisada, ya que se dispone de observaciones históricas donde el rendimiento de soja es conocido y se busca predecir dicho valor a partir de un conjunto de variables explicativas. La aplicación de modelos de aprendizaje automático permite evaluar el aporte de diferentes factores al rendimiento del cultivo y generar estimaciones que pueden resultar útiles para la planificación agrícola y el análisis de escenarios futuros.

## Objetivo general

Predecir el rendimiento de soja (kg/ha) en Argentina a partir de variables productivas y climáticas mediante modelos de aprendizaje automático, con el fin de identificar los factores que influyen en la productividad y generar estimaciones útiles para la planificación agrícola.

## Objetivos específicos

* Analizar la evolución temporal y espacial de la producción de soja en Argentina.
* Identificar las variables que presentan mayor relación con el rendimiento del cultivo.
* Incorporar variables climáticas (temperatura media, precipitación total y humedad relativa) para mejorar la capacidad predictiva de los modelos.
* Implementar y comparar distintos modelos de regresión.
* Evaluar el desempeño de los modelos mediante métricas de error.
* Determinar cuáles son los factores con mayor influencia sobre el rendimiento de la soja.


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
