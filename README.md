# 🩺 End-to-End Breast Cancer Classification

**Machine Learning Portfolio Project — Complete End-to-End Classification Pipeline** 🤖✨

**Author:** Mahmoud Badr  
**Role:** Data Scientist / Data Analyst  
**Location:** Egypt 🇪🇬  
**Dataset:** Breast Cancer Wisconsin (Diagnostic) — scikit-learn built-in

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F05033?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![NumPy](https://img.shields.io/badge/NumPy-Computing-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![Joblib](https://img.shields.io/badge/Model%20Persistence-joblib-FF6B6B?style=for-the-badge)](https://joblib.readthedocs.io)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

---

## 👤 **About the Author**

> **Mahmoud Badr** — Data Scientist / Data Analyst based in Egypt 🇪🇬  
> Passionate about building end-to-end ML pipelines: from raw data exploration to trained, evaluated, and persisted models ready for production.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/mahmoud-badr-39b43b308/)
[![Email](https://img.shields.io/badge/Email-Contact-red?style=flat-square&logo=gmail)](mailto:mahmoudbadr0220@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?style=flat-square&logo=github)](https://github.com/mahmoudbadr1234)

---

## 🎯 **Project Overview**

A portfolio-ready machine learning project demonstrating a **complete classification workflow**: data loading, exploratory analysis, preprocessing, model comparison, evaluation, feature interpretation, and model persistence.

> ⚠️ **Dataset note:** This repository uses scikit-learn's built-in Breast Cancer Wisconsin dataset as a self-contained, reproducible classification dataset so the project runs without downloading a CSV. The project title and business-style workflow are generic; this is **not** a customer-churn dataset and must not be presented as one.

| Component | Description | Status |
|-----------|-------------|--------|
| 📥 **Data Loading** | Load Breast Cancer Wisconsin dataset via sklearn | ✅ Complete |
| 🔍 **Exploratory Analysis** | Inspect 30 numeric features, distributions, correlations | ✅ Complete |
| 🧹 **Preprocessing** | Stratified train/test split, scaling pipeline | ✅ Complete |
| 🤖 **Model Training** | Logistic Regression, Random Forest, HistGradientBoosting | ✅ Complete |
| 📊 **Model Comparison** | Stratified 5-Fold Cross-Validation (F1 scoring) | ✅ Complete |
| 📈 **Evaluation** | Accuracy, Precision, Recall, F1, ROC-AUC, Confusion Matrix | ✅ Complete |
| 💾 **Model Persistence** | Best model saved as `.joblib` + metrics JSON | ✅ Complete |

---

## 📊 **Dataset Profile**

| Property | Value |
|----------|-------|
| 📄 **Observations** | 569 |
| 🔢 **Features** | 30 numeric (mean, se, worst measurements) |
| 🎯 **Target** | Binary (Malignant / Benign) |
| 📚 **Source** | `sklearn.datasets.load_breast_cancer` |
| ⚖️ **Class Balance** | Balanced binary classification |

---

## 🏆 **Results — Real Numbers**

### 🥇 Model Comparison (Stratified 5-Fold Cross-Validation)

| Rank | Model | CV F1 Mean | CV F1 Std |
|------|-------|------------|-----------|
| 🥇 **1st** | **Logistic Regression** | **0.9825** | 0.0078 |
| 🥈 **2nd** | HistGradientBoosting | 0.9755 | 0.0105 |
| 🥉 **3rd** | Random Forest | 0.9700 | 0.0135 |

**Selected model:** Logistic Regression — highest mean CV F1 score.

---

### 📋 Test Set Evaluation (Hold-out 20%, `random_state=42`)

| Metric | Value |
|--------|-------|
| 🎯 **Accuracy** | **0.9825** |
| ✅ **Precision** | **0.9861** |
| 🔄 **Recall** | **0.9861** |
| ⚖️ **F1-Score** | **0.9861** |
| 📈 **ROC-AUC** | **0.9954** |

### 🧮 Confusion Matrix

```
[[41,  1],
 [ 1, 71]]
```

| Metric | Count |
|--------|-------|
| ✅ True Negatives (Benign → Benign) | 41 |
| ❌ False Positives (Benign → Malignant) | 1 |
| ❌ False Negatives (Malignant → Benign) | 1 |
| ✅ True Positives (Malignant → Malignant) | 71 |

> **Note:** Even high-performing models make critical errors — always inspect confusion matrices and class-specific metrics alongside aggregate scores.

---

## 📁 **Repository Structure**

```
📦 end-to-end-classification/
├── 📂 notebooks/
│   └── notebooks_end_to_end_classification.ipynb   # 📓 Full ML workflow (EDA → Training → Evaluation)
├── 📂 src/
│   └── train.py                                    # 🐍 Training script (reproducible)
├── 📂 reports/
│   └── .gitkeep                                    # 📊 Output reports (model_comparison.csv, test_metrics.json)
├── 📂 models/                                      # 💾 Trained models (created after training)
│   └── best_model.joblib
├── 📄 requirements.txt                             # 📦 Python dependencies
├── 📄 .gitignore                                   # 🚫 Git ignore patterns
└── 📄 README.md                                    # 📝 This documentation
```

---

## 🛠️ **Tech Stack**

<div align="center">

| Category | Tools |
|----------|-------|
| 🐍 **Programming** | Python 3.8+ |
| 📊 **Data Processing** | Pandas, NumPy |
| 🤖 **Machine Learning** | Scikit-learn 1.3+ |
| 📈 **Visualization** | Matplotlib, Seaborn |
| 📓 **Development** | Jupyter Notebook |
| 💾 **Model Persistence** | joblib 1.3+ |
| 🔧 **Version Control** | Git + GitHub |

</div>

---

## 🔬 **Modeling Approach**

1. 📥 **Load** Breast Cancer Wisconsin dataset
2. ✂️ **Split** into train/test sets using stratification (preserve class balance)
3. 🔄 **Pipeline** — scikit-learn `Pipeline` keeps preprocessing inside cross-validation to prevent data leakage
4. 🤖 **Compare** Logistic Regression, Random Forest, HistGradientBoosting with stratified 5-Fold CV (F1 scoring)
5. 📊 **Evaluate** selected model on held-out test set
6. 💾 **Persist** best pipeline as `best_model.joblib` + metrics to `reports/`

---

## 🚀 **Quick Start Guide**

### 📋 **Prerequisites**

```bash
pip install -r requirements.txt
```

### ▶️ **1. Create & Activate Virtual Environment**

**Windows (PowerShell):**
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 🏋️ **2. Install Dependencies**

```bash
pip install -r requirements.txt
```

### 🏃 **3. Run Training Script**

```bash
python src/train.py
```

**Outputs created:**
- ✅ `models/best_model.joblib` — trained pipeline
- ✅ `reports/model_comparison.csv` — CV results per model
- ✅ `reports/test_metrics.json` — test set metrics

### 📓 **4. Explore the Notebook**

Open `notebooks/notebooks_end_to_end_classification.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab — run cells top to bottom.

---

## ⚠️ **Important Limitations**

| Limitation | Details |
|------------|---------|
| 🎓 **Educational only** | Classification exercise — **not** a medical product or clinical decision tool |
| 🔄 **Version variance** | Metrics may vary with library versions and random seeds |
| 📦 **Small dataset** | 569 observations — not sufficient for real-world clinical deployment |
| ⚖️ **Interpretation** | Always inspect confusion matrices + class-specific metrics alongside aggregate scores |

---

## 🔮 **Future Improvements**

- ⚗️ Add experiment tracking (MLflow / Weights & Biases)
- 📉 Add calibration curves and threshold analysis
- 🧠 Add model explainability (SHAP values, permutation importance)
- 🧪 Add automated unit tests + CI pipeline
- 📊 Replace teaching dataset with a business-aligned public dataset

---

## 📄 **License**

```
MIT License

Copyright (c) 2026 Mahmoud Badr

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 📞 **Contact**

**Mahmoud Badr**  
📧 Email: mahmoudbadr0220@gmail.com  
💼 LinkedIn: [linkedin.com/in/mahmoud-badr-39b43b308](https://www.linkedin.com/in/mahmoud-badr-39b43b308/)  
🐙 GitHub: [github.com/mahmoudbadr1234](https://github.com/mahmoudbadr1234)

---

<div align="center">

**⭐ If this project helped you, please give it a star!**

**Built with ❤️ and ☕ by Mahmoud Badr**

</div>
