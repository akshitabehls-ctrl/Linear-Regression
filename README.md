# 📌 Linear Regression From Scratch

This repository presents a manual implementation of linear regression using Python, NumPy and basic numerical operations. The objective is to derive the regression solution directly from first principles, apply it to a real dataset and evaluate model performance without relying on machine learning libraries.

---

## 📂 Contents

```
simple-linear-regression-from-scratch.ipynb
placement.csv
```

The notebook includes complete preprocessing, model derivation, parameter computation, prediction generation and visualisation.

---

## 📖 Mathematical framework

Linear regression models the target variable ( y ) as a linear function of predictor ( x ):

[
y = mx + b
]

where:

* ( m ) represents the slope (weight)
* ( b ) represents the intercept (bias)

The optimal parameters minimise the residual sum of squares:

[
\text{RSS}(m, b) = \sum_{i=1}^{n} (y_i - (mx_i + b))^2
]

Closed-form solutions for simple linear regression are computed as:

[
m = \frac{\sum_{i=1}^{n}(x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n}(x_i - \bar{x})^2}
]

[
b = \bar{y} - m\bar{x}
]

Predictions follow:

[
\hat{y} = mx + b
]


---

## 🔬 Notebook workflow

The notebook performs the following sequence:

* dataset loading and inspection
* feature-target extraction
* visualisation of linear trends
* manual computation of regression parameters
* prediction generation
* model performance evaluation
* predicted vs actual plotting

---

## 📈 Output

The model generates:

* best-fit regression parameters
* predicted values
* residual distributions
* scatter plot with regression line

---

## 🔧 Requirements

* Python
* NumPy
* Pandas
* Matplotlib

```bash
pip install numpy pandas matplotlib
```
