# credit-card-fraud-detection

A machine learning project for detecting credit card fraud using the [Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud) from Kaggle. This repository contains code written in Python using Jupyter Notebooks, along with a `requirements.txt` file for dependency management.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Results](#results)
- [Improvements and Future Work](#improvements-and-future-work)
- [Acknowledgements](#acknowledgements)

## Overview

Credit card fraud detection is a challenging problem due to the severe class imbalance and the dynamic nature of fraudulent transactions. This project explores various machine learning approaches to effectively detect fraudulent transactions by performing thorough data preprocessing, model training, and evaluation.

## Dataset

This project uses the [Credit Card Fraud Detection dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud) from Kaggle.  
- **Dataset Characteristics:**
  - The dataset comprises transactions made by European cardholders in September 2013.
  - It includes 284,807 transactions, with only 492 labeled as fraud (a highly imbalanced scenario).
- **Location in this Project:**  
  The dataset file `creditcard.csv` is stored in the `input/` folder.
- **License:**
    This creditcard.csv is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/

## Project Structure

├── input/ 

│ └── creditcard.csv # The dataset file from Kaggle 

├── data_preparation.ipynb # Notebook for cleaning and preprocessing data 

├── model_development.ipynb # Notebook for model training and evaluation 

├── requirements.txt # Python package dependencies and version information 

├── README.md # This file 


## Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/alestankiewicz/credit-card-fraud-detection.git
    cd credit-card-fraud-detection

2. **Set Up a Virtual Environment (Optional but Recommended):**
    ```bash
    python -m venv venv
    venv\Scripts\activate

3. **Install the Required Packages:**
    ```bash
    pip install -r requirements.txt

## Usage

- **Launch Jupyter Notebook:**
  ```bash
  jupyter notebook

- **Open the notebooks:**
  - data_preparation.ipynb for data cleaning and preprocessing.
  - model_development.ipynb for training models and evaluating performance.

## Methodology

This project employs multiple techniques and classifiers to tackle the challenge of imbalanced data in credit card fraud detection:

- **Data Preprocessing:**
  - Analyzing the data and standarization of numerical features.
  - Addressing the class imbalance using:
    - Random Undersampling
    - SMOTE (Synthetic Minority Oversampling Technique)

- **Model Training & Hyperparameter Tuning:**  
  - XGBoost and Random Forest classifiers are used on the preprocessed data.

  - A Cost-Sensitive Decision Tree Classifier with the balanced class_weight argument is also implemented on original imbalanced data.

  - RandomSearchCV is applied for hyperparameter optimization to find the best model configurations.

- **Evaluation:**  
  - The models are evaluated using metrics such as Precision, Recall, F1 Score, and average precision, precision - recall curve given the imbalanced nature of the dataset.

## Results

The experimental phase yielded insights into model performance with respect to handling imbalanced data:
  - A comparison of performance metrics across XGBoost, Random Forest, and the cost-sensitive decision tree model.

  - Detailed visualizations (provided within the notebooks) that show data analysis findings and compare model results.

## Improvements and Future Work
- **Automated Hyperparameter Optimization:**
    
    Investigating more robust techniques such as Bayesian Optimization for more efficient hyperparameter tuning.
- **Ensemble Techniques:**

    Combining multiple models to further address the class imbalance and improve detection accuracy.

## Acknowledgements

- This article [https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/] for providing valuable insights into SMOTE.
- This book [https://fraud-detection-handbook.github.io/fraud-detection-handbook/Foreword.html] for guiding me through fraud detection problem.
- Kaggle: For providing the dataset and contributing to the machine learning community.
- Open Source Contributors: For the libraries and frameworks used in this project.

