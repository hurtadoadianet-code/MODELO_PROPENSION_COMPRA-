# MODELO_PROPENSION_COMPRA CON AGENTE IA
Modelo de Machine Learning para predecir la propensión de compra de clientes, con integración de un agente de IA conversacional para consultas dinámicas en tiempo real.
Este proyecto desarrolla un ecosistema analítico completo para predecir la probabilidad de compra de los clientes. El flujo abarca desde el tratamiento de datos y modelado predictivo avanzado hasta la implementación de un agente de IA conversacional para facilitar la toma de decisiones basada en datos.

**Estructura del Proyecto**
El repositorio se organiza de la siguiente manera:

data/: Contiene el dataset utilizado para el entrenamiento y validación del modelo. Incluye variables demográficas y transaccionales.  

notebook/: Contiene el archivo .ipynb con el desarrollo completo de la solución, incluyendo el análisis estadístico, el entrenamiento de los modelos y la lógica del agente.  
**Contenido del Desarrollo**
**1. Análisis Exploratorio de Datos (EDA)**
Realizamos una inmersión profunda en los datos para identificar patrones de comportamiento.

Análisis Multivariado: Uso de matrices de histogramas y gráficos de violín para entender la distribución de variables como edad e ingreso anual.  

Segmentación Cualitativa: Visualización de la composición de la cartera por género, ocupación y nivel educativo con métricas de conversión porcentual.  

Detección de Leakage: Identificación proactiva de fuga de datos en variables con correlaciones extremas (como id_marca y cantidad) para asegurar la validez del modelo.  

**2. Metodología y Procesamiento**
Limpieza Estricta: Eliminación de ruidos y variables redundantes para optimizar la generalización.

Feature Engineering: Creación de variables dinámicas como precios y promociones específicas por visita y ratios de asequibilidad (price_income_ratio).  

Tratamiento de Nulos: Aplicación de imputación por mediana para garantizar la estabilidad de los algoritmos lineales y de ensamble.  

**3. Modelado Predictivo y Explicabilidad**
Se implementó un enfoque de competencia de modelos para seleccionar la mejor arquitectura:

Modelos Evaluados: Regresión Logística (Línea base), Random Forest y XGBoost.  

Métrica de Éxito: Selección basada en el AUC-ROC para maximizar la capacidad de discriminación entre compradores y no compradores.  

Explicabilidad (SHAP): Uso de valores SHAP para romper la "caja negra" del modelo, permitiendo entender qué factores (como promociones o frecuencia) impulsan realmente la propensión.  

**4. Agente de IA Conversacional**
Integración de un agente basado en LLMs que actúa como interfaz entre el modelo y el usuario de negocio.

Consultas en Lenguaje Natural: Permite filtrar predicciones y consultar estadísticas del modelo sin necesidad de escribir código.

Filtros Dinámicos: Capacidad de realizar segmentaciones en tiempo real sobre los resultados de propensión.

Tecnologías Utilizadas
Lenguaje: Python.

Análisis: Pandas, NumPy.

Visualización: Matplotlib, Seaborn.

Machine Learning: Scikit-learn, XGBoost.

Interpretabilidad: SHAP.  

IA Generativa: LangChain / OpenAI (según implementación del agente).
