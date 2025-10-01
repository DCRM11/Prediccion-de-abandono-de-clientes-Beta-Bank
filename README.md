🏦 Predicción de abandono de clientes – Beta Bank
📌 Propósito del proyecto
Desarrollar un modelo predictivo que permita identificar clientes en riesgo de abandonar el banco, optimizando la retención mediante el análisis de comportamiento histórico y métricas de clasificación como F1-score y AUC-ROC.
📝 Descripción
Los clientes de Beta Bank están abandonando la entidad progresivamente. Dado que retener clientes existentes es más rentable que adquirir nuevos, se requiere un modelo que anticipe el abandono. El proyecto utiliza datos históricos de comportamiento y contratos para entrenar modelos de clasificación, con el objetivo de alcanzar un F1-score mínimo de 0.59 y evaluar la métrica AUC-ROC como complemento.
💻 Funcionalidades
📥 Preparación de datos
• 	Limpieza del conjunto de datos.
• 	Codificación de variables categóricas (Geography, Gender).
• 	Ajuste de formatos y tipos de datos.
⚖️ Análisis de desequilibrio
• 	Identificación de desbalance en la variable objetivo  (≈80% permanecen, ≈20% abandonan).
• 	Evaluación de un modelo base sin corrección de clases.
🤖 Entrenamiento de modelos
• 	Aplicación de  en Random Forest, Decision Tree y Logistic Regression.
• 	Ajuste de hiperparámetros (, , ) en Random Forest.
• 	Comparación de rendimiento entre modelos.
📈 Evaluación de métricas
• 	F1-score por clase ().
• 	AUC-ROC para evaluar capacidad de discriminación.
• 	Comparación entre ambas métricas para validar robustez del modelo.
🔧 Herramientas utilizadas
• 	Python
• 	Pandas
• 	Scikit-learn
• 	Matplotlib
📊 Resultados
• 	Modelo base (sin corrección):
• 	F1-score para : 0.28
• 	Alta precisión para clase mayoritaria, bajo recall para clase minoritaria.
• 	Modelos corregidos:
• 	Regresión Logística: F1 = 0.50
• 	Árbol de Decisión: F1 = 0.47
• 	Bosque Aleatorio: F1 = 0.55 (mejor balance)
• 	Modelo final (Random Forest ajustado):
• 	F1-score para : 0.63
• 	AUC-ROC: 0.8656
• 	Buen balance entre precisión y recall, con capacidad de clasificación sólida.
✅ Conclusiones
El modelo final basado en Random Forest con hiperparámetros ajustados logró superar el umbral mínimo de F1-score (≥ 0.59), alcanzando un valor de 0.63. La métrica AUC-ROC de 0.8656 confirma su capacidad de discriminación entre clientes que permanecen y los que abandonan. Este modelo representa una herramienta útil para la retención estratégica de clientes en el sector bancario.
