Student Dropout Prediction

A machine learning project that analyzes student data to predict dropout risk using Logistic Regression and Support Vector Machine (SVM) classifiers.

Overview

This project explores which factors most strongly influence whether a student drops out, and builds classification models to predict dropout risk. It includes exploratory visualizations, model training, performance evaluation, and feature importance analysis.

Dataset

The project expects a dataset.csv file with a Target column indicating student outcome (values are mapped to 1 for Dropout and 0 otherwise). Column names are automatically stripped of extra whitespace during preprocessing.

Note: dataset.csv is not included in this repo — add your own dataset file in the project root before running the notebook.

What the notebook does
Data loading & cleaning — reads dataset.csv, fixes column name formatting, encodes the target variable, and drops missing values.
Exploratory analysis — visualizes the dropout distribution and the top features correlated with dropout.
Preprocessing — splits data into train/test sets (80/20) and standardizes features with StandardScaler.
Model training — trains two classifiers:
Logistic Regression (class_weight='balanced')
Support Vector Machine (class_weight='balanced')
Evaluation — reports accuracy, classification reports, and confusion matrices for both models, and compares them with an ROC curve / AUC score.
Feature importance — plots the top features influencing dropout based on logistic regression coefficients.
Tech stack
Python
pandas, numpy
matplotlib, seaborn
scikit-learn (Logistic Regression, SVM, preprocessing, metrics)
Getting started
Clone the repo:
bash
   git clone https://github.com/Nikki-py/student-dropout.git
   cd student-dropout
Install dependencies:
bash
   pip install numpy pandas matplotlib seaborn scikit-learn
Add your dataset.csv file to the project root.
Open Student_Dropout_Stats.ipynb in Jupyter or Google Colab and run all cells.
Results

The notebook prints accuracy and AUC scores for both models and displays:

Dropout class distribution
Correlation of top features with dropout
Confusion matrices for Logistic Regression and SVM
ROC curve comparing both models
Top 10 features influencing dropout risk
