# Equipo-c23-13-data

# Deteccion de fraudes con tarjetas de crédito

<img src="images\Deteccion.png" width="900">

### 📝 Índice:

- [**Introducción**](#introducción)
- [**Resumen del Proyecto**](#resumen)
- [**Objetivos**](#objetivos)
- [**Metodología**](#metodología)
   - [**Selección de Datos y Características**](#selección-de-datos-y-características)
   - [**Modelo de Predicción**](#modelo-de-predicción)
   - [**Evaluación del Modelo**](#evaluación-del-modelo)
- [**Descripción del Dataset**](#descripción-del-dataset)
   - [**Características del Dataset**](#características-del-dataset)
   - [**Verificación de la Calidad de los Datos**](#verificación-de-la-calidad-de-los-datos)
- [**Resultados y Evaluación**](#resultados-y-evaluación)
- [**Herramientas y Librerías Utilizadas**](#herramientas-y-librerías-utilizadas)
- [**Visualización de Resultados**](#visualización-de-resultados)
- [**Conclusión y Recomendaciones**](#conclusión-y-recomendaciones)
- [**Contacto**](#contacto)


### Introducción:

Este proyecto tiene como objetivo desarrollar un modelo de predicción de fraudes con tarjetas de crédito utilizando técnicas avanzadas de *Machine Learning*. El dataset utilizado proviene de Kaggle y contiene transacciones realizadas por titulares de tarjetas en Europa. 

El desafío es crear un modelo que pueda identificar patrones y predecir si una transacción es fraudulenta o no. Al detectar fraudes de manera más eficiente, los sistemas de tarjetas de crédito pueden prevenir pérdidas significativas y proteger a los usuarios.

La metodología empleada incluye la selección de características, entrenamiento del modelo mediante Árboles de Decisión con Aumento por Gradiente (ADAG), y la evaluación del rendimiento con métricas estándar.

### Resumen:

Este proyecto se centra en el análisis de un conjunto de datos de transacciones con tarjetas de crédito para predecir fraudes. Con un total de 568,630 transacciones, se utilizan 31 características para identificar patrones que permitan detectar actividades fraudulentas.

El modelo se entrena utilizando el algoritmo de Árboles de Decisión con Aumento por Gradiente (ADAG), conocido por su eficacia en tareas de clasificación binaria. El rendimiento del modelo se evalúa a través de métricas como AUC-ROC, precisión, sensibilidad y F1-score, con un enfoque en la validación cruzada para asegurar la generalización del modelo.

### Objetivos:

1. **Desarrollar un modelo predictivo** que clasifique transacciones como fraudulentas o no fraudulentas.
2. **Evaluar el rendimiento** del modelo utilizando métricas estándar de clasificación.

###  Metodología:
  #### Selección de Datos y Características:
  
  - El conjunto de datos utilizado en este proyecto proviene de Kaggle y contiene 568,630 transacciones de tarjetas de crédito realizadas por titulares europeos. Cada transacción tiene 31 características, divididas en cuatro grupos.

   - [Enlace al dataset de Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023)

  - Para la selección de características, se empleó el algoritmo de Árboles de Decisión con Aumento por Gradiente (ADAG), que ayuda a identificar las variables más relevantes para la predicción del fraude.

  #### Modelo de Predicción:
  
  - El modelo elegido para la predicción de fraudes es el **Árbol de Decisión con Aumento por Gradiente (ADAG)**. Este algoritmo se seleccionó debido a su excelente rendimiento y rapidez durante la fase de entrenamiento, lo que lo convierte en una opción ideal para tareas de clasificación binaria.

 - El ADAG es un modelo basado en árboles de decisión que combina múltiples árboles débiles para crear un modelo más robusto y preciso, lo que lo hace especialmente útil en problemas complejos como la detección de fraudes.

  #### Evaluación del Modelo:

 - **AUC-ROC**: La curva de características operativas del receptor, que mide la capacidad del modelo para distinguir entre las clases de fraude y no fraude.
- **Sensibilidad**: Mide la proporción de fraudes correctamente identificados.
- **Precisión**: Indica cuántas de las transacciones identificadas como fraudulentas realmente lo son.
- **Puntuación F1**: La media armónica entre la precisión y la sensibilidad, ofreciendo un balance entre ambas métricas.

Además, se utilizó **validación cruzada de k-subconjuntos (VCKS)** con k = 5, lo que asegura que el modelo se evalúa de manera confiable a través de diferentes particiones de los datos. 
 
### Descripción del Dataset :

  #### Características del Dataset:
  
  El conjunto de datos utilizado en este proyecto es un dataset público disponible en Kaggle que contiene información sobre transacciones realizadas con tarjetas de crédito. Fue recolectado por titulares de tarjetas en Europa durante 2023 y consta de **568,630 transacciones**.

Las características del conjunto de datos incluyen:

- **ID de la Transacción**: Identificador único para cada transacción.
- **V1 a V28**: 28 características anonimizadas que contienen información relevante sobre la transacción, como el tipo de compra, ubicación y detalles asociados a cada transacción, pero sin identificar al usuario o su información personal.
- **Amount**: El monto de la transacción en euros.
- **Clase**: La variable objetivo, que es una etiqueta binaria que indica si la transacción es fraudulenta (1) o no (0).

Este dataset está especialmente diseñado para abordar el problema de la **detección de fraudes** y es adecuado para la implementación de modelos de *Machine Learning* para clasificación binaria.

  #### Verificación de la Calidad de los Datos:
  
  -Antes de entrenar el modelo, se llevó a cabo un análisis exhaustivo de la calidad de los datos. El proceso incluyó:

- **Revisión de valores faltantes**: El conjunto de datos no presenta valores faltantes, lo que facilita el proceso de modelado sin necesidad de imputar o eliminar registros incompletos.
- **Verificación de consistencia**: Se aseguraron que los datos sean consistentes y que no haya valores atípicos que puedan afectar la calidad del modelo.

La calidad del dataset es alta, lo que permite realizar un entrenamiento efectivo del modelo sin complicaciones adicionales relacionadas con la limpieza de datos.

### Resultados y Evaluación: 

Tras el entrenamiento del modelo de Árboles de Decisión con Aumento por Gradiente (ADAG), se obtuvieron los siguientes resultados en el conjunto de prueba:

  - AUC-ROC: 0.99
  - Precisión: 0.99
  - Sensibilidad (Recall): 0.99
  - Puntuación F1: 0.99

Estos resultados indican que el modelo tiene una excelente capacidad para distinguir entre transacciones fraudulentas y no fraudulentas, manteniendo un equilibrio adecuado entre precisión y sensibilidad.

Además, la matriz de confusión mostró una alta tasa de verdaderos positivos y una baja tasa de falsos negativos, lo que sugiere que el modelo es eficaz en la identificación de fraudes sin generar un número significativo de alertas falsas.

#### Herramientas y Librerías Utilizadas:

 - **Pandas**: Librería de Python para manipulación y análisis de datos.
  
   <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Pandas_logo.svg/1200px-Pandas_logo.svg.png" width="100">
 

 - **NumPy**: Librería fundamental para computación numérica en Python.
  
   <img src="https://github.com/No-Country/c17-99-t-data-bi/assets/77640142/d411fef5-109c-4731-be2f-8aba77141a2b" width="100">


- **Matplotlib**: Librería fundamental para la generación de gráficos en dos dimensiones.

   <img src="https://github.com/No-Country/c17-99-t-data-bi/assets/77640142/34000e83-3e05-4e2c-9ed2-70cb0412ee3f" width="100">


- **Colaboratory con Python**: Utilizaremos Colaboratory, una plataforma de Google basada en Jupyter Notebooks, junto con las potentes librerías de Python para análisis de datos como Pandas, NumPy y Matplotlib.
  
   <img src="https://colab.research.google.com/img/colab_favicon_256px.png" width="60">

- **Slack**: Plataforma de comunicación para equipos.
  <br>
    <img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" width="100">

- **Python**: Lenguaje de programación utilizado para análisis de datos y desarrollo de aplicaciones.
  <br>
    <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" width="100">

- **Kaggle**: Plataforma de aprendizaje automático y ciencia de datos.
  <br>
        <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" width="100">

- **Discord**: Plataforma de comunicación para comunidades y grupos.
  <br>
    <img src="https://img.shields.io/badge/Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" width="100">

- **Google Meet**: Plataforma de videoconferencia de Google.
  <br>
    <img src="https://img.shields.io/badge/Google%20Meet-32A350?style=for-the-badge&logo=googlemeet&logoColor=white" width="100">

- **GitHub**: Plataforma de desarrollo colaborativo para proyectos de software.
  <br>
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" width="100">

###  Visualización de Resultados:

Para comprender el comportamiento del modelo y los datos, se generaron las siguientes visualizaciones clave:

**Distribución de Clases:**

Un gráfico de barras que muestra la distribución altamente desbalanceada entre transacciones legítimas (clase 0) y fraudulentas (clase 1). Menos del 1% de las transacciones son fraudulentas, lo que resalta la importancia de técnicas como SMOTE para balancear el dataset.

<img src="images\distribucion_clases.png" width="700">

**Matriz de Confusión:**

Una matriz que ilustra los verdaderos positivos, falsos positivos, verdaderos negativos y falsos negativos del modelo. Esto permite evaluar la capacidad del modelo para detectar fraudes sin generar demasiadas alertas falsas.

<img src="images\matriz_confusion.png" width="700">

**Curva ROC-AUC:**

Gráfico que muestra el rendimiento del modelo en términos de sensibilidad y especificidad. El modelo alcanzó un AUC-ROC de 0.99, indicando una excelente capacidad para distinguir entre clases.

<img src="images\roc.png" width="700">

**Importancia de Características:**

Un gráfico de barras que destaca las características más relevantes para el modelo (ej: V17, V14, V12), identificadas mediante el algoritmo ADAG. Esto ayuda a entender qué factores influyen en la detección de fraudes.

<img src="images\caracteristicas.png" width="700">

**Comparación entre Predicciones y Etiquetas Reales:**

<img src="images\comparacion.png" width="700">



###  Conclusión y Recomendaciones:
**Conclusiones:**

 - El modelo de Árboles de Decisión con Aumento por Gradiente (ADAG) demostró un alto rendimiento, con un AUC-ROC de 0.99, lo que indica una capacidad robusta para identificar transacciones fraudulentas.

 - El uso de SMOTE permitió manejar el desbalance de clases, mejorando la detección de fraudes sin sacrificar la precisión general.

 - Las características anonimizadas V17, V14 y V12 fueron las más influyentes en las predicciones, sugiriendo patrones específicos asociados a actividades fraudulentas.

**Recomendaciones:**

 - Optimización de hiperparámetros: Utilizar técnicas como Grid Search para afinar los parámetros del modelo y mejorar métricas como la precisión.

 - Implementación en tiempo real: Integrar el modelo en sistemas de procesamiento de transacciones para alertas inmediatas.

 - Recolección de más datos: Incluir variables adicionales como ubicación geográfica o tipo de comercio para enriquecer el análisis.

###  Contacto:

| Integrantes          | Rol                                     | GitHub                                        | LinkedIn                                                                           |
|----------------------|-----------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------|
| Jorge Adrian Perez   | Project Manager                          | [GitHub](https://github.com/jorgeperez23) | [LinkedIn](https://www.linkedin.com/in/jorge-perez-1b136446)                  |
| Miguel Angel Choque       | Analista de Datos                       | [GitHub](https://github.com/mickychog)       | [LinkedIn](https://www.linkedin.com/in/miguel-choque-garcia/)                                 |
| Bryan Hancco         | Analista de Datos                       | [GitHub](https://)       | [LinkedIn](https://)                                 |
| Micaela Kler         | Analista BI                       | [GitHub](https://)       | [LinkedIn](https://)                                 |
| Joaquin Pereira        | Analista BI                       | [GitHub](https://)       | [LinkedIn](https://)                                 |
| Jorge Adrian Perez  | Data Scientist , Machine Learning      | [GitHub](https://github.com/jorgeperez23) | [LinkedIn](https://www.linkedin.com/in/jorge-perez-1b136446)                     |
