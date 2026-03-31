# 🤖 Sistemas de Aprendizaje Automático (SAA)

> **Curso de Especialización en Inteligencia Artificial y Big Data**

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Colab](https://img.shields.io/badge/Google-Colab-F9AB00?style=flat-square&logo=google-colab&logoColor=white)](https://colab.research.google.com/)

---

## 📋 Descripción

Repositorio con todo el material práctico y teórico del módulo **Sistemas de Aprendizaje Automático**, parte del Curso de Especialización en Inteligencia Artificial y Big Data (FP). 

El contenido abarca el **pipeline completo de Machine Learning**: desde la exploración y preparación de datos, pasando por algoritmos supervisados y no supervisados, métricas de evaluación, hasta el entrenamiento de redes neuronales y CNNs con TensorFlow/Keras.

## 🗂️ Estructura del repositorio

```
SAA/
│
├── UD1_Introducion/                                    # Introducción y EDA básico
├── UD2_PreparacionDatos(ReduccionDimensionalidad)/      # Preparación de datos y reducción de dimensionalidad
├── UD3_AprendizajeAutomaticoSupervisado/                # Algoritmos supervisados
├── UD4_Metricas/                                       # Métricas de evaluación
├── UD5_AprendizajeAutomaticoNoSupervisado/              # Algoritmos no supervisados (Clustering)
├── UD6_EntrenamientoRedesNeuronales/                    # Redes Neuronales y CNNs
├── Datasets/                                           # Datasets centralizados
├── Examen/                                             # Exámenes (propio + años anteriores)
├── .gitignore                                          # Archivos excluidos del repositorio
└── README.md                                           # Este archivo
```

## 📘 Unidades Didácticas

### [UD1 — Introducción](./UD1_Introducion/)
Primer contacto con el entorno de trabajo (Google Colab) y las librerías de Python para ciencia de datos. Análisis exploratorio del dataset Titanic.

**Conceptos clave:** Pandas, NumPy, Matplotlib, Seaborn, estadísticas descriptivas, histogramas, boxplots.

---

### [UD2 — Preparación de Datos y Reducción de Dimensionalidad](./UD2_PreparacionDatos(ReduccionDimensionalidad)/)
La unidad más extensa. Cubre el pipeline completo de preprocesamiento y técnicas de selección/extracción de características.

**Conceptos clave:** Limpieza de datos, imputación de nulos, encoding categórico, normalización, PCA, LDA, métodos de filtro (varianza, correlación, ANOVA, chi-square), métodos wrapper (RFE, backward elimination), métodos embedded (Ridge, Lasso).

**Prácticas:** Adult, Horse Colic, Red Wine, Titanic, Boston, Zoo, BigQuery, Calidad del Aire CYL.

---

### [UD3 — Aprendizaje Automático Supervisado](./UD3_AprendizajeAutomaticoSupervisado/)
Algoritmos fundamentales de aprendizaje supervisado para clasificación y regresión.

**Conceptos clave:** Regresión Lineal (simple y múltiple), Regresión Logística, SVM/SVR, Árboles de Decisión, SGD.

**Prácticas:** Iris, Boston Housing, Credit Card Fraud Detection, Heart Disease.

---

### [UD4 — Métricas de Evaluación](./UD4_Metricas/)
Métricas para evaluar correctamente los modelos, técnicas de validación cruzada y optimización de hiperparámetros.

**Conceptos clave:** Accuracy, Precision, Recall, F1-Score, Matriz de Confusión, Curva ROC/AUC, MAE, MSE, RMSE, R², k-Fold Cross Validation, GridSearchCV.

---

### [UD5 — Aprendizaje No Supervisado](./UD5_AprendizajeAutomaticoNoSupervisado/)
Técnicas de clustering para segmentación y agrupamiento de datos sin etiquetas.

**Conceptos clave:** K-Means, método del codo, Silhouette Score, Clustering Jerárquico (Aglomerativo), PCA para visualización de clusters.

**Prácticas:** Samsung, Cars, Big Five Personality Test, Credit Card, Ship Performance.

---

### [UD6 — Entrenamiento de Redes Neuronales](./UD6_EntrenamientoRedesNeuronales/)
Diseño, entrenamiento y optimización de redes neuronales densas y convolucionales con Keras.

**Conceptos clave:** Keras Sequential API, funciones de activación (ReLU, Tanh), inicialización de pesos (Glorot), optimizadores (SGD, Adam, RMSprop), regularización (Dropout, BatchNorm, EarlyStopping), CNN, Data Augmentation.

**Prácticas:** Fashion MNIST, Simpsons Characters, CIFAR-10.

---

### [Datasets](./Datasets/)
Colección centralizada de todos los datasets utilizados en las prácticas y exámenes.

---

### [Examen](./Examen/)
Examen propio del curso (European Soccer Database, enero 2026) y recopilación de exámenes resueltos de convocatorias anteriores (2021–2025).

## 🛠️ Stack Tecnológico

| Categoría | Tecnologías |
|---|---|
| **Lenguaje** | Python 3.8+ |
| **Entorno** | Google Colab, Jupyter Notebook |
| **Datos** | Pandas, NumPy |
| **Visualización** | Matplotlib, Seaborn |
| **ML Clásico** | scikit-learn |
| **Deep Learning** | TensorFlow, Keras |
| **Estadística** | statsmodels, scipy, pingouin |
| **Otros** | missingno, graphviz, yellowbrick, OpenCV |

## 🚀 Inicio rápido

### Opción 1 — Google Colab (recomendado)
1. Navega hasta el notebook que desees.
2. Haz clic en el botón **"Open in Colab"** o copia la URL del archivo `.ipynb` en [Google Colab](https://colab.research.google.com/).
3. Sube o monta los datasets necesarios.

### Opción 2 — Ejecución local
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/SAA.git
   cd SAA
   ```
2. Crea un entorno virtual e instala las dependencias:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   pip install -r requirements.txt
   ```
3. Lanza Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

### Dependencias principales
```
pandas
numpy
matplotlib
seaborn
scikit-learn
tensorflow
keras
statsmodels
missingno
graphviz
yellowbrick
pingouin
opencv-python
prettytable
```

## 📊 Resumen de contenidos

| Unidad | Notebooks | Temas principales |
|---|---|---|
| UD1 | 1 | EDA, estadísticas descriptivas, visualización |
| UD2 | 13 | Limpieza, nulos, encoding, PCA, LDA, RFE, Ridge/Lasso |
| UD3 | 3 | Regresión, Logística, SVM, Árboles, SGD |
| UD4 | 1 | Accuracy, Precision, Recall, ROC, Cross-Validation |
| UD5 | 6 | K-Means, Clustering Jerárquico, Elbow, Silhouette |
| UD6 | 8 | MLP, CNN, hiperparámetros, regularización, Data Augmentation |
| Examen | 8 | Pipelines completos de ML sobre datasets reales |
| **Total** | **40** | — |

## 📄 Licencia

Este repositorio contiene material educativo desarrollado durante el Curso de Especialización en IA y Big Data. El uso de los datasets está sujeto a sus respectivas licencias originales (ver [Datasets/README.md](./Datasets/README.md)).

## 👤 Autor

**Daniel Porras Morales**  
Curso de Especialización en Inteligencia Artificial y Big Data  
Curso 2025-2026
