# predicting-house-price-using-linear-regression
# 🏠 House Price Prediction Using Linear Regression

## 📌 Project Overview

This project focuses on predicting house prices using **Machine Learning regression techniques**.

An end-to-end machine learning workflow was developed, covering data inspection, exploratory data analysis, data cleaning, missing-value treatment, categorical feature encoding, model training, evaluation, and model comparison.

**Linear Regression** was used as the primary predictive model and its performance was compared with **Ridge Regression**.

---

## 🎯 Project Objective

The main objective of this project is to build a machine learning model capable of predicting house prices based on property characteristics.

The project aims to:

* Explore the factors associated with house prices
* Clean and preprocess real-world housing data
* Handle missing numerical and categorical values
* Encode categorical variables
* Build regression models
* Evaluate model performance using multiple metrics
* Compare Linear Regression with Ridge Regression
* Interpret model coefficients and their relationship with house prices

---

## 📊 Dataset

**Dataset:** Ames Housing Dataset
**Source:** Kaggle

### Dataset Size

* **2,930 rows**
* **82 columns**

### Target Variable

`SalePrice` — House selling price

The dataset contains a combination of numerical and categorical property characteristics, including:

* Area measurements
* Number of rooms
* Garage information
* Basement information
* Year built and remodelled
* Property quality attributes
* Neighborhood
* House style
* Exterior type
* Kitchen quality
* Garage type
* Sale condition

---

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computing
* **Scikit-learn** — Machine learning and preprocessing
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook**

---

# 🔄 Project Workflow

## 1. Data Loading & Inspection

The Ames Housing dataset was loaded and inspected using Pandas.

The initial analysis included:

* Checking dataset dimensions
* Reviewing feature names
* Examining data types
* Inspecting the overall dataset structure using `df.info()`

---

## 2. Exploratory Data Analysis

Descriptive statistics were generated to understand the characteristics and distributions of the dataset.

The analysis included:

* Mean
* Standard deviation
* Minimum values
* Maximum values
* Feature distributions

### Target Variable Analysis

The distribution of `SalePrice` was examined using a histogram with KDE to understand house price variation across the dataset.

---

## 3. Data Cleaning & Preprocessing

The dataset contained missing values across multiple features.

### High-Missing-Value Features

Features with extremely high proportions of missing values were removed:

* `Pool QC`
* `Misc Feature`
* `Alley`
* `Fence`

### Numerical Features

Missing numerical values were handled using **median imputation**.

### Categorical Features

Missing categorical values were handled by replacing them with the `"None"` category where appropriate.

After preprocessing:

**No missing values remained in the processed dataset.**

---

## 4. Feature Analysis

### Correlation Analysis

A correlation heatmap was created to examine relationships between numerical variables and `SalePrice`.

This helped identify features that showed stronger relationships with house prices.

### Feature Coefficients

After model training, Linear Regression coefficients were analyzed to understand the direction of feature effects.

* **Positive coefficient:** Associated with an increase in predicted house price.
* **Negative coefficient:** Associated with a decrease in predicted house price.

---

## 5. Data Preparation

The dataset was divided into input features and the target variable.

```text
X = Input Features
y = SalePrice
```

### Train-Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

The split was performed using `train_test_split()` with:

```text
random_state = 42
```

---

## 6. Feature Encoding & Preprocessing Pipeline

Since the dataset contains both numerical and categorical variables, a preprocessing pipeline was developed using Scikit-learn.

### Numerical Features

* Median imputation for missing values

### Categorical Features

* Missing-value handling
* One-Hot Encoding
* Unknown category handling

The preprocessing steps were combined with the machine learning models using a **Scikit-learn Pipeline**.

---

# 🤖 Machine Learning Models

## 1. Linear Regression

Linear Regression was used as the primary predictive model.

The model learns relationships between property characteristics and house prices and uses these relationships to generate price predictions.

---

## 2. Ridge Regression

Ridge Regression was implemented as a regularized alternative to Linear Regression.

Its purpose was to:

* Reduce potential overfitting
* Introduce regularization
* Compare its predictive performance with standard Linear Regression

The model was configured with:

```text
alpha = 1
```

---

# 📏 Model Evaluation

The models were evaluated using three performance metrics.

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted house prices.

### Root Mean Squared Error (RMSE)

Measures prediction error in the original price units.

### R² Score

Measures the proportion of variation in house prices explained by the model.

A higher R² indicates better explanatory performance.

---

# 📊 Model Results

| Model                 |          MSE |          RMSE |     R² Score |
| --------------------- | -----------: | ------------: | -----------: |
| **Linear Regression** | 2.112274e+09 | **45,959.48** | **0.736544** |
| Ridge Regression      | 7.512047e+09 |     86,672.06 |     0.063049 |

### 🏆 Best Performing Model

**Linear Regression** achieved the best performance among the two evaluated models.

* **R² Score:** 0.7365
* **RMSE:** 45,959.48
* **MSE:** 2.112274e+09

The Linear Regression model explains approximately **73.65% of the variation in house prices** in the test data.

---

# 📈 Visualizations

The project includes several visualizations to understand the dataset and evaluate model performance.

### 1. House Price Distribution

A histogram with KDE was used to visualize the distribution of `SalePrice`.

### 2. Correlation Heatmap

A heatmap was created to identify relationships between numerical variables and house prices.

### 3. Actual vs. Predicted Prices

This visualization compares the actual house prices with the prices predicted by the model.

### 4. Residual Plot

A residual plot was used to examine prediction errors and assess the model's residual behaviour.

---

# 💡 Key Insights

The analysis demonstrates how property characteristics can be used to predict house prices through regression modelling.

Key observations include:

* Housing data contains both numerical and categorical variables requiring different preprocessing approaches.
* Missing-value treatment is an important part of preparing real-world datasets for machine learning.
* One-Hot Encoding allows categorical property characteristics to be incorporated into regression models.
* Linear Regression provided substantially better predictive performance than the evaluated Ridge Regression configuration.
* Model coefficients can provide useful information about the direction of relationships between features and predicted house prices.

---

# 🧠 Key Skills Demonstrated

This project demonstrates practical experience in:

* Exploratory Data Analysis
* Data Cleaning
* Missing Value Treatment
* Feature Preprocessing
* One-Hot Encoding
* Train-Test Splitting
* Machine Learning Pipelines
* Linear Regression
* Ridge Regression
* Model Evaluation
* MSE, RMSE & R²
* Residual Analysis
* Feature Coefficient Interpretation
* Data Visualization
* Model Comparison

---

# ✅ Conclusion

This project successfully developed an end-to-end machine learning workflow for **house price prediction** using the Ames Housing Dataset.

Two regression models were evaluated: **Linear Regression** and **Ridge Regression**.

Based on the reported test results, **Linear Regression performed substantially better**, achieving an R² score of **0.7365** and an RMSE of **45,959.48**.

The project demonstrates how data preprocessing, feature encoding, regression modelling, and model evaluation can be combined to build a practical machine learning solution for predicting house prices.

---

# 📁 Project Structure

```text
House-Price-Prediction/
│
├── House_Price_Prediction.ipynb
├── train.csv
├── README.md
│
└── images/
    ├── house_price_distribution.png
    ├── correlation_heatmap.png
    ├── actual_vs_predicted.png
    └── residual_plot.png
```

---

## 👩‍💻 Author

**Amna Naveed**
MPhil Statistics | Data Analyst
