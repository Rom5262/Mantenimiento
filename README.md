⚙️ PREDICCIÓN DE FALLAS: OPTIMIZANDO EL MANTENIMIENTO INDUSTRIAL ⚙️

📝 Descripción del Proyecto
Este proyecto se enfoca en el análisis de datos históricos de mantenimiento para predecir el Tiempo Medio Entre Fallas (TMEF) de activos críticos en una planta industrial. El objetivo principal es reducir el margen de error en la predicción de fallas para optimizar el inventario de refacciones y enfocar los esfuerzos de mantenimiento predictivo en los equipos más volátiles.

El trabajo incluyó preprocesamiento de datos de fecha, cálculo de TMEF por equipo, codificación de variables categóricas, y el desarrollo de un modelo de Machine Learning de Regresión para predecir el número de días hasta la siguiente falla.

🛠️ Tecnologías Utilizadas
Python: Lenguaje principal de análisis.

Pandas: Para manipulación de datos, limpieza de fechas, cálculo de TMEF, y codificación Dummy (equipos).

Scikit-learn: Para la división de datos (Train-Test Split), entrenamiento del modelo Random Forest Regressor y métricas de evaluación.

Matplotlib: Para la visualización de la distribución de fallas (Histograma) y la evaluación del modelo.

Joblib: Para la serialización (guardar) el modelo entrenado para su uso futuro.

🎯 Resultados Clave del Machine Learning
El modelo más robusto y de mejor rendimiento fue el Random Forest Regressor, entrenado para predecir la variable dias_hasta_falla.

Métrica	Resultado	Interpretación
Error Absoluto Medio (MAE)	3.40 días	El modelo se equivoca, en promedio, por solo 3 días y medio al predecir la fecha exacta de la siguiente falla.
Modelo Elegido	Random Forest	Superó la precisión del modelo base (Árbol de Decisión Simple), reduciendo el error de 3.54 a 3.40 días.

Exportar a Hojas de cálculo
🔍 Análisis de Criticidad (Importancia de Variables)
El análisis de la Importancia de Variables revela qué equipos son los más decisivos en el patrón de fallas.

Ranking	Equipo	Importancia en la Predicción
1	Motor Eléctrico	27.33%
2	Compresor	26.15%

Exportar a Hojas de cálculo
Conclusión Estratégica: El Motor Eléctrico y el Compresor causan la mayor variación en los tiempos de falla y, por lo tanto, la inversión en sensores, monitoreo o mantenimiento predictivo debe enfocarse principalmente en estos dos activos para tener el mayor impacto en la estabilidad de la operación.

📈 Conclusión de Distribución de Fallas (Histograma)
El análisis de la distribución de fallas reveló un patrón bimodal (dos picos), lo cual es crucial para la gestión de riesgos.

Patrón	Periodo de Falla	Significado Operacional
Pico de Mayor Riesgo	15 - 20 días	La tercera semana después del último mantenimiento es el periodo donde ocurre la mayor cantidad de fallas. Se requiere máxima atención en esta ventana.

Exportar a Hojas de cálculo
💾 Modelo Final Guardado
El modelo entrenado está serializado para su implementación y uso futuro sin requerir re-entrenamiento:

Nombre del Archivo: modelo_random_forest_TMEF.joblib

Herramienta: joblib

