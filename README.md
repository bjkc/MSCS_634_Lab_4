# MSCS 634 - Lab 4: Regression Analysis & Regularization Methods

## Overview
This laboratory assignment explores multiple regression modeling techniques using the official **Diabetes Dataset** loaded directly from `sklearn.datasets`. The main goal is to compare simple linear regression, multiple regression, polynomial regression, and regularization methods (Ridge and Lasso) to evaluate model accuracy, analyze parameter behavior, and address overfitting.

---

## Dataset Description
* **Source:** `sklearn.datasets.load_diabetes` (Real-world dataset)
* **Records:** 442 patient samples
* **Features:** 10 baseline predictor variables (age, sex, bmi, average blood pressure, s1-s6 blood serum measurements)
* **Target:** Quantitative measure of disease progression one year after baseline

---

## Lab Workflow
1. **Data Preparation**:
   - Loaded the standard Scikit-Learn Diabetes dataset directly (no synthetic data generation).
   - Verified data integrity and confirmed 0 missing values.
2. **Simple Linear Regression**:
   - Evaluated disease progression predictions using `bmi` as a single feature.
3. **Multiple Linear Regression**:
   - Expanded model training to incorporate all 10 independent baseline attributes.
4. **Polynomial Regression**:
   - Applied degree 2 polynomial feature transformations.
   - Evaluated higher degrees to demonstrate the clear transition into model overfitting as training error drops while testing error spikes.
5. **Regularization (Ridge & Lasso)**:
   - Standardized features using `StandardScaler`.
   - Applied Ridge ($L_2$) and Lasso ($L_1$) regularized regression to control model complexity and coefficient magnitudes.

---

## Model Comparison & Observations
* **Simple vs. Multiple Regression**: Incorporating all baseline medical predictors yields better $R^2$ performance than relying on `bmi` alone.
* **Polynomial Behavior**: Higher polynomial degrees lead to high variance and overfitting on test data, raising the RMSE test score significantly.
* **Ridge vs. Lasso**: Ridge regression distributes shrinkage across all terms, while Lasso forces minor feature coefficients down to zero, performing implicit feature selection.

---

## Repository Structure
* `lab4_regression.ipynb` - Complete Jupyter notebook with data preparation, models, evaluation metrics (MAE, MSE, RMSE, R²), and visualization plots.
* `README.md` - Assignment documentation and summary analysis.