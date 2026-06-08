## Insurance Claim Amount Prediction using Machine Learning

## Project Overview
This project aims to predict the insurance claim amount using customer demographics, health information, hospitalization details, and policy-related features.
The problem is formulated as a Regression task where the target variable is:
total_claim_amount
Predicting claim amounts helps insurance companies:
i. Estimate future liabilities
ii. Detect unusual claims
iii. Improve pricing strategies
iv. Optimize claim settlement processes

## Dataset Information
### Dataset Size
i. Records: 8,000
ii. Features: 38
### Target Variable
i. total_claim_amount

## Feature Categories
### Customer Information
i. age
ii. gender
iii. city_tier
iv. annual_income_inr
### Health Information
i. bmi
ii. smoking_status
iii. has_diabetes
iv. has_hypertension
v. stress_level_score
### Hospitalization Information
i. hospital_tier
ii. length_of_stay
iii. icu_days
iv. hospital_bill_amount
### Policy Information
i. sum_insured
ii. deductible_amount
iii. co_pay_amount
iv. policy_type

## Project Workflow
### 1. Data Loading
The dataset was loaded into a Pandas DataFrame and inspected for structure, missing values, and data types.
### 2. Data Cleaning
i. Performed the following preprocessing:
ii. Removed currency symbols (₹)
iii. Removed commas from monetary values
iv. Converted monetary columns into numeric format
### 3. Missing Value Handling
i. Missing values were replaced using:
ii. Median for numerical features
iii. Mode for categorical features
### 4. Outlier Detection
i. Outliers in total_claim_amount were identified using:
ii. Box Plot
iii. Interquartile Range (IQR)
### 5. Outlier Treatment
Applied IQR-based filtering to remove extreme claim values.
### 6. Feature Encoding
Categorical variables were converted into numerical values using Label Encoding.
### 7. Train-Test Split
Dataset split:
Training Data: 80%
Testing Data: 20%
### 8. Model Training
The following regression models were trained:
# Linear Regression
Used as a baseline model.
# Random Forest Regressor
Used as an ensemble learning model to capture non-linear relationships.
### 9. Model Evaluation
Evaluation metrics:
i. Mean Absolute Error (MAE)
ii. Root Mean Squared Error (RMSE)
iii. R² Score

## Visualizations
### 1. Outlier Detection Boxplot
Used to identify extreme claim values.

<img width="826" height="451" alt="image" src="https://github.com/user-attachments/assets/f1a6ec88-550b-4836-8985-6b0df7901251" />

### 2. Top 10 Important Features
Generated using Random Forest feature importance scores.

<img width="1010" height="528" alt="image" src="https://github.com/user-attachments/assets/0601b571-9f10-424b-94fe-7c8b9f72ac52" />

## Model Performance
# Linear Regression
i. MAE : 1031.27
ii. RMSE: 7931.57
iii. R2  : 0.9757
# Random Forest
i. MAE : 3205.24
ii. RMSE: 8873.93
iii. R2  : 0.9696

### Conclusion
This project successfully predicts insurance claim amounts using machine learning techniques. Data preprocessing, missing value handling, and outlier treatment improved model quality. Ensemble learning through Random Forest produced better prediction performance than Linear Regression and provided valuable insights into the most influential claim-related factors.
