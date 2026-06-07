# ChurnGuard — Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

Machine learning project to predict customer churn for a telecom company. Full pipeline from EDA to model evaluation, with Random Forest as the final model.

## Results

| Model | ROC-AUC | F1 Score |
|---|---|---|
| Random Forest | **~0.84** | **~0.636** |
| Logistic Regression | baseline | — |
| XGBoost | compared | — |

## Dataset

- **Source**: [Kaggle — Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- 7043 customers · 21 features · Binary target (Churn: Yes/No)
- Class imbalance: ~73% non-churn, ~27% churn

## Project Structure

```
churn-predictor/
├── data/
│   ├── raw/                  # Original dataset
│   └── processed/            # Scaled arrays and feature names
├── notebooks/
│   ├── 1.0-eda-initial-analysis.ipynb
│   ├── 1.0-pre_modelling.ipynb
│   └── 1.2-modelling.ipynb   # Final model
├── reports/figures/          # Plots and visualizations
├── requirements.txt
└── README.md
```

## Pipeline

1. **EDA** — distribution analysis, missing values, correlation matrix
2. **Preprocessing** — encoding, scaling, train/test split
3. **Modelling** — Logistic Regression, Random Forest, XGBoost
4. **Evaluation** — ROC curve, precision-recall curve, feature importance, confusion matrix

## Run

```bash
pip install -r requirements.txt
jupyter notebook
```

## Author

Christian Genovese — [LinkedIn](https://linkedin.com/in/christian-genovese) · University of Salerno
