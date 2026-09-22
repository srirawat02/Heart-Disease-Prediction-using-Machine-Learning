# Heart-Disease-Prediction-using-Machine-Learning

A machine learning project that predicts the risk of heart disease based on a patient's health and clinical information.

I worked on this project to understand the complete machine learning workflow, starting from exploring and cleaning the data to training different classification models and finally deploying the prediction model using Streamlit.

## Project Overview

The dataset contains information such as age, sex, chest pain type, resting blood pressure, cholesterol, maximum heart rate, exercise-induced angina, and other health-related features.

The goal of the project is to predict whether a person is at risk of heart disease (`1`) or not (`0`).

The final model is connected to a simple Streamlit application where users can enter their details and get a prediction.

## Features

- Exploratory Data Analysis (EDA)
- Data cleaning and preprocessing
- Handling zero values in cholesterol and resting blood pressure
- Categorical variable encoding
- Feature scaling using StandardScaler
- Training and comparing multiple classification models
- Model evaluation using Accuracy and F1 Score
- Saving the trained model using Joblib
- Streamlit web application for making predictions

## Dataset

The dataset contains **918 records and 12 columns**.

Some of the important features include:

- `Age`
- `Sex`
- `ChestPainType`
- `RestingBP`
- `Cholesterol`
- `FastingBS`
- `RestingECG`
- `MaxHR`
- `ExerciseAngina`
- `Oldpeak`
- `ST_Slope`

The target variable is:

- `HeartDisease` — 0 = No heart disease, 1 = Heart disease

## Exploratory Data Analysis

I started by looking at the structure of the dataset, checking for missing values and duplicates, and understanding the distribution of different features.

Some of the visualizations included:

- Heart disease class distribution
- Age distribution
- Resting blood pressure distribution
- Cholesterol distribution
- Maximum heart rate distribution
- Heart disease vs. sex
- Heart disease vs. chest pain type
- Heart disease vs. fasting blood sugar
- Cholesterol distribution by heart disease
- Age distribution by heart disease
- Correlation heatmap

## Data Cleaning & Preprocessing

During the data cleaning stage, I checked for missing values and duplicate records.

The dataset also contained zero values for some cholesterol and resting blood pressure entries. Instead of keeping those values, I replaced them with the mean of the non-zero values for the respective feature.

For the machine learning model:

- Categorical variables were converted into numerical features using one-hot encoding.
- Numerical features were standardized using `StandardScaler`.
- The data was split into training and testing sets using an 80/20 split.

## Machine Learning Models

I compared several classification algorithms:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Decision Tree
- Support Vector Machine (SVM)

The models were evaluated using:

- Accuracy
- F1 Score

After comparing the models, I used the **K-Nearest Neighbors (KNN)** model for the Streamlit application.

## Streamlit Application

The trained KNN model was saved along with the scaler and the expected feature columns using Joblib.

The Streamlit application allows the user to enter information such as:

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Fasting blood sugar
- Resting ECG
- Maximum heart rate
- Exercise-induced angina
- Oldpeak
- ST slope

The entered data is processed in the same format as the training data and passed to the trained model.

The application then displays either:

**High Risk of Heart Disease**

or

**Low Risk of Heart Disease**

> This project is for educational purposes only and should not be used as a medical diagnosis or substitute for professional medical advice.

## Tech Stack

**Programming Language**
- Python

**Libraries**
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Streamlit

**Tools**
- Jupyter Notebook
- GitHub
- VS Code
