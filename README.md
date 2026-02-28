# Redes Neuronales: Poco Profundas vs. Profundas

Repositorio de notebooks de Python como software demostrativo para una tarea académica sobre redes neuronales poco profundas (*shallow*) y profundas (*deep neural networks*).

## Descripción

Este proyecto explora y compara diferentes arquitecturas de redes neuronales, desde modelos clásicos y poco profundos hasta arquitecturas profundas modernas. Cada notebook es autocontenido y puede ejecutarse de forma independiente.

## Estructura del repositorio

```
notebooks/
├── 03_autoencoders.ipynb   # Introducción a los Autoencoders
└── 04_alexnet.ipynb        # Arquitectura AlexNet
```

## Notebooks

### 03 — Introducción a los Autoencoders
**Archivo:** `notebooks/03_autoencoders.ipynb`

Explora los autoencoders, una familia de redes neuronales no supervisadas que aprenden representaciones comprimidas de los datos.

Contenido:
- Introducción teórica: arquitectura encoder–espacio latente–decoder, tipos (vanilla, sparse, denoising, VAE)
- Implementación desde cero con PyTorch sobre MNIST
- Ejemplo 1: Autoencoder vanilla — reconstrucción de dígitos y visualización del espacio latente 2D
- Ejemplo 2: Denoising Autoencoder — eliminación de ruido gaussiano
- Ejemplo 3: Reducción de dimensionalidad — Autoencoder vs. PCA en 2D
- Ejemplo 4: Detección de anomalías — errores de reconstrucción para datos normales vs. anómalos

### 04 — AlexNet
**Archivo:** `notebooks/04_alexnet.ipynb`

Explora AlexNet, la arquitectura convolucional profunda que marcó el inicio de la revolución del deep learning en 2012.

Contenido:
- Introducción teórica: historia, innovaciones (ReLU, LRN, dropout, overlapping pooling), arquitectura capa a capa
- Implementación de AlexNet con PyTorch adaptada para CIFAR-10
- Ejemplo 1: Entrenamiento en CIFAR-10 — curvas de pérdida/accuracy y matriz de confusión
- Ejemplo 2: Transfer Learning — AlexNet pre-entrenado en ImageNet aplicado a CIFAR-10
- Ejemplo 3: Visualización de características — filtros y mapas de activación de cada capa
- Ejemplo 4: Comparación con arquitecturas simples (MLP, CNN de 2 capas)

## Instalación de dependencias

```bash
pip install -r requirements.txt
```

## Ejecución

```bash
jupyter notebook
```

Luego abre el notebook deseado desde la interfaz de Jupyter en tu navegador.

> **Nota:** Se recomienda usar GPU para acelerar el entrenamiento, aunque todos los notebooks funcionan también en CPU.

## Dependencias principales

- Python ≥ 3.8
- PyTorch + torchvision
- NumPy, Matplotlib, scikit-learn
- Jupyter

## Referencias principales

- Rumelhart, D. E., Hinton, G. E., & Williams, R. J. (1986). *Learning representations by back-propagating errors.* Nature, 323(6088), 533–536.
- Hinton, G. E., & Salakhutdinov, R. R. (2006). *Reducing the Dimensionality of Data with Neural Networks.* Science, 313(5786), 504–507.
- Krizhevsky, A., Sutskever, I., & Hinton, G. E. (2012). *ImageNet Classification with Deep Convolutional Neural Networks.* NeurIPS, 25.
- Goodfellow, I., Bengio, Y., & Courville, A. (2016). *Deep Learning.* MIT Press.