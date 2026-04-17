# 📝 Examen

## 📋 Descripción

Directorio con los **exámenes propios** del curso (2025-2026) y una recopilación de **exámenes de años anteriores** resueltos, que sirven como material de estudio y preparación. El contenido se organiza en dos bloques principales correspondientes a los dos parciales de la asignatura.

## 📂 Estructura

```
Examen/
│
├── Examen Enero/                                      # Primer parcial (ML clásico)
│   ├── 📄 Posibles Preguntas Examen.docx              # Banco de preguntas de repaso
│   │
│   ├── Examen_12-01-2026/                             # Examen propio (curso 2025-2026)
│   │   └── 📓 20260119_European_Soccer_DanielPorrasMorales.ipynb
│   │
│   └── Examenes Años Anteriores/
│       ├── Examen 2021/                               # Horse Colic
│       ├── Examen 2022/                               # FIFA 20
│       ├── Examen 2022 - Recu/                        # Game of Thrones
│       ├── Examen 2023/                               # Global Shark Attacks
│       ├── Examen 2023 - V2/                          # Airbnb Berlín
│       ├── Examen 2024/                               # Salaries
│       └── Examen 2025/                               # Reservas de Hotel
│
└── Examen Abril/                                      # Segundo parcial (Deep Learning / CNN)
    ├── 📓 Examen20260414_SAA_Daniel_Porras_Morales.ipynb  # Examen propio (14/04/2026)
    ├── 📄 Apuntes.md                                  # Apuntes completos de repaso
    ├── 📄 ApuntesCNN_Dimensiones.md                   # Ejercicios resueltos CNN
    ├── 🖼️ image.png                                   # Diagrama de backpropagation
    │
    └── JupyterNotebooks/                              # Exámenes y prácticas de lab. anteriores
        ├── 📓 Examen20230508_SAA_Daniel_Porras_Morales.ipynb
        ├── 📓 Examen20240429_SAA_Daniel_Porras_Morales.ipynb
        ├── 📓 Examen20250410_SAA_Daniel_Porras_Morales.ipynb
        ├── 📓 Lab_3_Experimentación_de_hiperparametros.ipynb
        ├── 📓 Lab_3_Experimentación_de_hiperparametros_CIFAR-10.ipynb
        └── 📓 Lab_4_Arquitecturas_CNN.ipynb
```

---

## 🎓 Exámenes propios — Curso 2025-2026

### Primer Parcial — Examen Enero (ML Clásico)

#### `20260119_European_Soccer_DanielPorrasMorales.ipynb`

| Aspecto | Detalle |
|---|---|
| **Fecha** | 12 de enero de 2026 |
| **Dataset** | European Soccer Database (`database.sqlite`) |
| **Celdas** | 77 (44 markdown, 33 código) |
| **Tipo de problema** | Regresión (`overall_rating` como variable objetivo) |

**Contenido del examen:**

| Fase | Preguntas | Descripción |
|---|---|---|
| **Exploración** | P1–P3 | Filas/columnas, nulos, valores categóricos |
| **Preparación** | P4–P9 | Clasificación vs regresión, eliminación de variables, imputación de nulos (media/moda), dummies, outliers |
| **Reducción dimensionalidad** | P10 | Feature importance, correlación Pearson, PCA |
| **Aprendizaje supervisado** | — | Regresión Lineal, SVR, Árboles de Decisión, GridSearchCV |

**Librerías:** pandas, numpy, matplotlib, seaborn, scikit-learn (PCA, SVR, DecisionTreeRegressor, LinearRegression, GridSearchCV), sqlite3.

---

### Segundo Parcial — Examen Abril (Deep Learning / CNN)

#### `Examen20260414_SAA_Daniel_Porras_Morales.ipynb`

| Aspecto | Detalle |
|---|---|
| **Fecha** | 14 de abril de 2026 |
| **Dataset** | MNIST (dígitos escritos a mano, 0-9) |
| **Tipo de problema** | Clasificación multiclase (10 clases) |
| **Duración** | 2 horas |
| **Restricciones** | ❌ Prohibido uso de IA generativa |

**Contenido del examen:**

| Fase | Pregunta | Descripción | Puntuación |
|---|---|---|---|
| **Preparación** | P1 | Normalización, distribución de clases, barajado | 0,25 pts |
| **Exp. 1 — FC** | P2 | Red Fully Connected (>90 % val_accuracy, Adam) | 1,00 pts |
| **Visualización** | P3 | Tabla de experimentación y gráficas comparativas | 0,25 pts |
| **Exp. 2 — CNN** | P4 | Red CNN (>96 % val_accuracy, SGD) | 1,50 pts |

**Resultados:**

| Experimento | Descripción | Val_Accuracy |
|---|---|---|
| Exp. 1 | Fully Connected, Adam | 97,72 % |
| Exp. 2 | CNN + BatchNormalization + SGD + Dropout 0.3 | 98,93 % |

**Librerías:** TensorFlow, Keras, NumPy, Matplotlib, PrettyTable.

---

## 📚 Exámenes de años anteriores — Primer Parcial (ML Clásico)

| Año | Convocatoria | Dataset | Notebook | Técnicas principales |
|---|---|---|---|---|
| **2021** | Ordinaria | Horse Colic | `Preparación_de_datos_Examen.ipynb` | Limpieza, imputación, PCA, Feature Importance |
| **2022** | Ordinaria | FIFA 20 | `FIFA_20.ipynb` | Regresión Lineal, Árboles de Decisión, PCA, K-Means |
| **2022** | Recuperación | Game of Thrones | `Examen_Game_of_Thrones.ipynb` | SVC, Decision Tree, Random Forest, Clustering, CNN (Keras) |
| **2023** | Ordinaria | Global Shark Attacks | `Examen20221212_Global_Shark_Attacks.ipynb` | Limpieza exhaustiva, PCA, Feature Importance |
| **2023** | V2 | Airbnb Berlín | `Examen_20230123_Precios_de_Airbnb_en_Berlin.ipynb` | Regresión Lineal, SVR, SVC, Decision Tree, PCA |
| **2024** | Ordinaria | Salaries | `Salaries.ipynb` | SVM (SVR), Árboles de Decisión, OneHotEncoder |
| **2025** | Ordinaria | Hotel Bookings | `20250113_Reservas_de_hotel.ipynb` | PCA, Logistic Regression, SVM, Decision Tree, Feature Importance |

## 📚 Exámenes de laboratorio anteriores — Segundo Parcial (Deep Learning)

| Año | Fecha | Dataset | Notebook | Técnicas principales |
|---|---|---|---|---|
| **2023** | 08/05/2023 | MNIST | `Examen20230508_SAA_Daniel_Porras_Morales.ipynb` | CNN, Dropout, `sparse_categorical_crossentropy` |
| **2024** | 29/04/2024 | MNIST | `Examen20240429_SAA_Daniel_Porras_Morales.ipynb` | CNN, Data Augmentation, SGD vs Adam, EarlyStopping |
| **2025** | 10/04/2025 | Fashion-MNIST | `Examen20250410_SAA_Daniel_Porras_Morales.ipynb` | CNN, Init a cero, Dropout, SGD, BatchNorm, Augmentation |

---

## 🔑 Patrón común de los exámenes

### Primer Parcial (ML Clásico)

1. **📊 Exploración de datos** — Dimensiones, tipos, primeras filas.
2. **🧹 Preparación de datos** — Nulos, categóricas, outliers, normalización.
3. **📉 Reducción de dimensionalidad** — Feature importance, correlación, PCA.
4. **🤖 Modelado supervisado** — Regresión y/o clasificación según la variable objetivo.
5. **❓ Preguntas teóricas** — Justificación de decisiones tomadas.

### Segundo Parcial (Deep Learning / CNN)

1. **📐 Preparación de datos** — Carga, reshape, normalización (0-1), análisis de sesgo.
2. **🏗️ Diseño de arquitectura** — CNN (Conv2D, MaxPooling2D, Dense, Dropout, BatchNorm).
3. **⚙️ Compilación** — Optimizador (Adam/SGD), loss, métricas.
4. **🏋️ Entrenamiento** — EarlyStopping, validation_split.
5. **📊 Experimentación** — Tabla comparativa y gráficas de accuracy/loss.
6. **📝 Conclusiones** — Justificación y análisis de resultados.

## 🛠️ Tecnologías recurrentes

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación de datos |
| `matplotlib` / `seaborn` | Visualización |
| `scikit-learn` | PCA, SVM/SVR, Decision Tree, Logistic Regression, métricas |
| `tensorflow` / `keras` | Redes neuronales (CNN, Dense, Dropout, BatchNorm, etc.) |
| `prettytable` | Tablas de experimentación |
| `missingno` | Visualización de nulos (exámenes 2021, 2023) |
| `statsmodels` | OLS, análisis estadístico |
| `sqlite3` | Carga de bases de datos SQLite (examen 2026) |
| `graphviz` | Visualización de árboles de decisión |

## ▶️ Cómo ejecutar

1. Abre el notebook deseado en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Asegúrate de que los datasets correspondientes estén accesibles (ver carpeta `Datasets/` o archivos locales en cada subcarpeta).
3. Ejecuta las celdas secuencialmente.

> 💡 **Consejo:** Los exámenes de años anteriores son excelente material de estudio. Cada uno de primer parcial cubre el pipeline completo de ML clásico, y cada uno de segundo parcial cubre el pipeline de entrenamiento de redes neuronales.
