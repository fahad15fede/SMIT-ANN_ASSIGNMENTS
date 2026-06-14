# Medical Insurance Cost Prediction using Artificial Neural Networks (ANN)

## Overview

This project uses an Artificial Neural Network (ANN) to predict medical insurance charges based on customer information such as age, gender, BMI, number of children, smoking status, and region.

The objective is to learn the relationship between customer attributes and insurance costs and accurately predict medical charges for new customers.

---

## Dataset

The dataset contains the following features:

| Feature  | Description                              |
| -------- | ---------------------------------------- |
| age      | Age of the customer                      |
| sex      | Gender of the customer                   |
| bmi      | Body Mass Index                          |
| children | Number of dependent children             |
| smoker   | Smoking status                           |
| region   | Residential region                       |
| charges  | Medical insurance cost (Target Variable) |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* TensorFlow / Keras
* Matplotlib

---

## Data Preprocessing

The following preprocessing steps were performed:

### Missing Value Handling

* Dataset was checked for missing values.
* No missing values were found.

### Categorical Feature Encoding

Categorical features were converted into numerical format using One-Hot Encoding.

Encoded Features:

* sex
* smoker
* region

### Feature Scaling

Numerical features were standardized using StandardScaler.

Scaled Features:

* age
* bmi
* children

---

## Train-Test Split

The dataset was divided into:

* Training Set: 80%
* Testing Set: 20%

Random State: 42

---

## ANN Architecture

The Artificial Neural Network consists of:

Input Layer

* Number of neurons equal to the number of input features after preprocessing

Hidden Layer 1

* 64 Neurons
* ReLU Activation

Hidden Layer 2

* 32 Neurons
* ReLU Activation

Hidden Layer 3

* 16 Neurons
* ReLU Activation

Output Layer

* 1 Neuron
* Linear Activation (Regression Output)

Model Configuration:

* Optimizer: Adam
* Loss Function: Mean Squared Error (MSE)
* Metric: Mean Absolute Error (MAE)

Training Parameters:

* Epochs: 100
* Batch Size: 32
* Validation Split: 20%

---

## Model Performance

| Metric                         | Value         |
| ------------------------------ | ------------- |
| Mean Absolute Error (MAE)      | 3677.10       |
| Mean Squared Error (MSE)       | 29,114,025.71 |
| Root Mean Squared Error (RMSE) | 5395.74       |
| R² Score                       | 0.8125        |

---

## Results and Observations

* The ANN model successfully learned the relationship between customer attributes and insurance charges.
* The model achieved an R² Score of 0.8125, indicating that approximately 81.25% of the variance in insurance charges was explained by the model.
* The average prediction error was approximately $3,677.
* Smoking status was found to have a strong influence on insurance costs.
* Age and BMI also contributed significantly to the prediction of medical charges.
* Training and validation losses decreased consistently, indicating successful learning without severe overfitting.
* The model demonstrated good performance in capturing non-linear relationships within the dataset.

---

## Project Structure

```text
Medical-Insurance-ANN/
│
├── insurance.csv
├── medical_insurance_ann.ipynb
|__ README.md
```

---

## Future Improvements

* Hyperparameter tuning
* Experimenting with different activation functions
* Early Stopping implementation
* Dropout regularization
* Testing deeper ANN architectures
* Comparing ANN performance with Random Forest and XGBoost models

---

## Conclusion

This project demonstrates how Artificial Neural Networks can be applied to regression problems. The model achieved an R² Score of 0.8125 and successfully predicted medical insurance charges using demographic and health-related features. The results show that ANN can effectively model complex, non-linear relationships in healthcare insurance datasets.
