# Credit Card Default Prediction

## Overview

This project aims to predict whether a credit card customer will default on their next payment using the UCI Credit Card dataset. Various machine learning techniques are applied to build and evaluate predictive models. This README file provides an overview of the project, including data preprocessing, model training, evaluation, and results.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Data Preprocessing](#data-preprocessing)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Cross-Validation](#cross-validation)
- [ROC Curve Analysis](#roc-curve-analysis)
- [Making Predictions](#making-predictions)
- [Results](#results)
- [Conclusion and Future Work](#conclusion-and-future-work)

## Project Overview

The objective of this project is to develop a machine learning model that can predict the likelihood of a credit card customer defaulting on their next payment. Accurate predictions can help financial institutions mitigate risk by identifying high-risk customers and taking proactive measures.

## Dataset

The dataset used in this project is the [UCI Credit Card dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset). It contains information about 30,000 credit card customers, including their demographic information, payment history, bill statements, and default status.

## Installation

To run this project, you need Python and several libraries installed. Follow these steps to set up your environment:

1. Clone this repository:
   ```bash
   git clone https://github.com/pixelfox01/credit-risk-analysis.git
   cd credit-risk-analysis
   ```
2. Create and activate a virtual environment
   ```bash
   python -m venv venv
   source venv/bin/activate # - Unix
   .\venv\Scripts\activate # - Windows
   ```
3. Install the required packages
   ```bash
   pip install -r requirements.txt
   ```

## Data Preprocessing

Data preprocessing steps include:

- Replacing missing or erroneous values in the EDUCATION and MARRIAGE columns.
- Standardizing numerical features using StandardScaler.
- Handling class imbalance using SMOTE (Synthetic Minority Over-sampling Technique).

## Model Training and Evaluation

Two machine learning models were trained and evaluated:

1. Logistic Regression: A simple, interpretable baseline model.
2. Random Forest: A more robust model capable of handling complex data interactions.

Performance was evaluated using confusion matrices, ROC curves, and various metrics such as accuracy, precision, recall, and AUC.

## Cross-Validation

10-fold cross-validation was performed to ensure the models' performance is robust and generalizes well to unseen data. This involved splitting the dataset into 10 folds, training the model on 9 folds, and testing it on the remaining fold, repeated 10 times.

## ROC Curve Analysis

ROC curves were plotted to visualize the trade-off between True Positive Rate and False Positive Rate at various threshold settings. The Area Under the Curve (AUC) was used to compare the models.

## Making Predictions

The trained Random Forest model was used to predict the probability of default for a sample user. This demonstrates the practical application of the model to new data.

## Results

- Logistic Regression: AUC = 0.73
- Random Forest: AUC = 0.76

The Random Forest model outperformed Logistic Regression in terms of AUC, indicating better performance in distinguishing between defaulters and non-defaulters.

## Conclusion and Future Work

In this project, we successfully built and evaluated models to predict credit card defaults. The Random Forest model provided better performance compared to Logistic Regression. Future steps include:

- Exploring advanced algorithms like XGBoost and LightGBM.
- Performing hyperparameter tuning.
- Improving feature engineering.
