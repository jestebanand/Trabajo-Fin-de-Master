# Trabajo Fin de Máster – Ciencia de Datos
## Medición de la gentrificación en los barrios del entorno de Madrid Río

## Descripción

Este repositorio contiene el desarrollo completo del **Trabajo Fin de Máster (TFM)** del Máster Universitario en Ciencia de Datos de la **Universitat Oberta de Catalunya (UOC)**.

El proyecto analiza los procesos de **gentrificación urbana en la ciudad de Madrid** desde una perspectiva espacial, temporal y multidimensional, con especial atención al entorno del proyecto de regeneración urbana **Madrid Río**.

Para ello, se construye un **panel de datos a nivel barrio–año (2018–2024)** combinando indicadores **socioeconómicos, inmobiliarios y ambientales**, procedentes de fuentes públicas oficiales. El objetivo es identificar patrones de transformación urbana y evaluar su posible relación con procesos de **gentrificación verde**.

El trabajo se apoya en técnicas de **preprocesamiento de datos, análisis exploratorio, visualización y aprendizaje automático no supervisado**, priorizando la trazabilidad y la replicabilidad del análisis.

## Metodología y herramientas

- **Lenguaje principal:** R  
- **Entorno de desarrollo:** RStudio  
- **Tipos de análisis realizados:**
  - Limpieza y estandarización de datos
  - Construcción de paneles temporales barrio–año
  - Análisis exploratorio y correlacional
  - Clustering no supervisado (k-means)
  - Interpretación de resultados mediante Random Forest
- **Análisis espacial:** uso de formatos GeoJSON para análisis territorial y visualización

## Estructura del repositorio

### Archivos principales

- **Tratamiento datos.Rmd**  
  Documento principal en R Markdown que contiene:
  - Carga de los datos
  - Limpieza y estandarización de variables
  - Integración de múltiples fuentes
  - Construcción del panel barrio–año (2018–2024)

### Datos

El directorio **Datos/** contiene las fuentes utilizadas en el proyecto, organizadas por temática.

#### Datos socioeconómicos

- **Datos/Socioeconomico por barrio/**
  - panel_indicadores_distritos_barrios_20XX.xls  
    (un archivo por año para el periodo 2018–2024)

Incluye indicadores de renta, educación, desempleo y otras variables socioeconómicas a nivel de distrito y barrio.

#### Datos ambientales (infraestructura verde)

- **Datos/Verde/**
  - SuperficieZonasVerdesDistritosCalles_20XX.xlsx  
    (un archivo por año para el periodo 2018–2024)

Incluye información sobre la superficie de zonas verdes y espacios ambientales del entorno urbano.

#### Datos inmobiliarios

- **Datos/Vivienda/**
  - Años de posesion 2018-2024.csv
  - Precio medio declarado 2018-2024.csv
  - Precio medio vivienda 2018-2024 barrios seleccionados.csv
  - Superficie media 2018-2024.csv
  - Transaccion de vivienda por tipo 2018-2024.csv
  - crédito hipoteca 2018-2024 barrios seleccionados.csv

Estos archivos recogen información sobre precios de vivienda, características del parque inmobiliario, financiación hipotecaria y dinámica del mercado residencial.

#### Datos geoespaciales

- **Datos/Limites administrativos por Barrios.json**  
  Archivo GeoJSON con los límites administrativos de los barrios de Madrid.

- **Datos/Madrid_rio.geojson**  
  Delimitación geoespacial del ámbito del proyecto Madrid Río, utilizada para el análisis espacial y comparativo.

## Reproducibilidad

El análisis puede reproducirse ejecutando el archivo **Tratamiento datos.Rmd**, siempre que se mantenga la estructura de carpetas indicada y se disponga de las librerías necesarias en R.

Los datos utilizados provienen de **fuentes públicas oficiales**, principalmente del Ayuntamiento de Madrid y portales de datos abiertos.

## Autoría

- **Autor del TFM:** Jorge Esteban Andaluz  
- **Directora del TFM:** Anna Muñoz Bollas  
- **Titulación:** Máster Universitario en Ciencia de Datos  
- **Universidad:** Universitat Oberta de Catalunya (UOC)

## Nota final

Este repositorio tiene un propósito **académico y de investigación**.  
Los resultados y conclusiones deben interpretarse en el contexto del estudio y no constituyen evaluaciones normativas de políticas públicas.
