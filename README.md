# HDI Prediction System

## Overview

The HDI Prediction System is a Machine Learning project that predicts the Human Development Index (HDI) of a country using socioeconomic indicators such as life expectancy, education index, and income index.

## Features

- User Management
- Country-wise HDI Prediction
- Machine Learning Model
- Prediction Reports
- Data Visualization
- Dataset Management

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Flask
- HTML
- CSS
- JavaScript
- MySQL

## ER Diagram

```mermaid
erDiagram

USER ||--o{ HDI_INPUT_DATA : submits
COUNTRY ||--o{ HDI_INPUT_DATA : belongs_to
HDI_INPUT_DATA ||--|| HDI_PREDICTION : generates
ML_MODEL ||--o{ HDI_PREDICTION : predicts
HDI_PREDICTION ||--o{ VISUALIZATION_REPORT : creates
DATASET ||--o{ ML_MODEL : trains
USER ||--o{ SESSION : has
```

## Project Structure

```
HDI-Prediction-System/
│
├── README.md
├── dataset/
├── models/
├── notebooks/
├── src/
├── static/
├── templates/
├── reports/
└── requirements.txt
```

## Future Improvements

- Deep Learning Models
- Real-Time Prediction
- Interactive Dashboard
- Cloud Deployment

## Author

Balaji
