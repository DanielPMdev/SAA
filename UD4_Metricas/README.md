# 📘 UD4 — Métricas de Evaluación

## 📋 Descripción

Unidad dedicada a las **métricas de evaluación** de modelos de Machine Learning, tanto para problemas de clasificación como de regresión. Se profundiza en la interpretación correcta de cada métrica, las técnicas de validación cruzada y la optimización de hiperparámetros con GridSearchCV.

## 🎯 Objetivos de aprendizaje

- Comprender y calcular métricas de **clasificación**: Accuracy, Precision, Recall, F-score, Curva ROC.
- Interpretar la **Matriz de Confusión** y sus componentes (TP, TN, FP, FN).
- Calcular métricas de **regresión**: MAE, MSE, RMSE, R².
- Aplicar **Stochastic Gradient Descent (SGD)** como alternativa eficiente.
- Implementar **k-Fold Cross Validation** para una evaluación robusta.
- Utilizar **GridSearchCV** para optimización de hiperparámetros.

## 📂 Estructura

```
UD4_Metricas/
└── 📓 U004_Métricas.ipynb    # Notebook principal con todas las métricas
```

## 📓 Notebook

### `U004_Métricas.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 92 (51 markdown, 41 código) |
| **Datasets** | Affairs Dataset, Iris, datos sintéticos |

**Contenido detallado:**

#### 🏷️ Clasificación

| Métrica | Descripción |
|---|---|
| **Accuracy** | Proporción de predicciones correctas |
| **Precision** | De los predichos positivos, cuántos son realmente positivos |
| **Recall (Sensibilidad)** | De los positivos reales, cuántos identificó el modelo |
| **F-score** | Media armónica de Precision y Recall |
| **Matriz de Confusión** | Tabla de TP, TN, FP, FN con `ConfusionMatrixDisplay` |
| **Curva ROC** | Relación entre TPR y FPR a distintos umbrales |
| **Evaluación multiclase** | Extensión de métricas a más de dos clases |

#### 📈 Regresión

| Métrica | Fórmula conceptual |
|---|---|
| **MAE** | Media de los errores absolutos |
| **MSE** | Media de los errores al cuadrado |
| **RMSE** | Raíz cuadrada del MSE |
| **R²** | Coeficiente de determinación (bondad de ajuste) |

#### ⚙️ Técnicas de validación y optimización

| Técnica | Descripción |
|---|---|
| **SGD** | Descenso de gradiente estocástico como clasificador/regresor |
| **k-Fold Cross Validation** | Partición en k subconjuntos para evaluación robusta |
| **GridSearchCV** | Búsqueda exhaustiva de la mejor combinación de hiperparámetros |

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación de datos |
| `matplotlib` / `seaborn` | Visualización |
| `scikit-learn` | Métricas, validación cruzada, GridSearchCV, modelos |
| `statsmodels` | Modelos estadísticos |
| `scipy` | Distribuciones estadísticas |
| `requests` | Descarga de datasets en línea |

## ▶️ Cómo ejecutar

1. Abre el notebook en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Ejecuta las celdas secuencialmente.
3. No se requieren datasets externos; los datos se cargan desde librerías (`load_iris`, URLs, etc.).
