# credit-risk-model
Credit card default prediction using Logistic Regression on the UCI dataset (30K clients, 81.6% accuracy, AUC 0.756) | Python · scikit-learn
# 💳 Credit Card Default Prediction
### Logistic Regression · UCI Dataset · 30,000 clients

[![Python](https://img.shields.io/badge/Python-3.x-blue)](https://github.com/Soumyadeeproy2001/credit-risk-model/edit/main/README.md)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange)](https://github.com/Soumyadeeproy2001/credit-risk-model/edit/main/README.md)
[![Accuracy](https://img.shields.io/badge/Accuracy-81.6%25-green)](https://github.com/Soumyadeeproy2001/credit-risk-model/edit/main/README.md)
[![AUC-ROC](https://img.shields.io/badge/AUC--ROC-0.756-purple)](https://github.com/Soumyadeeproy2001/credit-risk-model/edit/main/README.md)

## 🎯 Problem Statement
Can we predict which credit card clients will default
on their payment next month, using only data that was
already available?

## 📊 Dataset
- **Source**: UCI Machine Learning Repository
- **Reference**: Yeh & Lien (2009)
- **Size**: 30,000 clients, 23 features + 1 target
- **Target**: `default payment next month` (1 = default)
- **Class distribution**: 78% no default, 22% default

## ⚙️ Pipeline
1. Data cleaning & EDA (countplot, age distribution)
2. One-hot encoding of 9 categorical features (82 total)
3. 80/20 stratified train-test split
4. StandardScaler normalization (fit on train only)
5. Logistic Regression (max_iter=1000)

## 📈 Results
| Metric | Score |
|--------|-------|
| Accuracy | **81.6%** |
| AUC-ROC | **0.756** |
| Precision (default class) | 0.66 |
| Recall (default class) | 0.35 |
| F1-Score (default class) | 0.46 |

## 🔑 Key Insights
- **PAY_0** (September repayment status) is the strongest
  predictor — Odds Ratio 1.79×
- Higher **LIMIT_BAL** reduces default risk (OR 0.76×)
- **Recall gap** on the default class (0.35) indicates
  class imbalance — addressed in v2



## 🛠️ Tech Stack
Python · pandas · numpy · scikit-learn · seaborn · matplotlib


```bash
git clone https://github.com/[your-username]/credit-risk-model
pip install pandas numpy scikit-learn seaborn matplotlib openpyxl
jupyter notebook credit_risk.ipynb
```
