# ChurnGuard — Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat&logo=xgboost&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

Machine learning pipeline to predict customer churn for a telecom company. Includes full EDA, preprocessing, model comparison, hyperparameter tuning, and threshold optimization.

## Results

| Model | ROC-AUC | F1 Score | Recall |
|---|---|---|---|
| **Random Forest Tuned** ✅ | **0.84** | **0.636** | **0.78** |
| XGBoost Tuned | 0.83 | 0.623 | 0.73 |
| Logistic Regression | 0.84 | 0.615 | 0.79 |

Final model: **Random Forest** with optimized threshold (0.50) and `class_weight=balanced`.

## Top Features (Random Forest)

| Feature | Importance |
|---|---|
| Contract type | 0.166 |
| Tenure | 0.159 |
| Monthly Charges | 0.115 |
| Fiber Optic Internet | 0.062 |

## Dataset

- **Source**: [Kaggle — Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- 7043 customers · 21 features · Binary target (Churn: Yes/No)
- Class imbalance: ~73% non-churn, ~27% churn · handled via `class_weight=balanced`

## Pipeline

1. **EDA** — distribution analysis, missing values, correlation matrix, churn drivers
2. **Preprocessing** — binary encoding, ordinal encoding, StandardScaler, stratified 80/20 split
3. **Modelling** — Logistic Regression, Random Forest, XGBoost
4. **Tuning** — RandomizedSearchCV (50 iterations, 5-fold CV) for RF and XGBoost
5. **Threshold optimization** — Precision-Recall curve, optimal threshold at 0.50

## Project Structure

```
churn-predictor/
├── data/
│   ├── raw/                  # Original dataset
│   └── processed/            # Scaled arrays and feature names
├── notebooks/
│   ├── 1.0-eda-initial-analysis.ipynb
│   ├── 1.0-pre_modelling.ipynb
│   └── 1.2-modelling.ipynb
├── reports/figures/          # ROC curves, confusion matrices, feature importance
├── requirements.txt
└── README.md
```

## Run

```bash
pip install -r requirements.txt
jupyter notebook
```

## Author

Christian Genovese — [LinkedIn](https://linkedin.com/in/christian-genovese) · University of Salerno
