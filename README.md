# Exploring GAN Variants for Balancing Imbalanced Datasets

**Course:** Special Topics in Data Science  
**Student:** Tala Al-Rawashdeh  
**Supervised by:** Dr. Yousef Sanjalawe  

## 📌 Project Overview
This project addresses the severe class imbalance problem in medical image classification, specifically for Melanoma (skin cancer) detection. By generating synthetic malignant images using Generative Adversarial Networks (GANs), the objective is to balance the training dataset and significantly improve the sensitivity (Recall) of the diagnostic classifier, thereby reducing life-threatening False Negatives.

## 📊 Dataset
* **Source:** SIIM-ISIC Melanoma Classification Dataset
* **Imbalance Ratio:** 82% Benign (Safe) vs. 18% Malignant (Cancerous)
* **Preprocessing:** Images resized to 128x128 pixels (RGB) and normalized [-1, 1].

## 🧠 GAN Architectures Implemented
1. **Vanilla GAN:** Baseline model utilizing Dense layers.
2. **DCGAN (Deep Convolutional GAN):** Utilizes Conv2DTranspose layers to capture complex spatial hierarchies of skin lesions.
3. **LSGAN (Least Squares GAN):** Replaces BCE loss with Mean Squared Error (MSE) to stabilize training.

## 🏆 Key Results
A Deep CNN classifier was evaluated using strict class-weighted training on an unseen test set. 
* The **DCGAN** variant outperformed all others, successfully providing the most optimal synthetic features. It achieved the highest Recall (**68.4%**) and F1-Score (**0.544**), proving to be the most viable solution for minimizing False Negatives in this clinical dataset.

## 📁 Repository Contents
* `specialTT (2).ipynb`: The complete Python source code (Jupyter Notebook) covering data preprocessing, GAN model building/training, and final classifier evaluation.
