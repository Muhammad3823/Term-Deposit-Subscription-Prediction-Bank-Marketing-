# Term-Deposit-Subscription-Prediction-Bank-Marketing-

### Objective

Develop a predictive model to identify clients likely to subscribe to a term deposit, enabling the bank to optimize marketing resources and increase conversion rates for future campaigns.

### Approach

**1. Data Acquisition & Inspection**

* Integrated the **Bank Marketing Dataset** containing 45,210 observations and 17 features.
* Conducted initial data auditing to confirm a shape of  and examined the feature distribution.

**2. Feature Engineering & Preprocessing**

* **Target Encoding**: Mapped the categorical target variable `y` ('yes'/'no') to a binary numeric format (1/0) for model compatibility.
* **Automated Pipeline**: Implemented a `ColumnTransformer` to handle mixed data types:
* Applied `OneHotEncoder` to categorical features (e.g., job, marital status, education) to manage high-cardinality data.
* Utilized a `passthrough` remainder for numerical features to preserve their original distribution.


* **Strategic Splitting**: Employed a stratified 75/25 train-test split to ensure representative class distributions in both sets.

**3. Model Development**

* Constructed a robust machine learning **Pipeline** to prevent data leakage and ensure consistent preprocessing across folds.
* Evaluated multiple classification architectures, including:
* **Logistic Regression**: Optimized with the `SAGA` solver and increased iterations for convergence on high-dimensional data.
* **Random Forest Classifier**: Utilized for its ability to capture non-linear relationships and provide feature importance.



**4. Interpretability & Performance Evaluation**

* **Metrics**: Assessed model efficacy using F1-score, Confusion Matrices, and ROC-AUC curves to balance precision and recall.
* **Explainable AI (XAI)**: Integrated **SHAP (SHapley Additive exPlanations)** to demystify "black-box" predictions.
* **Waterfall Visualization**: Generated SHAP waterfall plots to quantify the positive or negative contribution of specific features (such as call `duration` or account `balance`) to individual client outcomes.

### Results & Insights

The modeling process identified critical drivers of campaign success:

* **Key Drivers**: Call duration and previous campaign outcomes significantly influenced subscription probability.
* **Operational Efficiency**: By targeting high-probability clients identified by the model, marketing teams can reduce "cold call" fatigue and focus on high-yield prospects.

### Possible Improvements

The framework can be further enhanced by:

* Implementing **SMOTE** or other oversampling techniques to further address the inherent class imbalance.
* Hyperparameter optimization via **GridSearchCV** to fine-tune model parameters for peak performance.
* Incorporating time-series analysis to account for seasonal trends in banking behavior.

---

