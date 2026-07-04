# Dataset Collection

## Overview

The dataset used in this project was collected from publicly available open-source platforms. Common sources for machine learning datasets include:

- Kaggle
- Data.gov
- UCI Machine Learning Repository

For this project, the **Human Development Index (HDI)** dataset was obtained from the GitHub repository associated with the guided project.

---

## Dataset Source

**Source:** GitHub (Guided Projects)

**Dataset Download Link:**

https://github.com/Guided-Projects/HumanDevelopmentIndex/tree/main/Dataset

---

## Dataset Description

The dataset contains information related to the Human Development Index (HDI) and its contributing factors. It is used to train and evaluate the machine learning model for predicting HDI values.

The dataset includes features such as:

- Country Name
- Life Expectancy
- Education Index
- Income Index
- Human Development Index (Target Variable)

---

## Steps to Use the Dataset

1. Download the dataset from the link above.
2. Save the dataset in the `dataset/` folder of the project.
3. Load the dataset using the Pandas library.
4. Explore the dataset to understand its structure and features.
5. Perform preprocessing before training the machine learning model.

---

## Loading the Dataset

```python
import pandas as pd

dataset = pd.read_csv("dataset/hdi_dataset.csv")
dataset.head()
```

---

## Summary

The dataset serves as the foundation of the HDI Prediction System. Proper understanding and preprocessing of the dataset are essential for building an accurate and reliable machine learning model.
