# Credit Card Users Churn Prediction

## Business Problem
Thera Bank is facing a significant decline in credit card users, which negatively impacts their revenue from various fees. The core business problem is to identify customers who are likely to churn from their credit card services. By predicting potential churners, the bank can implement targeted retention strategies to reduce customer attrition and financial losses.

## Dataset Used
The analysis utilizes a dataset containing customer-level information for Thera Bank'''s credit card users. Key features include:
*   **Demographics:** `Customer_Age`, `Gender`, `Education_Level`, `Marital_Status`.
*   **Financial Information:** `Income_Category`, `Card_Category`.
*   **Relationship Metrics:** `Months_on_book`, `Total_Relationship_Count`.
*   **Target Variable:** `Attrition_Flag`, which indicates whether a customer is an "Existing Customer" or an "Attrited Customer."

## Key Steps in the Analysis
1.  **Exploratory Data Analysis (EDA):** The notebook begins with EDA to uncover patterns, correlations, and insights within the data. This step is crucial for understanding the relationships between customer attributes and their likelihood of churning.
2.  **Feature Engineering:** New features are engineered from existing ones to enhance the predictive power of the models. This includes transforming categorical variables into a numerical format suitable for machine learning algorithms.
3.  **Handling Class Imbalance:** The dataset is imbalanced, with a smaller proportion of "Attrited" customers. The analysis employs both oversampling (e.g., SMOTE) and undersampling techniques to create a balanced dataset, which helps in training more robust models.
4.  **Model Building & Selection:** Several classification models, such as Logistic Regression, Decision Trees, Random Forest, and Gradient Boosting, are trained and evaluated. Based on initial performance metrics (e.g., recall, F1-score), the best-performing models are shortlisted for further optimization.
5.  **Hyperparameter Tuning:** To fine-tune the selected models, the analysis utilizes advanced techniques like `RandomizedSearchCV` and `BayesSearchCV`. These methods systematically search for the optimal combination of hyperparameters to maximize model performance.

## Final Conclusion
The analysis concludes by identifying the best-performing model after hyperparameter tuning. The final model provides a reliable tool for predicting customer churn. The output cells indicate that the model'''s performance is significant enough to be deployed by Thera Bank. By integrating this model into their operations, the bank can proactively identify at-risk customers and implement targeted interventions, ultimately reducing churn and securing their revenue streams.
