# Loading and Understanding the Dataset

## Overview

The dataset is loaded into a **Pandas DataFrame** to begin the data analysis process. The dataset is provided in **CSV (Comma-Separated Values)** format and contains various Human Development Index (HDI) indicators for different countries.

After loading the dataset, the `head()` method is used to display the first five rows. This provides a quick overview of the dataset's structure, available features, and sample values.

The dataset contains **195 rows** (countries) and **82 columns** (human development indicators).

---

## Import the Pandas Library

```python
import pandas as pd
```

---

## Load the Dataset

```python
dataset = pd.read_csv("dataset/hdi_dataset.csv")
```

---

## Display the First Five Rows

```python
dataset.head()
```

**Purpose:**
- Displays the first five rows of the dataset.
- Provides a quick overview of the available features.
- Helps verify that the dataset has been loaded correctly.

---

## Check the Dataset Shape

```python
dataset.shape
```

**Output:**

```python
(195, 82)
```

**Explanation:**
- **195 Rows** → Represents 195 countries.
- **82 Columns** → Represents 82 Human Development Index indicators and related features.

---

## Display Dataset Information

```python
dataset.info()
```

**Purpose:**
- Displays the total number of rows and columns.
- Shows the data type of each column.
- Identifies missing (null) values.
- Provides memory usage information.

---

## Summary

Loading the dataset into a Pandas DataFrame is the first step in the machine learning workflow. By inspecting the dataset using `head()`, `shape`, and `info()`, we gain an understanding of its structure, dimensions, features, and data quality before performing preprocessing, visualization, and model training.
