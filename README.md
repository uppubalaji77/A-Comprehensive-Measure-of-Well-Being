# Handling Missing Values

## Overview

Before training the machine learning model, it is essential to identify and handle missing (null) values in the dataset. Missing values can negatively impact the model's performance and lead to inaccurate predictions.

In this project, null values in the independent variables (**X**) are identified using the `isnull().sum()` method and replaced with the **mean value** of their respective columns using the `fillna()` method.

---

## Step 1: Check for Null Values

Use the following code to count the number of missing values in each selected input feature.

```python
X.isnull().sum()
```

**Purpose:**
- Detects missing (null) values in each column.
- Helps identify which features require preprocessing.
- Ensures data quality before model training.

---

## Step 2: Fill Null Values

Replace the missing values with the mean of each respective column.

```python
X = X.fillna(X.mean())
```

**Purpose:**
- Replaces null values with the column mean.
- Preserves the dataset size by avoiding row deletion.
- Improves the quality of the dataset for machine learning.

---

## Why Use the Mean?

Using the column mean is a common technique for handling missing numerical data because it:

- Maintains the overall distribution of the dataset.
- Prevents data loss by keeping all records.
- Reduces the impact of missing values on model performance.
- Prepares the dataset for effective machine learning.

---

## Summary

Handling missing values is a crucial preprocessing step that improves data quality and ensures the machine learning model receives complete and reliable input data. By identifying null values with `isnull().sum()` and replacing them using `fillna(X.mean())`, the dataset becomes ready for training and evaluation.
