# Data Visualization

## Overview

Data visualization is an important step in understanding the relationships between Human Development Index (HDI) and its influencing factors. In this project, multiple visualizations are created using **Matplotlib** and **Seaborn** to explore the dataset and identify important features for machine learning.

To keep the plots clear and readable, the first **20 rows** of the dataset are selected and stored in a new DataFrame named `data1`.

```python
data1 = dataset.head(20)
```

---

## 1. Display Unique Country Names

Retrieve all unique country names from the dataset.

```python
dataset["Country"].unique()
```

**Purpose:**
- Displays all unique countries.
- Verifies that there are no duplicate country names.
- Confirms the integrity of the dataset.

---

## 2. Mean Years of Schooling vs HDI

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.stripplot(
    x="Mean Years of Schooling",
    y="HDI Score",
    data=data1
)

plt.title("Mean Years of Schooling vs HDI")
plt.show()
```

**Purpose:**
- Shows the relationship between education and HDI.
- Helps determine whether higher education levels contribute to higher HDI scores.

---

## 3. Life Expectancy vs HDI

```python
sns.stripplot(
    x="Life Expectancy",
    y="HDI Score",
    data=data1
)

plt.title("Life Expectancy vs HDI")
plt.show()
```

**Purpose:**
- Visualizes the relationship between life expectancy and HDI.
- Demonstrates how longevity influences human development.

---

## 4. Correlation Heatmap

```python
plt.figure(figsize=(12,8))

sns.heatmap(
    dataset.corr(numeric_only=True),
    annot=True,
    cmap="coolwarm"
)

plt.title("Correlation Heatmap")
plt.show()
```

**Purpose:**
- Displays correlation coefficients between numerical features.
- Identifies features with the strongest relationship to the HDI Score.
- Helps select the most relevant input variables for model training.

---

## Visualization Summary

The visualizations help to:

- Understand the dataset structure.
- Identify relationships between HDI and key indicators.
- Detect feature importance.
- Support feature selection for machine learning.
- Improve model performance through exploratory data analysis.

---

## Technologies Used

- Pandas
- Matplotlib
- Seaborn
- NumPy
