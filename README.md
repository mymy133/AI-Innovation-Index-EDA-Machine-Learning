# AI-Innovation-Index-EDA-Machine-Learning

This project analyzes a dataset of 62 countries with metrics such as:
**Source:** [Kaggle – Salary Dataset]([https://www.kaggle.com/datasets/katerynameleshenko/ai-index/data])  

# 📌 Overview
This project analyzes a dataset of 62 countries with metrics such as:
Talent
Infrastructure
Operating Environment
Research
Development
Government Strategy
Commercial
Total score (composite index)
The workflow includes:
Exploratory Data Analysis (EDA) with visualizations by Region, Income group, and Political regime.
Linear regression models to predict the Total score.
Evaluation metrics: R² and Mean Absolute Error (MAE).


# 📊 EDA Highlights
Strongest correlations with Total score are for Talent, Research, and Commercial.
Europe has the highest number of countries in the dataset.
Most countries are Liberal democracies or Electoral democracies.

# 🤖 Modeling
Two regression models were built:

| Model | Features | Test Size | Random State | R² Score |
|-------|----------|-----------|--------------|----------|
| **Single Feature (Research)** | Research | 15% | 321 | 0.822 |
| **Multiple Features** | All numeric except Total score | 20% | 42 | 0.999 |


# 📈 Interpretation & Caveats
The single-feature model shows Research is a strong driver of the total index.
The multiple-feature model has near-perfect performance because Total score is likely derived from these same features (possible target leakage).
Dataset is small (62 rows) → metrics might be unstable without cross-validation.
Random train-test splits can affect results significantly.

# ✅ Conclusion
Research, Talent, and Commercial capacity are the top predictors of the Total score.
A simple model with only Research achieves R² ≈ 0.82.
The multiple-features model achieves R² ≈ 0.999, likely due to target leakage.
Policy implication: investing in research boosts overall innovation readiness.
Analytics implication: apply cross-validation and regularization to ensure generalization.




