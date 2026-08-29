# PCA aplicado a Ames Housing

## Objetivo

Reducir la dimensionalidad de variables numéricas del dataset Ames Housing y analizar cuánta información conserva cada componente principal.

## Metodología

1. Carga y exploración de los datos.
2. Selección de variables numéricas.
3. Imputación de valores faltantes con la media.
4. Estandarización con `StandardScaler`.
5. PCA con 16 componentes.
6. Análisis de varianza explicada y cargas factoriales.
7. Visualización de los dos primeros componentes.

## Estructura

- `notebooks/analisis_componentes_PCA.ipynb`: análisis completo.
- `data/train.csv`: dataset requerido, no incluido todavía.

## Ejecución

Coloca el archivo de Ames Housing con el nombre `train.csv` dentro de `data/` y ejecuta el notebook desde Jupyter o Google Colab.

## Competencias demostradas

Preprocesamiento, imputación, escalado, reducción de dimensionalidad, interpretación de varianza y visualización.
