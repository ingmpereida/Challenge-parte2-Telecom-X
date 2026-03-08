# 📊 Telecom X – Predicción de Cancelación (Churn) - Parte 2

![Status](https://img.shields.io/badge/Status-Finalizado-success)
![Data](https://img.shields.io/badge/Data-Telecom_X-blue)
![MIA](https://img.shields.io/badge/Desarrollado_por-MIA._C%C3%A9sar_Geovanni_Machuca_Pereida-orange)

## 🎯 Propósito del Análisis
El objetivo principal de este proyecto es construir un pipeline de Machine Learning capaz de **predecir la cancelación (churn)** de clientes en la empresa Telecom X. Al identificar a los clientes con alta probabilidad de abandono basándose en sus características financieras, demográficas y de servicio, la empresa puede implementar estrategias de retención proactivas y optimizar sus recursos.

---

## 📂 Estructura del Proyecto
* `TelecomX_parte2_LATAM_2.ipynb`: Cuaderno principal con el flujo completo (EDA, Preprocesamiento y Modelado).
* `datos_tratados.csv`: Conjunto de datos final tras la limpieza, codificación e ingeniería de variables.
* `visualizaciones/`: Carpeta que contiene los gráficos de importancia de variables, matrices de confusión y análisis de correlación (generados durante la ejecución).

---

## 🧠 Preparación de los Datos
El proceso de preparación fue diseñado siguiendo los estándares de rigor técnico para asegurar la generalización de los modelos:

### 1. Clasificación de Variables
* **Numéricas Continuas:** `tenure`, `MonthlyCharges`, `TotalCharges`.
* **Categóricas:** `gender`, `Partner`, `Dependents`, `InternetService`, `Contract`, `PaymentMethod`, entre otras.

### 2. Ingeniería y Transformación
* **Codificación:** Se aplicó *One-Hot Encoding* a las variables categóricas para transformarlas en formato numérico compatible con los algoritmos.
* **Normalización:** Se utilizó `StandardScaler` para las variables numéricas en modelos sensibles a la escala (como Regresión Logística), garantizando que variables de gran magnitud no sesguen el aprendizaje.
* **Tratamiento de Desbalance:** Dado que la clase de cancelación representaba solo el 26.5%, se aplicó **SMOTE** en el conjunto de entrenamiento para equilibrar las clases sintéticamente.

### 3. División del Dataset
Se realizó una separación estratificada (**Stratified Split**) del **75% para entrenamiento** y **25% para prueba**, asegurando que la proporción de cancelaciones se mantenga constante en ambos grupos para una evaluación justa.

---

## 📈 Insights y Visualizaciones Clave (EDA)
Durante el análisis, se obtuvieron hallazgos críticos:
* **El Factor Contrato:** Los clientes con contratos "Mes a Mes" tienen una correlación positiva de 0.40 con la cancelación.
* **Antigüedad:** La mediana de antigüedad de quienes cancelan es de solo 10 meses, frente a 38 meses de los clientes leales.
* **Fibra Óptica:** Es el servicio con mayor tasa de deserción, sugiriendo un punto de fricción en la experiencia del usuario o precio.

---

## ⚙️ Instrucciones de Ejecución

### Requisitos Previos
Es necesario contar con Python 3.8+ y las siguientes bibliotecas instaladas:
```bash
pip install pandas numpy scikit-learn seaborn matplotlib imbalanced-learn
