
# MNIST Handwritten Digit Classification using CNN

## Overview

This project implements a **Convolutional Neural Network (CNN)** to recognize handwritten digits using the MNIST dataset.

The model classifies grayscale images into 10 categories (0–9). It uses data augmentation, batch normalization, dropout, and callback functions to improve model performance and reduce overfitting.

## Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Convolutional Neural Networks (CNN)

## Dataset

The project uses the MNIST Handwritten Digits Dataset.

**Dataset Links:**
- [MNIST Official Dataset](http://yann.lecun.com/exdb/mnist/)
- [MNIST Dataset on Kaggle](https://www.kaggle.com/datasets/hojjatk/mnist-dataset)

| Description | Details |
|:---|---:|
| Total Images | 70,000 |
| Training Images | 60,000 |
| Testing Images | 10,000 |
| Image Dimensions | 28 × 28 |
| Color Mode | Grayscale |
| Number of Classes | 10 |

The dataset is automatically downloaded using TensorFlow/Keras. No manual download is required.

## Project Structure

```text
MNIST-Handwritten-Digit-Classification/
│
├── MNIST_CNN_Classification.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

## Installation and Setup

**1. Clone the repository**

Clone the repository and open the project folder in VS Code or Jupyter Notebook.

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Run the project**

Open `MNIST_CNN_Classification.ipynb` and execute all cells sequentially.

The MNIST dataset will be downloaded automatically when the notebook is executed for the first time.

## Model Architecture

The project uses a custom CNN consisting of:

- Input Layer (28 × 28 × 1)
- Data Augmentation (Random Rotation and Zoom)
- Two Convolutional Blocks (32 and 64 filters)
- Batch Normalization
- Max Pooling
- Dropout
- Flatten Layer
- Dense Layer (128 neurons, ReLU)
- Output Layer (10 neurons, Softmax)

## Training Configuration

| Parameter | Value |
|:---|:---|
| Optimizer | Adam |
| Learning Rate | 0.001 |
| Loss Function | Sparse Categorical Crossentropy |
| Batch Size | 128 |
| Maximum Epochs | 12 |
| Validation Split | 10% |
| ReduceLROnPlateau | Patience = 2 |
| Early Stopping | Patience = 4 |

## Model Evaluation

The model is evaluated on the untouched 10,000-image test dataset.

The evaluation includes:

- Test Loss and Accuracy
- Training and Validation Accuracy
- Training and Validation Loss
- Classification Report
- Confusion Matrix
- Misclassified Image Analysis
- Prediction Confidence

## Hardware Acceleration

The project checks GPU availability using TensorFlow. Training uses a compatible GPU when available; otherwise, it runs on the CPU.

## Author

**MNIST Handwritten Digit Classification**

A Deep Learning project built using Python, TensorFlow, Keras, and CNN.
