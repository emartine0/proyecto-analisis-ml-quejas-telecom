# proyecto-analisis-ml-quejas-telecom
Este conjunto de análisis combina analisis de machinelearning y visualización mostrando un trabajo completo de ciencia de datos sobre un conjunto de datos reales.

> ⚠️ **Aviso:** 
> Este proyecto fue desarrollado con fines educativos y de aprendizaje y se encuentra actualmente en fase de revisión y optimización. Tenga en cuenta que el código en Python y la estructura en Tableau contienen oportunidades de mejora.

## Contexto del Problema
Uno de los objetivos de la PROFECO es la protección de los derechos de las personas consumidoras frente a abusos en las relaciones comerciales, por lo tanto entre sus atribuciones se encuentra la de la atención a quejas de caracter comercial. Por lo tanto, lo que busca este análisis es mejorar el proceso de atención, esto es hacer los procesos de atención más eficientes y eficazes, lo cual se busca hacer identificando 4 puntos clave, que son:
- Identificar quejas recién ingresadas cuya predicción supere los 60 días para asignarles prioridad alta o canalizarlas por vías rápidas.
-  Un mapa o gráfico de barras que compare el promedio de días predichos por oficina de defensa del consumidor para nivelar la carga de trabajo entre oficinas.
-   identificar los casos "Críticos" (Baja probabilidad de acuerdo y resolución muy lenta).

## 📂 Estructura del Repositorio
```
proyecto-analisis-ml-quejas-telecom/
│
├── README.md
├── requirements.txt
├── LICENSE
│
├── data/
│   ├── raw/                      # Datos originales sin modificar (CSV descargado)
│   ├── processed/                # Datos limpios y listos para entrenar (features listos)
│   └── predictions/              # Datasets finales con las 3 predicciones para Tableau
│
├── notebooks/                    # Jupyter Notebooks para exploración e investigación
│   ├── 01_eda_limpieza.ipynb
│   ├── 02_nlp_clasificacion.ipynb
│   └── 03_modelado_predictivo.ipynb
│
├── src/                          # Código fuente modular en scripts .py (producción)
│   ├── __init__.py
│   ├── data_prep.py              # Limpieza y feature engineering
│   ├── train_classification.py   # Entrenamiento del modelo de conciliación
│   ├── train_regression.py       # Entrenamiento de tasa de recuperación y tiempo
│   └── predict.py                # Script para generar predicciones en datos nuevos
│
├── models/                       # Modelos guardados (.pkl o .joblib)
│   ├── model_conciliacion.joblib
│   ├── model_tasa.joblib
│   └── model_tiempo.joblib
│
└── tableau/                      # Archivos .twbx o enlaces al dashboard interactivo
    └── README.md
```




