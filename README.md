Credit Default Prediction Using XGBoost with SHAP Explainability
This project builds a machine learning model to predict whether a credit card client will default on their next payment.
A major focus is providing transparent and interpretable predictions using SHAP (SHapley Additive exPlanations), ensuring the model outputs are explainable for business and risk-management decisions.

🚀 Project Overview
The project uses the Default of Credit Card Clients Dataset and walks through the complete ML workflow:
✔ Data Cleaning & Preprocessing


Removed index column (Unnamed: 0)


Handled categorical and numeric separation


Fixed non-numeric values in target variable


Filled missing values appropriately


Renamed features from X1..X23 to meaningful real-world names


✔ Model Training


Model used: XGBoost Classifier


Train/Test split with stratification


End-to-end pipeline built using Scikit-Learn


✔ Model Evaluation (Test Set)
MetricScoreAUC0.7761Precision0.4725Recall0.6142F1-score0.5341Accuracy0.76
Confusion Matrix:
[[3763  910]
 [ 512  815]]


🔍 SHAP Interpretability
SHAP was used to explain both global (feature importance across all clients) and local (per-client) behaviour of the model.
🔹 Global SHAP — Top 5 Most Important Features


PAY_0 — Most recent repayment status


LIMIT_BAL — Credit limit


BILL_AMT1 — Most recent bill amount


PAY_AMT2 — Repayment two months ago


PAY_AMT1 — Repayment last month


Global SHAP outputs include:


shap_summary.png — Summary scatter plot


shap_bar.png — Bar plot of mean |SHAP| values


global_shap_importance.csv — Numerical feature importances



🎯 Local SHAP Explanations (3 Case Studies)
Three representative cases were selected:1️⃣ Low-Risk Client


Model predicted very low probability of default


SHAP shows strong negative contributions from large past payments


2️⃣ High-Risk Client


Model predicted high probability of default


Strong positive SHAP contributions from poor repayment status (PAY_0, PAY_2, etc.)


3️⃣ Surprising Case


The model predicted default against intuition


Local SHAP values reveal feature interactions causing the unusual prediction


For each case, the following files are included:


local_shap_<case>.csv


local_shap_bar_<case>.png


explanation_<case>.txt


These provide a complete breakdown of how features influenced the prediction.

📁 Repository Structure
your-repo/
│
├── README.md
│
├── notebook/
│   └── credit_default_shap.ipynb
│
├── data/
│   └── default_credit.csv   (optional – or provide download link)
│
├── models/
│   ├── pipeline_xgb.pkl
│   └── pipeline_xgb_best.pkl   (optional)
│
├── outputs/
│   ├── metrics.txt
│   ├── top5_shap.csv
│   ├── executive_summary.txt
│   ├── shap_summary.png
│   ├── shap_bar.png
│   ├── global_shap_importance.csv
│   ├── local_shap_low_risk.csv
│   ├── local_shap_high_risk.csv
│   ├── local_shap_surprising.csv
│   ├── local_shap_bar_low_risk.png
│   ├── local_shap_bar_high_risk.png
│   ├── local_shap_bar_surprising.png
│   ├── explanation_low_risk.txt
│   ├── explanation_high_risk.txt
│   └── explanation_surprising.txt


🛠 How to Run This Project


Clone the repository:
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git



Open the notebook in Google Colab:


Upload to Colab


Ensure dataset is in /content/drive/MyDrive/ or adjust path




Run all cells sequentially


Outputs are automatically generated in the outputs/ folder



📌 Key Business Insights


Recent repayment behavior (PAY_0, PAY_2, …) is the strongest predictor of risk


Higher credit limits reduce default risk


Larger recent repayments significantly decrease risk


SHAP values allow auditors and financial analysts to justify each prediction



Credit Default Prediction Using XGBoost with SHAP Explainability
This project builds a machine learning model to predict whether a credit card client will default on their next payment.
A major focus is providing transparent and interpretable predictions using SHAP (SHapley Additive exPlanations), ensuring the model outputs are explainable for business and risk-management decisions.

🚀 Project Overview
The project uses the Default of Credit Card Clients Dataset and walks through the complete ML workflow:
✔ Data Cleaning & Preprocessing


Removed index column (Unnamed: 0)


Handled categorical and numeric separation


Fixed non-numeric values in target variable


Filled missing values appropriately


Renamed features from X1..X23 to meaningful real-world names


✔ Model Training


Model used: XGBoost Classifier


Train/Test split with stratification


End-to-end pipeline built using Scikit-Learn


✔ Model Evaluation (Test Set)
MetricScoreAUC0.7761Precision0.4725Recall0.6142F1-score0.5341Accuracy0.76
Confusion Matrix:
[[3763  910]
 [ 512  815]]


🔍 SHAP Interpretability
SHAP was used to explain both global (feature importance across all clients) and local (per-client) behaviour of the model.
🔹 Global SHAP — Top 5 Most Important Features


PAY_0 — Most recent repayment status


LIMIT_BAL — Credit limit


BILL_AMT1 — Most recent bill amount


PAY_AMT2 — Repayment two months ago


PAY_AMT1 — Repayment last month


Global SHAP outputs include:


shap_summary.png — Summary scatter plot


shap_bar.png — Bar plot of mean |SHAP| values


global_shap_importance.csv — Numerical feature importances



🎯 Local SHAP Explanations (3 Case Studies)
Three representative cases were selected:
1️⃣ Low-Risk Client


Model predicted very low probability of default


SHAP shows strong negative contributions from large past payments


2️⃣ High-Risk Client


Model predicted high probability of default


Strong positive SHAP contributions from poor repayment status (PAY_0, PAY_2, etc.)


3️⃣ Surprising Case


The model predicted default against intuition


Local SHAP values reveal feature interactions causing the unusual prediction


For each case, the following files are included:


local_shap_<case>.csv


local_shap_bar_<case>.png


explanation_<case>.txt


These provide a complete breakdown of how features influenced the prediction.

📁 Repository Structure
your-repo/
│
├── README.md
│
├── notebook/
│   └── credit_default_shap.ipynb
│
├── data/
│   └── default_credit.csv   (optional – or provide download link)
│
├── models/
│   ├── pipeline_xgb.pkl
│   └── pipeline_xgb_best.pkl   (optional)
│
├── outputs/
│   ├── metrics.txt
│   ├── top5_shap.csv
│   ├── executive_summary.txt
│   ├── shap_summary.png
│   ├── shap_bar.png
│   ├── global_shap_importance.csv
│   ├── local_shap_low_risk.csv
│   ├── local_shap_high_risk.csv
│   ├── local_shap_surprising.csv
│   ├── local_shap_bar_low_risk.png
│   ├── local_shap_bar_high_risk.png
│   ├── local_shap_bar_surprising.png
│   ├── explanation_low_risk.txt
│   ├── explanation_high_risk.txt
│   └── explanation_surprising.txt


🛠 How to Run This Project


Clone the repository:
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git



Open the notebook in Google Colab:


Upload to Colab


Ensure dataset is in /content/drive/MyDrive/ or adjust path




Run all cells sequentially


Outputs are automatically generated in the outputs/ folder



📌 Key Business Insights


Recent repayment behavior (PAY_0, PAY_2, …) is the strongest predictor of risk


Higher credit limits reduce default risk


Larger recent repayments significantly decrease risk


SHAP values allow auditors and financial analysts to justify each prediction