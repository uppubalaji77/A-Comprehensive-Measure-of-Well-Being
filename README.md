# Project Structure

To maintain a clean, organized, and scalable project, create the folder structure shown below. Organizing files into dedicated directories improves project maintainability, simplifies navigation, and prevents path-related issues during development and deployment.

After creating the folders, place each file in its appropriate directory according to the project architecture.

## Folder Structure

```
HDI-Prediction-System/
│
├── dataset/
│   └── hdi_dataset.csv
│
├── models/
│   └── hdi_prediction_model.pkl
│
├── notebooks/
│   └── HDI_Analysis.ipynb
│
├── src/
│   ├── train_model.py
│   ├── predict.py
│   └── preprocessing.py
│
├── templates/
│   ├── index.html
│   └── result.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
│
├── reports/
│   └── visualization_report.pdf
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Directory Description

| Folder | Description |
|---------|-------------|
| `dataset/` | Stores the dataset used for training and testing the model. |
| `models/` | Contains the trained machine learning model files. |
| `notebooks/` | Jupyter notebooks used for data analysis and experimentation. |
| `src/` | Python source code for preprocessing, training, and prediction. |
| `templates/` | HTML templates used by the Flask web application. |
| `static/` | Static resources such as CSS, JavaScript, and images. |
| `reports/` | Stores generated reports and visualizations. |

---

## Verification

Before proceeding with development, ensure that:

- All folders have been created successfully.
- Every file is placed in the correct directory.
- The project structure matches the architecture shown above.
- Required dependencies have been installed.
- File paths are correctly configured.

A well-organized project structure improves readability, simplifies maintenance, and ensures that all modules, resources, and assets can be accessed correctly during development and deployment.
