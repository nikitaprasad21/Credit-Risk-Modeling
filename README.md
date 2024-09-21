# Credit Card User Risk Segmentation Project

## Project Background
This project was conducted for a leading financial institution, the company has been operational for over 15 years and operates in the banking sector, offering a wide range of credit cards and loans to its customers. The main objective of this project was to segment credit card users based on their risk levels. It aimed to develop a machine learning  model that accurately predicts the risk level associated with a customer, which can help the bank make informed decisions regarding credit limit, interest rates, and other credit-related policies.

**Key metrics** of interest include customer risk scores, credit utilization, and default likelihood. 

## Dataset Structures 

The primary data structure used for this analysis and modeling is the combination of two major sources:

* [Internal Bank Data](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/data/bank_data.xlsx): Customer account, payment history, and credit utilization, etc.
* [External CIBIL Data](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/data/cibil_data.xlsx): Historical credit scores and delinquency data, etc.

**Note**: The dataset comprised 50,000+ records, divided into 79 columns, the feature-target description you can see [here](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/data/Features_Target_Description.txt).

## Executive Summary

This project focused on categorizing credit card users into four risk segments to help the bank make better decisions around loans and credit limits. Customers were placed into one of four categories: P1 (low risk), P2 (medium risk), P3 (high risk), and P4 (severely high risk). These segments were used to assess how likely a customer is to default on their payments.

By understanding these risk levels:

* P1 and P2 customers are lower risk, and they help the bank reduce its overall credit risk and increase business.
* P3 customers can help the bank meet its business targets but require careful monitoringfor future recovery.
* P4 customers are extremely risky and should be excluded from loan or credit approval.

The model was designed to accurately predict these categories, and it will be improved over time by retraining on updated data. This ensures that the predictions become more reliable with each round of feedbacks from the stakeholders and the data science team.

## Codes
- The Python Pipeline used for Data Cleaning and Preprocessing, Feature Engineering and Selection, Model training and Evaluation as well as Hyperparameter Tuning to find best ML Algorithm can be found [here](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/notebooks/credit_risk_modeling.ipynb).
- The Python Pipeline used to classify the prospects into 4 different categories of risk using **XGBoost Classfier** can be found [here](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/notebooks/credit_risk_pipeline.ipynb).
- The Python Pipeline used for final evaluation of model on unseen dataset can be found [here](https://github.com/nikitaprasad21/Credit-Risk-Modeling/blob/main/notebooks/output_risk_pipeline.ipynb)


## Insights 
#### Category 1: Risk Segmentation

Customers are categorized into four segments: P1 (low risk), P2 (medium risk), P3 (high risk), and P4 (severely high risk).
* P1 and P2 customers offer the lowest risk, making them suitable for loan approvals.
* P3 customers, although riskier, can still help meet business targets with controlled monitoring.
* P4 customers pose the highest risk and should generally be excluded from receiving loans or credit.

#### Category 2: Risk Management:

Based on Risk Appetite the risk management can be classified into 3 categories:

* By focusing on P1 and P2 customers, the bank can significantly reduce its exposure to risky loans.
* Careful management of P3 customers can help in balancing business growth and risk.
* Excluding P4 customers ensures the bank avoids severe financial risks.

## Recommendations

Based on the insights, the following recommendations are suggested:

#### Category 1: Credit Approval Strategy:

* Approve credit for P1 and P2 customers as they have a low risk of defaulting.
* Approve loans for P3 customers with caution and ensure proper monitoring to minimize potential losses.
* Avoid granting credit to P4 customers due to their high likelihood of default.

#### Category 2: Risk Monitoring:

* Implement ongoing monitoring for P3 customers to manage the risk and ensure timely interventions.
  
#### Category 3: Model Updates:

* Retrain the model periodically (such as quarterly or yearly basis) using feedback from new data to improve its accuracy. This continuous updating will keep the model aligned with changing customer behavior and market conditions.

## Assumptions and Caveats
#### Assumptions:

* P1 and P2 customers are always considered lower risk, while P4 customers remain highly risky over time.
* The model predictions are based on the current data and will improve as more data becomes available.
* Customer risk profiles are assumed to remain stable over short periods but may shift, requiring model retraining.
  
#### Caveats:

* The risk levels may change due to unforeseen market conditions or customer behavior, so model predictions may need to be updated frequently.
* The feedback loop and retraining process will require consistent and clean data to ensure that the model remains effective.

