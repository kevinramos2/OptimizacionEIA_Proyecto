# Riesgo de incumplimiento crediticio: comparación de optimizadores y optimización de hiperparámetros

Proyecto final del curso **Optimización e Inteligencia Artificial**. Docente: María C. Torres.

**Integrantes.**

- Kevin Leandro Ramos Luna
 
- Daniel Felipe Garzón Acosta
 
- Ángel Efraín Pimienta Durán

- Daniel Ortega
 
- Manuel Mera Mera

**Video:** _(enlace de YouTube)_ · **Póster:** [`poster/`](poster/)

## Problema

Se busca predecir si un solicitante de crédito tendrá dificultades de pago (`TARGET = 1`) a partir de su información sociodemográfica y financiera.

- **Tipo de tarea:** clasificación binaria desbalanceada (≈ 8 % de incumplimiento).
- **Métrica principal:** ROC-AUC.

La optimización interviene en dos niveles:

1. **Entrenamiento:** se comparan 8 optimizadores para minimizar la entropía cruzada de un perceptrón multicapa (MLP):
   - SGD, Momentum, Nesterov, Adagrad, RMSprop, Adam, Nadam y AdamW.
2. **Hiperparámetros:**
   - MLP: Random Search vs. Optimización Bayesiana vs. Hyperband (Keras Tuner).
   - LightGBM: TPE vs. búsqueda aleatoria (Optuna).

## Datos

[Home Credit Default Risk – Kaggle](https://www.kaggle.com/competitions/home-credit-default-risk). Se usa `application_train.csv`:

| Etapa | Dimensiones |
|---|---|
| Datos originales | 307.511 registros × 122 columnas |
| Después del preprocesamiento | 307.507 × 236 atributos |

Los datos **no** están en el repositorio. Para descargarlos, aceptar las reglas de la competencia en Kaggle y luego:

```bash
kaggle competitions download -c home-credit-default-risk -f application_train.csv
```

## Cómo ejecutar

1. Abrir `ProyectoFinal_HomeCredit.ipynb` en Google Colab y activar la GPU (*Entorno de ejecución → Cambiar tipo de entorno → GPU*).
2. Subir `application_train.csv` a Google Drive en `MyDrive/home-credit-default-risk/`.
3. Ejecutar todas las celdas. Las figuras se guardan en `MyDrive/OptimizacionEIA_Proyecto/figuras/`.

## Estructura

```
├── ProyectoFinal_HomeCredit.ipynb   # notebook principal
├── figuras/                         # figuras exportadas para el póster
├── poster/                          # póster (.pptx y .pdf)
└── requirements.txt
```

## Resultados

_(Completar al terminar: tabla resumen y figuras principales.)_
