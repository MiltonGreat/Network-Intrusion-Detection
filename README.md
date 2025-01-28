# Anomaly Detection Model

### Overview

This repository contains the implementation of a machine learning model designed to detect network intrusions by identifying anomalous behavior in network traffic. The model is particularly useful in network security applications, such as identifying malicious activities, cyberattacks, or unusual patterns of traffic that could indicate vulnerabilities.

### Dataset

The dataset used in this project is a simulated military network environment consisting of both normal and anomalous (attack) connections. The features were collected from various TCP/IP network connections, and each connection is labeled as either normal or anomalous. The dataset includes:

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

- Precision: The model achieves perfect precision (1.00) for both classes, meaning all predictions for both normal and anomalous traffic are correct.
- Recall: The model also achieves perfect recall (1.00), indicating it successfully identifies all instances of both normal and anomalous traffic.
- F1-Score: Both classes have an F1-score of 1.00, demonstrating a perfect balance between precision and recall.

### Feature Importance

![screenshot-localhost_8888-2025 01 28-14_38_28](https://github.com/user-attachments/assets/3da9238d-7684-4532-848d-68307ff7423e)

The Random Forest model also provides insight into which features are most important for predicting network anomalies. The top features contributing to the classification include various traffic statistics, error rates, and host connection information.

### Future Enhancements

- Implement hyperparameter tuning for the Random Forest model.
- Explore other classifiers like Gradient Boosting, XGBoost, or LightGBM.
- Deploy the model as an API for real-time intrusion detection.

### Source

Dataset: [Network Intrusion Detection Dataset on Kaggle](https://www.kaggle.com/datasets/sampadab17/network-intrusion-detection/data)
