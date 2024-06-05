# Mejora de la calidad de imágenes de tumores cerebrales mediante GANs
## Introducción
La calidad de las imágenes en el ámbito médico es crucial para el diagnóstico, tratamiento y seguimiento de diversas enfermedades. En particular, la mejora de la calidad de las imágenes de resonancia magnética (MRI) de tumores cerebrales puede aumentar significativamente la precisión del diagnóstico y la eficacia del tratamiento. Este proyecto se centra en la aplicación de Redes Generativas Adversariales (GANs) para mejorar la resolución y calidad de estas imágenes médicas.
## Objetivo
El objetivo principal de este proyecto es desarrollar un modelo basado en GANs, específicamente una Super Resolution Generative Adversarial Network (SRGAN), que mejore la calidad de las imágenes de MRI de tumores cerebrales. Esto permitirá a los profesionales de la salud obtener imágenes más claras y detalladas, facilitando una mejor identificación y caracterización de las anomalías anatómicas y patológicas.
## Metodología
1.	**Dataset:** Utilizamos un conjunto de datos de imágenes de MRI de tumores cerebrales.
2.	**Preprocesamiento de Datos:** Las imágenes se normalizan y se escalan para adecuarlas al modelo.
3.	**Implementación del Modelo:** Se implementa una SRGAN, que incluye un generador y un discriminador.
4.	**Entrenamiento:** El modelo se entrena utilizando imágenes de baja resolución y sus correspondientes de alta resolución.
5.	**Evaluación:** Se evalúan las imágenes generadas mediante métricas como SSIM (Structural Similarity Index) y PSNR (Peak Signal-to-Noise Ratio).
## Arquitectura del Modelo
### Generador SRGAN
Para el generador de la SRGAN, se utilizan boques residuales utilizando la librería de Keras para aprender representaciones más profundas de las imágenes de baja resolución y de convolución para aumentar su tamaño y generar imágenes de alta resolución. Para los bloques residuales se utiliza la función de ‘residual_block’ que consiste en dos capas convolucionales seguidas de activaciones ReLU y normalización por lotes. El resultado de la segunda convolución se suma con la entrada original. Para la deconvolución, se utiliza la función ‘deconv2d’ que sirve para aumentar el tamaño de la imagen. 
### Discriminador SRGAN
El discriminador de este modelo utiliza capas convolucionales para procesar la imagen de entrada y finaliza con una capa densa que produce una salida de probabilidad.
## Resultados
El modelo SRGAN entrenado ha demostrado una mejora significativa en la calidad de las imágenes de resonancia magnética. Las imágenes generadas por el modelo presentan detalles más nítidos y claros en comparación con las imágenes de baja resolución originales. A través de un análisis visual, se observa una notable diferencia en la definición y claridad de las estructuras anatómicas, lo que refleja una mejora en la fidelidad y la resolución de las imágenes reconstruidas. A continuación, se presentan ejemplos visuales que demuestran la diferencia entre las imágenes de baja resolución y las imágenes de alta resolución generadas por nuestro modelo.

![image](https://github.com/alexxmartinezz/SRGAN_for_MRI/assets/106313490/e86366ba-57dd-47a8-a0de-53f0dac1c593)  ![image](https://github.com/alexxmartinezz/SRGAN_for_MRI/assets/106313490/d7ef103a-a98a-464e-83f6-916dca0d6c84)
## Conclusión
El uso de SRGANs para la mejora de la calidad de las imágenes de MRI de tumores cerebrales demuestra un gran potencial. Este enfoque no solo mejora la visualización de las estructuras anatómicas, sino que también puede influir positivamente en la precisión del diagnóstico y en las decisiones de tratamiento.
