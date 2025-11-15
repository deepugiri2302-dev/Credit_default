📊 Credit Risk Prediction Using Machine Learning
With Explainability (SHAP), Local & Global Interpretations, and Auto-Generated Reports

This project builds a complete Credit Risk Prediction System using machine learning, along with detailed model interpretability using SHAP (SHapley Additive exPlanations).
It predicts whether a loan applicant is likely to default or repay, and generates:

✔ Global SHAP feature importance

✔ Local SHAP waterfall plots

✔ Text explanations for individual predictions

✔ Evaluation metrics (AUC, accuracy, F1, precision, recall)

The project includes a 5MB synthetic credit risk dataset designed for ML training and explainability.

📁 Project Structure
project/
│
├── credit_risk_dataset_5mb.csv          # Input dataset
├── model_training.py                    # Main ML training script
├── explanations/                        # Auto-generated SHAP results
│   ├── global_shap_summary.png
│   ├── waterfall_*.png
│   └── explanation_*.txt
├── saved_model.pkl                      # Trained ML model
└── README.md

📘 Features
✔ Data Preprocessing

Cleans dataset

Splits features & target

Ordinal-encodes categorical variables

Handles unknown categories safely

✔ Model Training

Uses:

LightGBM Classifier (fast + accurate for tabular data)

Trains on the 5MB synthetic dataset:

50,000 samples

24 numerical/categorical features

Binary target: default

✔ Evaluation Metrics

Automatically prints:

ROC-AUC

Accuracy

Precision

Recall

F1 score

✔ Explainability (SHAP)

The code generates:

Global summary plot (feature importance)

Local waterfall plots (per applicant)

Human-readable explanations

Example explanation:

The model predicts DEFAULT because:
+ High debt-to-income ratio
+ Low FICO score
- Stable employment length reduced risk

📦 Installation & Requirements
🔧 1. Install Python packages

Run:

pip install pandas numpy scikit-learn lightgbm shap matplotlib tqdm


If Jupyter warning appears:

pip install ipywidgets

🧠 How to Run the Project
▶️ Step 1 — Place dataset in project folder

Ensure:

credit_risk_dataset_5mb.csv


is in the same directory as your Python script.

▶️ Step 2 — Run the training script
python model_training.py


This will:

Load dataset

Train LightGBM model

Evaluate metrics

Generate SHAP global plots

Save waterfall plots and textual explanations

📂 Output Files
📌 1. Global explanations

Located in:

explanations/global_shap_summary.png

📌 2. Local explanations (per test sample)

Generated as:

explanations/waterfall_<index>.png
explanations/explanation_<index>.txt

📌 3. Trained model

Saved as:

saved_model.pkl

🧪 Dataset Details

The dataset contains 24+ features:

Loan amount

Annual income

Employment length

Credit history

Debt-to-income

Utilization ratio

Credit lines

Inquiries

FICO score

Home ownership

Loan purpose

Mortgage accounts

And more…

Target variable:

default (0 = no default, 1 = default)

🏆 Results

The project produces:

Accurate credit risk predictions

Fully explainable results

Visual & text-based interpretation

Automated reporting per applicant

Perfect for:

Academic projects

ML explainability case studies

Credit scoring demonstrations

End-to-end Python ML pipelines

📮 Support

If you need:

📌 Clean full code

📌 GUI for credit scoring

📌 API version (Flask/FastAPI)

📌 PowerPoint / project report

📌 Deployment guide
