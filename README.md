# Loan Default Prediction

This repository contains a machine learning project that aims to predict loan defaults using a variety of data preprocessing, exploration, and modeling techniques. The dataset used is structured with various features related to loan information, borrower characteristics, and loan status.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Data Exploration](#data-exploration)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)
- [License](#license)

---

## Project Overview
Loan default prediction is crucial for financial institutions to reduce risk and improve lending practices. This project uses data exploration, feature engineering, and machine learning techniques to build a predictive model for loan defaults.

## Features
The dataset contains the following main features:

1. **loan_amnt**: The loan amount requested.
2. **term**: Loan duration in months (36 or 60).
3. **int_rate**: Interest rate.
4. **installment**: Monthly payment amount.
5. **grade and sub_grade**: Loan grading provided by the lender.
6. **emp_title**: Job title of the borrower.
7. **emp_length**: Employment length in years.
8. **home_ownership**: Type of home ownership (Rent, Own, Mortgage).
9. **annual_inc**: Annual income.
10. **verification_status**: Whether the income was verified.
11. **loan_status**: Target variable (Fully Paid or Charged Off).
12. **purpose**: Purpose of the loan.
13. **other fields**: Including address, zip code, dti (debt-to-income ratio), credit lines, and more.

## Installation

### Prerequisites
Ensure that you have the following packages installed:
- Python 3.6+
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scipy
- scikit-learn
- imbalanced-learn (for SMOTE)

### Set Up
1. Clone the repository:
   ```bash
   git clone https://github.com/username/repo-name.git
   cd repo-name

Data Exploration

Initial data exploration focuses on understanding the distribution of key features and examining potential relationships with the target variable loan_status. Key aspects include:

Descriptive statistics of numerical and categorical features.
Correlation analysis to identify multicollinearity.
Target variable distribution.
Visualization of feature relationships.

Data Preprocessing
Data preprocessing involves:

Handling Missing Values: Imputing missing values in features like mort_acc based on mean values grouped by total_acc.
Outlier Treatment: Removing outliers using z-score methods to ensure robust model performance.
Feature Engineering: Creating binary flags for features like pub_rec, mort_acc, and pub_rec_bankruptcies.
One-Hot Encoding: Encoding categorical variables like purpose, home_ownership, grade, and others.
Scaling: Normalizing numerical features using MinMaxScaler.

Modeling
The project uses LogisticRegression as the primary model. Steps include:

Data Splitting: Splitting the data into training and testing sets with a stratified sampling approach.
SMOTE Oversampling: Handling class imbalance using SMOTE.
Cross-Validation: Evaluating model performance with KFold cross-validation to ensure model generalization.
Hyperparameter Tuning: Fine-tuning model parameters to improve accuracy.

Evaluation
Model performance is assessed through:

Confusion Matrix: Visualizing true positives, false positives, true negatives, and false negatives.
Classification Report: Precision, recall, F1-score, and accuracy metrics.
ROC-AUC Score: Measuring model discrimination ability.
Precision-Recall Curve: Examining model performance in imbalanced settings.
