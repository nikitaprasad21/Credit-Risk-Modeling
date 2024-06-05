# **Credit Risk Segmentation Project**

### **Problem Statement:**

The main objective of this project was to segment credit card users based on their risk levels. It aimed to develop a model that accurately predicts the risk level associated with a customer, which can help the bank make informed decisions regarding credit limit, interest rates, and other credit-related policies.

### **Project Process:**

The project was executed using Python, with the following steps:

1. **Data Collection:** Gathered data from two sources; the bank's internal systems and national CIBIL data.
2. **Data Preprocessing:** The data was cleaned by handling missing values and removing irrelevant columns. The data from both sources were then merged using the common 'prospect id' column.
3. **Feature Engineering:** Created new features that could improve the predictive power of the model.
4. **Feature Selection:** Used the Chi-squared test and ANOVA to reduce the number of features and minimize multicollinearity.
5. **Model Training:** Trained a multiclass classification model using XGBoost.
6. **Model Evaluation:** The model achieved an overall accuracy of 0.78 and an F1 score of 0.76.
7. **Hyperparameter Tuning:** Used Grid Search CV to fine-tune the model parameters, achieving a testing accuracy of 78.01% from 77.83%.

This project demonstrated the effectiveness of using machine learning techniques in credit risk segmentation to mitigate credit risk and optimize financial strategies in the banking sector.
