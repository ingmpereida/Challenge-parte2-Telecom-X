# **Predicción de Churn – Telecom X**

Misión: Desarrollar un pipeline de Machine Learning capaz de anticipar la cancelación de clientes para la empresa Telecom X.

Este proyecto aborda el fenómeno del Churn (fuga de clientes) utilizando técnicas avanzadas de procesamiento de datos y modelos predictivos, permitiendo a la empresa pasar de una postura reactiva a una estrategia de retención proactiva.

**Estructura del Proyecto**
El desarrollo se divide en tres etapas críticas:

**1. Preparación y Feature Engineering**

* Limpieza: Eliminación de identificadores irrelevantes para evitar el sobreajuste.
* Codificación: Transformación de variables categóricas mediante One-Hot Encoding.
* Tratamiento de Desbalance: Aplicación de SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar la clase minoritaria (clientes que cancelan).
* Escalado: Estandarización de variables numéricas (StandardScaler) para modelos sensibles a la magnitud.

**2. Modelado Predictivo**

Se evaluaron y contrastaron dos arquitecturas distintas:

* Regresión Logística: Seleccionada por su robustez y alto Recall (80%), permitiendo identificar a la gran mayoría de clientes en riesgo.
* Random Forest: Utilizado para capturar relaciones no lineales, aunque presentó una tendencia al overfitting que requiere una poda de hiperparámetros.

**3. Análisis de Importancia de Variables**

Se identificaron los "Drivers" clave del negocio:

* Contrato Mes a Mes: El principal indicador de riesgo.
* Antigüedad (Tenure): El factor de lealtad más fuerte; el riesgo cae drásticamente tras los 38 meses.
* Fibra Óptica: Segmento tecnológico con mayor tasa de deserción, identificado como punto de mejora operativa.

**Tecnologías Utilizadas**
* Lenguaje: Python 3.x
* Entorno: Google Colab / Jupyter Notebook
* Bibliotecas Clave:
* Pandas & NumPy: Manipulación de datos.
* Scikit-Learn: Modelado y preprocesamiento.
* Imbalanced-learn: Balanceo de clases (SMOTE).
* Matplotlib & Seaborn: Visualización estadística.

**Resultados y Conclusiones**
El modelo final (Regresión Logística) alcanzó un F1-Score del 62% y un Recall del 80% en el conjunto de prueba.

**Estrategias de Retención Recomendadas:**
* Incentivos de Contrato: Migrar clientes de planes mensuales a anuales.
* Onboarding Crítico: Campañas de soporte intensivo durante los primeros 12 meses.
* Auditoría de Fibra: Revisar la propuesta de valor del servicio de fibra óptica debido a su alta correlación con el churn.

**Contenido del Repositorio**
* TelecomX_parte2_LATAM_2.ipynb: Notebook principal con el desarrollo del pipeline.
* datos_tratados.csv: Dataset procesado y listo para entrenamiento.
* README.md: Descripción del proyecto (este archivo).


Desarrollado por: MIA. César Geovanni Machuca Pereida

Fecha: Marzo 2026
