# Redes Neuronales Poco Profundas (Shallow Neural Networks)

## Descripción

Este repositorio contiene notebooks de Python como software demostrativo para una tarea académica sobre **redes neuronales poco profundas (shallow neural networks)**. Se implementan y analizan dos modelos clásicos:

1. **Perceptrón Simple de Rosenblatt** (1958)
2. **ADALINE – Adaptive Linear Neuron** (Widrow & Hoff, 1960)

Cada notebook incluye introducción teórica, implementación desde cero (sin scikit-learn para el modelo), ejemplos prácticos con el dataset Iris y compuertas lógicas, visualizaciones con matplotlib y referencias bibliográficas.

---

## Estructura del repositorio

```
alzheimers-classification-shallow-vs-deep-nn/
├── notebooks/
│   ├── 01_perceptron_simple_rosenblatt.ipynb   # Perceptrón de Rosenblatt
│   └── 02_adaline.ipynb                         # ADALINE (GD y SGD)
├── README.md
└── requirements.txt
```

---

## Instalación de dependencias

Se recomienda usar un entorno virtual de Python (3.8+):

```bash
# Crear entorno virtual (opcional)
python -m venv venv
source venv/bin/activate        # Linux/macOS
# venv\Scripts\activate         # Windows

# Instalar dependencias
pip install -r requirements.txt
```

---

## Ejecución de los notebooks

```bash
# Iniciar Jupyter Notebook
jupyter notebook

# O Jupyter Lab
jupyter lab
```

Luego, abrir la carpeta `notebooks/` en la interfaz web y ejecutar los notebooks en orden.

---

## Descripción de cada notebook

### `01_perceptron_simple_rosenblatt.ipynb`

- **Introducción teórica**: Historia del Perceptrón (Rosenblatt, 1958), modelo matemático (`z = w·x + b`, función escalón), regla de aprendizaje (`w = w + η(y - ŷ)x`) y limitaciones (Minsky & Papert, 1969).
- **Implementación**: Clase `Perceptron` con métodos `fit()` y `predict()`.
- **Ejemplo 1**: Dataset Iris (clasificación binaria Setosa vs Versicolor), curva de convergencia y frontera de decisión.
- **Ejemplo 2**: Compuertas lógicas AND y OR (el perceptrón las resuelve).
- **Ejemplo 3**: Compuerta XOR (el perceptrón **no** puede resolverla — no es linealmente separable).

### `02_adaline.ipynb`

- **Introducción teórica**: Historia de ADALINE (Widrow & Hoff, 1960), regla Delta/LMS (`w = w + η(y - z)x`), descenso de gradiente y función de costo MSE.
- **Implementación**: Clases `AdalineGD` (batch gradient descent) y `AdalineSGD` (stochastic gradient descent).
- **Ejemplo 1**: Dataset Iris con distintos learning rates (η = 0.1, 0.01, 0.0001) — divergencia vs convergencia lenta.
- **Ejemplo 2**: Efecto de la estandarización de features con `StandardScaler`.
- **Ejemplo 3**: Comparación entre Batch GD y SGD.
- **Ejemplo 4**: Tabla y gráfico comparativo entre Perceptrón y ADALINE.

---

## Referencias principales

- Rosenblatt, F. (1958). *The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain*. Psychological Review, 65(6), 386–408.
- Widrow, B., & Hoff, M. E. (1960). *Adaptive Switching Circuits*. IRE WESCON Convention Record, Part 4, 96–104.
- Minsky, M., & Papert, S. (1969). *Perceptrons: An Introduction to Computational Geometry*. MIT Press.
- Haykin, S. (2009). *Neural Networks and Learning Machines*. 3rd ed., Pearson.
- Raschka, S. (2015). *Python Machine Learning*. Packt Publishing.
- Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*. Springer.