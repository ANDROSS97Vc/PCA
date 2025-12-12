Evaluación Experimental de un Modelo de Regresión Logística con Preprocesamiento Avanzado, Balanceo SMOTE y Reducción Dimensional (PCA)

Este documento describe un proceso experimental orientado a evaluar el desempeño de un modelo de Regresión Logística aplicado a un conjunto de datos biomédicos. El enfoque integra técnicas de preprocesamiento avanzado, balanceo de clases, reducción de dimensionalidad y validación repetida con múltiples configuraciones, con el objetivo de determinar la estabilidad y efectividad del modelo bajo diferentes escenarios.

Objetivo del Estudio

El propósito central es analizar cómo varían las métricas de desempeño del modelo al modificar:

El número de componentes principales utilizados en la etapa de reducción dimensional.

La semilla aleatoria empleada en la división de datos, el algoritmo SMOTE y el PCA.

La combinación de ambas variables permite evaluar la robustez del modelo, la sensibilidad a cambios estructurales en el conjunto de entrenamiento y la contribución del preprocesamiento al desempeño final.

Proceso de Preprocesamiento

El flujo de preprocesamiento aplicado al conjunto de datos incluye varios pasos orientados a corregir inconsistencias, reducir valores extremos y estandarizar la información:

Hard Clipping:
Los valores de las variables numéricas principales (edad, altura, peso y presiones arteriales) se limitan dentro de un rango clínicamente razonable para eliminar valores distorsionados o físicamente imposibles.

Imputación de valores faltantes:
Se reemplazan los valores ausentes mediante media (en el caso de variables numéricas) o moda (en variables categóricas).

Winsorización:
Se ajustan los valores extremos mediante el recorte de los percentiles inferiores y superiores, reduciendo el impacto de observaciones atípicas sin eliminarlas.

Estandarización:
Las características numéricas se normalizan para garantizar escalas comparables durante el proceso de aprendizaje.

Corrección del desbalanceo:
Se aplica el método SMOTE para generar nuevas muestras sintéticas de la clase minoritaria, equilibrando así la distribución de las clases.
