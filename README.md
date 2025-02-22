# Melanoma Detection  

> This project focuses on developing a **Convolutional Neural Network (CNN)** model to accurately detect **melanoma**, one of the most life-threatening types of skin cancer. Melanoma accounts for **75% of skin cancer-related deaths**, making **early detection crucial**. A robust AI-based system that analyzes skin images and assists dermatologists in identifying melanoma can significantly improve diagnostic efficiency and potentially save lives.

## Table of Contents  
- [Problem Statement](#problem-statement)  
- [Project Pipeline](#project-pipeline)  
- [Technologies Used](#technologies-used)  
- [Acknowledgements](#acknowledgements)  

## Problem Statement  

### **Business Understanding**  

The dataset consists of **2,357 images** of both malignant and benign skin lesions, sourced from the **International Skin Imaging Collaboration (ISIC)**. These images are categorized based on the ISIC classification system, with some classes slightly imbalanced due to the varying prevalence of different skin conditions.

The dataset includes images of the following skin conditions:  

- **Actinic keratosis**  
- **Basal cell carcinoma**  
- **Dermatofibroma**  
- **Melanoma**  
- **Nevus**  
- **Pigmented benign keratosis**  
- **Seborrheic keratosis**  
- **Squamous cell carcinoma**  
- **Vascular lesion**  

### **Business Goal**  

The goal of this project is to develop a **multiclass classification model** using a **custom CNN in TensorFlow** to accurately classify different types of skin lesions. The model is intended to aid **dermatologists** in **early melanoma detection**, improving the chances of **timely medical intervention** and better patient outcomes.  

### **Business Risk**  

- Incorrect classification of skin conditions may result in **misdiagnosis**, leading to **inappropriate treatment plans** or **missed early intervention opportunities**.  
- **False negatives** in melanoma detection could be life-threatening if early warning signs are overlooked.  

---

## Project Pipeline  

### **1. Data Reading and Understanding**  
- Define paths for both training and testing image datasets.  
- Load image data and explore its structure.  

### **2. Dataset Creation**  
- Split data into **training** and **validation** sets, ensuring a balanced distribution.  
- Resize images to **180x180 pixels** for consistency.  
- Set an appropriate batch size (**32**).  

### **3. Dataset Visualization**  
- Implement visualization techniques to display **one example from each class**.  

### **4. Model Building & Training (Initial Model)**  
- Build a **CNN model** for **nine-class classification**.  
- Normalize pixel values between **0 and 1** to facilitate model convergence.  
- Select an appropriate **optimizer and loss function**.  
- Train the model for **~20 epochs** and evaluate performance.  
- Analyze **overfitting/underfitting trends**.  

### **5. Data Augmentation**  
- Apply a **data augmentation** strategy to improve model generalization and prevent overfitting.  

### **6. Model Building & Training (With Augmented Data)**  
- Train the CNN model again using **augmented data**.  
- Re-evaluate **performance improvements** and compare with the initial model.  

### **7. Class Distribution Analysis**  
- Examine the **class distribution** in the dataset.  
- Identify **underrepresented classes** and **dominant classes**.  

### **8. Handling Class Imbalances**  
- Utilize the **Augmentor** library to **balance class distributions** by generating synthetic images.  

### **9. Model Building & Training (With Rectified Class Imbalance)**  
- Train the CNN model with **balanced data** to **improve classification performance**.  
- Extend training to **~30 epochs** and analyze performance changes.  
- Compare results to **previous models** and assess improvements.  

---

## Technologies Used  

- **TensorFlow** – Deep learning framework for CNN model training.  
- **Keras** – High-level API for building and optimizing neural networks.  
- **Python** – Core programming language for implementation.  
- **Augmentor** – Library for **data augmentation** to address class imbalances.  

---

## Acknowledgements  

- **ISIC (International Skin Imaging Collaboration)** – For providing the dataset.  
- **TensorFlow/Keras Documentation** – For guidance in model development and optimization.  
