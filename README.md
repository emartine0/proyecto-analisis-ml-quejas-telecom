# proyecto-analisis-ml-quejas-telecom
Este conjunto de análisis combina analisis de machinelearning y visualización mostrando un trabajo completo de ciencia de datos sobre un conjunto de datos reales.

> ⚠️ **Aviso:** 
> Este proyecto fue desarrollado con fines educativos y de aprendizaje y se encuentra actualmente en fase de revisión y optimización. Tenga en cuenta que el código en Python y la estructura en Tableau contienen oportunidades de mejora.

## Contexto del Problema
Uno de los objetivos de la PROFECO es la protección de los derechos de las personas consumidoras frente a abusos en las relaciones comerciales, por lo tanto entre sus atribuciones se encuentra la de la atención a quejas de caracter comercial. Por lo tanto, lo que busca este análisis es mejorar el proceso de atención, esto es hacer los procesos de atención más eficientes y eficazes, lo cual se busca hacer identificando 4 puntos clave, que son:
- Identificar quejas recién ingresadas cuya predicción supere los 60 días para asignarles prioridad alta.
- Identificar los casos "Críticos" (Baja probabilidad de acuerdo y resolución muy lenta).
- Identificar las reclamaciones monetarias cuyo tasa de recuperacion sea menor al 65% para dar mayor prioridad.
- Identificar los casos "Criticos" (Baja probabilidad de recuperacion y tasa de recuperación muy baja)
---
## Arquitectura de Machine Learning:
- Modelo 1 (Clasificación): Predicción de resultado (Conciliado vs. No Conciliado).
- Modelo 2 (Regresión Logarítmica): Estimación del tiempo de resolución (Días).
- Modelo 3 (Clasificación): Predicción de resultado (Monto Recuperado vs. Monto No Recuperado).
- Modelo 4 (Regresión Basado en Arboles): Estimación de la tasa de recuperación.
---
## Resultados e Impacto (Métricas)
El modelo de clasificación (Random Forest) alcanzó un AUC-ROC de 0.76 en el conjunto de prueba no visto. Mientras que el error medio absoluto (MAE) del modelo de tiempo fue ______. Este resultado se considera altamente aceptable y robusto para la predicción de comportamiento de conciliación en telecomunicaciones, considerando que los datos dependen de factores de negociación no estructurados.
---
## Integración con Tableau

---
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




