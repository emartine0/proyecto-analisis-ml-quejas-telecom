# proyecto-analisis-ml-quejas-telecom
Este conjunto de análisis combina analisis de machinelearning y visualización mostrando un trabajo completo de ciencia de datos sobre un conjunto de datos reales.

proyecto-analisis-ml-quejas-telecom/
│
├── .gitignore
├── README.md
├── requirements.txt
├── LICENSE
│
├── data/
│   ├── raw/                  # Datos originales sin modificar (CSV descargado)
│   ├── processed/            # Datos limpios y listos para entrenar (features listos)
│   └── predictions/          # Datasets finales con las 3 predicciones para Tableau
│
├── notebooks/                # Jupyter Notebooks para exploración e investigación
│   ├── 01_eda_limpieza.ipynb
│   ├── 02_nlp_clasificacion.ipynb
│   └── 03_modelado_predictivo.ipynb
│
├── src/                      # Código fuente modular en scripts .py (producción)
│   ├── __init__.py
│   ├── data_prep.py          # Limpieza y feature engineering
│   ├── train_classification.py # Entrenamiento del modelo de conciliación
│   ├── train_regression.py     # Entrenamiento de tasa de recuperación y tiempo
│   └── predict.py            # Script para generar predicciones en datos nuevos
│
├── models/                   # Modelos guardados (.pkl o .joblib)
│   ├── model_conciliacion.joblib
│   ├── model_tasa.joblib
│   └── model_tiempo.joblib
│
└── tableau/                  # Archivos .twbx o enlaces al dashboard interactivo
    └── README.md
