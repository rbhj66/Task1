# Task 1 - Customer Churn Classification

## 📌 Project Overview

This project implements a supervised machine learning classification system to predict whether a telecom customer is likely to churn.

The objective is to build, evaluate, and compare multiple classification algorithms using a real-world customer churn dataset.

Two machine learning algorithms are compared:

* Logistic Regression
* Random Forest Classifier

The models are evaluated using multiple classification metrics including Accuracy, Precision, Recall, F1 Score, and ROC-AUC.

---

## 🎯 Objective

The main objectives of this project are:

1. Perform data preprocessing.
2. Explore the customer churn dataset.
3. Split the dataset into training and testing sets.
4. Train multiple classification algorithms.
5. Compare model performance.
6. Apply 5-Fold Stratified Cross-Validation.
7. Evaluate models using standard classification metrics.
8. Select the best-performing model.
9. Save the trained model for further deployment.

---

## 📊 Dataset

The project uses the **IBM Telco Customer Churn Dataset**.

The dataset contains information about telecom customers, including:

* Customer demographics
* Account information
* Contract information
* Internet services
* Payment methods
* Monthly charges
* Total charges
* Customer tenure
* Churn status

### Target Variable

`Churn`

| Value | Meaning             |
| ----- | ------------------- |
| 0     | Customer will stay  |
| 1     | Customer will churn |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

---

## 🔄 Machine Learning Workflow

The project follows the following workflow:

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Feature & Target Separation
   ↓
Train-Test Split
   ↓
Data Preprocessing
   ↓
Model Training
   ↓
Logistic Regression
   ↓
Random Forest
   ↓
Cross-Validation
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Best Model Selection
   ↓
Model Saving
```

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Converted `TotalCharges` into numerical format.
* Handled missing values.
* Removed the `customerID` column because it does not provide useful predictive information.
* Converted the target variable `Churn` from categorical values into binary values.
* Standardized numerical features using `StandardScaler`.
* Encoded categorical variables using `OneHotEncoder`.

---

## 📈 Exploratory Data Analysis

Several visualizations were created to understand the dataset and customer churn patterns.

The notebook includes:

* Customer churn distribution
* Churn percentage
* Contract type vs churn
* Monthly charges vs churn
* Tenure distribution by churn

These visualizations help identify important patterns associated with customer churn.

---

## 🤖 Machine Learning Models

### 1. Logistic Regression

Logistic Regression is used as a baseline classification model.

It estimates the probability that a customer belongs to the churn class.

### 2. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees.

It is useful for capturing nonlinear relationships and interactions between customer features.

---

## 🔬 Train-Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

Stratified splitting was used to maintain a similar distribution of churn and non-churn customers in both datasets.

---

## 🔁 Cross-Validation

A **5-Fold Stratified Cross-Validation** strategy was used to evaluate model stability.

ROC-AUC was used as the primary cross-validation scoring metric.

This helps determine whether the model performs consistently across different subsets of the dataset.

---

## 📏 Evaluation Metrics

The following metrics were used:

### Accuracy

Measures the percentage of correctly classified customers.

### Precision

Measures how many customers predicted as churners actually churned.

### Recall

Measures how many actual churners were correctly identified.

### F1 Score

Provides a balance between Precision and Recall.

### ROC-AUC

Measures the model's ability to distinguish between churn and non-churn customers across different classification thresholds.

---

## 📊 Model Comparison

The notebook generates a comparison table containing:

| Model               |              Accuracy |             Precision |                Recall |              F1 Score |               ROC-AUC |
| ------------------- | --------------------: | --------------------: | --------------------: | --------------------: | --------------------: |
| Logistic Regression | Generated in Notebook | Generated in Notebook | Generated in Notebook | Generated in Notebook | Generated in Notebook |
| Random Forest       | Generated in Notebook | Generated in Notebook | Generated in Notebook | Generated in Notebook | Generated in Notebook |

The actual values are generated automatically when the notebook is executed.

---

## 📉 Visualizations

The notebook includes:

* Model performance comparison
* Confusion matrix
* ROC curve
* Cross-validation performance

These plots provide visual evidence of model performance.

---

## 🏆 Model Selection

The model with the highest test-set ROC-AUC score is automatically selected as the final model.

The selected model is saved using Joblib.

```text
model/customer_churn_model.pkl
```

This saved model is used later in **Task 2** for API deployment.

---

## 💾 Project Structure

```text
Task-1-Classification/
│
├── Task1_Customer_Churn_Classification.ipynb
│
├── model/
│   └── customer_churn_model.pkl
│
└── README.md
```

---

## ▶️ How to Run

### Step 1: Clone the Repository

Clone the GitHub repository to your computer.

### Step 2: Open the Notebook

Open:

```text
Task1_Customer_Churn_Classification.ipynb
```

using Jupyter Notebook or JupyterLab.

### Step 3: Run the Notebook

Run all cells sequentially.

The dataset is loaded automatically from the provided dataset URL.

### Step 4: Check Results

The notebook will generate:

* Data analysis
* Visualizations
* Model metrics
* Cross-validation results
* ROC curves
* Confusion matrix
* Best model

### Step 5: Model Output

The trained model will be saved as:

```text
model/customer_churn_model.pkl
```

---

## 🔗 Connection With Task 2

The trained model generated in Task 1 is used in Task 2 to create a REST API using FastAPI.

```text
Task 1
Machine Learning Model
        ↓
customer_churn_model.pkl
        ↓
Task 2
FastAPI
        ↓
Docker
        ↓
Model Deployment
```

---

## 🔗 Connection With Task 3

The same trained model is analyzed in Task 3 for:

* Feature importance
* SHAP explainability
* Local explanations
* Gender-based fairness analysis
* Bias detection
* Mitigation recommendations

```text
Task 1 Model
     ↓
Task 3
Explainability + Fairness + Bias Analysis
```

---

## ✅ Task 1 Deliverables

The following deliverables are included:

* [x] Data preprocessing
* [x] Train-test split
* [x] Logistic Regression
* [x] Random Forest
* [x] 5-Fold Cross-Validation
* [x] Accuracy
* [x] Precision
* [x] Recall
* [x] F1 Score
* [x] ROC-AUC
* [x] Confusion Matrix
* [x] ROC Curve
* [x] Model comparison
* [x] Trained model file
* [x] Jupyter Notebook

---

## 👩‍💻 Internship Project

This project was completed as part of an internship assignment focused on supervised machine learning, model evaluation, deployment, fairness, and explainability.
