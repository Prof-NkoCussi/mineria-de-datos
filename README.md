# Minería de Datos

Trabajos y ejercicios de **Minería de Datos** 

Cubren el ciclo típico de un proyecto de datos: exploración y visualización, preprocesamiento, modelos de clasificación y regresión, clustering, reducción de dimensionalidad, árboles y ensambles, y procesamiento de texto.

**Autor:** Nicolás Cussi

## Proyectos

| # | Notebook | Técnicas | Datos |
|---|----------|----------|-------|
| 01 | [Parcial: Bank Marketing](proyectos/01_parcial_bank_marketing_regresion_logistica.ipynb) | Regresión logística, manejo de valores `unknown`, codificación one-hot, escalado, ajuste del hiperparámetro `C`, evaluación con clases desbalanceadas | Dataset real [Bank Marketing (UCI)](data/README.md), 41.188 registros |
| 02 | [Árbol de decisión con Penguins](proyectos/02_arbol_decision_penguins.ipynb) | Árbol de decisión, visualización del árbol, matriz de confusión, análisis de interpretabilidad | Dataset `penguins` de seaborn (≈ 98,5 % de accuracy en test) |
| 03 | [EDA, PCA y clustering de clientes](proyectos/03_eda_pca_clustering_clientes_banco.ipynb) | Análisis exploratorio, correlaciones, PCA, K-Means (con y sin PCA) | Dataset ficticio de 8 clientes |
| 04 | [Riesgo crediticio](proyectos/04_riesgo_crediticio_arboles_random_forest.ipynb) | Árbol de decisión, `GridSearchCV`, Random Forest, ROC-AUC, importancia por permutación, selección de umbral | Datos sintéticos con relaciones conocidas (3.000 clientes) |

## Ejercicios

| # | Notebook | Técnicas |
|---|----------|----------|
| 01 | [Visualización de datos](ejercicios/01_visualizacion_datos.ipynb) | Histogramas, boxplot, pairplot, heatmap, violin plot |
| 02 | [Preprocesamiento de datos](ejercicios/02_preprocesamiento_datos.ipynb) | Imputación, outliers (IQR), normalización y estandarización, codificación de categóricas |
| 03 | [Clustering](ejercicios/03_clustering_kmeans_dbscan.ipynb) | K-Means, DBSCAN, método del codo, Silhouette, Davies-Bouldin |
| 04 | [Regresión logística y múltiple](ejercicios/04_regresion_logistica_y_multiple.ipynb) | Clasificación y regresión, métricas (accuracy, R², MSE, MAE) |
| 05 | [NLP: Naive Bayes y LSTM](ejercicios/05_nlp_naive_bayes_lstm.ipynb) | Limpieza de texto, TF-IDF, Naive Bayes, red neuronal LSTM |

## Sobre los datos

- El **proyecto 01** usa un dataset real y requiere descargarlo (ver [`data/README.md`](data/README.md)).
- El **proyecto 02** descarga `penguins` automáticamente desde seaborn (necesita conexión a internet).
- Varios ejercicios usan **datasets ficticios muy pequeños** (6 a 8 registros) pensados para practicar la técnica. Cada notebook lo aclara al inicio y, donde corresponde, discute por qué sus métricas no son generalizables.
- El **proyecto 04** usa datos **sintéticos** generados con un proceso conocido, lo que permite verificar si los modelos recuperan las relaciones reales.

## Cómo ejecutarlo

```bash
git clone <url-del-repositorio>
cd mineria-de-datos

python -m venv .venv
source .venv/bin/activate        # En Windows: .venv\Scripts\activate
pip install -r requirements.txt

jupyter lab
```

Los notebooks usan rutas relativas y deben abrirse desde su carpeta. TensorFlow solo es necesario para `ejercicios/05_nlp_naive_bayes_lstm.ipynb`.

## Estructura

```
mineria-de-datos/
├── proyectos/      # trabajos con análisis y conclusiones
├── ejercicios/     # prácticas de cada técnica
├── data/           # datasets (ver data/README.md)
├── requirements.txt
└── README.md
```
