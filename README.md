# Machine Learning Project Name

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/yourusername/your-repo-name/blob/main/LICENSE)
[![Python Version](https://img.shields.io/badge/python-3.10%2B-green)](https://www.python.org/downloads/release/python-377/)

## Project Overview

Briefly describe the purpose and goals of your machine learning project. Explain the problem you're tackling and why it's important.

## Table of Contents


- [Dependencies](#dependencies)
- [Data](#data)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Results and Insights](#results-and-insights)
- [Future Work](#future-work)
- [Contributions and License](#contributions-and-license)



## Dependencies

List of the main libraries and packages used:
* Pandas
* Numpy
* Scikit-learn
* Scipy
* Matplotlib
* Seaborn


## Data
Data source: https://www.kaggle.com/datasets/parisrohan/credit-score-classification
DATA OVERVIEW
* 'id': A unique identifier for each data record.
* 'customer_id': An identifier for each customer, allowing you to associate multiple records with the same individual.
* 'month': The month of the data record, indicating when the data was collected or relevant.
* 'name': The name of the customer, which may be used for identification purposes.
* 'age': The age of the customer, providing information about their age demographic.
* 'ssn': The Social Security Number (SSN) of the customer, a unique identifier used for verification.
* 'occupation': The occupation or profession of the customer, which can help understand their employment status.
* 'annual_income': The annual income of the customer, a crucial financial parameter.
* 'monthly_inhand_salary': The monthly salary or income available to the customer after deductions.
* 'num_bank_accounts': The number of bank accounts held by the customer, indicating their banking activity.
* 'num_credit_card': The number of credit cards held by the customer, reflecting their credit usage.
* 'interest_rate': The interest rate associated with the customer's financial products, such as loans or credit cards.
* 'num_of_loan': The number of loans the customer has, providing insight into their debt obligations.
* 'type_of_loan': The types of loans the customer holds, which can include mortgages, personal loans, etc.
* 'delay_from_due_date': The delay in payment from the due date for loans or credit cards, indicating their payment behavior.
* 'num_of_delayed_payment': The number of delayed payments made by the customer.
* 'changed_credit_limit': Changes in the customer's credit limit, which can affect their credit utilization.
* 'num_credit_inquiries': The number of credit inquiries made by the customer, potentially affecting their credit score.
* 'credit_mix': The composition of the customer's credit accounts, which can impact their credit profile.
* 'outstanding_debt': The amount of outstanding debt owed by the customer.
* 'credit_utilization_ratio': The ratio of credit used to the total available credit, a key factor in credit scoring.
* 'credit_history_age': The age of the customer's credit history, influencing their creditworthiness.
* 'payment_of_min_amount': How customers handle the minimum payment amount on credit cards or loans.
* 'total_emi_per_month': The total Equated Monthly Installment (EMI) payments made by the customer.
* 'amount_invested_monthly': The amount the customer invests on a monthly basis, if applicable.
* 'payment_behaviour': The behavior of the customer regarding their payments, reflecting their financial responsibility.
* 'monthly_balance': The monthly balance in the customer's financial accounts.
* 'credit_score': The target variable representing the customer's credit score, which we aim to predict.

## Exploratory Data Analysis (EDA)
The data that I used has 100.000 rows and 27 features including target feature. 

## Data Preprocessing

### Categorical Features Handling Plan
* month:
int64 --> str
This column will be encoded

* occupation:
_______ values will be deleted.
Values will be imputed using the mode, which represents the most common value associated with each unique Customer_ID
This column will be encoded.

* type_of_loan:
Get every specific loan type.
Binary encoding. If a person has that specific loan type in the cell, it will be True otherwise False.
Implement mode imputer to missing values

* credit_mix:
_ values will be deleted,
Missing values will be imputed using the mode, which represents the most common value associated with each unique Customer_ID,
This column will be encoded.

* payment_of_min_amount:
NM values will be deleted,
Missing values will be imputed using the mode, which represents the most common value associated with each unique Customer_ID,
This column will be encoded.

* payment_behaviour:
!@9#%8 values will be deleted,
Missing values will be imputed using the mode, which represents the most common value associated with each unique Customer_ID,
This column will be encoded.

* credit_score:
This column is the target. There are three values; Standard, Poor, Good. They will be replaced as Poor --> 0, Good --> 1, Standard --> 2

* name / ssn / customer_id¶:
These columns will be deleted at the end of the categorical feature handling process.

## Model Building
Explain the machine learning algorithm(s) you used and any techniques for model selection or hyperparameter tuning.

## Model Evaluation
Detail how you evaluated the performance of your model(s). Include relevant metrics and discuss the results.

## Results and Insights
Share the final evaluation metrics of your model. Interpret the results in terms of the problem you aimed to solve.

## Future Work
Discuss potential improvements, enhancements, or additional analyses that could be explored in the future.

## Contributions and License
State whether you're open to contributions or feedback from others. Specify the license for your project.

This project is licensed under the MIT License.
