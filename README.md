Customer Churn Analysis

Introduction

This project provides an in-depth analysis of customer churn using a dataset containing various customer attributes. Customer churn, or attrition, is a critical business metric representing the rate at which customers stop using a service or product. Understanding the drivers behind churn is essential for developing effective retention strategies and maintaining a healthy customer base. This repository contains the Python notebook used for exploratory data analysis (EDA) to identify patterns and insights related to customer churn.

Objective
The primary objectives of this project are:

To perform data loading, cleaning, and preprocessing to prepare the dataset for analysis.

To conduct comprehensive exploratory data analysis (EDA) to uncover significant factors influencing customer churn.

To quantify the overall churn rate and examine churn across different customer segments and service categories.

To visualize the relationships between various features (demographics, services, billing) and churn behavior.

To present data-driven insights that can assist businesses in formulating targeted customer retention initiatives.

Implementation Steps
My analysis for this project involved the following steps, as executed in the provided Jupyter notebook:

Data Loading and Initial Inspection:

The Customer Churn.csv dataset was loaded into a Pandas DataFrame.

An initial df.info() check confirmed 7043 entries and 21 columns, with data types including object, int64, and float64.

df.head() was used to display the first few rows, showing columns such as customerID, gender, SeniorCitizen, Partner, Dependents, tenure, various service types, Contract, PaperlessBilling, PaymentMethod, MonthlyCharges, TotalCharges, and Churn.

Data Preprocessing and Cleaning:

Identified that the TotalCharges column contained blank spaces for some entries. These were replaced with '0' and then converted to float data type using df["TotalCharges"].replace(" ", "0").astype("float").

Checked for missing values using df.isnull().sum(), confirming no missing values across all columns after the TotalCharges conversion.

Checked for duplicate rows using df.duplicated().sum(), finding 0 duplicate rows.

Verified for duplicate customerID values using df['customerID'].duplicated().sum(), confirming 0 duplicate customer IDs.

Converted the SeniorCitizen numerical column (0/1) into a more readable categorical format ('no'/'yes') for better interpretability during analysis.

Exploratory Data Analysis (EDA) and Visualization:

Calculated and visualized the overall churn distribution.

Analyzed churn counts and percentages across various categorical features like gender, Contract, InternetService, and PaymentMethod using seaborn.countplot and matplotlib.pyplot.pie.

Explored the descriptive statistics of numerical columns (SeniorCitizen, tenure, MonthlyCharges, TotalCharges) using df.describe().

Results
Based on the detailed analysis within the notebook, the following quantitative results and key observations were obtained:

Overall Churn Distribution:

A total of 7043 customers were analyzed.

5174 customers did not churn (remained with the service).

1869 customers churned (left the service).

This translates to an overall churn rate of approximately 26.54% (1869 / (5174 + 1869) * 100), with 73.46% of customers retained.

Gender-wise Churn:

Female Churn: Out of 3488 female customers, 939 churned.

Male Churn: Out of 3555 male customers, 930 churned.

The churn rate is very similar between genders, indicating gender is not a primary churn predictor.

Churn by Contract Type:

Month-to-month contracts: Showed the highest churn numbers, with 1655 customers churning out of 3875 on this contract type. This represents a churn rate of approximately 42.7% for this group.

One year contracts: Only 166 customers churned out of 1473, a churn rate of approximately 11.3%.

Two year contracts: Only 48 customers churned out of 1695, indicating a very low churn rate of approximately 2.8%. This clearly shows that longer contracts lead to significantly lower churn.

Churn by Internet Service:

Fiber optic internet service users accounted for 1297 churned customers, the highest among internet service types, out of 3096 customers with Fiber optic. This is a churn rate of approximately 41.9% for this group.

DSL internet service users had 459 churned customers out of 2421 with DSL, a churn rate of approximately 18.9%.

Customers with No internet service had the lowest churn, with only 113 churned customers out of 1522 in this category, a churn rate of approximately 7.4%.

Churn by Payment Method:

Electronic check was associated with the highest number of churned customers, with 1294 churns out of 2365 using this payment method. This is a churn rate of approximately 54.7% for this group.

Mailed check had 308 churns out of 1612 customers, a churn rate of approximately 19.1%.

Bank transfer (automatic) had 258 churns out of 1544 customers, a churn rate of approximately 16.7%.

Credit card (automatic) had 232 churns out of 1522 customers, a churn rate of approximately 15.2%.

Contact Information
Name: Pranjal Joshi

Email: pranjaljoshi2811@gmail.com

GitHub: https://github.com/pranjal2811

LinkedIn: https://www.linkedin.com/in/pranjaljoshi2811
