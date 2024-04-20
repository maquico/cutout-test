# Convolutional Neural Networks (CNN) with Cutout

Este proyecto implementa la técnica de regularización conocida como Cutout en redes neuronales convolucionales utilizando el conjunto de datos CIFAR-100 y la arquitectura ResNet18. La técnica de Cutout consiste en recortar regiones aleatorias de las imágenes durante el entrenamiento para mejorar la generalización y mitigar el sobreajuste en el modelo.

## Authors

- [Gleidy Espinal](https://github.com/GleidyEspinal)
- [Angel Moreno](https://github.com/maquico)
- [Allen Silverio](https://github.com/Allensilverio)
- [Rolbik Urbáez](https://github.com/Wolbik)
- [Huan Hao Wu Wu](https://github.com/huanhaowu)


## Installation


## Installation

Instalar Poetry para gestionar las dependencias del proyecto de manera eficiente.

```bash
  pip install poetry
```

Activar el entorno virtual creado por Poetry para aislar las dependencias del proyecto.

```bash
  poetry shell
```
Instalar las dependencias del proyecto especificadas en el archivo pyproject.toml.

```bash
  poetry install
```
Crear la carpeta 'data' en el directorio raíz del proyecto. Esta carpeta se utilizará para almacenar los datos del conjunto de datos CIFAR-100 y cualquier otro dato necesario para el entrenamiento.

```bash
  mkdir data
```

**Entrenar el modelo utilizando la técnica de Cutout.**
```bash
  python train.py --dataset cifar100 --model resnet18 --data_augmentation --cutout --length 8
```
Este comando inicia el entrenamiento del modelo ResNet18 utilizando el conjunto de datos CIFAR-100 y aplicando la técnica de regularización Cutout con una longitud de 8, lo que recorta regiones aleatorias de las imágenes para mejorar la generalización y evitar el sobreajuste.

**Entrenar el modelo sin aplicar la técnica de Cutout.**
```bash
  python train.py --dataset cifar100 --model resnet18 --data_augmentation --length 8
```
Este comando entrena el modelo ResNet18 sin aplicar la técnica de Cutout en el conjunto de datos CIFAR-100. Es útil para comparar el rendimiento del modelo con y sin la técnica de regularización Cutout.

  

## Acknowledgements

Este proyecto se basa en el paper "Improved Regularization of Convolutional Neural Networks with Cutout" y utiliza la implementación de Cutout proporcionada por los autores del paper. Agradecemos a los autores por su contribución a la comunidad de aprendizaje automático.

  
