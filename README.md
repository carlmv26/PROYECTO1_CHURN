# Predicción de Abandono de Clientes (Churn Prediction) usando Machine Learning

## 🎯 Objetivo
Desarrollar modelos de machine learning para predecir el abandono de clientes en una empresa de telecomunicaciones, identificando 
los factores clave que influyen en el churn y proponiendo estrategias de retención.

## 📊 Dataset
Telco Customer Churn Dataset

Variables: demográficas, servicios contratados, facturación y comportamiento del cliente

## 🔍 Análisis Exploratorio (EDA)- Balance del dataset
  El dataset presenta desbalance:

    ~73% clientes que no abandonan
    ~27% clientes que sí abandonan


- Hallazgos clave

  * Clientes con contrato mensual presentan mayor churn
  * Clientes con Fiber Optic tienen mayor tasa de abandono
  * Electronic check está altamente asociado al churn
  * El género no influye significativamente

- Variables numéricas

  * Tenure: clientes nuevos abandonan más
  * MonthlyCharges: mayor costo → mayor churn
  * TotalCharges: fuerte relación con permanencia

## ⚙️ Preprocesamiento

  - Eliminación de variables irrelevantes (customerID)
  - Conversión de variables categóricas (One-Hot Encoding)
  - Escalado de variables numéricas
  - División en train/test (80/20)

## 🤖 Modelos Utilizados

  - Regresión Logística (baseline)
  - Random Forest

## 📈 Evaluación de Modelos

- Regresión Logística
  * Buen balance general
  * Mejor recall para detectar churn

- Random Forest
  * Mejor desempeño en clase mayoritaria
  * Más conservador en predicción de churn

- Comparación clave
  * La Regresión Logística tuvo mejor recall
  * En problemas de churn, el recall es más importante que accuracy

## ⚠️ Importancia del Recall
El error más costoso es el falso negativo:

  - Cliente que se va y no fue detectado
  - Impacto directo en ingresos

## 📊 Interpretación del Modelo
Variables más importantes:

  * TotalCharges
  * MonthlyCharges
  * Tenure
  * Tipo de servicio (Fiber Optic)
  * Método de pago (Electronic Check)

## 🧠 Insights de Negocio

  - Clientes nuevos son más propensos a abandonar
  - Clientes con altos costos mensuales presentan mayor riesgo
  - Métodos de pago automáticos reducen churn
  - Contratos largos aumentan la retención

## 💡 Recomendaciones

  * Incentivar contratos a largo plazo
  * Implementar estrategias de retención en clientes nuevos
  * Promover pagos automáticos
  * Revisar la calidad/precio del servicio Fiber Optic

## 🚀 Tecnologías utilizadas

  - Python
  - Pandas, NumPy
  - Scikit-learn
  - Matplotlib, Seaborn


