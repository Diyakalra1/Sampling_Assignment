# Sampling_Assignment
# Sampling Techniques and Model Comparison on Credit Card Fraud Dataset

## Overview
This project studies the effect of different sampling techniques on the performance of machine learning models using a credit card fraud detection dataset.  
The dataset is highly imbalanced, which can negatively affect model performance. To address this issue, multiple sampling techniques are applied to balance the data before training the models.

The objective of this project is to identify which sampling technique gives the highest accuracy for each machine learning model.

---

## Dataset
- Dataset Name: Creditcard_data.csv  
- Source: GitHub (provided in the assignment)  
- Problem Type: Binary Classification  
- Target Column: Class  
  - 0: Non-Fraud  
  - 1: Fraud  

The dataset contains a severe class imbalance, with fraudulent transactions forming a very small percentage of the data.

---

## Data Preprocessing
- The dataset is standardized using feature scaling.
- The class imbalance is handled using different sampling techniques.
- The balanced datasets are split into training and testing sets with a 70:30 ratio.

---

## Sampling Techniques
Five different sampling techniques are used:

| Sampling Code | Description |
|--------------|------------|
| Sampling1 | Random Under Sampling |
| Sampling2 | Random Over Sampling |
| Sampling3 | SMOTE |
| Sampling4 | Partial Over Sampling |
| Sampling5 | Partial Under Sampling |

---

## Machine Learning Models
Five machine learning models are trained on each sampled dataset:

| Model Code | Algorithm |
|----------|----------|
| M1 | Logistic Regression |
| M2 | Decision Tree |
| M3 | Random Forest |
| M4 | Support Vector Machine |
| M5 | Naive Bayes |

---

## Experiment Setup
- Feature standardization is applied before model training.
- Each sampled dataset is divided into 70 percent training data and 30 percent testing data.
- Model performance is evaluated using accuracy as the metric.

---

## Results

### Accuracy Table

| Model | Sampling1 | Sampling2 | Sampling3 | Sampling4 | Sampling5 |
|------|-----------|-----------|-----------|-----------|-----------|
| M1 | 33.33 | 91.70 | 91.52 | 91.52 | 28.57 |
| M2 | 66.67 | 98.91 | 96.94 | 99.00 | 85.71 |
| M3 | 33.33 | 99.78 | 99.34 | 100.00 | 71.43 |
| M4 | 16.67 | 96.51 | 96.94 | 97.26 | 14.29 |
| M5 | 50.00 | 78.17 | 73.36 | 78.55 | 42.86 |

---

## Best Sampling Technique for Each Model

| Model | Best Sampling Technique | Accuracy |
|------|------------------------|----------|
| M1 | Sampling2 | 91.70 |
| M2 | Sampling4 | 99.00 |
| M3 | Sampling4 | 100.00 |
| M4 | Sampling4 | 97.26 |
| M5 | Sampling4 | 78.55 |

---

## Observations
- Sampling technique has a significant impact on model performance.
- Random Over Sampling and Partial Over Sampling consistently produce higher accuracies.
- Random Forest achieves the highest accuracy of 100 percent with Sampling4.
- Under sampling methods generally result in lower accuracy due to loss of important data.
- No single model performs best under all sampling techniques, but Sampling4 performs well across most models.

---


## Conclusion
This project demonstrates that handling class imbalance is essential for fraud detection problems.  
Different sampling techniques influence machine learning models in different ways.  
Partial Over Sampling provides the most consistent and accurate results across multiple models in this study.

---

## Author
Diya Kalra
