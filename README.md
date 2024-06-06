# Diabetes Prediction Using Machine Learning Models

## Overview
This repository contains the implementation of a study on diabetes prediction using various machine learning algorithms. The project focuses on preprocessing techniques, feature analysis, handling class imbalance, and evaluating multiple classifiers to predict diabetes onset.

## Features
- **Data Preprocessing**: Includes dataset cleaning, feature analysis, outlier removal (using standard deviation and IQR methods), and normalization.
- **Classification Algorithms**: Utilizes Logistic Regression, Decision Tree, SVM, Gaussian Naive Bayes, Multi-layer Perceptron, and Random Forest classifiers.
- **Class Imbalance Handling**: Implements various techniques such as over-sampling (k-means SMOTE), under-sampling (ENN, NCR), and combined sampling (SMOTE-Tomek, SMOTE-ENN).
- **Data Correlation Analysis**: Identifies key features correlated with diabetes risk, such as blood glucose level, HbA1c level, age, and BMI.

## Methodology
1. **Data Preprocessing**:
   - **Dataset Cleaning**: Removing duplicates and correcting data types.
   - **Feature Analysis and Outlier Removal**:
     - **Standard Deviation Method**: Removes data points beyond a specified number of standard deviations from the mean.
     - **IQR Method**: Removes data points outside the interquartile range.
   - **Normalization and Feature Transformation**: Equal-depth binning for numerical features and sequential numbering for categorical features.

2. **Classification**:
   - Evaluated several algorithms:
     - Logistic Regression
     - Decision Tree
     - Support Vector Machine (SVM)
     - Gaussian Naive Bayes
     - Multi-layer Perceptron (MLP)
     - Random Forest
   - **Class Imbalance Handling**:
     - **Over-sampling**: k-means SMOTE
     - **Under-sampling**: Edited Nearest Neighbours (ENN), Neighbourhood Cleaning Rule (NCR)
     - **Combined Sampling**: SMOTE-Tomek, SMOTE-ENN

## Results
- **Outlier Detection and Handling**:
  - Standard Deviation Method: 
    - Old normalization, no undersampling: 
      - Accuracy: 97%
      - Recall (diabetes=1): 2%
    - Old normalization, undersampling (max size 5000):
      - Accuracy: 84%
      - Recall (diabetes=1): 78%
  - IQR Method: 
    - Old normalization, no undersampling:
      - Accuracy: 95%
      - Recall (diabetes=1): 29%
    - Old normalization, undersampling (max size 10000):
      - Accuracy: 86%
      - Recall (diabetes=1): 79%
  - Over-sampling (K-means SMOTE):
    - Model: Random Forest
    - Accuracy: 95%
    - Recall (diabetes=1): 96%
  - Under-sampling (Edited Nearest Neighbours):
    - Model: Random Forest
    - Accuracy: 97%
    - Recall (diabetes=1): 61%
  - Under-sampling (Neighbourhood Cleaning Rule):
    - Model: Random Forest
    - Accuracy: 99%
    - Recall (diabetes=1): 96%
  - Combined Sampling (SMOTE-Tomek):
    - Model: Decision Tree Classifier
    - Accuracy: 92%
    - Recall (diabetes=1): 95%
    - Model: Random Forest
    - Accuracy: 96%
    - Recall (diabetes=1): 94%

## Conclusion
The study demonstrates the effectiveness of machine learning models in predicting diabetes. The comprehensive approach, including data preprocessing and handling class imbalance, enhances the accuracy and reliability of predictions. Further validation with larger and more diverse datasets is recommended to improve clinical decision-making and healthcare outcomes.

## Authors
- Gaurang Dixit
- Amogh Huddar
- Shiv Shankar Prajapati

## License
This project is licensed under the MIT License - see the LICENSE file for details.
