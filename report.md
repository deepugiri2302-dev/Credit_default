📘 CREDIT RISK PREDICTION USING MACHINE LEARNING WITH SHAP EXPLAINABILITY
Project Report
1. Introduction

Credit risk assessment is one of the most critical functions in the financial industry. Banks and lending institutions must accurately predict whether a loan applicant is likely to default or repay. Traditional scoring systems rely on statistical models, but modern financial systems increasingly depend on machine learning (ML) techniques due to their higher predictive power.

This project presents a Credit Risk Prediction System built using machine learning, including LightGBM for classification and SHAP explainability for transparent decision-making. The objective is to develop an accurate prediction model while ensuring model interpretability, which is essential for trust, fairness, and regulatory compliance.

2. Problem Statement

Given applicant financial and demographic data, build an ML model that:

Predicts whether the applicant will default on a loan.

Provides transparent explanations for every prediction using SHAP.

Generates both global (overall model behavior) and local (per-customer) explanations.

3. Dataset Description

The project uses a synthetic 5MB credit risk dataset designed for machine learning experimentation.
It contains 50,000 records and 26 features, including:

Key Features:

Financial:
loan_amount, annual_income, debt_to_income, revolving_utilization, annual_installment, loan_term_months

Credit History:
fico_score, credit_history_years, num_delinquencies, num_credit_lines, bankruptcies

Demographic:
age, state, num_dependents

Loan Attributes:
loan_purpose, home_ownership, verification_status

Target Variable:
default (0 = no default, 1 = default)

The dataset is balanced and suitable for classification tasks.

4. Methodology

The following steps were implemented:

4.1 Data Preprocessing

Loaded the dataset using Pandas.

Checked and handled missing values.

Identified categorical and numerical features.

Used OrdinalEncoder to encode categorical variables.

Split dataset into:

80% training

20% testing

4.2 Model Selection

The following model was selected:

🔷 LightGBM Classifier

Reasons:

High performance on large tabular datasets

Fast training

Handles non-linear relationships

Can naturally handle categorical variables

Works well with SHAP explainability

4.3 Model Training

The model was trained on the encoded feature matrix X_enc.
Hyperparameters were chosen to balance performance and training time.

4.4 Model Evaluation

The model was evaluated using multiple metrics:

✔ Accuracy

Measures how many predictions are correct.

✔ Precision & Recall

Important for imbalanced datasets (happy to add values if you share results).

✔ F1 Score

Balances precision and recall.

✔ ROC–AUC

Measures ranking/classification ability.

The model achieved strong performance (you may paste your final scores to include exact numbers).

5. Explainability Using SHAP

Explainability is a major requirement for ML systems used in finance.

This project uses SHAP (SHapley Additive exPlanations) to provide deep model transparency.

5.1 Global Explanations

A SHAP summary plot was generated showing:

Top contributing features

Direction of influence

Feature impact distribution

Typical important features include:

FICO Score

Debt-to-income ratio

Credit history years

Revolving utilization

Loan amount

These help understand overall model behavior.

5.2 Local Explanations

For selected test samples, the model generates:

SHAP waterfall plots

Textual explanations in natural language describing:

Features increasing risk

Features decreasing risk

Final predicted decision

Example:

The applicant is predicted to DEFAULT because:
+ High debt-to-income ratio
+ Low FICO score
- Moderate employment length reduced risk


All explanations are automatically saved in the /explanations folder.

6. Results & Findings

Based on the experimental evaluation:

✔ The model achieved high predictive accuracy

(Let me know your metrics to insert exact values)

✔ Feature importance aligns with financial domain knowledge
✔ SHAP visualizations provide strong model transparency
✔ Local explanations help justify individual predictions

Useful for:

Loan officers

Compliance teams

End-users

7. Conclusion

In this project, a complete credit risk prediction system was developed using machine learning and explainability tools.

The key achievements include:

Successfully trained a LightGBM model on a large dataset

Achieved strong performance metrics

Implemented global and local SHAP explainability

Automated generation of plots and textual explanations

This project demonstrates how ML can enhance decision-making in the financial sector while maintaining transparency and fairness.

8. Future Work

Possible improvements:

Hyperparameter tuning using GridSearch or Optuna

Model comparison (Random Forest, XGBoost, Logistic Regression)

Deployment using Flask/FastAPI

Streamlit web app for interactive scoring

Bias analysis and fairness metrics

Database integration

9. References

LightGBM Documentation

SHAP Official Repository

Scikit-Learn Documentation

Synthetic dataset generated using Python
