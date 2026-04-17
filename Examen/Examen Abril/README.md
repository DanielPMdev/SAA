# 📝 Examen Abril — Segundo Parcial (Deep Learning / CNN)

## 📋 Descripción

Directorio con el **examen del segundo parcial** (abril 2026) y material de preparación (apuntes teóricos, ejercicios resueltos y exámenes de laboratorio de convocatorias anteriores). El contenido cubre arquitecturas de redes neuronales convolucionales (CNN), backpropagation, experimentación de hiperparámetros y entrenamiento de modelos con Keras/TensorFlow.

## 📂 Estructura

```
Examen Abril/
│
├── 📓 Examen20260414_SAA_Daniel_Porras_Morales.ipynb   # Examen propio (14/04/2026)
├── 📄 Apuntes.md                                       # Apuntes completos de repaso
├── 📄 ApuntesCNN_Dimensiones.md                        # Ejercicios resueltos CNN (dimensiones y parámetros)
├── 🖼️ image.png                                        # Diagrama de backpropagation
│
└── JupyterNotebooks/                                   # Exámenes y prácticas de laboratorio anteriores
    ├── 📓 Examen20230508_SAA_Daniel_Porras_Morales.ipynb
    ├── 📓 Examen20240429_SAA_Daniel_Porras_Morales.ipynb
    ├── 📓 Examen20250410_SAA_Daniel_Porras_Morales.ipynb
    ├── 📓 Lab_3_Experimentación_de_hiperparametros.ipynb
    ├── 📓 Lab_3_Experimentación_de_hiperparametros_CIFAR-10.ipynb
    └── 📓 Lab_4_Arquitecturas_CNN.ipynb
```

## 🎓 Examen propio — Curso 2025-2026

### `Examen20260414_SAA_Daniel_Porras_Morales.ipynb`

| Aspecto | Detalle |
|---|---|
| **Fecha** | 14 de abril de 2026 |
| **Dataset** | MNIST (dígitos escritos a mano, 0-9) |
| **Tipo de problema** | Clasificación multiclase (10 clases) |
| **Duración** | 2 horas |
| **Restricciones** | ❌ Prohibido uso de IA generativa |
| **Entrega** | `.ipynb` + `.pdf` |

**Contenido del examen:**

| Fase | Pregunta | Descripción | Puntuación |
|---|---|---|---|
| **Preparación** | P1 | Normalización, análisis de distribución de clases, barajado de datos | 0,25 pts |
| **Exp. 1 — FC** | P2 | Red Fully Connected (Dense) que supere 90 % val_accuracy. Optimizador Adam | 1,00 pts |
| **Visualización** | P3 | Tabla de experimentación (`PrettyTable`) y funciones de gráficas comparativas | 0,25 pts |
| **Exp. 2 — CNN** | P4 | Red CNN que supere 96 % val_accuracy. Optimizador SGD | 1,50 pts |

**Resultados obtenidos:**

| Experimento | Descripción | Accuracy | Loss | Val_Accuracy | Val_Loss |
|---|---|---|---|---|---|
| Exp. 1 | Fully Connected, Adam, sin convolucionales | 0.9820 | 0.0549 | 0.9772 | 0.0821 |
| Exp. 2 | CNN + BatchNormalization + SGD + Dropout 0.3 | 0.9931 | 0.0250 | 0.9893 | 0.0370 |

**Librerías:** TensorFlow, Keras (Sequential, Conv2D, MaxPooling2D, Dense, Flatten, Dropout, BatchNormalization, EarlyStopping), NumPy, Matplotlib, PrettyTable.

---

## 📄 Material de estudio

### `Apuntes.md`

Resumen completo de repaso para el examen que incluye:

| Sección | Contenido |
|---|---|
| **Código para Gráficas** | Funciones `plot_acc`, `plot_loss`, `plot_compare_losses`, `plot_compare_accs` |
| **Tabla de Experimentos** | Código con `PrettyTable` para registrar métricas por época |
| **Arquitectura CNN** | Patrón estándar Conv2D → BN → MaxPool → Dense → Dropout → Softmax |
| **SGD vs ADAM** | Comparativa de velocidad, memoria y generalización |
| **BatchNormalization** | Cómo y dónde ubicarlo; efecto en entrenamiento con SGD |
| **Dropout** | Tasas 0.3 vs 0.5; impacto en accuracy |
| **Data Augmentation** | `ImageDataGenerator`: ventajas y desventajas a corto plazo |
| **EarlyStopping** | Configuración típica: monitor, patience, restore_best_weights |
| **Funciones de pérdida** | `sparse_categorical_crossentropy`, `categorical_crossentropy`, `binary_crossentropy` |
| **Init a cero** | Problema de ruptura de simetría: la red NO aprende |
| **Backpropagation** | Operaciones elementales (suma, multiplicación, máximo, escalar) con diagrama |
| **CNN: Dimensiones** | Fórmulas y 10 ejercicios resueltos (Conv2D y MaxPool) |

### `ApuntesCNN_Dimensiones.md`

Ejercicios resueltos de cálculo de dimensiones de salida y parámetros entrenables para capas Conv2D y MaxPooling2D. Incluye la tabla-resumen de 10 ejercicios con detección de configuraciones inválidas por stride incompatible.

---

## 📚 Exámenes de laboratorio anteriores

| Año | Fecha | Dataset | Notebook | Técnicas principales |
|---|---|---|---|---|
| **2023** | 08/05/2023 | MNIST | `Examen20230508_SAA_Daniel_Porras_Morales.ipynb` | CNN (Conv2D, MaxPooling2D), Dropout, `sparse_categorical_crossentropy` |
| **2024** | 29/04/2024 | MNIST | `Examen20240429_SAA_Daniel_Porras_Morales.ipynb` | CNN, Data Augmentation, SGD vs Adam, EarlyStopping, comparativa de hiperparámetros |
| **2025** | 10/04/2025 | Fashion-MNIST | `Examen20250410_SAA_Daniel_Porras_Morales.ipynb` | CNN básica (32-64 filtros), Init a cero, Dropout 0.3/0.5, SGD, BN, Augmentation, `PrettyTable` |

## 🔧 Prácticas de laboratorio

| Práctica | Notebook | Contenido |
|---|---|---|
| **Lab 3** | `Lab_3_Experimentación_de_hiperparametros.ipynb` | Experimentación de hiperparámetros con redes neuronales |
| **Lab 3 (CIFAR-10)** | `Lab_3_Experimentación_de_hiperparametros_CIFAR-10.ipynb` | Experimentación de hiperparámetros sobre CIFAR-10 |
| **Lab 4** | `Lab_4_Arquitecturas_CNN.ipynb` | Arquitecturas CNN avanzadas |

## 🔑 Patrón común de los exámenes de laboratorio

1. **📐 Preparación de datos** — Carga, reshape, normalización (0-1), análisis de distribución de clases.
2. **🏗️ Diseño de la arquitectura** — CNN con Conv2D, MaxPooling2D, Flatten, Dense, Dropout, BatchNormalization.
3. **⚙️ Compilación** — Optimizador (Adam o SGD), loss (`sparse_categorical_crossentropy`), métricas (`accuracy`).
4. **🏋️ Entrenamiento** — Con `EarlyStopping`, `validation_split` o `validation_data`.
5. **📊 Experimentación** — Tabla comparativa de métricas y gráficas de accuracy/loss por epoch.
6. **📝 Conclusiones** — Justificación de las decisiones de arquitectura y análisis de resultados.

## 🛠️ Tecnologías recurrentes

| Librería | Uso |
|---|---|
| `tensorflow` / `keras` | Definición, compilación y entrenamiento de modelos (Sequential, Conv2D, Dense, etc.) |
| `numpy` | Manipulación de arrays y cálculos numéricos |
| `matplotlib` | Visualización de gráficas de entrenamiento (accuracy, loss) |
| `prettytable` | Tabla de registro de experimentos |

## ▶️ Cómo ejecutar

1. Abre el notebook deseado en [Google Colab](https://colab.research.google.com/) o Jupyter Notebook.
2. Asegúrate de tener `tensorflow`, `keras`, `numpy`, `matplotlib` y `prettytable` instalados.
3. Ejecuta las celdas secuencialmente.

> 💡 **Consejo:** Los exámenes de años anteriores son excelente material de estudio. Cada uno cubre el pipeline completo de entrenamiento de redes neuronales, desde la preparación de datos hasta las conclusiones.
