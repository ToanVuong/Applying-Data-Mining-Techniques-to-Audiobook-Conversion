# Applying Data Mining Techniques to Audiobook Conversion

## 1. Project Introduction

This project focuses on analyzing audiobook user behavior data to predict the likelihood of **customer conversion / continued purchases**.

### Background

* Audiobooks are becoming increasingly popular and are gradually changing consumer behavior.
* The objective of this project is to study the factors influencing customer conversion.
* The data was collected over **2 years**, and conversion outcomes were tracked over an additional **6 months**.

### Objectives

* Analyze customer audiobook usage behavior
* Build a predictive model for customer repurchase likelihood
* Segment potential customers to propose appropriate business strategies

---

## 2. Team Information

* **Supervisor:** Assoc. Prof. Dr. Tran Minh Quang
* **Group:** 05

### Team Members

* Hoang Anh Khoa – 2470601
* Le Minh – 2110354
* Pham Thanh Tu – 2491076
* Le Quoc Thang – 2110549
* Vuong Minh Toan – 2491057

---

## 3. Dataset

The dataset consists of **14,084 rows** and **12 columns**, with no missing values.

### Key Features

* **Book_length(mins)_length**: Total audiobook duration (minutes)
* **Price_overall**: Total price of the book
* **Price_avg**: Average price
* **Review**: Number of reviews
* **Review10/10**: Average rating (scale of 10)
* **Minutes_listened**: Total listening time
* **Completion**: Completion rate
* **Support_requests**: Number of support requests
* **Target**: Target variable – whether the customer continues purchasing

### Feature Groups

* **Content**: book duration, total price, average price
* **Behavior**: reviews, average rating, listening time, completion rate
* **Interaction**: support requests, repurchase decision

---

## 4. Methodology

The analysis was conducted using **Python in Jupyter Notebook**.

### Main Steps

1. Exploratory data analysis
2. Data preprocessing
3. Descriptive statistics
4. Random Forest model building
5. Model evaluation
6. Customer segmentation and strategy recommendations

---

## 5. Exploratory Data Analysis

* **Histograms** were used to observe the distribution of variables
* Examined data distribution before preprocessing

---

## 6. Data Preprocessing

### Purpose

Preprocessing helps clean and standardize data before feeding it into the model, improving accuracy and reliability.

### Steps

* Data loading
* Missing value checking
* Removing or imputing missing values
* Outlier detection and removal
* Data normalization (if necessary)

### Methods Used

* **IQR (Interquartile Range)**
* **Z-score**

### Results

* Original dataset: **14,084 rows**
* After removing outliers in **Book_length(mins)_length** and **Support_requests**: **13,467 rows**

### Observations

* Presence of many outliers
* Uneven variable distributions
* Some features show high variance

---

## 7. Descriptive Statistics

Statistical measures include:

* Mean
* Standard deviation (std)
* Min / Max
* Percentiles

Additionally, the team used:

* **Scatter plots** to observe relationships between variables
* **Correlation analysis** to evaluate feature relationships
* **Target distribution analysis** to check class balance

---

## 8. Model: Random Forest

### Introduction

Random Forest is a machine learning model in the **ensemble learning** family, combining multiple **decision trees** to improve accuracy.

It was introduced by Leo Breiman in 2001 and is commonly used for:

* **Classification**
* **Regression**

### Core Techniques

* **Bagging (Bootstrap Aggregation)**
* **Random Feature Selection**

### Bootstrap Sampling

A technique that samples data with replacement to create multiple subsets for training decision trees.

### Bagging

* Create multiple subsets using bootstrap sampling
* Train each decision tree on a different subset
* Aggregate results:

  * **Classification**: majority voting
  * **Regression**: average prediction

### Random Feature Selection

Randomly select a subset of features at each node to increase diversity and reduce overfitting.

### Random Forest Workflow

1. Split data using bootstrap sampling
2. Randomly select feature subsets at each node
3. Train individual decision trees
4. Aggregate predictions from all trees

### Advantages

* Reduces overfitting
* Works well with large datasets and many features
* Strong generalization ability

### Disadvantages

* Slower with very large datasets
* Difficult to interpret
* Not optimal for highly imbalanced data

### Key Parameters

* **n_estimators**: number of trees
* **max_features**: number of features per split
* **bootstrap**: whether to use bootstrap sampling
* **max_samples**: proportion of data per tree
* **max_depth**: maximum depth of trees

---

## 9. Evaluation Metrics

* **Precision**: proportion of correct positive predictions
* **Recall**: ability to identify actual positives
* **F1-score**: harmonic mean of Precision and Recall
* **Macro Average**: unweighted mean across classes
* **Weighted Average**: weighted mean based on class size

---

## 10. Model Results

The team performed:

* Determination of **optimal threshold**
* **Confusion Matrix analysis**
* Model evaluation using Precision, Recall, and F1-score

> Note: The presentation file does not include detailed numerical values, so this README focuses on methodology and key concepts.

---

## 11. Customer Segmentation & Strategy

### Feature Importance

The team identified key features and used the **top 4 most influential features** for customer segmentation.

### Segmentation Results

* **High-potential customers**:

  * Frequent return behavior
  * Higher spending

* **Low-potential customers**:

  * Low purchase frequency
  * Limited spending

### Strategy Recommendations

#### For High-Potential Customers

* Focus on retention
* Personalize recommendations
* Promote high-value products
* Offer tailored incentives to increase customer lifetime value

#### For Low-Potential Customers

* Attract with promotions
* Recommend affordable products
* Improve user experience
* Increase likelihood of future conversion

---

## 12. Tools Used

* Python
* Jupyter Notebook
* Data visualization techniques (Histogram, Boxplot, Scatter Plot, Correlation Heatmap)
* Random Forest model

---

## 13. Conclusion

The project applied a comprehensive data mining pipeline, from data exploration and preprocessing to modeling and customer segmentation.

Results indicate that Random Forest is an effective approach for predicting audiobook customer conversion and provides a foundation for developing targeted business strategies.

---

## 14. Future Work

* Compare Random Forest with other models such as Logistic Regression, XGBoost, LightGBM
* Hyperparameter tuning using Grid Search / Random Search
* Handle imbalanced data using SMOTE or class weighting
* Build dashboards for monitoring customer segments
* Integrate the model into recommendation systems / CRM

