
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
<img width="615" height="493" alt="Screenshot 2026-03-10 175938" src="https://github.com/user-attachments/assets/cf795537-cde1-4b7e-8b6d-e74bf5637b4d" />

* Brain MRI images organized into:

  * Training folder
  * Testing folder
* Each folder contains subfolders for each tumor class
<img width="632" height="450" alt="Screenshot 2026-03-10 180014" src="https://github.com/user-attachments/assets/e922b992-e673-4a61-94d1-e13ea2edb492" />

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
<img width="459" height="312" alt="image" src="https://github.com/user-attachments/assets/19b16614-e0ad-494b-a05b-e18ac3905ba6" />


* **VGG16 Feature Extraction**

  * Pre-trained deep learning model
  * Extracts high-level image features

---

### 🔹 3. Models Used

* **SVM (Support Vector Machine)**

  * RBF Kernel (Non-linear)
  * Linear Kernel

 <img width="738" height="450" alt="image" src="https://github.com/user-attachments/assets/43f0d179-d4b7-46f7-a979-99b46de6f10d" />


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

## 🛠️ Tech Stack

* Python
* OpenCV
* NumPy, Pandas
* Scikit-learn
* XGBoost
* TensorFlow / Keras
* Matplotlib, Seaborn


