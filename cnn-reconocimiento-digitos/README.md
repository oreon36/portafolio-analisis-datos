# 🧠 Reconocimiento de Dígitos Manuscritos con CNN

Proyecto de **Deep Learning y Computer Vision** orientado a la clasificación automática de dígitos manuscritos del **0 al 9** mediante una **Red Neuronal Convolutiva (CNN)** desarrollada con TensorFlow/Keras.

## 🎯 Objetivo

Construir, evaluar y optimizar un modelo capaz de reconocer imágenes de dígitos en escala de grises de **8 × 8 píxeles**.

El proyecto reproduce un caso aplicable a procesos como digitalización de formularios, lectura automática de códigos, automatización documental y reconocimiento de información escrita.

## 📊 Dataset

El dataset utilizado contiene:

- **1.797 imágenes**
- **64 variables de píxeles** por observación
- **1 variable objetivo:** `label`
- **10 clases:** dígitos del 0 al 9
- Imágenes de **8 × 8 píxeles**
- Intensidades originales entre **0 y 16**
- Clases aproximadamente balanceadas

Los datos se normalizan al rango `[0,1]` y posteriormente se transforman de `(n, 64)` a `(n, 8, 8, 1)` para ser procesados por la CNN.

## 🧩 Metodología

El proyecto sigue un flujo completo de Machine Learning:

1. Exploración y validación de los datos.
2. Visualización de las imágenes.
3. Normalización de píxeles.
4. Transformación a tensor 4D.
5. División en entrenamiento, validación y prueba.
6. Construcción de una CNN base.
7. Evaluación mediante métricas de clasificación.
8. Construcción de una CNN optimizada.
9. Regularización mediante `Dropout`.
10. Control del entrenamiento con `EarlyStopping`.
11. Comparación entre modelo base y optimizado.
12. Análisis visual de errores.
13. Función de inferencia para nuevas imágenes.
14. Persistencia del modelo entrenado.

## 🏗️ Arquitectura

El modelo optimizado sigue, de forma general, la arquitectura:

```text
Imagen 8×8×1
    ↓
Conv2D (32 filtros, 3×3, ReLU)
    ↓
MaxPooling2D (2×2)
    ↓
Conv2D (64 filtros, 3×3, ReLU)
    ↓
MaxPooling2D (2×2)
    ↓
Flatten
    ↓
Dense (128, ReLU)
    ↓
Dropout (0.30)
    ↓
Dense (10, Softmax)
```

La capa `Softmax` genera una distribución de probabilidades entre las diez clases.

## ⚙️ Entrenamiento y optimización

Se comparan dos enfoques:

**Modelo base:** una capa convolutiva, MaxPooling, capa densa y salida Softmax.

**Modelo optimizado:** segundo bloque convolutivo, mayor capacidad en la capa densa, `Dropout(0.30)`, `EarlyStopping` y Adam con `learning_rate=0.001`.

Esta comparación permite comprobar si una arquitectura más profunda y regularizada mejora realmente la generalización sobre datos no vistos.

## 📈 Evaluación

El notebook evalúa ambos modelos utilizando:

- Accuracy
- Loss
- Precision
- Recall
- F1-score
- Matriz de confusión
- Curvas de entrenamiento y validación
- Inspección visual de predicciones
- Análisis de clasificaciones incorrectas

> Los valores finales de las métricas se generan al ejecutar el notebook. No se incluyen resultados inventados en este README.

## 💡 Valor del proyecto

Además de entrenar una CNN, el proyecto demuestra capacidad para:

- transformar un problema visual en un pipeline reproducible;
- seleccionar una arquitectura acorde al tipo de dato;
- separar correctamente entrenamiento, validación y prueba;
- detectar y controlar sobreajuste;
- comparar modelos con criterios objetivos;
- interpretar errores y no limitar el análisis a una sola métrica;
- preparar una función de inferencia reutilizable.

## 🗂️ Estructura recomendada

```text
cnn-reconocimiento-digitos/
│
├── data/
│   └── digitos_mnist_simple.xlsx
│
├── notebooks/
│   └── reconocimiento_digitos_cnn.ipynb
│
├── README.md
└── requirements.txt
```

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio.
2. Crea un entorno virtual de Python.
3. Instala las dependencias:

```bash
pip install -r requirements.txt
```

4. Abre el notebook:

```bash
jupyter notebook
```

5. Ejecuta las celdas en orden.

También puede ejecutarse en **Google Colab**, cargando previamente el dataset.

## 🧰 Tecnologías

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow
- Keras
- Jupyter Notebook

## 🔭 Próximas mejoras

Como evolución del proyecto se podrían incorporar:

- Data Augmentation
- Batch Normalization
- búsqueda sistemática de hiperparámetros
- comparación CNN vs. red neuronal densa
- una API de inferencia
- una interfaz web para dibujar un número y clasificarlo en tiempo real

## 👤 Autor

**Héctor A. López Giménez**  
Técnico en Data Science  
Portafolio de proyectos de **Data Science · Machine Learning · Deep Learning**
