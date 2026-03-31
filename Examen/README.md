# 📝 Examen

## 📋 Descripción

Directorio con el **examen propio** del curso (2025-2026) y una recopilación de **exámenes de años anteriores** resueltos, que sirven como material de estudio y preparación.

## 📂 Estructura

```
Examen/
│
├── 📄 Posibles Preguntas Examen.docx                # Banco de preguntas de repaso
│
├── Examen_12-01-2026/                                # Examen propio (curso 2025-2026)
│   └── 📓 20260119_European_Soccer_DanielPorrasMorales.ipynb
│
└── Examenes Años Anteriores/
    ├── Examen 2021/                                  # Horse Colic
    ├── Examen 2022/                                  # FIFA 20
    ├── Examen 2022 - Recu/                           # Game of Thrones
    ├── Examen 2023/                                  # Global Shark Attacks
    ├── Examen 2023 - V2/                             # Airbnb Berlín
    ├── Examen 2024/                                  # Salaries
    └── Examen 2025/                                  # Reservas de Hotel
```

## 🎓 Examen propio — Curso 2025-2026

### `20260119_European_Soccer_DanielPorrasMorales.ipynb`

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

## 📚 Exámenes de años anteriores

| Año | Convocatoria | Dataset | Notebook | Técnicas principales |
|---|---|---|---|---|
| **2021** | Ordinaria | Horse Colic | `Preparación_de_datos_Examen.ipynb` | Limpieza, imputación, PCA, Feature Importance |
| **2022** | Ordinaria | FIFA 20 | `FIFA_20.ipynb` | Regresión Lineal, Árboles de Decisión, PCA, K-Means |
| **2022** | Recuperación | Game of Thrones | `Examen_Game_of_Thrones.ipynb` | SVC, Decision Tree, Random Forest, Clustering, CNN (Keras) |
| **2023** | Ordinaria | Global Shark Attacks | `Examen20221212_Global_Shark_Attacks.ipynb` | Limpieza exhaustiva, PCA, Feature Importance |
| **2023** | V2 | Airbnb Berlín | `Examen_20230123_Precios_de_Airbnb_en_Berlin.ipynb` | Regresión Lineal, SVR, SVC, Decision Tree, PCA |
| **2024** | Ordinaria | Salaries | `Salaries.ipynb` | SVM (SVR), Árboles de Decisión, OneHotEncoder |
| **2025** | Ordinaria | Hotel Bookings | `20250113_Reservas_de_hotel.ipynb` | PCA, Logistic Regression, SVM, Decision Tree, Feature Importance |

## 🔑 Patrón común de los exámenes

Todos los exámenes siguen una estructura similar:

1. **📊 Exploración de datos** — Dimensiones, tipos, primeras filas.
2. **🧹 Preparación de datos** — Nulos, categóricas, outliers, normalización.
3. **📉 Reducción de dimensionalidad** — Feature importance, correlación, PCA.
4. **🤖 Modelado supervisado** — Regresión y/o clasificación según la variable objetivo.
5. **❓ Preguntas teóricas** — Justificación de decisiones tomadas.

## 🛠️ Tecnologías recurrentes

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación |
| `matplotlib` / `seaborn` | Visualización |
| `scikit-learn` | PCA, SVM/SVR, Decision Tree, Logistic Regression, métricas |
| `missingno` | Visualización de nulos (exámenes 2021, 2023) |
| `statsmodels` | OLS, análisis estadístico |
| `sqlite3` | Carga de bases de datos SQLite (examen 2026) |
| `graphviz` | Visualización de árboles de decisión |

## ▶️ Cómo ejecutar

1. Abre el notebook deseado en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Asegúrate de que los datasets correspondientes estén accesibles (ver carpeta `Datasets/` o archivos locales en cada subcarpeta).
3. Ejecuta las celdas secuencialmente.

> 💡 **Consejo:** Los exámenes de años anteriores son excelente material de estudio. Cada uno cubre el pipeline completo de ML, desde la exploración hasta el modelado.
