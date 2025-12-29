# Term-Deposit-Subscription-Prediction-Bank-Marketing-

Objective
Predict whether a client will subscribe to a term deposit based on demographic and campaign-related data to optimize marketing conversion rates.

Approach
1. Data Loading

Imported essential libraries: pandas, numpy, matplotlib, and sklearn.

Loaded the bank marketing dataset (bank-full.csv) consisting of 45,210 records and 17 features.

Performed initial inspection using .shape and .head() to verify data integrity.

2. Data Exploration & Preprocessing

Analyzed feature types and identified a class imbalance (5,289 'yes' vs. 39,921 'no').

Mapped the target variable y to binary format (0 for 'no', 1 for 'yes').

Used a ColumnTransformer with OneHotEncoder to process categorical features while passing through numerical data.

3. Model Training & Pipeline

Split data into training (75%) and testing (25%) sets using stratification to maintain class proportions.

Built a machine learning Pipeline to automate preprocessing and model execution.

Trained and compared models including Logistic Regression and Random Forest Classifier.

4. Performance Evaluation & Explainability

Evaluated models using Confusion Matrices, Classification Reports (F1-score), and ROC-AUC curves.

Integrated SHAP (SHapley Additive exPlanations) to interpret model decisions.

Generated waterfall plots to visualize the specific impact of features like "duration" or "balance" on individual predictions.

Results & Insights
The analysis provided a transparent view of the model's logic:

Top Predictors: Call duration and previous campaign outcomes were key indicators of success.

Clarity: SHAP values successfully identified why specific clients were predicted as "likely to subscribe," allowing for personalized follow-ups.

Balance: Stratified splitting ensured the model remained robust despite the minority class size.

Possible Improvements
The model and insights can be enhanced by:

Implementing SMOTE (Synthetic Minority Over-sampling Technique) to better address the class imbalance.

Hyperparameter tuning using GridSearchCV or RandomizedSearchCV for the Random Forest model.

Adding economic indicator features (e.g., consumer price index) to provide more external context.
