# Informe Final

## Predicción del rendimiento de soja en Argentina mediante K-Nearest Neighbors

### Objetivo

El objetivo de este proyecto fue desarrollar un modelo de aprendizaje automático capaz de predecir el rendimiento de soja en Argentina utilizando variables productivas y climáticas.

### Fuentes de datos

Se utilizaron dos conjuntos de datos:

- Dataset de producción de soja obtenido de Datos Abiertos Argentina.
- Dataset climático elaborado a partir de información obtenida desde NASA POWER.

### Preprocesamiento

Se realizaron las siguientes tareas:

- Verificación de valores faltantes y registros duplicados.
- Filtrado del período 1981-2023.
- Agregación de los datos productivos a nivel provincial.
- Recalculo del rendimiento provincial.
- Integración de los datos productivos y climáticos mediante un merge utilizando provincia y año.

### Variables utilizadas

Variables predictoras:

- anio
- provincia_nombre (codificada mediante variables dummy)
- superficie_sembrada_ha
- superficie_cosechada_ha
- produccion_tm
- precipitacion_total
- temperatura_media
- humedad_relativa

Variable objetivo:

- rendimiento_kgxha

### Modelos evaluados

Se implementaron y compararon los siguientes algoritmos:

| Modelo | R² |
|----------|----------|
| Regresión Lineal | 0.369066335855048|
| Árbol de Decisión | 0.2639872050800339|
| Support Vector Regressor | 0.3434155465162122 |
| KNN | 0,391 |

### Modelo seleccionado

El modelo K-Nearest Neighbors presentó el mejor desempeño.

Se aplicó StandardScaler para normalizar las variables y se evaluaron distintos valores del hiperparámetro K.

El mejor resultado se obtuvo con K = 4.

### Resultados

Métricas obtenidas:

- R² = 0,391
- MAE = 357,02 kg/ha
- RMSE = 463,89 kg/ha

El modelo logró explicar aproximadamente el 39 % de la variabilidad observada en el rendimiento de soja.

### Conclusiones

Los resultados indican que las variables productivas y climáticas incorporadas poseen capacidad explicativa sobre el rendimiento del cultivo.

Si bien el nivel de predicción alcanzado es moderado, debe considerarse que el rendimiento agrícola es un fenómeno complejo influenciado por numerosos factores que no fueron incluidos en este estudio. Entre ellos pueden mencionarse las características físicas y químicas del suelo, las variedades de soja utilizadas, las prácticas de manejo agronómico, la fertilización aplicada, la incidencia de plagas y enfermedades, así como la ocurrencia de eventos climáticos extremos.

A pesar de estas limitaciones, el trabajo permitió demostrar la aplicabilidad de técnicas de aprendizaje automático en el análisis de problemas agropecuarios y evidenció la importancia de las variables climáticas en la productividad agrícola. Además, se logró integrar conocimientos vinculados a la ciencia de datos y a las ciencias ambientales, obteniendo una herramienta capaz de generar estimaciones útiles para el estudio y la planificación de la producción de soja.

Como líneas futuras de investigación, se propone incorporar nuevas variables explicativas, realizar un ajuste más exhaustivo de hiperparámetros y evaluar algoritmos más avanzados, tales como Random Forest, Gradient Boosting o XGBoost, con el objetivo de mejorar la capacidad predictiva y profundizar el análisis de los factores que determinan el rendimiento del cultivo.
