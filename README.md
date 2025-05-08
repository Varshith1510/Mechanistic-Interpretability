# Mechanistic Interpretability for Logistic Regression

This project explores **mechanistic interpretability** for a **logistic regression model**, focusing on how model predictions are influenced by input features. Using **SHAP (SHapley Additive exPlanations)** values, predictions are broken down to a granular level to understand which features push predictions toward positive or negative classes.

## Objective

To interpret the internal mechanics of a logistic regression model trained on a binary classification task (e.g., Titanic survival prediction), using SHAP summary and force plots.

## Methodology

- Trained a logistic regression model on tabular data.
- Visualized feature impacts using:
  - **SHAP Summary Plot**: Highlights overall feature influence across the dataset.
  - **SHAP Force Plot**: Breaks down individual predictions into positive or negative contributors.

## How to interpret these plots

### SHAP Summary Plot

- **Positive SHAP values** → contribute to predicting the **positive class** (e.g., survival in our case).
- **Negative SHAP values** → contribute to the **negative class** (e.g., non-survival in our case).

**Examples:**
- `Sex`: Females (class 0) had high positive SHAP values, implying higher survival chances.
- `Age`: Elderly passengers had more negative SHAP values, implying less or no chances of survival.

### SHAP Force Plot

- Displays **log-odds (f(x))** before applying the logistic function.
- Arrows show feature contributions:
  - **Red arrows**: Push toward positive class (survival).
  - **Blue arrows**: Push toward negative class (non-survival).
- Useful for interpreting **individual predictions**.
