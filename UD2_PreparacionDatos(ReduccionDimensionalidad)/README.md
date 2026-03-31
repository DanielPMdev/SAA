# 📘 UD2 — Preparación de Datos y Reducción de Dimensionalidad

## 📋 Descripción

Unidad central del módulo dedicada a las técnicas de **preprocesamiento de datos** y **reducción de dimensionalidad**. Se aborda todo el pipeline de preparación: limpieza, tratamiento de valores nulos, codificación de variables categóricas, normalización, detección de outliers, y métodos de selección y extracción de características (PCA, LDA, métodos de filtrado y wrapper).

## 🎯 Objetivos de aprendizaje

- Comprender y ejecutar un pipeline completo de preparación de datos.
- Tratar valores nulos, outliers y variables categóricas.
- Aplicar técnicas de normalización y estandarización.
- Reducir la dimensionalidad con métodos de filtro (varianza, correlación, ANOVA, chi-square).
- Implementar métodos wrapper (backward elimination, RFE).
- Aplicar métodos embedded (Ridge, Lasso).
- Dominar PCA (Análisis de Componentes Principales) y LDA.

## 📂 Estructura

```
UD2_PreparacionDatos(ReduccionDimensionalidad)/
│
├── 📄 U002.1. Preparación de datos.pdf              # Apuntes teóricos
├── 📄 U002.1. Preparación de datos.pptx              # Presentación: fundamentos
├── 📄 U002.2. Preparación de datos. Selección.pptx   # Presentación: selección de características
├── 📄 U002.3. Preparación de datos. Transformación.pptx  # Presentación: transformaciones
├── 🎬 SAA_Test_UD2.mkv                               # Vídeo del test de la unidad
│
├── 📓 U002_P6_Reducción_dimensionalidad_Boston.ipynb  # Métodos wrapper y embedded (Boston)
├── 📓 U002_P7_Reducción_dimensionalidad_Métodos_de_filtro.ipynb  # Métodos de filtrado
├── 📓 U002_P11__Preparación_de_datos_Horse_Colic.ipynb  # Preparación avanzada (Horse Colic)
│
├── Practica_Adults/          # Práctica: Adult Census Income
├── Practica_Cancer_PCA/      # Práctica: PCA sobre Breast Cancer
├── Practica_Horse/           # Práctica: Horse Colic
├── Practica_PCA/             # Práctica: PCA genérico
├── Practica_RedWine/         # Práctica: Red Wine Quality
├── Practica_Titanic/         # Práctica: Titanic (preparación de datos)
├── Practica_Wine_PCA/        # Práctica: PCA sobre Wine
│
├── Tarea2_BigQuery/          # Tarea: Limpieza con BigQuery
├── Tarea2_CalidadAireCYL/    # Tarea: Calidad del Aire en CYL
└── Tarea2_Zoo/               # Tarea: Reducción dimensionalidad Zoo
```

## 📓 Notebooks — Prácticas guiadas

### Preparación de datos

| Notebook | Dataset | Tema principal | Técnicas clave |
|---|---|---|---|
| `Practica_Adults/U002_P1_Preparación_de_datos_Adult.ipynb` | Adult Census | Preprocesamiento completo | Codificación categórica, tratamiento de nulos (`?`), binning |
| `Practica_Horse/U002_P4_Horse_Colic.ipynb` | Horse Colic | Limpieza de datos clínicos | `missingno`, imputación, `RandomForestRegressor` para nulos |
| `Practica_RedWine/U002_P2_Red_Wine.ipynb` | Red Wine Quality | Comprensión y limpieza | Discretización, normalización, eliminación de outliers |
| `Practica_RedWine/U002_P2_Red_Wine_Solution.ipynb` | Red Wine Quality | Solución de la práctica | Versión resuelta con todos los pasos completados |
| `Practica_Titanic/U002_P3_Titanic.ipynb` | Titanic | Procesado completo | Datos categóricos y numéricos, `RandomForestRegressor` |
| `U002_P11__Preparación_de_datos_Horse_Colic.ipynb` | Horse Colic | Preparación avanzada | Limpieza exhaustiva campo a campo, PCA, Feature Importance |

### Reducción de dimensionalidad

| Notebook | Dataset | Tema principal | Técnicas clave |
|---|---|---|---|
| `U002_P6_Reducción_dimensionalidad_Boston.ipynb` | Boston Housing | Métodos wrapper y embedded | Correlación, Backward Elimination, RFE, Ridge, Lasso |
| `U002_P7_Reducción_dimensionalidad_Métodos_de_filtro.ipynb` | Varios (Iris, etc.) | Métodos de filtrado | Varianza, Pearson, LDA, ANOVA, Chi-Square, ColumnTransformer |
| `Practica_PCA/U002_P8.ipynb` | PCA.csv genérico | PCA básico | `StandardScaler`, PCA, visualización de componentes |
| `Practica_Cancer_PCA/U002_P9_PCA_Breast_Cancer.ipynb` | Breast Cancer | PCA sobre datos médicos | `MinMaxScaler`, `StandardScaler`, PCA |
| `Practica_Wine_PCA/U002_P10_PCA_Wine.ipynb` | Wine | PCA sobre vinos | `MinMaxScaler`, `StandardScaler`, PCA |

## 📓 Notebooks — Tareas evaluables

| Notebook | Dataset | Tema |
|---|---|---|
| `Tarea2_BigQuery/U002_T1_BigQuery.ipynb` | BigQuery Public Dataset | Limpieza y preparación de datos de telecomunicaciones |
| `Tarea2_CalidadAireCYL/U002_T2_CalidadAireCYL` | Calidad del Aire CYL | Análisis exploratorio de datos medioambientales |
| `Tarea2_Zoo/U002_T2_Reducción_dimensionalidad_Zoo.ipynb` | Zoo | Correlación (Pearson, Spearman), Backward Elimination, RFE, Ridge, Lasso, PCA, LDA |

## 📊 Material teórico

| Archivo | Contenido |
|---|---|
| `U002.1. Preparación de datos.pdf` | Apuntes completos de la unidad |
| `U002.1. Preparación de datos.pptx` | Fundamentos de preparación de datos |
| `U002.2. Preparación de datos. Selección.pptx` | Métodos de selección de características |
| `U002.3. Preparación de datos. Transformación.pptx` | Transformaciones (normalización, encoding, etc.) |

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `pandas` | Manipulación de DataFrames |
| `numpy` | Operaciones numéricas |
| `matplotlib` / `seaborn` | Visualización de datos |
| `scikit-learn` | PCA, RFE, scalers, `RandomForestRegressor`, LDA |
| `missingno` | Visualización de valores nulos |
| `statsmodels` | Backward elimination, OLS |
| `pingouin` | Test ANOVA |
| `google-cloud-bigquery` | Acceso a BigQuery (tarea) |

## ▶️ Cómo ejecutar

1. Abre los notebooks en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Ajusta las rutas de los archivos CSV si es necesario (algunas prácticas referencian rutas de Google Drive).
3. Instala dependencias adicionales si se requieren:
   ```bash
   pip install missingno pingouin statsmodels
   ```
4. Ejecuta las celdas secuencialmente.

> ⚠️ **Nota:** Algunos notebooks utilizan `google.colab.drive` para montar Google Drive. Si ejecutas en local, actualiza las rutas de carga de datos.
