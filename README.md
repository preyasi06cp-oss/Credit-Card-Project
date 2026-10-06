# 💳 Credit Card Default Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting whether a credit card customer is likely to default on their next month's payment using Machine Learning classification algorithms.

The project uses the **Credit Card Default dataset** and performs complete data preprocessing, exploratory data analysis, feature engineering, feature selection, data balancing, transformation, scaling, model training, and performance comparison.

The main objective is to identify the best-performing Machine Learning algorithm for predicting credit card payment default.

---

## 🎯 Objectives

- Analyze customer credit card data.
- Explore the structure and characteristics of the dataset.
- Identify missing values and duplicate records.
- Analyze relationships between features using correlation.
- Rename columns for better understanding.
- Convert categorical values into machine-readable format.
- Detect and handle outliers using the IQR method.
- Handle class imbalance using SMOTE.
- Select important features using SelectKBest.
- Transform and scale the data.
- Train multiple Machine Learning classification models.
- Compare model performance using Accuracy, Precision, F1-Score, and Recall.
- Identify the best-performing model.

---

## 📊 Dataset

The project uses the `creditcard.csv` dataset.

The dataset contains information related to customers':

- Demographic details
- Education
- Marital status
- Previous payment status
- Bill amounts
- Previous payment amounts
- Credit card payment behavior

### Target Variable

The target variable is:

`default payment next month`

It is renamed to:

`target`

The target represents whether the customer defaults on the next month's payment.

- `0` → No Default
- `1` → Default

---

## 🔍 Exploratory Data Analysis

The following operations were performed to understand the dataset:

- Dataset loading
- First and last record inspection
- Dataset shape
- Column identification
- Dataset information
- Statistical summary
- Missing value analysis
- Duplicate record detection
- Correlation analysis
- Correlation heatmap
- Target class distribution

A correlation heatmap was created using Seaborn to visualize relationships between numerical features.

---

## 🧹 Data Preprocessing

### 1. Column Renaming

Several columns were renamed to make their meaning easier to understand.

Examples:

- `PAY_0` → `SEP_PAY`
- `PAY_2` → `AUG_PAY`
- `PAY_3` → `JUL_PAY`
- `BILL_AMT1` → `SEP_BILL`
- `PAY_AMT1` → `SEP_PAYMENT`
- `default payment next month` → `target`

---

### 2. Categorical Value Conversion

Categorical values were converted into meaningful labels.

Examples:

- Gender:
  - `1` → `M`
  - `2` → `F`

- Marriage:
  - `1` → `MARRIED`
  - `2` → `SINGLE`
  - Other values → `OTHERS`

- Education:
  - `1` → `UG`
  - `2` → `PG`
  - `3` → `HIGH_SCHOOL`
  - Other values → `OTHERS`

- Target:
  - `1` → `YES`
  - `0` → `NO`

---

### 3. Outlier Treatment

Outliers were identified using boxplots.

The **Interquartile Range (IQR)** method was used to detect and limit extreme numerical values.

---

### 4. Label Encoding

Label Encoding was applied to categorical variables such as:

- Gender
- Target

---

### 5. One-Hot Encoding

One-Hot Encoding was applied to:

- Education
- Marriage

This converts categorical values into numerical features suitable for Machine Learning algorithms.

---

## ⚖️ Handling Class Imbalance

The dataset contains an imbalance between default and non-default customers.

To address this problem, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied.

SMOTE generates synthetic samples for the minority class to create a more balanced dataset.

---

## 🎯 Feature Selection

The project uses:

**SelectKBest + f_classif**

to identify the most important features for classification.

The top **25 features** were selected for model training.

Feature scores were also calculated and ranked to understand the importance of each feature.

---

## 🔄 Data Transformation

The **PowerTransformer** with the Yeo-Johnson method was used to transform numerical features and reduce skewness.

---

## 📏 Feature Scaling

**StandardScaler** was used to standardize the selected features before training the Machine Learning models.

---

## 🤖 Machine Learning Algorithms

Five classification algorithms were implemented and compared:

### 1. Logistic Regression

A linear classification algorithm used as a baseline model.

### 2. Decision Tree

A tree-based classification algorithm that makes predictions using a series of decision rules.

### 3. Random Forest

An ensemble learning algorithm that combines multiple decision trees to improve prediction performance.

### 4. AdaBoost

An ensemble algorithm that combines multiple weak learners to create a stronger classifier.

### 5. Gradient Boosting

An ensemble technique that builds models sequentially to reduce prediction errors.

---

## 📈 Model Evaluation

The models were evaluated using:

- **Accuracy**
- **Precision**
- **F1-Score**
- **Recall**
- **Classification Report**

### Evaluation Metrics

**Accuracy**  
Measures the overall percentage of correctly classified predictions.

**Precision**  
Measures how many predicted positive cases were actually positive.

**Recall**  
Measures how many actual positive cases were correctly identified.

**F1-Score**  
Provides a balance between Precision and Recall.

---

## 📊 Model Comparison

The performance of all five algorithms is stored in a Pandas DataFrame for easy comparison.

The final comparison includes:

| Model | Accuracy | Precision | F1-Score | Recall |
|---|---:|---:|---:|---:|
| Logistic Regression | - | - | - | - |
| Decision Tree | - | - | - | - |
| Random Forest | - | - | - | - |
| AdaBoost | - | - | - | - |
| Gradient Boosting | - | - | - | - |

> The values are generated when the Jupyter Notebook is executed.

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (imblearn)

---

## 📁 Project Structure

```text
Credit-Card-Default-Prediction/
│
├── credit card project.ipynb
├── creditcard.csv
└── README.md
