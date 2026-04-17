
#  Brain Tumor Classification using SVM, PCA, XGBoost & VGG16

## 📌 Overview

This project focuses on **classifying brain tumor MRI images** into different categories using machine learning and deep learning techniques.

The goal is to compare traditional methods like **Support Vector Machines (SVM)** with advanced approaches such as **XGBoost** and **VGG16-based feature extraction**.

---

## 🎯 Objectives

* Classify MRI images into:

  * Glioma Tumor
  * Meningioma Tumor
  * Pituitary Tumor
  * No Tumor
* Compare performance of:

  * SVM (Linear vs RBF Kernel)
  * PCA-based feature reduction
  * XGBoost classifier
  * Deep feature extraction using VGG16
* Analyze the impact of training data size on model performance

---

## 📂 Dataset

* Brain MRI images organized into:

  * Training folder
  * Testing folder
* Each folder contains subfolders for each tumor class

---

## ⚙️ Methodology

### 🔹 1. Data Preprocessing

* Convert images to grayscale
* Resize to fixed size (64×64 / 128×128)
* Flatten images into vectors
* Normalize pixel values

---

### 🔹 2. Feature Engineering

* **PCA (Principal Component Analysis)**

  * Reduces dimensionality
  * Retains important variance

* **VGG16 Feature Extraction**

  * Pre-trained deep learning model
  * Extracts high-level image features

---

### 🔹 3. Models Used

* **SVM (Support Vector Machine)**

  * RBF Kernel (Non-linear)
  * Linear Kernel

* **XGBoost Classifier**

  * Applied on:

    * Raw features
    * PCA features
    * VGG16 features

---

### 🔹 4. Evaluation Metrics

* Accuracy
* F1-Score
* Sensitivity (Recall)
* Specificity

---

## 📊 Results Summary

| Model           | Accuracy | F1 Score | Sensitivity | Specificity   |
| --------------- | -------- | -------- | ----------- | ------------- |
| SVM (Linear)    | ~40%     | Low      | Low         | Moderate      |
| SVM (RBF)       | ~63%     | Medium   | Medium      | High          |
| Raw + XGBoost   | ~64%     | Medium   | Medium      | High          |
| PCA + XGBoost   | ~70%     | Good     | Good        | High          |
| VGG16 + XGBoost | **~73%** | **Best** | **High**    | **Very High** |

---

## 📈 Key Observations

* RBF kernel performs better than Linear due to **non-linear MRI patterns**
* PCA improves performance by removing noise
* XGBoost handles high-dimensional data effectively
* VGG16 provides the **best feature representation**, leading to highest accuracy

---

## 📉 Training Size Analysis

* Models were trained with:

  * 20%, 40%, 60%, 80% data

### 🔍 Trend:

* Accuracy increases with more training data
* RBF improves significantly
* Linear model shows limited improvement

---

## 🧠 Conclusion

* Feature extraction plays a **critical role** in medical image classification
* Traditional ML (SVM) performs reasonably well
* Deep learning-based feature extraction (**VGG16**) significantly boosts performance
* Best model: **VGG16 + XGBoost**

---

## 🚀 Future Improvements

* Data augmentation (rotation, flipping, zoom)
* Hyperparameter tuning (GridSearchCV)
* Fine-tuning VGG16 or using EfficientNet
* Deployment using Streamlit / Flask

---

## 🛠️ Tech Stack

* Python
* OpenCV
* NumPy, Pandas
* Scikit-learn
* XGBoost
* TensorFlow / Keras
* Matplotlib, Seaborn


