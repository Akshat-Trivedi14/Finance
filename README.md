# Finance
-Data and Exploratory Data Analysis (EDA) Insights
-Project Objective: The project's goal is to predict customer default payments on credit cards in Taiwan and build a model to estimate the probability of default for risk management purposes. The Kolmogorov-Smirnov (K-S) chart is the primary evaluation metric.

-Data Quality: The initial dataset contained 35 duplicate records, which were dropped, resulting in 29,965 unique records. There were no null values in the dataset.

=Target Variable Imbalance: The response variable, default payment next month (IsDefaulter), is imbalanced, with 23,335 non-defaulters ('No') and 6,630 defaulters ('Yes').

-Gender (SEX): There are more female (18,091) than male (11,874) customers in the dataset.

-Education: The majority of customers have a University (14,019) or Graduate School (10,563) education level.

-Marital Status (MARRIAGE): The customer base is predominantly Single (15,945) or Married (13,643).

-Age: The customer count peaks at age 29 (1,602), and most defaults occur in the 25-40 age range.


## 📊 Model Performance Comparison

| Model                          | Train Accuracy | Test Accuracy | Precision | Recall | F1-Score | ROC AUC Score | Key Observation |
|--------------------------------|----------------|----------------|------------|---------|-----------|----------------|------------------|
| **Logistic Regression**         | 0.849          | 0.851          | 0.769      | 0.920   | 0.838     | 0.861          | Good performance; high recall indicates it's good at identifying positive cases. |
| **Random Forest Classifier**    | 0.999          | 0.866          | 0.832      | 0.893   | 0.861     | 0.868          | Highest overall test performance, but significantly overfit on the training data. |
| **Gradient Boosting Classifier**| 0.840          | 0.839          | 0.785      | 0.880   | 0.830     | 0.843          | Acceptable performance, with better balance between train/test accuracy than Random Forest. |
| **Support Vector Classifier (SVC)** | 0.855      | 0.854          | 0.775      | 0.920   | 0.841     | 0.863          | Similar performance to Logistic Regression. |
