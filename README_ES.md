# PROJECT_ML_JOAQUINVILLAR_ONLINE_DS_THEBRIDGE

## Clasificación de Préstamos

### 1. Objetivo 🎯
En este proyecto de Machine Learning, se busca desarrollar un modelo capaz de predecir la probabilidad de que un solicitante de crédito no pague su préstamo, basándonos en un conjunto de datos de clientes a quienes ya se les ha otorgado un crédito.

El objetivo es identificar aquellos clientes con un alto riesgo de incumplir sus pagos, para evitar conceder préstamos a perfiles similares en el futuro, minimizando así las pérdidas crediticias. Por otro lado, el modelo también ayudará a identificar a los buenos clientes, quienes han pagado o están en proceso de pagar el crédito, para concederles préstamos en el futuro.

### 2. Dataset 📊
El dataset utilizado se ha obtenido de Kaggle y contiene información sobre préstamos otorgados a clientes, con sus respectivas características y el estado de pago de los mismos. Puedes acceder al dataset aquí.

En el dataset, se tiene información tanto de clientes que han cumplido con sus pagos (situación favorable) como de clientes que no han devuelto el préstamo (situación desfavorable).

Objetivo del modelo: Identificar a los clientes morosos (class 0, "charged-off") y evitar concederles créditos en el futuro, además de premiar a los buenos pagadores.

### 3. Metodología 📝
- Preprocesamiento de datos: El dataset presenta un desbalance en la variable target (lo que indica si el préstamo fue incumplido o no). Se utilizó la técnica de UnderSampling para balancear los datos, es decir, reducir la cantidad de ejemplos de la clase mayoritaria (clientes que sí pagaron) para mejorar el rendimiento del modelo.

- Modelos utilizados:

    - Regresión Logística: Para evaluar la relación entre las características de los clientes y la probabilidad de incumplimiento.

    - Random Forest: Un modelo de ensemble para mejorar la precisión y robustez.

    - XGBoost: Un algoritmo avanzado de boosting para optimizar la predicción, que en este caso proporcionó un rendimiento superior.

- Optimización de Parámetros: Se realizó una optimización de parámetros en el modelo usando técnicas de Grid Search para mejorar los resultados obtenidos por el modelo. El modelo final fue entrenado con la técnica de UnderSampling para asegurar una mayor equidad en la clasificación de ambas clases.

- Métricas utilizadas:

    - Matriz de Confusión: Para evaluar el desempeño del modelo.

    - Recall de la clase 0 (Charged-off): Dado el desbalance en el dataset, el recall de la clase 0 es especialmente importante. Queremos asegurarnos de que el modelo sea capaz de identificar correctamente a los clientes morosos.

### 4. Estructura del Repositorio 📂
El repositorio tiene la siguiente estructura de carpetas:
```
src/
│
├── data_sample/              # Muestra del dataset utilizado en el proyecto.
├── img/                      # Imágenes usadas en el proyecto.
├── notebooks/                # Notebooks usados para la experimentación.
├── results_notebook/         # Notebook final que resume todo el proceso.
├── models/                   # Modelos guardados en formato joblib.
└── utils/                    # Funciones y módulos auxiliares.
```
### 5. Exposición en Video 🎥
El proyecto también incluye una exposición en formato vídeo de los resultados obtenidos, la cual cubre los siguientes puntos:

- Introducción al problema: Descripción de la importancia de predecir qué clientes no pagarán sus préstamos para evitar pérdidas.

- Planteamiento del problema técnico: Cómo se utiliza Machine Learning para clasificar a los clientes en función de su riesgo de impago.

- Descripción del dataset: Breve descripción de las características del dataset y el proceso de Análisis Exploratorio de Datos (EDA) realizado.

- Resultados: Comparación entre los modelos probados (Regresión Logística, Random Forest, XGBoost) y la justificación de la selección del modelo final.

- Conclusiones y mejoras futuras: Reflexión sobre cómo se puede mejorar el modelo en el futuro y las decisiones que se tomarán con base en los resultados.

### 6. Modelo Final 🏆
El modelo final se ha guardado en formato joblib para su posterior uso y despliegue.

### 7. Conclusión 💡
Este proyecto muestra cómo aplicar técnicas de Machine Learning a problemas del mundo real, en este caso, la clasificación de clientes según su capacidad de pago de préstamos. Gracias al análisis y modelado de los datos, es posible tomar decisiones más informadas y reducir el riesgo de pérdidas en el sector financiero.