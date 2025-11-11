### 🚗 OLA Driver Attrition Prediction
📌 Project Overview

This project focuses on predicting driver attrition (whether a driver will leave the company or not) for Ola, an Indian transportation company providing ride-hailing services.
As a Data Scientist in the Analytics Department, the goal is to analyze and model the driver data from 2019–2020 to identify key factors contributing to attrition and build predictive models using Ensemble Learning techniques.

🧾 Problem Statement

To predict whether a driver will leave the company or not based on their demographic, performance, and business-related data.

📂 Dataset Description
Column Name	Description
MMMM-YY	Reporting Date (Monthly)
Driver_ID	Unique ID for each driver
Age	Age of the driver
Gender	Gender (0 = Male, 1 = Female)
City	City Code of the driver
Education_Level	0 = 10+, 1 = 12+, 2 = Graduate
Income	Monthly average income
Date_of_Joining	Joining date of the driver
Last_Working_Date	Last working day of the driver (if applicable)
Joining_Designation	Designation at the time of joining
Grade	Grade at the time of reporting
Total_Business_Value	Total business acquired in a month
Quarterly_Rating	Rating on a scale of 1–5
🧠 Concepts Tested

Ensemble Learning: Bagging, Boosting (GBDT, XGBoost), Stacking

KNN Imputation of Missing Values

Handling Imbalanced Dataset

Feature Engineering and Aggregation

🧩 Tasks Performed
1️⃣ Exploratory Data Analysis (EDA)

Checked data shape and data types

Displayed statistical summary of all attributes

Conducted univariate analysis (distribution plots, histograms)

Performed bivariate analysis (correlation plots, pair plots)

2️⃣ Data Pre-processing
a. Data Type Conversion

Converted date columns (Date_of_Joining, Last_Working_Date, MMMM-YY) to datetime format

b. Missing Value Treatment

Checked for missing values

Applied KNN Imputation (only on numerical features)

c. Data Aggregation

Aggregated multiple records per driver using GroupBy Driver_ID

d. Feature Engineering

Created new derived features:

Quarterly_Rating_Increase: 1 if the rating improved

Income_Increase: 1 if monthly income increased

Target: 1 if Last_Working_Date is present (indicating driver left)

e. Statistical Summary

Summarized the derived dataset post feature engineering

f. Correlation Analysis

Visualized correlations between independent variables

g. Encoding

Encoded categorical variables using Label Encoding / One-Hot Encoding

h. Class Imbalance Treatment

Handled imbalance using SMOTE (Synthetic Minority Oversampling Technique)

i. Scaling

Applied StandardScaler / MinMaxScaler for normalization

3️⃣ Model Building

Applied multiple ensemble learning methods:

🪵 Bagging

Implemented Random Forest Classifier

🚀 Boosting

Implemented Gradient Boosting Decision Trees (GBDT)

Implemented XGBoost with hyperparameter tuning

🧱 Stacking

Combined multiple base learners to improve performance

4️⃣ Model Evaluation
a. Classification Report

Displayed precision, recall, F1-score, and accuracy for each model

b. AU-ROC Curve

Plotted ROC curves for model comparison

c. Insights

Identified key factors influencing driver attrition

Compared model performance and discussed trade-offs

📊 Results Summary
Model	Accuracy	Precision	Recall	F1-Score	ROC-AUC
Random Forest (Bagging)	...	...	...	...	...
GBDT (Boosting)	...	...	...	...	...
XGBoost (Boosting + Tuning)	...	...	...	...	...
Stacking Classifier	...	...	...	...	...

(Fill actual results after training)

💡 Key Insights

Drivers with low quarterly ratings, low income growth, and lower grades were more likely to leave.

Boosting models (especially XGBoost) provided superior performance due to better handling of class imbalance and feature interactions.

Feature engineering significantly improved model interpretability and accuracy.

🧰 Technologies Used
Category	Tools / Libraries
Language	Python
Data Analysis	Pandas, NumPy
Visualization	Matplotlib, Seaborn
Machine Learning	Scikit-learn, XGBoost
Imputation	KNNImputer
Imbalance Handling	SMOTE
Model Evaluation	Scikit-learn metrics
📁 Project Structure
📦 OLA_Driver_Attrition_Prediction
│
├── 📄 README.md
├── 📊 OLA_Driver_Attrition.ipynb
├── 📂 data/
│   ├── ola_driver_data.csv
│
├── 📂 models/
│   ├── random_forest.pkl
│   ├── xgboost.pkl
│
├── 📂 visuals/
│   ├── correlation_heatmap.png
│   ├── roc_curves.png
│
└── 📄 requirements.txt

🏁 Conclusion

This project demonstrates a full data science workflow — from EDA and data cleaning to feature engineering, model building, and evaluation — for predicting driver attrition.
It leverages ensemble learning techniques to achieve a balance between accuracy and interpretability, providing actionable insights for Ola’s HR and operations teams.
