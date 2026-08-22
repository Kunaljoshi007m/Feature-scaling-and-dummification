# Feature Scaling and Dummification
---

## Aim

To understand and implement various **feature preprocessing techniques** used in Machine Learning, including:

* Feature Scaling
* Standardization
* Normalization
* Robust Scaling
* Clustering
* Missing Value Handling
* Categorical Data Encoding
* One-Hot Encoding
* Dictionary-Based Encoding
* Ordinal Encoding
* KNN-Based Class Imputation
* Handling Imbalanced Classes

---

# Numerical Data Processing

## Dataset

**Heart Disease Dataset**

Dataset file:

`heart.csv`

The dataset contains patient-related attributes such as:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Fasting Blood Sugar
* Resting ECG
* Maximum Heart Rate
* Exercise-Induced Angina
* Oldpeak
* Slope
* Number of Major Vessels
* Thalassemia
* Target

---

## Topics Covered

### 1. Min-Max Scaling

Min-Max Scaling transforms numerical values into a specified range, in this practical **0 to 1**.

The `age` feature was scaled using Min-Max Scaling.

### Result

The age values were converted into values between 0 and 1.

---

### 2. Standardization

Z-Score Standardization was applied to the `trestbps` feature.

Standardization transforms the feature so that:

* Mean ≈ 0
* Standard Deviation ≈ 1

### Result

The standardized `trestbps` feature obtained:

* Mean: **0**
* Standard Deviation: **1.0**

---

### 3. Robust Scaling

Robust Scaling was applied to the `chol` feature.

This technique is useful when numerical data contains **outliers**, as it uses the median and interquartile range instead of the mean and standard deviation.

---

### 4. Normalization

Normalization was performed using the `age` and `thalach` features.

Two normalization techniques were explored:

* **L2 Normalization**
* **Max Normalization**

L2 normalization scales observations based on their Euclidean norm, while Max normalization scales each observation according to its maximum value.

---

### 5. K-Means Clustering

K-Means clustering was used to group patients based on:

* Age
* Cholesterol

Two clusters were created.

A new **group** attribute was assigned to each observation to identify its cluster.

---

### 6. Handling Missing Numerical Values

Missing numerical values were introduced into sample data containing:

* `oldpeak`
* `chol`

Three approaches were explored:

#### Dropping Missing Observations

Rows containing missing values were removed.

#### Mean Imputation

Missing values were replaced with the mean of the corresponding feature.

#### Median Imputation

Missing values were replaced with the median of the corresponding feature.

### Result

Both mean and median imputation successfully replaced the missing numerical values while retaining all observations.

---

# Categorical Data & Imbalanced Classes

## Dataset

**Laptop Price Dataset**

Dataset file:

`laptop_price.csv`

Important attributes include:

* Company
* Type Name
* RAM
* Operating System
* Screen Size
* Price

---

## Topics Covered

### 1. Data Preparation

The `RAM` feature originally contains values such as:

* 4GB
* 8GB
* 16GB
* 32GB

The RAM values were converted into numerical form for use in further machine-learning operations.

---

### 2. One-Hot Encoding

One-Hot Encoding was performed on the `TypeName` categorical feature.

The dataset contains categories such as:

* 2 in 1 Convertible
* Gaming
* Netbook
* Notebook
* Ultrabook
* Workstation

Each category was represented using binary numerical features.

---

### 3. Dictionary-Based Feature Encoding

Dictionary-based encoding was performed using:

* Company
* Operating System

The categorical values were transformed into numerical feature representations.

The generated features included different companies and operating systems such as:

* Acer
* Apple
* Asus
* Dell
* HP
* Lenovo
* MSI
* Windows 10
* Linux
* macOS
* Chrome OS
* Android

---

### 4. Binning and Ordinal Encoding

The `Price_euros` feature was divided into three categories:

| Category | Rank |
| -------- | ---: |
| Low      |    1 |
| Medium   |    2 |
| High     |    3 |

This demonstrates how continuous numerical data can be converted into ordered categorical groups.

---

### 5. Missing Class Imputation Using KNN

K-Nearest Neighbors classification was used to predict artificially removed values from the `OpSys` feature.

The prediction used features such as:

* Price
* Screen Size
* RAM

### Result

The missing operating-system classes were predicted as:

* Windows 10
* Windows 10

---

### 6. Handling Imbalanced Classes

A Random Forest Classifier with **balanced class weights** was used to demonstrate handling of imbalanced classes.

The `Company` feature was used as the target class.

The dataset contains companies such as:

* Acer
* Apple
* Asus
* Dell
* HP
* Lenovo
* MSI
* Microsoft
* Razer
* Samsung
* Xiaomi
* And other laptop manufacturers

Using balanced class weights helps give appropriate importance to classes that have fewer observations.

---

# Techniques Used

| Technique              | Purpose                                                           |
| ---------------------- | ----------------------------------------------------------------- |
| Min-Max Scaling        | Scale numerical features between a fixed range                    |
| Standardization        | Convert features to a standard distribution                       |
| Robust Scaling         | Scale data while reducing the effect of outliers                  |
| L2 Normalization       | Normalize observations using Euclidean norm                       |
| Max Normalization      | Normalize observations using their maximum value                  |
| K-Means                | Group similar observations into clusters                          |
| Mean Imputation        | Replace missing values with the mean                              |
| Median Imputation      | Replace missing values with the median                            |
| One-Hot Encoding       | Convert nominal categories into binary features                   |
| Dictionary Encoding    | Convert dictionary-based categorical data into numerical features |
| Binning                | Convert continuous values into categories                         |
| Ordinal Encoding       | Represent ordered categories numerically                          |
| KNN Classification     | Predict missing categorical class values                          |
| Balanced Random Forest | Handle imbalanced classes                                         |

---

# Tools & Technologies

* **Python**
* **NumPy**
* **Pandas**
* **Scikit-learn**
* **Jupyter Notebook / Google Colab**

---

# Repository Structure

```text
feature-scaling-and-dummification/
│
├── README.md
├── heart.csv
├── laptop_price.csv
├── practical_3A.py
└── practical_3B.py
```

---

# Learning Outcomes

After completing this practical, the following concepts were understood:

* How to scale numerical features
* Difference between normalization and standardization
* How robust scaling handles outliers
* How K-Means can group observations
* Different methods for handling missing numerical values
* How categorical variables can be converted into numerical representations
* How One-Hot Encoding works
* How dictionary-based encoding represents categorical features
* How continuous values can be converted into ordered categories
* How KNN can be used to predict missing categorical classes
* How balanced class weights can help with imbalanced datasets

---

# Conclusion

Practical 3A and 3B demonstrate essential **data preprocessing and feature engineering techniques** used in Machine Learning.

Practical 3A focuses primarily on **numerical data**, including scaling, standardization, normalization, clustering, and missing-value handling.

Practical 3B focuses on **categorical data and imbalanced classes**, including one-hot encoding, dictionary encoding, ordinal encoding, KNN-based class prediction, and balanced classification.

Together, these practicals provide a foundation for preparing real-world datasets before applying Machine Learning algorithms.
