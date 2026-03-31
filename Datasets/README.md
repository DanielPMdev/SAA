# 📁 Datasets

## 📋 Descripción

Directorio centralizado con todos los **datasets** utilizados a lo largo del módulo. Los notebooks de cada unidad pueden referenciar estos archivos directamente o incluir copias locales en sus propias carpetas.

## 📊 Catálogo de Datasets

| Archivo | Tamaño | Unidad(es) | Descripción |
|---|---|---|---|
| `Samsung.csv` | 3.4 KB | UD5 | Datos de sensores Samsung para clustering |
| `mtcars.csv` | 1.7 KB | UD5 | Motor Trend Car Road Tests (32 coches, 11 variables) |
| `CC GENERAL.csv` | 903 KB | UD5 | Comportamiento de clientes de tarjetas de crédito para segmentación |
| `Ship_Performance_Dataset.csv` | 726 KB | UD5 | Rendimiento de barcos para clustering |
| `salaries.csv` | 210 KB | Examen 2024 | Salarios para regresión y clasificación |
| `character-predictions.csv` | 216 KB | Examen 2022-Recu | Predicciones de personajes de Game of Thrones |
| `listings_berlin.csv` | 2.9 MB | Examen 2023-V2 | Listados de Airbnb en Berlín |
| `GSAF5.csv` | 2.5 MB | Examen 2023 | Global Shark Attack File |
| `database.csv` | 260 KB | — | Base de datos auxiliar |
| `hotel_bookings.csv` | 16.9 MB | Examen 2025 | Reservas de hotel para preparación y modelado |
| `creditcard.csv` | 150.8 MB | UD3 | Transacciones de tarjeta de crédito (detección de fraude) |
| `personality.csv` | 416.3 MB | UD5 | Big Five Personality Test (test de personalidad masivo) |
| `database.sqlite` | 313 MB | Examen 2026 | European Soccer Database (SQLite) |
| `kaggle_simpson_testset.zip` | 11.2 MB | UD6 | Imágenes de test de personajes de Los Simpsons |
| `simpsons_dataset.zip` | 541.9 MB | UD6 | Dataset de entrenamiento de personajes de Los Simpsons |

## ⚠️ Notas importantes

- **Archivos grandes:** `personality.csv` (~416 MB), `simpsons_dataset.zip` (~542 MB), `database.sqlite` (~313 MB) y `creditcard.csv` (~151 MB) son archivos muy pesados. Considera usar [Git LFS](https://git-lfs.github.com/) si deseas incluirlos en el repositorio.
- **Formatos:** La mayoría son CSV, con un archivo SQLite y dos archivos ZIP con imágenes.
- **Rutas:** Los notebooks suelen referenciar estos archivos mediante rutas de Google Drive. Si trabajas en local, ajusta las rutas según la ubicación del directorio `Datasets/`.

## 📥 Fuentes originales

| Dataset | Fuente |
|---|---|
| Titanic | [Kaggle - Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic) |
| Credit Card Fraud | [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |
| Adult Census | [UCI ML Repository - Adult](https://archive.ics.uci.edu/ml/datasets/adult) |
| Red Wine Quality | [UCI ML Repository - Wine Quality](https://archive.ics.uci.edu/ml/datasets/wine+quality) |
| Big Five Personality | [Kaggle - Big Five Personality Test](https://www.kaggle.com/datasets/tunguz/big-five-personality-test) |
| Simpsons Characters | [Kaggle - The Simpsons Characters](https://www.kaggle.com/datasets/alexattia/the-simpsons-characters-dataset) |
| European Soccer DB | [Kaggle - European Soccer Database](https://www.kaggle.com/datasets/hugomathien/soccer) |
| Hotel Bookings | [Kaggle - Hotel Booking Demand](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) |
| mtcars | Dataset integrado en R, exportado a CSV |
