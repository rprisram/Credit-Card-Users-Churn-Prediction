# Personal Loan Campaign Prediction for AllLife Bank

## Business Problem

AllLife Bank, a US bank with a large base of liability customers, aims to expand its loan business by converting existing depositors into personal loan customers. A previous campaign yielded a 9% conversion rate, and the marketing department seeks to improve this by targeting customers with a higher probability of purchasing a loan. This project focuses on building a predictive model to identify these potential customers, understand the key drivers of loan purchases, and define customer segments for targeted marketing.

## Dataset

The analysis uses a dataset of AllLife Bank's liability customers, containing the following attributes:

*   **ID**: Customer ID
*   **Age**: Customer’s age in completed years
*   **Experience**: Years of professional experience
*   **Income**: Annual income of the customer (in thousand dollars)
*   **ZIP Code**: Home address ZIP code
*   **Family**: Family size of the customer
*   **CCAvg**: Average spending on credit cards per month (in thousand dollars)
*   **Education**: Education level (1: Undergrad, 2: Graduate, 3: Advanced/Professional)
*   **Mortgage**: Value of house mortgage if any (in thousand dollars)
*   **Personal Loan**: Did this customer accept the personal loan offered in the last campaign? (Target Variable)
*   **Securities Account**: Does the customer have a securities account with the bank?
*   **CD Account**: Does the customer have a certificate of deposit (CD) account with the bank?
*   **Online**: Does the customer use internet banking facilities?
*   **CreditCard**: Does the customer use a credit card issued by AllLife Bank?

## Analysis and Modeling

The project follows a structured approach to solve the business problem:

1.  **Exploratory Data Analysis (EDA):** The initial phase involves data cleaning, handling missing values, and exploring the relationships between different customer attributes and their distribution.

2.  **Outlier Treatment:** Outliers in the data are identified and treated to prevent them from skewing the model's performance.

3.  **Feature Engineering:** New features are created from existing ones to better capture the underlying patterns in the data.

4.  **Class Imbalance:** The dataset is imbalanced, with a small percentage of customers having taken a personal loan. This is addressed by using techniques like SMOTE (Synthetic Minority Over-sampling Technique) or by applying class weights to the models to give more importance to the minority class.

5.  **Model Building:**
    *   **Base Model:** A baseline model is established to set a benchmark for performance.
    *   **Decision Tree with Pruning:** A Decision Tree classifier is built and optimized using:
        *   **Pre-pruning:** Techniques like limiting the tree's depth or setting a minimum number of samples per leaf to prevent overfitting.
        *   **Post-pruning (Cost Complexity Pruning):** The tree is first grown to its full extent and then pruned back based on a cost complexity parameter (ccp_alpha) to find the optimal tree size.
    *   **Model Hypertuning:** The hyperparameters of the final model are tuned using techniques like GridSearchCV to find the best combination for optimal performance. The significance of key hyperparameters is also analyzed.

## Conclusion

The final model provides a reliable tool for AllLife Bank to identify customers with a high propensity to take a personal loan. The model's insights into the key drivers of loan uptake (such as income, education, and credit card spending) allow the marketing team to create more targeted and effective campaigns. By focusing on the customer segments identified by the model, the bank can significantly improve its loan conversion rate and grow its asset customer base.
