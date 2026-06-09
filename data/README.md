# **Dataset de Producción de Soja en Argentina**

## **Descripción del dataset y orígen**

El dataset principal utilizado corresponde a la serie histórica de producción de soja en Argentina para el período 1941-2023. Cuenta con 12316 registros. Cada registro representa información productiva a nivel departamental e incluye variables relacionadas con superficie sembrada, superficie cosechada, producción y rendimiento.
El mismo fue obtenido de la página web https://www.datos.gob.ar/dataset/agroindustria-soja---siembra-cosecha-produccion-rendimiento y contiene aproximadamente más de 80 años de registros a nivel provincial y departamental. 
Las principales variables del conjunto de datos son:

*cultivo_nombre*: nombre del cultivo, que en este caso corresponde a la soja

*anio*: año del registro

*campania*: campaña agrícola correspondiente

*provincia_nombre y provincia_id*: identifican la provincia donde se cultiva

*departamento_nombre y departamento_id*: indican la subdivisión administrativa dentro de la provincia

*superficie_sembrada_ha*: superficie sembrada, expresada en hectáreas

*superficie_cosechada_ha*: superficie cosechada, expresada en hectáreas

*produccion_tm*: producción total, medida en toneladas métricas

*rendimiento_kgxha*: rendimiento promedio, expresado en kilogramos por hectárea. 

Como etapa inicial del proyecto se realizó el proceso de preprocesamiento y limpieza del dataset soja-serie-1941-2023.csv, que contiene información histórica sobre la producción de soja en Argentina. En primer lugar, se cargaron los datos utilizando la biblioteca Pandas y se efectuó una exploración inicial para conocer la estructura del conjunto de datos, sus variables y características generales. 

Posteriormente, se verificó la existencia de valores faltantes, registros duplicados y posibles inconsistencias en los tipos de datos. También se revisó la presencia de valores negativos en las variables productivas, ya que estos no tendrían sentido desde el punto de vista agronómico. 

Debido a que los datos climáticos que serán incorporados al análisis se encuentran disponibles únicamente a partir de 1981, se filtraron los registros para conservar exclusivamente las observaciones comprendidas entre 1981 y 2023. Y dado que el dataset original se encuentra a nivel departamental y los datos climáticos fueron recopilados a nivel provincial, se realizó una agregación de la información agrupando los registros por provincia y año. Para ello se sumaron las superficies sembradas, las superficies cosechadas y la producción total de todos los departamentos pertenecientes a cada provincia. 

Posteriormente, se recalculó el rendimiento provincial en kilogramos por hectárea utilizando la producción total y la superficie cosechada total de cada provincia. Finalmente, se analizaron posibles valores atípicos mediante diagramas de caja para las variables de rendimiento y producción. 

Por último, se hizo una verificacón de las provincias de las cuales hay registros en este dataset. Esto sirvió para realizar el segundo dataset ("registro_climatico_por provincia_1981_2023")

Como resultado de este proceso se obtuvo un dataset de 631 regisrtros consolidado a nivel provincial y anual, preparado para su integración con las variables climáticas y su posterior utilización en modelos de regresión orientados a predecir el rendimiento de soja en Argentina.

El segundo dataset es de mi autoría y se denomina **"registro_climatico_por provincia_1981_2023"**. El mismo lo realicé recopilando datos meteorológicos de las distintas provincias, obtenidos de la página "NASA Power".
Contiene las siguientes variables:

*provincia*: se refiere a la provincia a la cual corresponden los datos.

*anio*: año en el que fueron recolectados esos datos.

*precipitacion_total*: precipitación total en el año por provincia.

*temperatura_media*: temperatura media medida por año y por provincia.

*humedad_relativa*: humedad relativa medida por año y por provincia.

Ya tengo todos los datos pero aún no terminé de completar este dataset. En estos días subiré el archivo actualizado y completo y lo voy a unir con el dataset original para así trabajar con uno solo.
