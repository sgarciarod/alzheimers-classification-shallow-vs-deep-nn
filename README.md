# 🧠 Clasificación de Enfermedad de Alzheimer usando Redes Neuronales Shallow vs Deep

## 📌 Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar y comparar modelos basados en **redes neuronales poco profundas (Shallow Neural Networks)** y **redes neuronales profundas (Deep Neural Networks)** para la clasificación binaria de la enfermedad de Alzheimer utilizando datos clínicos tabulares.

El trabajo se realiza en el marco del curso de Redes Neuronales, con énfasis en el análisis del efecto de la profundidad del modelo sobre el desempeño y la capacidad de generalización.

Actualmente, el proyecto se encuentra en la fase de implementación y evaluación de una **Shallow Neural Network** como línea base. Posteriormente, se desarrollará una **Deep Neural Network** para comparar el efecto de la profundidad en el desempeño del modelo.

---

## 👥 Integrantes

- Santiago García Rodriguez
- Maria Paula Carvajal
- Diana Barrero Malagon
- Johan Albarracin Gomez
Curso de Redes Neuronales - Grupo 2 – 2026

---

## 📊 Dataset

Se utiliza el dataset público **“Alzheimer’s Disease Dataset”** disponible en Kaggle
https://www.kaggle.com/datasets/rabieelkharoua/alzheimers-disease-dataset/data 

Características principales:

- Aproximadamente 2.149 muestras
- Alrededor de 34 variables clínicas y demográficas
- Variable objetivo binaria: Alzheimer vs No Alzheimer
- Dataset sintético diseñado para experimentación en aprendizaje automático

⚠️ Nota: El dataset es sintético y no corresponde a una cohorte clínica real.

La implementación de la **Red Neuronal Deep** se desarrollará en una siguiente etapa, con el objetivo de comparar si una mayor profundidad mejora el desempeño del modelo y su capacidad de generalización.

---

## 📈 Resultados actuales - Shallow Neural Network

La red neuronal superficial fue entrenada sobre el dataset clinico y evaluada en un conjunto de prueba independiente. Los resultados obtenidos fueron:

| Métrica | Valor |
|--------|-------|
| Accuracy | **85.14%** |
| Precision | **78.45%** |
| Recall | **79.82%** |
| F1-score | **79.13%** |
| ROC-AUC | **0.9130** |

### Matriz de confusión

| Real / Predicción | No Alzheimer | Alzheimer |
|-------------------|-------------:|----------:|
| **No Alzheimer**  | 184 | 25 |
| **Alzheimer**     | 23  | 91 |

### Interpretación general

- El modelo logró una **buena capacidad de discriminación** entre pacientes con y sin Alzheimer.
- El valor de **ROC-AUC = 0.9130** indica un desempeño sólido para una arquitectura simple.
- El **recall de 79.82%** muestra que el modelo identificó cerca de 4 de cada 5 casos positivos.
- Estos resultados convierten a la **Shallow Neural Network** en una línea base válida para compararla posteriormente con una arquitectura más profunda.

---

## 📚 Comparación con la literatura

Para contextualizar el desempeño de la **Shallow Neural Network**, se compararon los resultados obtenidos con trabajos recientes que utilizaron el mismo dataset tabular de Alzheimer.

| Modelo / Estudio | Accuracy | Observación |
|------------------|----------|-------------|
| **Shallow Neural Network (este proyecto)** | **85.14%** | Línea base neuronal implementada en esta fase |
| **Random Forest - Biswas et al.** | **91.19%** | Modelo clásico optimizado con técnicas adicionales |
| **LightGBM + Random Forest - Mahamud et al.** | **96.35%** | Ensamble con mejor desempeño reportado |

### Interpretación

Los resultados muestran que la **Shallow Neural Network** alcanza un desempeño sólido como modelo base, aunque todavía se encuentra por debajo de enfoques más avanzados reportados en la literatura. Esta diferencia es esperable, ya que los estudios de referencia incorporan estrategias adicionales como optimización de hiperparámetros, balanceo de clases, selección de variables y ensambles.

Por tanto, el principal valor del modelo actual no es superar el estado del arte, sino establecer una **línea base neuronal clara, reproducible y metodológicamente consistente**. Esta base permitirá, en la siguiente etapa del proyecto, implementar una **Deep Neural Network** y evaluar si una mayor profundidad mejora de manera real el desempeño y la capacidad de generalización.

### Referencias

- Biswas et al. *Performance-optimized Alzheimer's detection using machine learning with SMOTE and randomized hyperparameter tuning*.
- Mahamud et al. *Enhancing Alzheimer's disease detection: An explainable machine learning approach with ensemble techniques*.

## 🚀 Trabajo futuro

Las siguientes etapas del proyecto incluyen:

- Implementación de una **Deep Neural Network**
- Comparación Shallow vs Deep bajo las mismas condiciones experimentales
- Análisis del efecto de la profundidad en métricas como **F1-score**, **ROC-AUC** y **recall**
- Evaluación de estabilidad y generalización del modelo
