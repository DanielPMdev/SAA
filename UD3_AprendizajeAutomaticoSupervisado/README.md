# 📘 UD3 — Aprendizaje Automático Supervisado

## 📋 Descripción

Unidad dedicada a los **algoritmos de aprendizaje supervisado**, tanto de clasificación como de regresión. Se cubren los principales modelos del ecosistema scikit-learn con ejemplos prácticos, desde modelos lineales hasta árboles de decisión y SVM, aplicados a datasets reales.

## 🎯 Objetivos de aprendizaje

- Comprender la diferencia entre regresión y clasificación.
- Implementar y evaluar modelos de **Regresión Lineal** (simple y múltiple).
- Aplicar **Regresión Logística** para problemas de clasificación binaria.
- Entrenar y visualizar **Support Vector Machines (SVM)** para clasificación y regresión (SVR).
- Construir e interpretar **Árboles de Decisión** (clasificación y regresión).
- Aplicar **Stochastic Gradient Descent (SGD)**.
- Evaluar modelos con métricas: accuracy, precision, recall, F1, curva ROC, R², MSE, MAE.

## 📂 Estructura

```
UD3_AprendizajeAutomaticoSupervisado/
│
├── 📄 U003. Aprendizaje supervisado.pdf                      # Apuntes teóricos
├── 📓 U003_P1_Aprendizaje_supervisado_I.ipynb                # Práctica principal (todos los algoritmos)
├── 📓 U003_P4_Credit_Card.ipynb                               # Detección de fraude con tarjeta de crédito
│
└── Ejercicios/
    └── AprendizajeSupervisado_II/
        ├── 📓 U003_P2_Aprendizaje_supervisado_II.ipynb       # Ejercicios: Heart Disease
        └── heart.csv                                          # Dataset cardiopatías
```

## 📓 Notebooks

### `U003_P1_Aprendizaje_supervisado_I.ipynb` — Práctica principal

| Aspecto | Detalle |
|---|---|
| **Celdas** | 166 (82 markdown, 84 código) |
| **Datasets** | Iris, Boston Housing, datos sintéticos |

**Algoritmos cubiertos:**

| Algoritmo | Tipo | Descripción |
|---|---|---|
| **Regresión Lineal** | Regresión | Simple y múltiple, coeficiente de determinación R², función de coste |
| **Regresión Logística** | Clasificación | Clasificación binaria con frontera de decisión |
| **SVM (SVC)** | Clasificación | Kernels lineales, visualización de hiperplano separador |
| **SVR** | Regresión | Support Vector Regression con distintos kernels |
| **Árboles de Decisión** | Ambos | Clasificación con Iris, regresión, visualización con Graphviz |
| **SGD Classifier** | Clasificación | Descenso de gradiente estocástico |

**Métricas de evaluación:** Accuracy, Precision, Recall, F1-Score, Curva ROC, AUC, MAE, MSE, R².

---

### `U003_P4_Credit_Card.ipynb` — Detección de fraude

| Aspecto | Detalle |
|---|---|
| **Celdas** | 47 (17 markdown, 30 código) |
| **Dataset** | `creditcard.csv` — transacciones de tarjeta de crédito |

**Pipeline completo:**

1. **Comprensión de datos** — Exploración del dataset desbalanceado.
2. **Limpieza** — Valores nulos, outliers.
3. **Reducción de dimensionalidad** — Varianza, correlación, PCA.
4. **Desbalanceo de clases** — Análisis del impacto en el modelo.
5. **Entrenamiento de modelos:**
   - Logistic Regression
   - SVC (Support Vector Classification)
   - Decision Tree

---

### `U003_P2_Aprendizaje_supervisado_II.ipynb` — Ejercicio Heart Disease

| Aspecto | Detalle |
|---|---|
| **Celdas** | 55 (14 markdown, 41 código) |
| **Dataset** | `heart.csv` — predicción de cardiopatías |
| **Algoritmos** | Logistic Regression, SVC, Decision Tree |
| **Métricas** | Accuracy, Recall, Confusion Matrix |

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación de datos |
| `matplotlib` / `seaborn` | Visualización |
| `scikit-learn` | Modelos supervisados, métricas, train/test split |
| `graphviz` | Visualización de árboles de decisión |
| `statsmodels` | Regresión OLS, test estadísticos |

## ▶️ Cómo ejecutar

1. Abre los notebooks en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Para `U003_P4_Credit_Card.ipynb`, descarga `creditcard.csv` desde la carpeta `Datasets/` o ajusta la ruta.
3. Instala `graphviz` si no está disponible:
   ```bash
   pip install graphviz
   ```
4. Ejecuta las celdas secuencialmente.

> ⚠️ **Nota:** El dataset `creditcard.csv` (~150 MB) puede requerir tiempo de carga. Algunos notebooks referencian rutas de Google Drive.
