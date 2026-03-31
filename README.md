# Computer Vision with Deep Learning: Fashion MNIST

## Project Overview
This repository contains a complete end-to-end Deep Learning pipeline for multi-class image classification using the Fashion MNIST dataset. 

Developed as part of the Artificial Intelligence curriculum under the guidance of Prof. Angelo, the primary objective of this project was to demystify the "black box" of Neural Networks. Rather than simply deploying a pre-built model, the focus was on manually tuning hyperparameters, understanding the mathematical transformations between layers, and thoroughly explaining the code architecture to prove a deep comprehension of how a Multilayer Perceptron (MLP) processes visual spatial data.

## Tech Stack
* **Framework:** `TensorFlow` / `Keras`
* **Data Processing:** `NumPy`
* **Visualization:** `Matplotlib`, `Seaborn`

## Architecture & Engineering Decisions
To classify 28x28 pixel grayscale images into 10 distinct clothing categories, the network was built with a conscious focus on the transition from 2D spatial structures to 1D processing arrays:

1. **Input Normalization:** Image pixels (0-255) were normalized to floating-point values (0.0 - 1.0) to ensure gradient descent stability and faster convergence.
2. **Flattening Layer (`Flatten`):** A crucial step for MLP architectures, serializing the 2D image matrix into a 1D array of 784 neurons.
3. **Hidden Representation (`Dense`):** A 128-neuron layer utilizing the `ReLU` activation function to extract non-linear features efficiently.
4. **Classification Layer (`Dense`):** A 10-neuron output layer using `Softmax` to generate a normalized probability distribution across all 10 clothing classes.
5. **Loss Function:** `sparse_categorical_crossentropy` was selected as the optimal metric for mutually exclusive integer labels.

## Visual Validation & Performance

The model achieved over **91% training accuracy** and **88% validation accuracy**, demonstrating strong generalization with minimal overfitting.

### 1. Learning Curves
Monitoring the model's accuracy and loss over 10 epochs ensures the network is effectively learning without memorizing the noise in the training data.

<img width="1389" height="490" alt="Curves" src="https://github.com/user-attachments/assets/d929cc35-dfcc-42a4-9c7b-19ba5204cb6f" />

### 2. Confusion Matrix
The confusion matrix provides a granular view of the network's sensitivity, highlighting exactly where the model excels and where classes visually overlap (e.g., confusing a T-shirt with a standard Shirt).

<img width="928" height="790" alt="matrix2" src="https://github.com/user-attachments/assets/145b73b8-d549-4865-9e81-3cca20ec4750" />

### 3. Real-World Inference
To prove the model's practical efficiency, the grid below shows the Neural Network making real-time predictions on unseen test data. The text highlights successful classifications (Green) and prediction errors (Red).

<img width="1298" height="590" alt="image" src="https://github.com/user-attachments/assets/a426a156-cc0e-4f87-b9b7-df7ee18b5dd1" />


---
**Author:** Victor Cesar de Mecê Prando
**LinkedIn:** [victor-prando1](https://www.linkedin.com/in/victor-prando1/)
