# Anomaly Detection Model

### Overview

This repository contains the implementation of a machine learning model designed to detect anomalies in a given dataset. The model is particularly useful in scenarios such as fraud detection, network security monitoring, and identifying irregular patterns in customer behavior.

### Dataset

The dataset includes:

- Train_data.csv: Used for training the model.
- Test_data.csv: Used for evaluating the model's performance.

Each connection record consists of 41 features (38 quantitative and 3 qualitative) and a target label indicating whether the connection is normal or anomalous.

### Features

- Categorical Features: protocol_type, service, flag
- Quantitative Features: Traffic statistics, error rates, and host features

- Target Variable:
- 0: Normal
- 1: Anomalous

## Model Workflow:

1. **Data Preprocessing**:
   - Non-numeric columns are encoded using label encoding.
   - Categorical features are one-hot encoded.
   - Feature scaling is applied for standardization.
   
2. **Modeling**:
   - Random Forest Classifier is used for anomaly detection.
   - SMOTE (Synthetic Minority Over-sampling Technique) is applied to balance the dataset and prevent model bias toward the majority class.
   
3. **Evaluation**:
   - The model is evaluated using precision and AUC-PR scores to measure its ability to correctly identify anomalies.

### Key Results

##### Classification Report:

              precision    recall  f1-score   support

         0.0       0.99      0.99      0.99      3516
         1.0       0.99      0.99      0.99      4042

    accuracy                           0.99      7558
   macro avg       0.99      0.99      0.99      7558
weighted avg       0.99      0.99      0.99      7558

##### Feature Importance

Visualized the top 20 features contributing to the classification using the Random Forest model. The most significant features include traffic statistics and error rates.

### Future Enhancements

- Implement hyperparameter tuning for the Random Forest model.
- Explore other classifiers like Gradient Boosting, XGBoost, or LightGBM.
- Deploy the model as an API for real-time intrusion detection.

### Source

https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection/data
