# Breast-cancer-classification using machine learning 
This project builds a predictive system to classify breast cancer as malignant or benign using the Breast Cancer Wisconsin (Diagnostic) dataset from the UCI Machine Learning Repository. The system leverages an SVM classifier with hyperparameter tuning and a complete scikit-learn pipeline. In addition, a Flask API is provided to deploy the model for real-time predictions.

## Table of Contents
 [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Model Training](#model-training)
  - [Making Predictions](#making-predictions)
  - [Flask API Deployment](#flask-api-deployment)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Acknowledgements](#acknowledgements)

## Overview

Breast cancer is one of the most common cancers among women. Early detection is critical to effective treatment. This project uses the Breast Cancer Wisconsin (Diagnostic) dataset, which contains 569 samples with 30 features (e.g., radius, texture, perimeter, area, etc.) and corresponding labels. An SVM classifier with an RBF kernel is tuned using GridSearchCV, achieving high accuracy. The project also includes a Flask API for deploying the predictive system.

## Features

- **Data Acquisition:**  
  Fetches the Breast Cancer Wisconsin (Diagnostic) dataset using the `ucimlrepo` package.

- **Data Preprocessing:**  
  - Splits the data into training and testing sets.
  - Standardizes features using `StandardScaler`.
  - Reshapes target labels to avoid warnings.

- **Model Training and Tuning:**  
  - Uses an SVM classifier with hyperparameter tuning via GridSearchCV.
  - Evaluates model performance using accuracy, precision, recall, F1-score, and a confusion matrix.

- **Deployment:**  
  - Saves the trained pipeline (including preprocessing) using `joblib`.
  - Provides a Flask API for real-time predictions.

## Installation

Install required packages:
scikit-learn
matplotlib
seaborn
pandas
numpy
joblib
Flask
ucimlrepo (if available)

## Usage
Model Training
Run the model_training.py script to load the dataset, preprocess the data, train the SVM model with hyperparameter tuning, evaluate the model, and save the pipeline:

python model_training.py
This script will output:

Best hyperparameters found.
Test accuracy, classification report, and a plotted confusion matrix.
A saved model file (breast_cancer_classifier.pkl).
Making Predictions
To test predictions on new data, you can run a separate script (e.g., predict_sample.py):


Flask API Deployment
To deploy the model via a Flask API, run the app.py script:

## Project Structure
graphql
Copy
Edit
Breast-Cancer-Classification/
├── model_training.py       # Script for training and saving the model
├── app.py                  # Flask API for real-time predictions
├── predict_sample.py       # Example script to predict for a single data point
├── requirements.txt        # List of required Python packages
└── README.md               # This file


## Dependencies
Python 3.x
scikit-learn
numpy
pandas
matplotlib
seaborn
joblib
Flask
ucimlrepo (if available)

## Acknowledgements
Thanks to the open-source community for providing robust libraries like scikit-learn, pandas, numpy, and Flask.
Special thanks to the UCI Machine Learning Repository for the Breast Cancer Wisconsin (Diagnostic) dataset.
Inspiration from several machine learning and deep learning projects in healthcare.

---

Feel free to adjust the text to match your project specifics or add additional sections if needed. This README should provide a clear and comprehensive introduction to your project for anyone visiting your GitHub repository.

