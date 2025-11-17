
# 🔍 GitIngest Project Summary — Credit Default Prediction

This repository contains a full interpretable machine learning pipeline using the **Default of Credit Card Clients Dataset**.

---

## 📊 Model Performance (Test Set)

- **AUC:** 0.7761
- **Precision:** 0.4725
- **Recall:** 0.6142
- **F1-score:** 0.5341

Confusion Matrix:

---

## 🧠 Global SHAP Feature Importance
Top 5 features:
  feature  mean_abs_shap
    PAY_0       0.554533
LIMIT_BAL       0.224891
BILL_AMT1       0.158520
 PAY_AMT2       0.127405
 PAY_AMT1       0.114219

---

## 🧩 Local SHAP Explanations
Three sample cases analyzed:
- Low-risk client
- High-risk client
- Surprising client

Each case includes:
- CSV of SHAP values  
- Horizontal bar plot  
- Text explanation  

---

## 📁 Output Files Generated

- metrics.txt
- top5_shap.csv
- executive_summary.txt
- shap_summary.png
- shap_bar.png
- local_shap_*.csv
- local_shap_bar_*.png
- explanation_*.txt
- pipeline_xgb.pkl (if saved)
- pipeline_xgb_best.pkl (if saved)

---

## 📝 Notes
This file automatically summarizes the project for GitIngest.  
GitIngest will combine this with your README.md to generate a rich description.
