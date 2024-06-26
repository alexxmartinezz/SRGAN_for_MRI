# Improving the Quality of Brain Tumor Images Using GANs
## Introduction
The quality of images in the medical field is crucial for the diagnosis, treatment, and monitoring of various diseases. Specifically, enhancing the quality of MRI images of brain tumors can significantly increase diagnostic accuracy and treatment efficacy. This project focuses on the application of Generative Adversarial Networks (GANs) to improve the resolution and quality of these medical images.

## Objective
The primary objective of this project is to develop a GAN-based model, specifically a Super Resolution Generative Adversarial Network (SRGAN), to enhance the quality of MRI images of brain tumors. This will enable healthcare professionals to obtain clearer and more detailed images, facilitating better identification and characterization of anatomical and pathological anomalies.

## Methodology
  1. **Dataset:** We use a dataset of MRI images of brain tumors. Available at: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset
  2. **Data Preprocessing:** Images are normalized and scaled to fit the model.
  3. **Model Implementation:** An SRGAN is implemented, which includes a generator and a discriminator.
  4. **Training:** The model is trained using low-resolution images and their corresponding high-resolution images.
  5. **Evaluation:** The generated images are evaluated using metrics such as SSIM (Structural Similarity Index) and PSNR (Peak Signal-to-Noise Ratio).
## Model Architecture
### SRGAN Generator
For the SRGAN generator, residual blocks are used with the Keras library to learn deeper representations of low-resolution images and convolution to upscale and generate high-resolution images. The 'residual_block' function, consisting of two convolutional layers followed by ReLU activations and batch normalization, is used for residual blocks. The output of the second convolution is added to the original input. The 'deconv2d' function is used for deconvolution to increase image size.

### SRGAN Discriminator
The discriminator in this model uses convolutional layers to process the input image and ends with a dense layer that produces a probability output.

## Results
The trained SRGAN model has shown a significant improvement in the quality of MRI images. The images generated by the model exhibit sharper and clearer details compared to the original low-resolution images. A visual analysis reveals a notable difference in the definition and clarity of anatomical structures, reflecting an improvement in the fidelity and resolution of the reconstructed images. Below are visual examples demonstrating the difference between the low-resolution images and the high-resolution images generated by our model.
![image](https://github.com/alexxmartinezz/SRGAN_for_MRI/assets/106313490/e86366ba-57dd-47a8-a0de-53f0dac1c593)  ![image](https://github.com/alexxmartinezz/SRGAN_for_MRI/assets/106313490/d7ef103a-a98a-464e-83f6-916dca0d6c84)
 

## Conclusion
The use of SRGANs to enhance the quality of MRI images of brain tumors demonstrates great potential. This approach not only improves the visualization of anatomical structures but can also positively influence diagnostic accuracy and treatment decisions.
