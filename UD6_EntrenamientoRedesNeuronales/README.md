# 📘 UD6 — Entrenamiento de Redes Neuronales

## 📋 Descripción

Unidad avanzada dedicada al **entrenamiento de redes neuronales** con TensorFlow/Keras. Se cubren desde redes densas básicas (MLP) hasta **Redes Neuronales Convolucionales (CNN)**, con un enfoque práctico en la experimentación sistemática de hiperparámetros y arquitecturas.

## 🎯 Objetivos de aprendizaje

- Construir y entrenar redes neuronales con **Keras Sequential API**.
- Comprender el impacto de funciones de activación (ReLU vs Tanh).
- Experimentar con inicialización de pesos (Zero, Glorot, Normal aleatoria).
- Comparar optimizadores (SGD, RMSprop, Adamax, Adam).
- Aplicar técnicas de regularización: **Dropout**, **BatchNormalization**, **EarlyStopping**.
- Diseñar y evaluar arquitecturas **CNN** para clasificación de imágenes.
- Aplicar Data Augmentation y analizar matrices de confusión.

## 📂 Estructura

```
UD6_EntrenamientoRedesNeuronales/
│
├── 📄 UT5. Entrenamiento Redes Neuronales (Parte 1).pptx   # Teoría: fundamentos de NN
├── 📄 UT5. Entrenamiento Redes Neuronales (Parte 2).pptx   # Teoría: técnicas avanzadas
│
├── 📓 Lab 1 Entrenamiento_Redes_Neuronales.ipynb             # Lab 1: Primera red neuronal
├── 📓 Lab 2_ Aspectos_prácticos_de_las_redes_neuronales.ipynb # Lab 2: Aspectos prácticos
├── 📓 Lab_3_Experimentación_de_hiperparametros.ipynb          # Lab 3: Hiperparámetros (Simpsons)
├── 📓 Lab_3_Experimentación_de_hiperparametros_CIFAR-10.ipynb # Lab 3: Hiperparámetros (CIFAR-10)
│
└── Ejercicios/
    ├── 📄 Ejercicios Regla de la Cadena _ Backpropagation.docx  # Ejercicios teóricos
    ├── 📄 UT5_Ejercicios_CNN.docx                                # Ejercicios CNN
    ├── 📓 Lab 1 Entrenamiento_Redes_Neuronales.ipynb             # Ejercicio Lab 1
    ├── 📓 Lab 2_ Aspectos_prácticos_de_las_redes_neuronales.ipynb # Ejercicio Lab 2
    ├── 📓 Lab_3_Experimentación_de_hiperparametros.ipynb          # Ejercicio Lab 3
    ├── 📓 Lab_3_Experimentación_de_hiperparametros_CIFAR-10.ipynb # Ejercicio Lab 3 (CIFAR-10)
    └── 📓 Lab_4_Arquitecturas_CNN.ipynb                           # Lab 4: CNN Simpsons
```

## 📓 Notebooks

### Lab 1 — Primera Red Neuronal

| Aspecto | Detalle |
|---|---|
| **Celdas** | 39 (24 markdown, 15 código) |
| **Dataset** | Fashion MNIST (via `keras.datasets`) |

**Contenido:**

1. Información y exploración del dataset Fashion MNIST.
2. Preparación de datos para la red neuronal (normalización, reshape).
3. Definición de un modelo `Sequential` con capas `Dense`.
4. Entrenamiento y evaluación en datos de test.

---

### Lab 2 — Aspectos Prácticos

| Aspecto | Detalle |
|---|---|
| **Celdas** | 40 (25 markdown, 15 código) |
| **Dataset** | Fashion MNIST |

**Experimentos:**

| # | Tema | Variantes comparadas |
|---|---|---|
| 1 | Funciones de activación | ReLU, Sigmoid, Tanh |
| 2 | Inicialización de pesos | Zeros, Glorot Uniform, He Normal |
| 3 | Optimizadores | SGD, RMSprop, Adam |
| 4 | Regularización | Dropout, BatchNormalization, L2 Regularization |

Incluye train-validation-test split y análisis detallado de cada experimento.

---

### Lab 3 — Experimentación de Hiperparámetros

| Aspecto | Detalle |
|---|---|
| **Celdas** | 76 (35 markdown, 41 código) |
| **Datasets** | Simpsons (imágenes) / CIFAR-10 |

**10 experimentos sistemáticos:**

| Exp | Comparación |
|---|---|
| 1 | Visualización y preparación del dataset |
| 2 | ReLU vs Tangente Hiperbólica |
| 3 | Zero vs Glorot Uniform (inicialización) |
| 4 | Aleatoria Normal vs Glorot Uniform |
| 5 | SGD vs RMSprop |
| 6 | SGD vs Adamax |
| 7 | Aumento de batch size (512) |
| 8 | Aplicar BatchNormalization |
| 9 | Aumentar parámetros por capa |
| 10 | Aplicar Dropout 0.2 |

Se incluye una versión con **Simpsons dataset** (imágenes cargadas desde zip) y otra con **CIFAR-10**.

---

### Lab 4 — Arquitecturas CNN *(solo en Ejercicios)*

| Aspecto | Detalle |
|---|---|
| **Celdas** | 77 (42 markdown, 35 código) |
| **Dataset** | Simpsons (clasificación de personajes) |

**8 experimentos con arquitecturas CNN progresivas:**

- Capas convolucionales con distintas configuraciones de filtros.
- Pooling, Dropout, BatchNormalization.
- Data Augmentation (`RandomFlip`, `RandomRotation`, `RandomZoom`, `RandomTranslation`).
- `GlobalAveragePooling2D`, `ReduceLROnPlateau`.
- `confusion_matrix` y `classification_report` para análisis de errores.

## 📊 Material teórico

| Archivo | Contenido |
|---|---|
| `UT5. Entrenamiento Redes Neuronales (Parte 1).pptx` | Fundamentos: perceptrón, funciones de activación, backpropagation |
| `UT5. Entrenamiento Redes Neuronales (Parte 2).pptx` | Técnicas avanzadas: regularización, optimizadores, CNN |
| `Ejercicios/Ejercicios Regla de la Cadena _ Backpropagation.docx` | Ejercicios matemáticos de backpropagation |
| `Ejercicios/UT5_Ejercicios_CNN.docx` | Ejercicios teóricos sobre CNN |

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `tensorflow` / `keras` | Construcción y entrenamiento de redes neuronales |
| `keras.layers` | `Dense`, `Dropout`, `BatchNormalization`, `Flatten`, Conv2D, etc. |
| `keras.callbacks` | `EarlyStopping`, `ReduceLROnPlateau` |
| `keras.optimizers` | SGD, RMSprop, Adam, Adamax |
| `numpy` | Manipulación de arrays |
| `matplotlib` | Visualización de curvas de entrenamiento e imágenes |
| `seaborn` | Matrices de confusión |
| `scikit-learn` | `confusion_matrix`, `classification_report` |
| `cv2` (OpenCV) | Carga y procesamiento de imágenes |
| `prettytable` | Tablas resumen de experimentos |

## ▶️ Cómo ejecutar

1. Abre los notebooks en [Google Colab](https://colab.research.google.com/) (recomendado para GPU).
2. Para los Labs 3 y 4 (Simpsons), se requiere descargar los datasets de imágenes comprimidos desde `Datasets/`:
   - `simpsons_dataset.zip` (~542 MB)
   - `kaggle_simpson_testset.zip` (~11 MB)
3. Instala dependencias adicionales si es necesario:
   ```bash
   pip install opencv-python prettytable
   ```
4. Ejecuta las celdas secuencialmente. Los Labs 3-4 pueden requerir **GPU** para tiempos razonables.

> ⚠️ **Nota:** Los notebooks con dataset Simpsons montan Google Drive para acceder a los zips. Si ejecutas en local, descomprime manualmente y ajusta las rutas.
