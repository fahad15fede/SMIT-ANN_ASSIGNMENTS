# SMIT ANN Assignments

This repository contains three Artificial Neural Network (ANN) projects developed as part of the SMIT Deep Learning assignment. Each project demonstrates the complete machine learning workflow including data preprocessing, feature engineering, train-test splitting, ANN model development, training, evaluation, and result analysis.

---

## Projects Included

### 1. Bank Customer Churn Prediction

**Problem Type:** Binary Classification

Predicts whether a bank customer is likely to leave the bank based on customer demographics, account information, and banking behavior.

#### Features

* Credit Score
* Country
* Gender
* Age
* Tenure
* Balance
* Products Number
* Credit Card Status
* Active Member Status
* Estimated Salary

#### ANN Architecture

```text
Input Layer
↓
Dense(64, ReLU)
↓
Dropout(0.3)
↓
Dense(32, ReLU)
↓
Dropout(0.3)
↓
Dense(16, ReLU)
↓
Dropout(0.2)
↓
Dense(1, Sigmoid)
```

#### Techniques Used

* Missing Value Analysis
* One-Hot Encoding
* Feature Scaling using StandardScaler
* Early Stopping
* Dropout Regularization

#### Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* Classification Report

---

### 2. Loan Approval Prediction

**Problem Type:** Binary Classification

Predicts whether a loan application should be approved or rejected based on applicant financial information and credit history.

#### Features

* Number of Dependents
* Education
* Self Employment Status
* Annual Income
* Loan Amount
* Loan Term
* CIBIL Score
* Residential Assets Value
* Commercial Assets Value
* Luxury Assets Value
* Bank Asset Value

#### ANN Architecture

```text
Input Layer
↓
Dense(16, ReLU)
↓
Dense(8, ReLU)
↓
Dense(1, Sigmoid)
```

#### Techniques Used

* Label Encoding
* Feature Scaling using StandardScaler
* Binary Classification

#### Model Performance

| Metric            | Value  |
| ----------------- | ------ |
| Training Accuracy | 97.95% |
| Test Accuracy     | 97.19% |

#### Classification Report

| Class         | Precision | Recall | F1-Score |
| ------------- | --------- | ------ | -------- |
| Rejected Loan | 0.96      | 0.97   | 0.96     |
| Approved Loan | 0.98      | 0.98   | 0.98     |

#### Observations

* The ANN achieved excellent classification performance.
* CIBIL score and financial asset information strongly influenced loan approval decisions.
* The model generalized well with minimal overfitting.

---

### 3. Medical Insurance Cost Prediction

**Problem Type:** Regression

Predicts medical insurance charges based on customer demographic and health-related information.

#### Features

* Age
* Gender
* BMI
* Number of Children
* Smoking Status
* Region

#### ANN Architecture

```text
Input Layer
↓
Dense(64, ReLU)
↓
Dense(32, ReLU)
↓
Dense(16, ReLU)
↓
Dense(1)
```

#### Techniques Used

* One-Hot Encoding
* Feature Scaling using StandardScaler
* Regression using ANN

#### Model Performance

| Metric   | Value         |
| -------- | ------------- |
| MAE      | 3677.10       |
| MSE      | 29,114,025.71 |
| RMSE     | 5395.74       |
| R² Score | 0.8125        |

#### Observations

* The model explained approximately 81.25% of the variance in insurance charges.
* Smoking status had the strongest influence on insurance costs.
* Age and BMI also significantly impacted predictions.
* The ANN successfully captured non-linear relationships within the dataset.

---

## Technologies Used

* Python
* Pandas
* NumPy
* TensorFlow / Keras
* Scikit-Learn
* Matplotlib

---

## Machine Learning Workflow

1. Data Loading
2. Data Exploration
3. Data Cleaning
4. Feature Encoding
5. Feature Scaling
6. Train-Test Split
7. ANN Model Development
8. Model Training
9. Model Evaluation
10. Result Analysis

---

## Key Concepts Practiced

* Artificial Neural Networks (ANN)
* Binary Classification
* Regression
* ReLU Activation Function
* Sigmoid Activation Function
* Dropout Regularization
* Early Stopping
* Feature Scaling
* One-Hot Encoding
* Model Evaluation Metrics

---

## Repository Structure

```text
SMIT-ANN_ASSIGNMENTS/

├── Bank_Customer_Churn/
│   ├── dataset
│   ├── notebook
│   └── README.md
│
├── Loan_Approval_Prediction/
│   ├── dataset
│   ├── notebook
│   └── README.md
│
├── Medical_Insurance_Cost/
│   ├── dataset
│   ├── notebook
│   └── README.md
│
└── README.md
```

---

## Conclusion

These projects demonstrate the application of Artificial Neural Networks to both classification and regression tasks. Through preprocessing, feature engineering, ANN architecture design, and evaluation, the models achieved strong predictive performance across real-world banking, finance, and healthcare datasets.
