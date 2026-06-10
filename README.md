# Mini proyecto de Series Temporales y Pronóstico

## Objetivo
Construir un proyecto reproducible de forecasting con skforecast, aplicando un flujo completo de trabajo con
series temporales: comprensión del problema, preparación de datos, modelado, evaluación, ajuste, incorporación
de variables exógenas y comunicación de resultados.

## Dataset
El archivo utilizado es:

*appliances_energy_docente.csv*

El dataset utilizado para elproyecto fue brindado por el profesor. 

### Columnas del dataset:
-***fecha***: Fecha y hora del registro.

-***consumo_electrodomesticos***: Consumo de energía de los electrodomésticos de la vivienda. Es la variable objetivo.

-***temperatura_zona_1***: Temperatura registrada en una zona interior de la vivienda.

-***humedad_zona_1***: Humedad relativa registrada en una zona interior de la vivienda.

-***temperatura_exterior***: Temperatura exterior registrada al momento de la medición.

-***presion_atmosferica***: Presión atmosférica registrada.

-***humedad_exterior***: Humedad relativa exterior.

-***velocidad_viento***: Velocidad del viento.

-***punto_rocio***: Temperatura de punto de rocío, relacionada con la humedad del aire.

## Identifiación del problema
Tema general: consumo eléctrico residencial.

Variable temporal: fecha.

Variable objetivo: consumo_electrodomesticos.

Frecuencia original: cada 10 minutos.

Frecuencia de trabajo: horaria.

Horizonte de predicción: próximas 24 horas.

El problema consiste en predecir el consumo futuro de energía de electrodomésticos a partir de datos históricos registrados en el tiempo.

## Etapas del proyecto
El trabajo se desarrolla en cinco etapas:

**Planteamiento del problema y descripción del dataset**
Se identifica la variable temporal, la variable objetivo, la frecuencia original, la frecuencia de trabajo, el horizonte de predicción y posibles variables exógenas.

**Preparación temporal y análisis exploratorio**
Se convierte la columna de fecha, se ordenan los datos cronológicamente, se define el índice temporal, se trabaja con frecuencia horaria y se analizan patrones iniciales de la serie.

**Modelo base univariante con skforecast**
Se construye un primer modelo utilizando únicamente la historia de la variable objetivo consumo_electrodomesticos.

**Backtesting, métricas y ajuste univariante**
Se evalúa formalmente el modelo univariante respetando el orden temporal. Se aplican métricas de error, backtesting y búsqueda de mejores configuraciones de lags e hiperparámetros.

**Modelo multivariante con variables exógenas, comparación y conclusiones**
Se incorporan variables adicionales del dataset, como temperatura, humedad, presión atmosférica, viento y punto de rocío. Luego se comparan los resultados del modelo multivariante con el modelo univariante.

## Estructura del repositorio
miniproyecto-series-temporales/

├── README.md

├── requirements.txt

├── informe.pdf

├── notebooks/

│   └── Mini_proyecto_AA.ipynb

├── data/

│   ├── raw/

│   │   └── appliances_energy_docente.csv

│   └── processed/

│       └── appliances_energy_horario.csv

└── models/

    └── mejor_modelo.pkl

## Descripción de carpetas y archivos
*README.md*: descripción general del proyecto e instrucciones básicas de ejecución.

*requirements.txt*: listado de librerías necesarias para ejecutar el proyecto.

*informe.pdf*: informe breve con la explicación del problema, metodología, resultados y conclusiones.

*notebooks/*: contiene el notebook principal documentado y ejecutable.

*data/raw/*: contiene el dataset original entregado por el docente.

*data/processed/*: contiene el dataset procesado utilizado para el modelado.

*models/*: contiene el mejor modelo entrenado guardado.

## Integrantes
Pedro De Souza

Gelenn Ferreira

Katerin Gonzalez
