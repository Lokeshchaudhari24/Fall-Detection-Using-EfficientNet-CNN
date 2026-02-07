# Fall Detection Using EfficientNet CNN

## Overview
This project implements a **Deep Learning–based Fall Detection System** using a **Convolutional Neural Network (CNN)** with **EfficientNetB0** as the backbone.  
The model classifies images into **Fall** and **Non-Fall** categories and is designed to assist in monitoring elderly or vulnerable individuals in healthcare and safety environments.

The system uses **transfer learning**, data augmentation, fine-tuning, and achieves strong classification performance. A simple **Gradio-based interface** is also included for real-time image prediction.

---

## Problem Statement
Falls are one of the leading causes of serious injury among elderly people and patients under medical supervision. Manual monitoring is inefficient and unreliable.

The objective of this project is to:
- Automatically detect human falls from images
- Reduce response time in emergency situations
- Provide a scalable and AI-based safety solution

---

## Dataset Description
- **Type:** Image dataset (Fall / Non-Fall)
- **Classes:** Binary classification  
  - `Fall`
  - `Non-Fall`
- **Image Size:** Resized to model input dimensions
- **Channels:** RGB (3-channel images)

---

## Model Architecture
The model is built using **EfficientNetB0** with transfer learning:

- Pre-trained **EfficientNetB0** (ImageNet weights)
- Custom classification head:
  - Global Average Pooling
  - Batch Normalization
  - Dropout (for regularization)
  - Dense layer with Sigmoid activation
- Binary classification output

---

## ⚙️ Training Strategy
- **Data Augmentation:**
  - Random Flip
  - Random Rotation
  - Random Zoom
- **Optimizer:** Adam
- **Loss Function:** Binary Cross-Entropy
- **Initial Training:** Frozen base model
- **Fine-Tuning:** Unfreezing top layers after initial training
- **Learning Rates:**
  - Initial: `0.001`
  - Fine-tuning: `1e-4`

---

## Model Performance
- High training and validation accuracy
- Reduced overfitting due to:
  - Data augmentation
  - Dropout layers
  - Fine-tuning strategy
- Smooth convergence observed in accuracy and loss curves

---

## Evaluation & Visualization
- Accuracy vs Epoch plots
- Loss vs Epoch plots
- Prediction visualization on unseen images
- Correct classification of Fall / Non-Fall cases

---

├── model.ipynb
├── README.md
├── requirements.txt

---

🛠 Technologies & Tools Used

Programming Language: Python

Deep Learning Framework: TensorFlow / Keras

Model: EfficientNetB0

Libraries:

    NumPy

    Matplotlib

    OpenCV

    Gradio
----

🎯 Key Skills Demonstrated

Convolutional Neural Networks (CNN)

Transfer Learning

EfficientNet Architecture

Data Augmentation

Model Fine-Tuning

Binary Image Classification

Model Deployment with Gradio
