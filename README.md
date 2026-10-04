# Churn Radar — Predict, Explain, Retain

> Who will leave, why, and which customers are worth saving first.

![status](https://img.shields.io/badge/status-design%20stage-lightgrey) ![sprint](https://img.shields.io/badge/sprint-Weeks%203--4-blue) ![project](https://img.shields.io/badge/portfolio-02%2F08-0891b2)

| | |
|---|---|
| **Category** | Data Science / ML |
| **Domain** | Telecom / SaaS |
| **Stack** | SQL · Python · scikit-learn · XGBoost · SHAP · Power BI |
| **Status** | 🚧 Scoped — implementation not started |

## Overview

A churn-prediction system built on a unified Customer 360 dataset. It goes beyond accuracy: every customer gets a churn probability, the reasons behind it (SHAP), and a priority score that weighs risk against customer value, so the retention team knows exactly where to spend its budget.

## Business problem

A telecom / SaaS company is losing customers and needs to know who will churn, why, which customers to target first, and how much revenue is at risk.

## What this project demonstrates

- End-to-end supervised ML workflow with a fair model comparison
- Feature engineering from behavioural data
- Model explainability with SHAP
- Optimising for business value, not only accuracy

## Key points

- Customer 360 table joining subscriptions, usage, payments and support tickets
- Behavioural feature engineering (tenure, usage trend, payment delays, complaints, contract type)
- Model ladder: logistic-regression baseline → Random Forest → XGBoost / LightGBM, compared fairly
- Evaluation on ROC-AUC, precision/recall, Precision@K, plus revenue at risk and revenue saved
- SHAP explanations per customer (e.g. 82% risk: low usage, recent complaints, short contract)
- Priority score = churn probability × customer value × expected retention uplift, shown in a Power BI dashboard

## Planned architecture

```text
Customer data (subscriptions, usage, payments, tickets)
   ↓
Customer 360 table
   ↓
Feature engineering & EDA
   ↓
Baseline → advanced models
   ↓
Evaluation & SHAP explainability
   ↓
Priority score & retention dashboard
```

## Planned deliverables

- [ ] Customer 360 dataset
- [ ] EDA notebook
- [ ] Training pipeline and model comparison
- [ ] Per-customer SHAP explanations
- [ ] Power BI retention dashboard
- [ ] Retention strategy & business case

## Success metrics

- ROC-AUC, precision, recall, F1, Precision@K / Recall@K
- Revenue at risk and revenue potentially saved
- Priority = churn probability × customer value × expected retention uplift

## Planned structure

```text
data/  notebooks/  src/{data,features,models}  dashboard/  docs/
```

## Roadmap

- [x] Scope and README
- [ ] Data collection / generation
- [ ] Core implementation
- [ ] Evaluation and business-impact estimate
- [ ] Demo, write-up and interview notes

---

Part of my **Data & AI × Business Consulting** portfolio, a 16-week sprint of 8 projects going from data and BI to ML, GenAI, agents, automation and AI strategy. See all projects on my [GitHub profile](https://github.com/Amine-Charrou).

*Amine Charrou · Final-year Data Science & AI engineering student, ENSA Agadir · [LinkedIn](https://www.linkedin.com/in/amine-charrou/)*
