# Linear Regression: Analytical Implementation and Model Validation

This repository documents the analytical implementation of **simple** and **multiple** linear regression using Python and NumPy, developed without machine learning libraries. The project focuses on deriving regression parameters mathematically, implementing the complete modelling pipeline from first principles, and validating results against scikit-learn for correctness and convergence.

The work is divided across two notebooks:

* **Simple Linear Regression (from scratch)**
* **Multiple Linear Regression (from scratch + sklearn comparison)**

This structure allows for progressive exploration, beginning with single variable estimation and extending into higher dimensional regression via matrix algebra.

---

## Project Objectives

1. Derive regression parameters analytically rather than algorithmically.
2. Implement simple linear regression using statistical closed-form equations.
3. Implement multiple linear regression using the Normal Equation.
4. Integrate intercept computation through feature augmentation.
5. Validate parameter estimates and predictions against scikit-learn.
6. Compare model behaviour across univariate and multivariate settings.

---

## Mathematical Formulation

### Simple Linear Regression

The relationship between predictor ( x ) and response ( y ) is modeled as:

$$
y = mx + b
$$


Closed-form estimates are obtained using sample statistics:

$$
m = \frac{\sum (x - \bar{x})(y - \bar{y})}{\sum (x - \bar{x})^2}
$$

$$
b = \bar{y} - m\bar{x}
$$


---

### Multiple Linear Regression

For multiple predictors, the model generalises to:

$$
\hat{y} = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n
$$

Written in matrix form:

$$
\hat{y} = X\beta
$$

Coefficient estimation follows the **Normal Equation**:

$$
\beta = (X^{T}X)^{-1}X^{T}y
$$

The intercept term is incorporated by augmenting ( X ) with a column of ones.

---

## Implementation Overview

### Notebook 1: *Simple Linear Regression*

* univariate dataset selection
* parameter estimation using summary statistics
* prediction generation
* visualisation of regression line
* manual error assessment

### Notebook 2: *Multiple Linear Regression*

* multivariate dataset formulation
* regression class implementation
* parameter computation via matrix algebra
* scikit-learn regression fitting
* prediction and performance comparison
* alignment of coefficients and intercepts

---

## Validation and Cross-Verification

Both models were cross-checked against scikit-learn outputs to verify:

* parameter equivalence
* prediction consistency
* error minimisation
* numerical stability

---

## Results

The notebooks demonstrate:

* accurate coefficient estimation in both cases
* stable prediction behaviour
* convergence with sklearn outcomes
* interpretable parameter structure
* clear visual and numerical diagnostics

Residual plots, predicted–actual comparisons, and evaluation metrics reinforce regression reliability.

---

## Requirements

```
Python
NumPy
Pandas
Matplotlib
scikit-learn (for comparison)
```

Installation:

```bash
pip install numpy pandas matplotlib scikit-learn
```

---

## Repository Structure

```
simple-linear-regression-from-scratch.ipynb
multiple-linear-regression-scratch-sklearn.ipynb
README.md
```
