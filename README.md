💳 Fraud Detection using Machine Learning
📌 Project Overview

This project focuses on detecting fraudulent financial transactions using machine learning techniques. The dataset contains transaction-level information, and the objective is to build a robust classification model capable of identifying fraudulent transactions accurately.

Fraud detection is a highly imbalanced classification problem, where fraudulent transactions represent only a small percentage of total transactions. Special attention has been given to handling class imbalance and choosing appropriate evaluation metrics.

🎯 Objectives

Perform Exploratory Data Analysis (EDA)

Engineer meaningful features

Handle class imbalance effectively

Train multiple machine learning models

Evaluate model performance using appropriate metrics

Predict fraud for unseen transactions

📊 Exploratory Data Analysis (EDA)

The following steps were performed:

Checked dataset structure and missing values

Analyzed class imbalance (Fraud vs Non-Fraud)

Explored transaction types and fraud distribution

Generated correlation heatmap for numerical features

Key observation:

Fraud cases were highly imbalanced.

Fraud was mostly observed in specific transaction types such as TRANSFER and CASH_OUT.

🧠 Feature Engineering

To improve model performance, the following features were created:

balanceDiffOrig → Difference between old and new origin balance

balanceDiffDest → Difference between destination balances

isOrigZero → Indicator if origin balance becomes zero

isDestZero → Indicator if destination balance was zero

Categorical variables were encoded using one-hot encoding.

🤖 Models Used

The following classification models were implemented:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Gradient Boosting Classifier

Class weights were used to handle imbalance.

📈 Evaluation Metrics

Since the dataset is highly imbalanced, accuracy is not a reliable metric.

Instead, the following metrics were used:

Precision

Recall

F1-Score

ROC-AUC Score

Recall is especially important in fraud detection because missing fraudulent transactions can be costly.

🏆 Model Performance

Logistic Regression provided strong baseline performance.

Decision Tree showed higher variance and risk of overfitting.

Random Forest performed better due to ensemble learning.

Gradient Boosting captured non-linear patterns effectively.

Tree-based ensemble models outperformed linear models due to complex fraud patterns.

🔍 Prediction on Unseen Data

The trained model was tested on unseen transaction data by:

Applying the same feature engineering steps

Aligning columns with training data

Using the trained model to predict fraud probability

This simulates real-world fraud detection systems.

🛠 Technologies Used

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

🚀 Future Improvements

Hyperparameter tuning using GridSearchCV

Handling imbalance using SMOTE

Threshold tuning for better fraud recall

Deploying the model using Flask/FastAPI

Adding real-time fraud monitoring pipeline
