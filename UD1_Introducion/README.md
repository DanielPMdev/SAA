# 📘 UD1 — Introducción al Aprendizaje Automático

## 📋 Descripción

Unidad introductoria del módulo **Sistemas de Aprendizaje Automático**. Se presenta el entorno de trabajo (Google Colab), las librerías fundamentales del ecosistema Python para ciencia de datos y se realiza un primer análisis exploratorio de datos (EDA) sobre el clásico dataset **Titanic**.

## 🎯 Objetivos de aprendizaje

- Familiarizarse con Google Colab como entorno de desarrollo.
- Importar y manipular datasets con **Pandas**.
- Calcular estadísticas descriptivas: media, mediana, moda, desviación estándar y varianza.
- Generar visualizaciones básicas: histogramas, diagramas de barras, boxplots y gráficos de dispersión.

## 📂 Estructura

```
UD1_Introducion/
└── Practica_Titanic/
    ├── U001_Práctica1_Google_Colab.ipynb   # Notebook principal
    ├── Práctica1_Google Colab.pdf          # Enunciado / guía de la práctica
    └── titanic_train.csv                   # Dataset Titanic (entrenamiento)
```

## 📓 Notebooks

### `U001_Práctica1_Google_Colab.ipynb`

| Aspecto | Detalle |
|---|---|
| **Tema** | EDA básico sobre el dataset Titanic |
| **Celdas** | 34 (15 markdown, 19 código) |
| **Dataset** | `titanic_train.csv` — 891 pasajeros, 12 variables |

**Contenido del notebook:**

1. **Importación de librerías** — Pandas, NumPy, Matplotlib, Seaborn, Statistics.
2. **Carga del dataset** — Lectura del CSV y primeras inspecciones (`head()`, `info()`).
3. **Estadísticas descriptivas** — Media, mediana, moda, desviación estándar, varianza.
4. **Representación gráfica:**
   - Histogramas (distribución de edad, tarifa, etc.)
   - Subplots para comparativas
   - Diagramas de barras (supervivencia por clase, sexo)
   - Boxplots (detección de outliers)
   - Gráficos de dispersión (scatter plots)

## 🛠️ Tecnologías utilizadas

| Librería | Uso |
|---|---|
| `pandas` | Manipulación de DataFrames |
| `numpy` | Operaciones numéricas |
| `matplotlib` | Visualización de datos |
| `seaborn` | Visualización estadística avanzada |
| `statistics` | Cálculos estadísticos nativos de Python |

## ▶️ Cómo ejecutar

1. Abre el notebook en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Asegúrate de que el archivo `titanic_train.csv` se encuentra accesible (mismo directorio o ruta ajustada).
3. Ejecuta las celdas secuencialmente.

## 📊 Dataset

| Campo | Descripción |
|---|---|
| `PassengerId` | Identificador único del pasajero |
| `Survived` | Supervivencia (0 = No, 1 = Sí) |
| `Pclass` | Clase del billete (1, 2, 3) |
| `Name` | Nombre del pasajero |
| `Sex` | Sexo |
| `Age` | Edad |
| `SibSp` | Nº de hermanos/cónyuges a bordo |
| `Parch` | Nº de padres/hijos a bordo |
| `Ticket` | Número de billete |
| `Fare` | Tarifa pagada |
| `Cabin` | Número de cabina |
| `Embarked` | Puerto de embarque (C, Q, S) |
