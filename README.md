# Project 101 - Explainable AI Finance

## Overview
Project 101 is focused on building an **Explainable AI (XAI) model** for financial stock data.  
The project aims to analyze historical stock data, engineer features, train machine learning models, and generate explainable predictions for better financial decision-making.

---

## Current Progress (Updated as of 2025-12-21 at 4:06 AM)

### 1. Data Loading and Cleaning
- Loaded historical stock data from CSV.
- Converted `Date` column to datetime type for time series operations.
- Cleaned `Vol.` (trading volume) column:
  - Converted "M" and "K" suffixes to numeric values.
  - Filled missing values using forward/backward fill.
- Converted `Change %` column to float.
- Verified no missing data remains.

### 2. Data Exploration
- Visualized closing price over time.
- Basic summary statistics generated.

---

## Next Steps
- Feature Engineering:
  - Create technical indicators (moving averages, RSI, etc.)
  - Prepare features and target variables for modeling
- Model Training:
  - Train Random Forest, Linear Regression, or other models
- Explainability:
  - Apply SHAP, feature importance, and generate explanations
- Model Evaluation:
  - Visualize performance metrics and validate predictions

---

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/HassanMBaragbah/Project_101.git
```

2. Create a virtual environment and install dependencies:
```bash
python -m venv venv
source venv/Scripts/activate  # Windows
pip install -r requirements.txt
```


3. Open the notebooks in Jupyter or VS Code and run cells sequentially.