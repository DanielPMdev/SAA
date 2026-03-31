# 📘 UD5 — Aprendizaje Automático No Supervisado

## 📋 Descripción

Unidad centrada en los **algoritmos de aprendizaje no supervisado**, principalmente técnicas de **clustering**. Se trabaja con K-Means como algoritmo principal, junto con métodos de validación como el método del codo (Elbow Method) y el coeficiente Silhouette, además de explorar clustering jerárquico como alternativa.

## 🎯 Objetivos de aprendizaje

- Comprender la diferencia entre aprendizaje supervisado y no supervisado.
- Implementar el algoritmo **K-Means** para segmentación de datos.
- Determinar el número óptimo de clusters con el **método del codo** y **Silhouette Score**.
- Aplicar **PCA** para visualización de clusters en alta dimensionalidad.
- Implementar **Clustering Jerárquico (Aglomerativo)** como alternativa a K-Means.
- Interpretar y categorizar los resultados del clustering.

## 📂 Estructura

```
UD5_AprendizajeAutomaticoNoSupervisado/
│
├── 📓 U005_P1__Clustering_Samsung_CAP.ipynb                  # K-Means sobre datos Samsung
├── 📓 U005_P2_Cars.ipynb                                      # K-Means sobre dataset de coches
├── 📓 U005_P4_Big_Five_Personality_Test.ipynb                 # K-Means sobre test de personalidad
├── 📓 U005_P7_Credit Card Dataset for Clustering.ipynb        # Clustering de tarjetas de crédito
│
└── Tareas/
    ├── 📓 Credit_Card.ipynb                                   # Tarea: Clustering + Jerárquico
    └── 📓 Ship_Performance.ipynb                              # Tarea: K-Means rendimiento de barcos
```

## 📓 Notebooks — Prácticas guiadas

### `U005_P1__Clustering_Samsung_CAP.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 42 (20 markdown, 22 código) |
| **Dataset** | `Samsung.csv` |
| **Técnicas** | K-Means, preprocesamiento con `LabelEncoder` |

---

### `U005_P2_Cars.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 17 (solo código) |
| **Dataset** | `mtcars.csv` |
| **Técnicas** | K-Means, `LabelEncoder`, LassoCV para selección de features |

---

### `U005_P4_Big_Five_Personality_Test.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 36 (14 markdown, 22 código) |
| **Dataset** | `personality.csv` (~416 MB, muestreo requerido) |

**Pipeline:**

1. **Muestreo** — Selección de subconjunto por el tamaño del dataset.
2. **Preparación** — Eliminación de atributos, tratamiento de nulos.
3. **K-Means:**
   - Determinación de k óptimo con `KElbowVisualizer`.
   - Entrenamiento y asignación de clusters.
   - Análisis e interpretación de perfiles de personalidad.
   - Visualización con PCA (2D).
4. **Predicción** — Clasificación de nuevos individuos en clusters existentes.

---

### `U005_P7_Credit Card Dataset for Clustering.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 26 (10 markdown, 16 código) |
| **Dataset** | `CC GENERAL.csv` |

**Pipeline:**

1. **Comprensión y limpieza** — Nulos, outliers.
2. **Reducción de dimensionalidad** — Varianza, Correlación, PCA.
3. **Clustering** — K-Means con `silhouette_score`.

## 📓 Notebooks — Tareas evaluables

### `Tareas/Credit_Card.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 35 (12 markdown, 23 código) |
| **Técnicas adicionales** | **Clustering Jerárquico (Aglomerativo)**, dendrograma con `scipy` |
| **Diferencia vs práctica** | Incluye `AgglomerativeClustering` y `KElbowVisualizer` |

---

### `Tareas/Ship_Performance.ipynb`

| Aspecto | Detalle |
|---|---|
| **Celdas** | 24 (9 markdown, 15 código) |
| **Dataset** | `Ship_Performance_Dataset.csv` |

**Pipeline estructurado:**

1. Importación y análisis exploratorio.
2. Preprocesamiento (`StandardScaler`, `MinMaxScaler`).
3. Método del codo con `KElbowVisualizer`.
4. Entrenamiento K-Means.
5. Análisis y categorización de clusters.

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `pandas` / `numpy` | Manipulación de datos |
| `matplotlib` / `seaborn` | Visualización |
| `scikit-learn` | K-Means, PCA, scalers, `silhouette_score`, `AgglomerativeClustering` |
| `yellowbrick` | `KElbowVisualizer` para método del codo |
| `scipy` | Dendrogramas para clustering jerárquico |

## ▶️ Cómo ejecutar

1. Abre los notebooks en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Asegúrate de tener los datasets necesarios desde `Datasets/` o ajusta las rutas.
3. Instala dependencias adicionales:
   ```bash
   pip install yellowbrick
   ```
4. Ejecuta las celdas secuencialmente.

> ⚠️ **Nota:** El dataset `personality.csv` (~416 MB) es muy grande. El notebook aplica muestreo para hacer viable su procesamiento.
