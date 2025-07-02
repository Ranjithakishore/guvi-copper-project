# guvi-copper-project

## Overview

This project is an Industrial Copper Modeling Application that predicts the selling price and status (Won/Lost) of copper sales orders using machine learning models. It provides a Streamlit web interface for user interaction and includes data preprocessing, exploratory analysis, model training, and prediction functionalities.

---

## Project Structure

- `copper_main.py`  
  Streamlit app for predicting selling price and status using trained models.
- `copper_test.ipynb`  
  Jupyter notebook for data exploration, preprocessing, model training, evaluation, and saving models.
- `data/Copper_Set.csv`  
  Main dataset containing copper sales records.
- `model.pkl`, `scaler.pkl`, `t.pkl`, `s.pkl`  
  Artifacts for the selling price regression model and its encoders/scalers.
- `cmodel.pkl`, `cscaler.pkl`, `ct.pkl`  
  Artifacts for the status classification model and its encoders/scalers.
- `requirements.txt`  
  Python dependencies for the project.

---

## Data Description

The dataset ([data/Copper_Set.csv](data/Copper_Set.csv)) contains the following columns:
- `id`, `item_date`, `quantity tons`, `customer`, `country`, `status`, `item type`, `application`, `thickness`, `width`, `material_ref`, `product_ref`, `delivery date`, `selling_price`

---

## Usage

### 1. Data Exploration & Model Training

Open and run [`copper_test.ipynb`](copper_test.ipynb) to:
- Clean and preprocess the data (handle missing values, convert types, log-transform skewed features).
- Visualize distributions and correlations.
- Train a Decision Tree Regressor for selling price prediction.
- Train a Decision Tree Classifier for status prediction.
- Save trained models and encoders as `.pkl` files.

### 2. Web Application

Run the Streamlit app to interactively predict selling price and status:

```sh
streamlit run copper_main.py
