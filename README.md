# Churn Predictor Model

## 📋 Descrizione Progetto
Progetto di Machine Learning per predire il churn dei clienti di una compagnia telefonica.

## 📊 Dataset
- **Nome**: Telco Customer Churn
- **Fonte**: [Kaggle - Blastchar](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Descrizione**: Dati di 7043 clienti con 21 features
- **Target**: Churn (Yes/No)
- **Posizione**: `data/raw/telco_churn.csv`

## 🎯 Obiettivi
- Analizzare i fattori che influenzano il churn
- Sviluppare un modello predittivo
- Identificare clienti a rischio

## 📂 Struttura Progetto
```
churn-predictor/
├── data/
│   ├── raw/              # Dati originali
│   └── processed/        # Dati processati
├── notebooks/
│   └── 1_0-eda-initial-analysis.ipynb
├── src/                  # Codice sorgente (future)
├── reports/             # Report e visualizzazioni (future)
└── README.md
```

## 🔍 Fase 1: Exploratory Data Analysis (EDA)
**Status**: ✅ Completata

### Risultati principali:
- Dataset: 7043 righe × 21 colonne
- Missing values: 11 in TotalCharges (gestiti)
- Target sbilanciato: ~73% non-churn, ~27% churn
- Mix di features numeriche e categoriche

**Notebook**: `notebooks/1_0-eda-initial-analysis.ipynb`

## 🚀 Prossimi Step
- [ ] Feature Engineering
- [ ] Preprocessing
- [ ] Model Selection
- [ ] Hyperparameter Tuning
- [ ] Evaluation

## 👨‍💻 Autore
Christian - UNISA

## 📅 Ultimo aggiornamento
Gennaio 2025
