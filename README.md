# End-to-End Classification | Data Science Portfolio Project

A portfolio-ready machine learning project demonstrating a complete classification workflow: data loading, exploratory analysis, preprocessing, model comparison, evaluation, feature interpretation, and model persistence.

> **Dataset note:** This repository uses scikit-learn's built-in Breast Cancer Wisconsin dataset as a self-contained, reproducible classification dataset so the project runs without downloading a CSV. The project title and business-style workflow are generic; this is **not** a customer-churn dataset and must not be presented as one. For a genuinely business-focused churn portfolio project, replace the loader with a documented public churn dataset and update the analysis accordingly.

## Project goals

- Explore a real, labeled tabular dataset.
- Build a reproducible preprocessing + modeling pipeline.
- Compare Logistic Regression, Random Forest, and HistGradientBoosting.
- Evaluate models using accuracy, precision, recall, F1, ROC-AUC, and a confusion matrix.
- Save the best model and metrics for reproducibility.
- Practice clean project structure and documentation.

## Dataset

The notebook loads the Breast Cancer Wisconsin (Diagnostic) dataset through `sklearn.datasets.load_breast_cancer`. It contains 569 observations, 30 numeric features, and a binary target. The target labels are provided by scikit-learn. This dataset is used for learning only; it is not a clinical tool.

## Repository structure

```text
.
├── notebooks/
│   └── end_to_end_classification.ipynb
├── src/
│   └── train.py
├── reports/
│   └── .gitkeep
├── models/                 # created after training
├── requirements.txt
├── .gitignore
└── README.md
```

## Quick start

### 1. Create and activate a virtual environment

**Windows (PowerShell):**
```powershell
python -m venv .venv
.venv\\Scripts\\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the training script

```bash
python src/train.py
```

The script prints model metrics and creates:
- `models/best_model.joblib`
- `reports/model_comparison.csv`
- `reports/test_metrics.json`

### 4. Explore the notebook

Open `notebooks/end_to_end_classification.ipynb` in Jupyter or upload it to Google Colab, then run cells from top to bottom.

## Modeling approach

1. Load and inspect the dataset.
2. Split into train/test sets using stratification.
3. Use a scikit-learn `Pipeline` to keep preprocessing inside cross-validation and prevent leakage.
4. Compare Logistic Regression, Random Forest, and HistGradientBoosting with stratified cross-validation.
5. Evaluate the selected model on a held-out test set.
6. Save the trained pipeline and evaluation outputs.

## Metrics

The script reports accuracy, precision, recall, F1-score, and ROC-AUC. No metric is a substitute for understanding class balance, error costs, and the context in which a model may be used.

## Results

The model comparison and test-set evaluation produced the following numbers (run on the Breast Cancer Wisconsin dataset with a fixed `random_state=42`):

### Cross-Validation (Stratified 5-Fold, F1 scoring)

| Model | CV F1 Mean | CV F1 Std |
|-------|------------|-----------|
| **Logistic Regression** | **0.9825** | 0.0078 |
| HistGradientBoosting | 0.9755 | 0.0105 |
| Random Forest | 0.9700 | 0.0135 |

**Selected model:** Logistic Regression (highest mean CV F1)

### Test Set Evaluation (Hold-out 20%)

| Metric | Value |
|--------|-------|
| **Accuracy** | **0.9825** |
| **Precision** | **0.9861** |
| **Recall** | **0.9861** |
| **F1-Score** | **0.9861** |
| **ROC-AUC** | **0.9954** |

### Confusion Matrix

```
[[41,  1],
 [ 1, 71]]
```

- True Negatives (Benign correctly predicted): 41
- False Positives (Benign predicted as Malignant): 1
- False Negatives (Malignant predicted as Benign): 1
- True Positives (Malignant correctly predicted): 71

The single misclassified benign and malignant case each highlight that even high-performing models can make critical errors—this is why confusion matrices and class-specific metrics matter alongside aggregate scores.

## Important limitations

- This is an educational classification exercise, not a medical product or clinical decision tool.
- Results can vary with library versions and random seeds.
- The dataset is small and does not establish real-world performance.
- Model performance should be interpreted alongside confusion matrices, class-specific metrics, and potential dataset bias.

## Future improvements

- Add a stronger experiment-tracking workflow.
- Add calibration and threshold analysis.
- Add explainability with permutation importance or SHAP.
- Add automated tests and continuous integration.
- Replace the teaching dataset with a well-documented dataset aligned with a specific business question.

## Author

**Mahmoud Badr**  
[LinkedIn](https://www.linkedin.com/in/mahmoud-badr-39b43b308/)
