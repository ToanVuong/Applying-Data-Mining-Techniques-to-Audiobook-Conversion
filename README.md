# 🎧 Applying Data Mining Techniques to Audiobook Conversion

## 📌 1. Project Introduction

This project focuses on analyzing audiobook user behavior data to predict the likelihood of **customer conversion / continued purchases**.

### Background

* Audiobooks are increasingly popular and reshaping consumer behavior
* The project aims to identify factors influencing customer conversion
* Data was collected over **2 years**, with outcomes tracked for **6 additional months**

### Objectives

* 🔍 Analyze audiobook usage behavior
* 🤖 Build a predictive model for repurchase likelihood
* 🎯 Segment customers for business strategy recommendations

---

## 👥 2. Team Information

* **Supervisor:** Assoc. Prof. Dr. Tran Minh Quang
* **Group:** 05

### Team Members

* Hoang Anh Khoa – 2470601
* Le Minh – 2110354
* Pham Thanh Tu – 2491076
* Le Quoc Thang – 2110549
* Vuong Minh Toan – 2491057

---

## 📊 3. Dataset

* 📦 **14,084 rows** | **12 columns**
* No missing values

### Key Features

* **Book_length(mins)_length**: Duration
* **Price_overall / Price_avg**: Pricing
* **Review / Review10/10**: Ratings
* **Minutes_listened**: Listening time
* **Completion**: Completion rate
* **Support_requests**: Support interactions
* **Target**: Repurchase prediction

### Feature Groups

* Content
* Behavior
* Interaction

---

## ⚙️ 4. Methodology

* Python + Jupyter Notebook

### Main Steps

1. 🔍 Exploratory Data Analysis
2. 🧹 Data Preprocessing
3. 📊 Descriptive Statistics
4. 🌲 Random Forest Modeling
5. 📏 Model Evaluation
6. 🎯 Customer Segmentation

---

## 📈 5. Exploratory Data Analysis

* Use Histogram to observe distributions
* Inspect data before preprocessing

---

## 🧹 6. Data Preprocessing

### Purpose

Improve data quality to enhance model accuracy

### Steps

* Load data
* Check missing values
* Remove or impute missing data
* Remove outliers
* Normalize if needed

### Methods

* IQR
* Z-score

### Results

* 📉 From **14,084 → 13,467 rows**

### Observations

* Presence of outliers
* Uneven distributions
* Some features show high variance

---

## 📊 7. Descriptive Statistics

* Mean, Std, Min, Max, Percentiles

### Additional Analysis

* Scatter Plot
* Correlation Analysis
* Target Distribution

---

## 🌲 8. Model: Random Forest

### Introduction

Random Forest is an ensemble learning model that combines multiple decision trees to improve accuracy.

### Core Techniques

* Bagging
* Random Feature Selection

### Workflow

1. Bootstrap sampling
2. Random feature selection
3. Train decision trees
4. Aggregate predictions

### Advantages

* ✅ Reduce overfitting
* 📊 Strong performance on large datasets
* 🌍 Good generalization

### Disadvantages

* ⚠️ Slower on large data
* Hard to interpret
* Not ideal for highly imbalanced data

### Key Parameters

* n_estimators
* max_features
* bootstrap
* max_samples
* max_depth

---

## 📏 9. Evaluation Metrics

* Precision
* Recall
* F1-score
* Macro Average
* Weighted Average

---

## 📊 10. Model Results

* 🎯 Optimal threshold selection
* Confusion Matrix analysis
* Evaluation using classification metrics

> Note: Detailed metric values are not included in the presentation

---

## 👥 11. Customer Segmentation & Strategy

### Feature Importance

Top 4 most influential features were selected

### Segments

* 💎 High-potential customers: frequent return, higher spending
* ⚪ Low-potential customers: low frequency, limited spending

### Strategies

**High-potential**

* 🔒 Focus on retention
* 🎯 Personalize recommendations
* 💰 Promote high-value products

**Low-potential**

* 🏷️ Use promotions
* 💵 Recommend affordable products
* ⚡ Improve user experience

---

## 🛠️ 12. Tools Used

* Python
* Jupyter Notebook
* Data visualization (Histogram, Boxplot, Scatter Plot, Heatmap)
* Random Forest

---

## 🏁 13. Conclusion

The project applied a complete data mining pipeline and demonstrated that Random Forest is effective for predicting audiobook customer conversion.

---

## 🚀 14. Future Work

* Compare with other models (Logistic Regression, XGBoost, LightGBM)
* Hyperparameter tuning
* Handle imbalanced data
* Build dashboards
* Integrate into CRM / recommendation systems


👉 “ít chữ hơn – nhìn như slide thuyết trình 10 điểm”
👉 hoặc version “chuẩn ATS CV (đi apply ML/Data)” 👍
