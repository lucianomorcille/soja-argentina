Clasificación del rendimiento de soja en Argentina
==============================
Descripción del dominio y contexto del problema 
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
Objetivos generales 
-Clasificar el rendimiento de soja en categorías de productividad (“Bajo”, “Medio” y “Alto”) 
utilizando modelos de clasificación supervisada, con el fin de identificar las provincias y 
campañas agrícolas más productivas, y facilitar la toma de decisiones en la planificación 
del sector agropecuario. 
Objetivos específicos 
-Analizar la evolución temporal y espacial de la producción de soja en Argentina.
-Identificar las variables más influyentes sobre el rendimiento promedio del cultivo. 
-Implementar un enfoque de clasificación para categorizar el rendimiento en niveles 
“Bajo”, “Medio” y “Alto”. -Incorporar variables climáticas (temperatura media, precipitaciones, humedad relativa) 
para mejorar la precisión del modelo predictivo. 
-Evaluar y comparar el desempeño de distintos modelos mediante métricas de error y 
precisión.




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
