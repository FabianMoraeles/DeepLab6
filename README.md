# DeepLab6: Transfer Learning y Fine-Tuning

Laboratorio 6 de CC3092 Deep Learning y Sistemas Inteligentes, Universidad del Valle de Guatemala. Fabián Morales.

Se comparan tres estrategias para clasificar CIFAR-10: una CNN entrenada desde cero, VGG-16 preentrenada como feature extractor y VGG-16 con fine-tuning de sus bloques superiores, midiendo desempeño y costo computacional.

## Contenido

- Lab6.ipynb: notebook completo y ejecutado con exploración de datos, investigación, definición de los modelos, 14 iteraciones de entrenamiento, medición de recursos, experimento con 10 % de los datos, evaluación final sobre test y discusión.
- figuras: gráficas generadas por el notebook.
- resultados: métricas de cada iteración en JSON, tabla comparativa en CSV y registro del entrenamiento.

## Resultados en test

| Modelo | Accuracy | F1 macro | F1 con 10 % de datos | GFLOPs por imagen |
|---|---|---|---|---|
| CNN desde cero | 0.9292 | 0.9291 | 0.7253 | 0.42 |
| VGG-16 feature extractor | 0.8953 | 0.8952 | 0.8407 | 30.93 |
| VGG-16 fine-tuning | 0.9420 | 0.9419 | 0.8850 | 30.93 |

## Reproducir

Crear un entorno con Python 3.14, instalar las dependencias con pip install -r requirements.txt y ejecutar el notebook de principio a fin. CIFAR-10 y los pesos de VGG-16 se descargan automáticamente. En una GPU NVIDIA GeForce RTX 5070 Ti la ejecución completa toma alrededor de 80 minutos.
