# Credit Card Fraud Detection Using Machine Learning

## Overview

This project focuses on detecting fraudulent credit card transactions using various machine learning models. Given the highly imbalanced nature of fraud detection datasets, the project implements multiple algorithms to identify the most effective model for detecting fraud.

## Dataset Description

The dataset used in this project contains anonymized credit card transaction data, which includes:

- **Amount**: The transaction amount.
- **Class**: The label indicating whether a transaction is fraudulent (`1`) or not (`0`).
- **Features V1 to V28**: Principal components obtained through PCA, which anonymize the sensitive features.

The `Time` feature was dropped as it was not relevant to the fraud detection task.

## Project Steps

### 1. Data Preprocessing
- The dataset was loaded and preprocessed to handle the imbalance between fraud and non-fraud cases.
- The `Amount` feature was standardized using `StandardScaler`.

### 2. Exploratory Data Analysis (EDA)
- Basic statistics were computed for both fraud and non-fraud cases to understand their characteristics.
- The proportion of fraud cases was calculated to highlight the dataset's imbalance.

### 3. Data Splitting
- The data was split into training and testing sets with an 80-20 ratio.
- Features were separated from the target label (`Class`) for modeling.

### 4. Model Implementation
Several machine learning models were implemented and evaluated for fraud detection:

- **Decision Tree Classifier**: A simple decision tree with a maximum depth of 4.
- **K-Nearest Neighbors (KNN)**: A KNN classifier with 5 neighbors.
- **Logistic Regression**: A logistic regression model.
- **Support Vector Machine (SVM)**: An SVM classifier.
- **Random Forest Classifier**: A random forest model with a maximum depth of 4.
- **XGBoost Classifier**: An XGBoost classifier with a maximum depth of 4.

### 5. Model Evaluation
Each model was evaluated using the following metrics:

- **Accuracy Score**: The proportion of correct predictions out of all predictions made.
- **F1 Score**: The harmonic mean of precision and recall, providing a balance between the two.

### 6. Confusion Matrix Visualization
Confusion matrices were generated and visualized for each model to provide a detailed view of their performance in terms of true positives, false positives, true negatives, and false negatives.

### 7. Comparative Analysis
A comparative analysis of the models was conducted using both accuracy and F1 scores. The results were visualized using a bar chart to highlight the performance of each model.

## Key Results

- **K-Nearest Neighbors** and **XGBoost** models showed the highest performance in detecting fraudulent transactions, as indicated by both their accuracy and F1 scores.
- The **Decision Tree** and **Logistic Regression** models performed adequately but were outperformed by more complex models like **Random Forest** and **XGBoost**.

## Visualization

The project includes visualizations such as:

- Confusion matrices for each model to analyze their prediction performance.
- A bar chart comparing the accuracy and F1 scores of different machine learning models.

## Conclusion

The project successfully demonstrates the application of multiple machine learning models to detect credit card fraud. While simpler models like Decision Trees and Logistic Regression provide a good baseline, advanced models like XGBoost and K-Nearest Neighbors offer superior performance. The findings underscore the importance of using robust machine learning techniques in fraud detection to minimize financial losses and enhance security.

## Future Work

Future improvements could include:

- Implementing more advanced techniques like ensemble learning and deep learning.
- Experimenting with other feature engineering techniques to improve model performance.
- Addressing the class imbalance problem using techniques like SMOTE or ADASYN to further improve model accuracy.
