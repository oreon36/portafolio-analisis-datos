# Reducción de Dimensionalidad aplicada a perfiles estudiantiles

Proyecto de portafolio de Data Science donde se comparan **PCA** y **t-SNE** para visualizar perfiles estudiantiles y evaluar la utilidad de PCA como preparación para modelos predictivos.

## Objetivo

Reducir variables académicas y demográficas a representaciones más compactas para:

- visualizar patrones de estudiantes;
- interpretar perfiles de desempeño;
- comparar PCA y t-SNE;
- validar si PCA puede apoyar un flujo predictivo.

## Técnicas utilizadas

- EDA y análisis de correlación
- StandardScaler
- PCA 2D y PCA 3D
- Varianza explicada acumulada
- Loadings de componentes principales
- t-SNE con varios valores de perplexity
- Random Forest con validación cruzada

## Estructura sugerida del repositorio

```text
.
├── Portfolio_Reduccion_Dimensionalidad_PCA_tSNE.ipynb
├── README.md
├── requirements.txt
└── data/
    └── prueba_estudiantes.csv
```

## Resultado principal

PCA conserva gran parte de la información con pocos componentes y es más apropiado para pipelines predictivos. t-SNE muestra agrupamientos visualmente más separados y funciona mejor como herramienta exploratoria y de comunicación.

## Cómo ejecutarlo

```bash
pip install -r requirements.txt
jupyter notebook Portfolio_Reduccion_Dimensionalidad_PCA_tSNE.ipynb
```
