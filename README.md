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
- [Model Evaluation / Results and Insights](#model-evaluation)
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
#### DATA OVERVIEW
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
#### How did I approach to preprocessing to each column is explained in the notebook more clearly.
* There were very strange values almost all of the features.
* I handled one by one all of the categorical features for the sake of modularity.
* I handled numeric features in three steps; first I take care of all the float features then integer features, final step was to handle credit_history_age feature.


## Model Building
* As usually the case, transformed dataset divided by using train_test_split
* Then, standard scaler implemented to numeric features only(I didn't implement standard scaler to categorical columns which transformed to encoded binary columns). `fit_transform` used for train set, `tranform` used for test set.
* `models` and `params` dictioneries were created to be used in `GridSearchCV`
* `GridSearchCV` has executed to find best model and it's paramaters.
  

## Model Evaluation / Results and Insights
* When F1 scorer used best model was RandomForestClassifier with {'max_depth': None, 'n_estimators': 128} 
* F1 score was 0.8064 in `GridSearchCV` and 0.81 in the test set that was created in the beginning for evaluation.
* Confusion matrix and classification report:
  ![image](https://github.com/doga-yilmaz/credit_score_predictions/assets/110274753/de2ddbd7-08cf-4072-a5a5-e4ee8835bffc)



## Future Work

* The dataset initially consisted of 27 columns, but as it grew to include more than 50 columns, the computational cost increased significantly. To address this challenge and improve computational efficiency, dimension reduction techniques like PCA, LLE, and t-SNE can be implemented, allowing us to reduce the dataset's dimensionality while preserving important information for analysis and modeling.
* Additional machine learning algorithms and paramater settings can be explored with using `GridSearchCV`
* Scaler implemented to only numeric columns, all columns can be transformed by same or different scalers.
* NLP can be impelemented instead of encoding to columns like payment_behavior and type_of_loan. With doing this we can have less columns

## Contributions and License
I am open to contributions. This project was my first experience, so I welcome and appreciate any feedback., I am waiting for your feedbacks to imporove myself.

This project is licensed under the MIT License.

Contact via LinkedIn: https://www.linkedin.com/in/doğa-yılmaz-779105247/
