# Feature Selection

## Overview

Feature selection is an important step in the machine learning process. In this stage, the dataset is divided into **independent variables (X)** and the **dependent variable (Y)**.

- **Independent Variables (X):** These are the input features used to train the machine learning model.
- **Dependent Variable (Y):** This is the target variable that the model predicts, which is the **HDI Score**.

Selecting the appropriate features improves the model's accuracy and helps identify the factors that influence the Human Development Index.

---

## Independent Variables (X)

The independent variables are selected from the dataset using their column index positions. These columns contain the input features required for training the model.

Example features include:

- Country
- Life Expectancy
- Mean Years of Schooling
- Expected Years of Schooling
- Gross National Income (GNI)
- Other HDI-related indicators

```python
X = dataset.iloc[:, [2, 5, 6, 7, 8]].values
```

**Purpose:**
- Stores all input features.
- Used to train the machine learning model.
- Represents the factors that influence the HDI score.

---

## Dependent Variable (Y)

The dependent variable is the **HDI Score**, which is the value the model aims to predict.

```python
Y = dataset.iloc[:, 4].values
```

**Purpose:**
- Stores the target variable.
- Used during model training and evaluation.
- Represents the Human Development Index (HDI) score.

---

## Summary

Feature selection separates the dataset into input features (**X**) and the target variable (**Y**). This prepared data is then used for preprocessing, model training, testing, and evaluation, enabling the machine learning model to learn the relationship between the selected indicators and the HDI score.
