# Train-Test Split

## Overview

Splitting the dataset into **training** and **testing** sets is an essential step in the machine learning workflow. It enables the model to learn from one portion of the data and then evaluate its performance on unseen data.

The **training dataset** is used to train the machine learning model by learning the relationship between the input features and the target variable.

The **testing dataset** is used to evaluate how well the trained model performs on new, unseen data. This helps determine whether the model can generalize effectively rather than simply memorizing the training data.

---

## Import the Required Library

```python
from sklearn.model_selection import train_test_split
```

---

## Split the Dataset

```python
X_train, X_test, Y_train, Y_test = train_test_split(
    X,
    Y,
    test_size=0.2,
    random_state=42
)
```

---

## Parameters

| Parameter | Description |
|-----------|-------------|
| `X` | Independent variables (input features). |
| `Y` | Dependent variable (HDI Score). |
| `test_size=0.2` | Uses 20% of the data for testing and 80% for training. |
| `random_state=42` | Ensures reproducible results by using the same random split every time. |

---

## Output

The dataset is divided into four parts:

- **X_train** – Training input features
- **X_test** – Testing input features
- **Y_train** – Training target values
- **Y_test** – Testing target values

---

## Benefits of Train-Test Split

- Prevents overfitting.
- Evaluates model performance on unseen data.
- Measures the model's ability to generalize.
- Provides reliable performance evaluation.
- Supports accurate model validation before deployment.

---

## Summary

The `train_test_split()` function from Scikit-learn divides the dataset into training and testing subsets. The model is trained using the training data and evaluated using the testing data, ensuring that it performs well on unseen data before deployment.
