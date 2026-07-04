# Importing Required Libraries

Before developing the machine learning model, it is important to import all the required Python libraries that will be used throughout the project. These libraries provide the necessary tools for loading datasets, performing data preprocessing, creating visualizations, training machine learning models, and evaluating their performance.

Importing all required libraries at the beginning of the program helps maintain an organized and efficient workflow. It also improves code readability, simplifies debugging, and ensures that all dependencies are available before data analysis and model development begin.

## Required Libraries

### NumPy

```python
import numpy as np
```

**Purpose:**
- Numerical computations
- Array operations
- Mathematical functions

---

### Pandas

```python
import pandas as pd
```

**Purpose:**
- Load CSV datasets
- Data cleaning
- Data manipulation
- Data analysis

---

### Matplotlib

```python
import matplotlib.pyplot as plt
```

**Purpose:**
- Create graphs and charts
- Visualize trends
- Plot model results

---

### Seaborn

```python
import seaborn as sns
```

**Purpose:**
- Statistical data visualization
- Heatmaps
- Pair plots
- Distribution plots
- Correlation analysis

---

### Scikit-learn

```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
```

**Purpose:**
- Split the dataset into training and testing sets
- Train the Linear Regression model
- Evaluate model performance

---

### Pickle

```python
import pickle
```

**Purpose:**
- Save the trained machine learning model
- Load the model for future predictions

---

### Flask

```python
from flask import Flask, render_template, request
```

**Purpose:**
- Build the web application
- Handle user requests
- Display prediction results

---

## Complete Import Statements

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import pickle

from flask import Flask, render_template, request
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
```

## Summary

These libraries form the foundation of the HDI Prediction System. They support data preprocessing, visualization, machine learning model development, model serialization, and deployment through the Flask web application.
