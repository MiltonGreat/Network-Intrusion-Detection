# Network-Intrusion-Detection

### Overview

This project focuses on detecting network intrusions using machine learning techniques. The dataset consists of a variety of simulated intrusions in a military network environment. The primary goal is to identify normal and anomalous connections, leveraging Random Forest classification for anomaly detection.

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

### Project Workflow

##### Data Preprocessing
- Handled missing values and duplicates.
- Encoded categorical features using one-hot encoding.
- Standardized numerical features using StandardScaler.

##### Exploratory Data Analysis (EDA)
- Visualized the class distribution.
- Analyzed correlations to select the most relevant features.

##### Feature Selection
- Retained features with correlations above a threshold of 0.1.
- Used one-hot encoding for categorical variables and scaled numeric features.

##### Model Building
- Trained a Random Forest classifier to distinguish between normal and anomalous connections.
- Split the data into training and validation sets (70/30 split).

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
