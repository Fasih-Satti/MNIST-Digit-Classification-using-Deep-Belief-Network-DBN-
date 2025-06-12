# MNIST Digit Classification using Deep Belief Network (DBN)

A Python implementation of a Deep Belief Network (DBN) for classifying handwritten digits from the MNIST dataset.

## 📌 Overview
- Trains a DBN model using **Restricted Boltzmann Machines (RBMs)** + **Logistic Regression**
- Achieves **95.8% test accuracy** with the improved model
- Includes demo code to predict digits from custom images

## 🛠️ Technologies Used
- Python 3
- Libraries: 
  - `scikit-learn` (for RBM and Logistic Regression)
  - `numpy` & `pandas` (data processing)
  - `matplotlib` (visualization)
  - `Pillow` (image loading)

## 📂 Repository Structure
DBN-MNIST/
├── mnist_model.h5 # Trained model (HDF5 format)
├── DBN_MNIST.ipynb # Main Jupyter notebook with code
├── eight.png # Sample test image
└── README.md

## 🚀 How to Use
1. **Train the model**:
   ```python
   # Load dataset
   mnist = fetch_openml('mnist_784', version=1)
   X = mnist.data / 255.0
   y = mnist.target.astype(int)
   
   # Train DBN pipeline
   dbn.fit(X_train, y_train)
   📊 Results
Model Version	Train Accuracy	Test Accuracy
Basic DBN	94.89%	94.39%
Improved DBN	96.03%	95.84%
