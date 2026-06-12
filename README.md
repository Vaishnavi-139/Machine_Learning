# Comparative Analysis of Machine Learning Classifiers for Handwritten Digit Recognition on MNIST

## Overview

This project presents a comprehensive comparative study of multiple machine learning classification algorithms on the MNIST handwritten digit recognition dataset. The objective is to evaluate the effectiveness of different supervised learning techniques for multi-class image classification and identify the best-performing model based on various evaluation metrics.

The project implements and compares:

* Decision Tree Classifier
* Random Forest Classifier
* Gaussian Naïve Bayes
* K-Nearest Neighbors (KNN)
* Multi-Layer Perceptron (Neural Network)

Performance is evaluated using k-fold cross-validation, accuracy, precision, recall, F1-score, and confusion matrices.

---

## Dataset

### MNIST Handwritten Digits Dataset

The MNIST dataset contains grayscale images of handwritten digits (0–9).

**Dataset Characteristics**

* 70,000 images
* 28 × 28 pixels per image
* 10 digit classes
* 784 features per sample

Dataset loaded using:

```python
from sklearn.datasets import fetch_openml

sample = fetch_openml(name='mnist_784', version=1)
```

---

## Project Workflow

### 1. Data Collection

* Fetch MNIST dataset from OpenML
* Convert labels to integer format

### 2. Data Splitting

Dataset divided into:

* Training Set: 70%
* Test Set: 30%

```python
train_test_split(X, Y, test_size=0.3, random_state=42)
```

### 3. Model Training

The following models were trained and evaluated:

#### Decision Tree

* Tree-based classification
* Easy interpretability
* Fast training

#### Random Forest

* Ensemble learning approach
* Multiple decision trees
* Improved generalization

#### Gaussian Naïve Bayes

* Probabilistic classifier
* Assumes feature independence

#### K-Nearest Neighbors (KNN)

* Instance-based learning
* Classification based on neighborhood similarity

#### Multi-Layer Perceptron (MLP)

* Feed-forward neural network
* Learns complex non-linear decision boundaries

---

## Evaluation Metrics

The models were evaluated using:

### Accuracy

Measures overall prediction correctness.

### Precision

Measures quality of positive predictions.

### Recall

Measures ability to correctly identify positive instances.

### F1 Score

Harmonic mean of precision and recall.

### Confusion Matrix

Provides detailed class-wise prediction analysis.

---

## Cross-Validation Results

| Model                | 5-Fold Cross Validation Accuracy |
| -------------------- | -------------------------------- |
| Decision Tree        | 85.95%                           |
| Random Forest        | 96.71%                           |
| Gaussian Naïve Bayes | 55.02%                           |
| KNN                  | 96.79%                           |
| Neural Network (MLP) | 95.98%                           |

### Observations

* KNN achieved the highest cross-validation accuracy.
* Random Forest closely matched KNN performance.
* Neural Networks delivered strong classification performance.
* Decision Trees performed reasonably but suffered from overfitting.
* Naïve Bayes showed significantly lower performance due to strong independence assumptions.

---

## Test Set Performance

### Decision Tree

* Accuracy: 86.8%
* Precision: 86.78%
* Recall: 86.8%
* F1 Score: 86.78%

### Random Forest

* Accuracy: 96.57%
* Precision: 96.57%
* Recall: 96.57%
* F1 Score: 96.57%

### Key Finding

Random Forest and KNN emerged as the most effective classifiers for handwritten digit recognition on the MNIST dataset.

---

## Technologies Used

* Python
* NumPy
* Pandas
* Scikit-Learn
* OpenML
* Google Colab

---

## Repository Structure

```text
├── MTL782_A2.ipynb
├── README.md
└── Results/
    ├── Confusion_Matrices
    ├── Evaluation_Metrics
    └── Model_Comparisons
```

---

## Learning Outcomes

* Supervised Machine Learning
* Multi-Class Classification
* Model Evaluation Techniques
* Cross-Validation
* Hyperparameter Understanding
* Ensemble Learning
* Neural Networks
* Performance Analysis

---

## Future Improvements

* Hyperparameter tuning using GridSearchCV and RandomizedSearchCV
* Feature reduction using PCA
* CNN-based deep learning implementation
* Model deployment using Flask or Streamlit
* Automated experiment tracking

---

## Authors

* Mohit Raj Modi
* Neelam Kumari Meena
* Vaishnavi Priya
* Kinjal Anchhara

---
