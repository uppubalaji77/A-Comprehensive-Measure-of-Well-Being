# Flask Web Application

## Overview

After training and saving the machine learning model, the next step is to develop a web application using **Flask**. Flask provides a lightweight framework for building web applications, handling user requests, and displaying prediction results.

The trained HDI prediction model is loaded using the **Pickle** module, while **NumPy** is used to process numerical input data before passing it to the model for prediction.

---

## Import Required Libraries

Import the required libraries for the Flask application.

```python
from flask import Flask, render_template, request
import numpy as np
import pickle
```

**Purpose:**
- **Flask** – Creates the web application and manages routes.
- **Pickle** – Loads the trained machine learning model.
- **NumPy** – Handles numerical input data for prediction.

---

## Initialize the Flask Application

Create a Flask application and load the saved HDI prediction model.

```python
app = Flask(__name__)

model = pickle.load(open("models/hdi_prediction_model.pkl", "rb"))
```

**Purpose:**
- Initializes the Flask application.
- Loads the trained model into memory.
- Makes the model available for predictions.

---

## Home Route

The home route displays the application's main page.

```python
@app.route("/")
def home():
    return render_template("home.html")
```

**Purpose:**
- Handles requests to the home page.
- Renders the `home.html` template.
- Introduces the HDI Prediction System.

---

## Prediction Route

The `/predict` route receives user input, processes it, and generates an HDI prediction.

```python
@app.route("/predict", methods=["POST"])
def predict():

    input_features = [float(x) for x in request.form.values()]

    final_input = np.array([input_features])

    prediction = model.predict(final_input)

    output = round(prediction[0], 3)

    return render_template(
        "index.html",
        prediction_text=f"Predicted HDI Score: {output}"
    )
```

**Purpose:**
- Accepts user input from the HTML form.
- Converts the input into numerical values.
- Passes the input to the trained model.
- Generates the predicted HDI score.
- Displays the prediction on the web page.

---

## Run the Flask Application

```python
if __name__ == "__main__":
    app.run(debug=True)
```

**Purpose:**
- Starts the Flask development server.
- Enables debugging for easier development and testing.

---

## Application Workflow

1. User opens the web application.
2. The home page is displayed.
3. The user enters HDI-related input values.
4. The input is sent to the `/predict` route.
5. The trained model generates the HDI prediction.
6. The predicted HDI score is displayed on the web page.

---

## Summary

The Flask web application serves as the deployment interface for the HDI Prediction System. It loads the saved machine learning model, accepts user input through a web form, processes the data, and returns the predicted Human Development Index (HDI) score in a user-friendly format.
