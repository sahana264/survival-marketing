# Survival Analysis for Marketing

Predict when customers will churn, upgrade or buy again - with solid statistics

## Table of Contents

### Part I - Foundations

1. **Introduction : Why Survival Analysis in Marketing**
- Why time-to-event is different from churn classification
- Examples : subscription cancellations, repeat purchase, upgrade timing
- How cesoring appears in marketing data

2. **Core Concepts**
- Survival function $$S(t)$$
- Hazard function $$h(t)$$ and cumulative hazard $$H(t)$$ 
- Right, left and interval censoring
- Data structure: $$((T, \delta, X)) $$

3. **Exploratory Survival Analysis**
- Kaplan-Meier estimator (derivation & Greenwood variance)
- Nelson-Aalen cumulative hazard
- Comparing cohorts with log-rank and weighted log-rank tests
- Visualising retention curves

---

### Part 2 - Classical Statistical Models


4. **Cox Proportional Hazards** 
- Model $$h(t|X)=h_0(t)\exp(\beta^\top X\)$$
- Partial likelihood & score equations
- Interpreting hazard ratios for marketing covariates
- Checking the proportional hazards assummption (Schoenfeld residuals, time-varying effects)

5. **Parametric and Accelerated Failiure Time Models (AFT) Models**
- Exponential, Weibull, Log-normal, Log-logistic
- AFT model: $$(\log T = X\beta+\sigma\varepsilon)\$$
- Model Selection using AIC/BIC

6. **Model Evaluation Checklist**
- Cocncordance index (C-index)
- Integrated Brier Score and time-dependent AUC
- Calibration of survival curves
- Feature importance: hazard ratios, permutation, SHAP

---

### Part III - Machine Learning Approaches

7. **Random Survival Models**
- Survival trees and log-rank splitting
- Minimal depth & permutation importance
- Marketing example : heterogeneous churn drivers

8. **Boosted Survival Models**
- Gradient boosting with Cox-Partial likelihood
- XGBoost / LightGBM AFT survival objectives
- CatBoost with custom survival loss (great for categorical marketing features)

9. **Deep Survival Models**
- DeepSurv (neural network + Cox loss)
- Extensions : DeepHit and other neural survival models
- When to use deep models for clickstream or embedding features

---

### Part IV - Applications and Deployment
10. **Customer Lifetime Value (CLV)**
- Using survival to predict expected lifetime and monetary value
- Discounting and revenue forecasting

11. **Campaign & Cohort Retention Analysis**
- Comparing retention curves between campaign groups
- Measuring incremental lift

12. **Product Adoption & Upgrade Timing**
- Time to up-sell/cross-sell
- Forecasting product adoption

13. **Practical Workflow & MLOps Notes**
- Data preparation and feature engineering
- Pipelines, versioning, and monitoring hazard shift

14. **Case Studies**
- Subscription churn prediction end-to-end
- E-commerce reorder & CLV forecasting
- Campaign test vs. control analysis
