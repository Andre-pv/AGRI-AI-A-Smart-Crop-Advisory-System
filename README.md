# AGRI-AI-A-Smart-Crop-Advisory-System

## Abstract

This project focuses on predicting agricultural crop yield based on key environmental and cultivation parameters using machine learning techniques. The workflow began with Exploratory Data Analysis (EDA) to understand relationships among variables such as region, soil type, crop type, rainfall, temperature, fertiliser and irrigation usage, and weather conditions.

Subsequent data preprocessing involved encoding categorical features, scaling numerical values, and transforming binary inputs to prepare the dataset for modelling. Multiple regression models, including Linear Regression and K-Nearest Neighbours (KNN) Regression, were evaluated to identify the best-performing algorithm for yield prediction.

In addition to yield estimation, a rule-based recommendation system was integrated to provide actionable agronomic insights. This system analyses predicted yield alongside crop-specific environmental thresholds to suggest corrective measures such as irrigation adjustments, fertilizer usage, temperature stress mitigation, and alternative crop recommendations.

After evaluation using Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² score, the final model was saved using joblib. A user-friendly web-interface was developed using Python Flask and deployed on a cloud platform, thus enabling accessible and end-to-end decision support for precision agriculture.

## Quick Access Links

* Dataset: [Kaggle - Agriculture Crop Yield Dataset](https://www.kaggle.com/datasets/samuelotiattakorah/agriculture-crop-yield)
* Google Colab Notebook: [EDA and ML Model](https://colab.research.google.com/drive/1gK2qG30H0BKwfNKX7yXnu5DDnJjMKRM8?usp=sharing)
* Model Hosting: [Hugging Face](https://huggingface.co/skcept/crop-yield-prediction)
* Website Hosting: [Render](https://crop-yield-prediction-063b.onrender.com)


## Technologies Used

* Python
* Pandas, NumPy
* scikit-learn
* Flask
* HTML/CSS

## Project Structure

```bash
crop-yield-prediction/
├── static/                 # CSS, images, uploads
├── templates/              # HTML templates
├── .env                    # Environment variables (Hugging Face token)
├── app.py                  # Main Flask application
├── config.py               # Environment & configuration handling
├── model_loader.py         # Loads ML models and encoders
├── preprocessing.py        # Data preprocessing & feature scaling
├── recommendation_engine.py# Rule-based crop recommendations
├── yield_correction.py     # Yield adjustment & threshold logic
├── requirements.txt        # Project dependencies
├── README.md               # Project documentation

```

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/Andre-pv/crop-yield-prediction.git
cd crop-yield-prediction
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Flask app

```bash
python main.py
```

Visit `http://localhost:5000` in your browser.

## Input Parameters

The web app takes the following input fields:

* Region (North, South, East, West)
* Soil Type (Clay, Loam, Sandy, Peaty, Chalky, Silt)
* Crop (Rice, Maize, Wheat, Barley, Cotton, Soybean)
* Rainfall (mm)
* Temperature (Celsius)
* Fertiliser Used (Yes/No)
* Irrigation Used (Yes/No)
* Weather Condition (Sunny, Rainy, Cloudy)
