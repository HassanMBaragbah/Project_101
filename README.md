# Project 101 - Explainable AI Finance

## Overview
Project 101 is focused on building an **Explainable AI (XAI) model** for financial stock data.  
The project aims to analyze historical stock data, engineer features, train machine learning models, and generate explainable predictions for better financial decision-making.


## Goals
- Build a clean and reproducible ML pipeline from EDA → Feature Engineering → Modeling → Explainability.
- Avoid common time-series pitfalls such as data leakage.
- Provide global and local explanations for model decisions (trust, transparency, and error analysis).


---

## Workflow Summary
1. **EDA (01)**  
   Inspect dataset structure and quality, then save a cleaned version for reproducibility.

2. **Feature Engineering (02)**  
   Create interpretable features that reflect market behavior:
   - momentum (returns + lags)
   - trend (moving averages)
   - risk/uncertainty (volatility)
   - participation (volume change)

3. **Baseline Modeling (03)**  
   Train a Random Forest classifier with a **time-based split** (chronological 80/20) to avoid leakage.

4. **Explainability (04)**  
   Use **SHAP** to:
   - understand global feature influence (summary plot)
   - explain a single prediction (waterfall plot)
   - explain misclassifications (error analysis)

## Target Definition
Binary classification:
- `target = 1` if next day close > current day close
- `target = 0` otherwise

## Reproducibility Notes
- Processed datasets are saved under `data/processed/` to avoid re-running preparation steps.
- The trained baseline model is saved under `models/` for consistent explainability and comparisons.

## How to Run
1. Install dependencies:
```bash
pip install -r requirements.txt
```
2. Run notebooks in order:

01_data_exploration.ipynb

02_feature_engineering.ipynb

03_modeling_baseline.ipynb

04_model_explainability.ipynb

## Key Deliverables

Cleaned dataset (```stock_data_clean.csv```)

Engineered feature dataset (```stock_features_v1.csv```)

Baseline model (```rf_baseline_v1.pkl```)

Explainability notebook with SHAP global/local explanations and error analysis

## License

For educational and portfolio purposes.