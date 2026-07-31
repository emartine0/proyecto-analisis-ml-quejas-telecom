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

## Arquitectura de Machine Learning
- Modelo 1 (Clasificación): Predicción de resultado (Conciliado vs. No Conciliado).
- Modelo 2 (Regresión Logarítmica): Estimación del tiempo de resolución (Días).
- Modelo 3 (Clasificación): Predicción de resultado (Monto Recuperado vs. Monto No Recuperado).
- Modelo 4 (Regresión Basado en Arboles): Estimación de la tasa de recuperación.

---

## Resultado e Impacto (Métricas)
Los modelos de clasificación alcanzaron un AUC-ROC de _______  y _______, respectivamente, en el conjunto de prueba no visto. Por otro lado, el error medio absoluto (MAE) fue de ____ y ____, respectivamente. Estos resultados se consideran altamente aceptables y robustos para la predicción de comportamientos para los 4 objetivos principales de este análisis, considerando que los datos dependen de factores de negociación no estructurados.


### Integración con Tableau

---

## 📂 Estructura del Repositorio
```
proyecto-analisis-ml-quejas-telecom/
│
├── README.md
├── requerimientos.txt
├── LICENSE
│
├── datos/                        # Datos originales, datos de preanalisis y datos analizados 
│   ├── quejas_telecom.csv
│   ├── quejas_telecom_lf.csv
│   └── quejas_telecom_ml.csv            
│
├── notebooks/                    # Jupyter Notebooks para exploración e investigación
│   ├── 01_eda_limpieza.ipynb
│   └── 02_modelado_predictivo.ipynb
│  
├── src/                          # Código fuente modular en scripts .py (producción)
│   ├── __init__.py
│   ├── prep_datos.py             # Limpieza y feature engineering
│   ├── tr_clasificacion.py       # Entrenamiento del modelo de conciliación y recuperación
│   ├── tr_regresion.py           # Entrenamiento del tiempo de resolucion y la tasa de recuperación
│   └── predict.py                # Script para generar predicciones en datos nuevos
│
├── modelos/                      # Modelos guardados (.pkl o .joblib)
│   ├── modelo_conciliacion.joblib
|   ├── modelo_tiempo.joblib
|   ├── modelo_recuperacion.jobli
│   └── modelo_tasa.joblib
│
└── tableau/                      # Archivos .twbx y enlaces al dashboard interactivo
    └── README.md
```




