# 🧼 CIFAR-10 Image Denoising with Convolutional Autoencoder

> A deep learning mini-project to clean noisy images using an unsupervised learning approach on the CIFAR-10 dataset.

---

## 📌 Table of Contents
- [🎯 Problem Statement](#-problem-statement)
- [📊 Dataset](#-dataset)
- [🧠 Project Explanation](#-project-explanation)


---

## 🎯 Problem Statement

In real-world scenarios like medical imaging, satellite analysis, or security footage, images often come with **unwanted noise** that reduces clarity and effectiveness.

This project aims to:
> Build a **Convolutional Autoencoder** model that learns to **denoise images from the CIFAR-10 dataset**, reconstructing clear images from their noisy counterparts.

---

## 📊 Dataset

We use the **CIFAR-10** dataset, which consists of:
- 60,000 32x32 color images in 10 different classes
- 50,000 for training and 10,000 for testing

📂 Dataset Source:  
[CIFAR-10 Official Site](https://www.cs.toronto.edu/~kriz/cifar.html)  
✅ You can load it using:
```python
from keras.datasets import cifar10


🧠 Project Explanation
This project demonstrates how to use a Convolutional Autoencoder (CAE) to denoise images from the CIFAR-10 dataset. The key idea is to train a deep learning model to remove noise from images using an unsupervised learning approach.

🔍 What Is an Autoencoder?
An autoencoder is a type of neural network that learns to compress input data into a lower-dimensional representation and then reconstruct it back. It has two main parts:

Encoder: Compresses the input image into a smaller, latent representation.

Decoder: Reconstructs the original image from the compressed representation.

📸 Why Denoising?
In many real-world applications (e.g., medical imaging, satellite photos, security footage), images often contain unwanted noise due to various factors like sensor quality or environmental interference. Removing this noise improves image clarity and reliability for further analysis.

🧪 Project Steps
Add Noise to CIFAR-10 Images
To simulate real-world conditions, artificial noise (such as Gaussian noise) is added to the clean CIFAR-10 images. These noisy images will serve as inputs for the autoencoder.

Build the Convolutional Autoencoder
The CAE architecture uses convolutional layers instead of dense layers to better capture spatial features in images. It compresses noisy images to a latent space and reconstructs clean versions from them.

Train the Autoencoder
The model is trained using noisy images as input and clean images as target output, learning to remove noise by minimizing the reconstruction error.

Evaluate Performance
After training, the model is tested on unseen noisy images. The output denoised images are compared with the original clean images using metrics like:

Mean Squared Error (MSE)

Peak Signal-to-Noise Ratio (PSNR)

🎯 Why Use a Convolutional Autoencoder?
Autoencoders learn efficient, compressed representations of images, making them ideal for denoising.

Convolutional layers are particularly effective for image data, capturing spatial features and reducing noise while preserving image structure.

The model does not require class labels, making it a powerful unsupervised learning tool.

This approach demonstrates how deep learning can be applied to clean up noisy image data—a technique that can be extended to real-world domains where image quality is critical.

## 🖼️ Denoising Output Example

Below is a visual comparison of CIFAR-10 images before and after denoising:

![Denoising Output](Output.png)
