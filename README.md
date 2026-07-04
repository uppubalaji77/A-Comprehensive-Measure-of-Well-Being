# Model Prediction and Evaluation

## Overview

After training the Linear Regression model, the next step is to generate predictions using the testing dataset and evaluate the model's performance. The predicted HDI values are compared with the actual HDI values to determine how accurately the model performs. Evaluation metrics such as the **R-squared (R²) score** are used to measure the model's predictive capability.

---

## Generate HDI Predictions

Use the trained model to predict HDI values for the testing dataset.

```python
y_pred = model.predict(X_test)

print(y_pred)
```

**Purpose:**
- Generates predicted HDI scores.
- Displays the predicted values.
- Enables comparison with the actual HDI scores.

---

## Calculate the R-Squared (R²) Score

The R-squared score measures how well the independent variables explain the variation in the dependent variable.

```python
from sklearn.metrics import r2_score

r2 = r2_score(Y_test, y_pred)

print("R² Score:", r2)
```

**Purpose:**
- Evaluates the performance of the Linear Regression model.
- A value closer to **1.0** indicates a better fit and higher prediction accuracy.

---

## Test the Model with a Single Input

Validate the model by predicting the HDI score for an individual data point.

```python
sample_prediction = model.predict([X_test[0]])

print(sample_prediction)
```

**Purpose:**
- Tests the model using a single sample.
- Verifies that the model produces predictions for new input data.

---

## Display Actual HDI Values

Print the actual HDI scores from the testing dataset.

```python
print(Y_test)
```

**Purpose:**
- Displays the ground truth values.
- Used for comparison with the predicted values.

---

## Display Predicted HDI Values

Print the predicted HDI scores.

```python
print(y_pred)
```

**Purpose:**
- Displays the model's predicted values.
- Allows comparison with the actual HDI scores.

---

## Compare Actual vs Predicted Values

```python
import pandas as pd

comparison = pd.DataFrame({
    "Actual HDI": Y_test,
    "Predicted HDI": y_pred
})

print(comparison.head())
```

**Purpose:**
- Compares actual and predicted HDI scores.
- Helps evaluate prediction accuracy.
- Identifies any significant differences between actual and predicted values.

---

## Summary

The trained Linear Regression model generates HDI predictions using the testing dataset. The **R² score** is calculated to evaluate model performance, while the comparison of **actual** and **predicted** HDI values confirms the accuracy and reliability of the model before deployment.
