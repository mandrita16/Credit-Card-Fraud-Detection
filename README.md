# Credit Card Fraud Detection Using Machine Learning

## Overview

Fraudulent financial transactions pose a significant challenge to financial institutions and businesses worldwide. Detecting fraudulent activities quickly and accurately is crucial for reducing financial losses and improving transaction security.

This project implements a machine learning-based fraud detection system that analyzes transaction-related data and classifies transactions as either legitimate or fraudulent. Multiple classification algorithms are trained and compared to determine the most effective model for fraud detection.

The project also includes a user-driven prediction system where users can provide transaction feature values and receive a fraud prediction based on the trained machine learning model.

---

## Problem Statement

Traditional rule-based fraud detection systems often struggle to identify new or evolving fraud patterns. Machine learning techniques can learn complex patterns from historical transaction data and improve fraud detection accuracy.

The objective of this project is to:

- Detect fraudulent transactions using machine learning.
- Compare the performance of multiple classification algorithms.
- Evaluate models using standard classification metrics.
- Build an interactive fraud prediction system.

---
## Project Structure
```text
Credit-Card-Fraud-Detection/
│
├── cdd.csv                # Download separately from Kaggle
├── fraud_detection.ipynb
├── README.md
└── requirements.txt
```

## Machine Learning Approach

This project follows a supervised learning approach where historical transaction records are used to train classification models.

The target variable:

```text
Class = 0 → Legitimate Transaction
Class = 1 → Fraudulent Transaction
```

The trained model learns transaction patterns and predicts whether new transactions are likely to be fraudulent.

---

## Algorithms Implemented

### Random Forest Classifier

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction accuracy and reduce overfitting.

**Advantages:**
- Handles large datasets efficiently
- Robust against overfitting
- Works well with complex feature interactions

---

### Logistic Regression

Logistic Regression is a statistical classification algorithm commonly used for binary classification problems.

**Advantages:**
- Fast and interpretable
- Effective baseline model
- Suitable for binary prediction tasks

---

### Support Vector Machine (SVM)

SVM identifies the optimal decision boundary that separates fraudulent and legitimate transactions.

**Advantages:**
- Effective in high-dimensional spaces
- Strong classification performance
- Works well with complex datasets

---

### K-Nearest Neighbors (KNN)

KNN classifies a transaction based on the labels of its nearest neighboring transactions.

**Advantages:**
- Simple implementation
- Non-parametric approach
- Effective for pattern-based classification

---

## Project Workflow

### 1. Import Required Libraries

The project utilizes Python libraries for:

- Data manipulation
- Machine learning
- Model evaluation

Libraries used:

- Pandas
- Scikit-Learn

---

### 2. Data Loading

Transaction data is loaded into a Pandas DataFrame.

```python
data = pd.read_csv("cdd.csv")
```

---

### 3. Feature and Target Selection

The dataset is separated into:

#### Features (X)

Transaction attributes used for prediction.

#### Target Variable (y)

Fraud classification label.

```python
X = data.drop('Class', axis=1)
y = data['Class']
```

---

### 4. Data Splitting

The dataset is divided into:

- Training Set (80%)
- Testing Set (20%)

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

This ensures unbiased model evaluation.

---

### 5. Model Training

The following classifiers are trained:

- Random Forest
- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

Each model learns patterns from historical transaction data.

---

### 6. Model Evaluation

Models are evaluated using:

#### Accuracy Score

Measures overall prediction accuracy.

#### Confusion Matrix

Provides a breakdown of:

- True Positives
- True Negatives
- False Positives
- False Negatives

#### Classification Report

Includes:

- Precision
- Recall
- F1-Score
- Support

---

### 7. Fraud Prediction System

The trained Random Forest model is used for real-time prediction.

Users enter transaction feature values:

```python
Enter value for Feature1:
Enter value for Feature2:
...
```

The model then predicts:

```text
Fraudulent Transaction
```

or

```text
Legitimate Transaction
```

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- Scikit-Learn

### Machine Learning Techniques

- Random Forest
- Logistic Regression
- Support Vector Machine
- K-Nearest Neighbors

---

## Evaluation Metrics

The following metrics are used to assess model performance:

| Metric | Purpose |
|----------|----------|
| Accuracy | Overall prediction performance |
| Precision | Measures fraud detection correctness |
| Recall | Measures ability to identify fraud |
| F1-Score | Balance between precision and recall |
| Confusion Matrix | Detailed classification analysis |

---

## Project Structure

```text
Credit-Card-Fraud-Detection/
│
├── credit card fraud detection model.py
├── README.md
├── requirements.txt
└── 
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/mandrita16/Credit-Card-Fraud-Detection.git
```

Navigate to the project directory:

```bash
cd Credit-Card-Fraud-Detection
```

Install required packages:

```bash
pip install -r requirements.txt
```

---

## Requirements

```txt
pandas
scikit-learn
numpy
```

---

## Results

The project compares multiple machine learning algorithms to identify the most effective fraud detection model.

Performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

Random Forest generally demonstrates strong performance due to its ensemble learning capabilities and ability to capture complex fraud patterns.

---

## Future Enhancements

### Feature Scaling

Implement StandardScaler for SVM and KNN models to improve performance.

### Hyperparameter Optimization

Use GridSearchCV or RandomizedSearchCV for model tuning.

### Cross Validation

Improve model reliability using k-fold cross validation.

### Advanced Models

Experiment with:

- XGBoost
- LightGBM
- CatBoost

### Deployment

Deploy the model using:

- Streamlit
- Flask
- FastAPI

### Real-Time Fraud Detection

Integrate with transaction processing systems for real-time fraud monitoring.

---

## Learning Outcomes

Through this project, I gained practical experience in:

- Supervised Machine Learning
- Classification Algorithms
- Fraud Detection Systems
- Model Comparison
- Performance Evaluation
- Predictive Analytics
- User-Driven Prediction Systems

---

## Author

**Mandrita Dasgupta**

Machine Learning | Data Science | Data Analytics | AI
