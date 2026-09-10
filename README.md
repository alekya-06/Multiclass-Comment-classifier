# Comment Category Prediction

Machine learning project for the **Kaggle Comment Category Prediction Challenge**, finished as part of the **MLP (Machine Learning Practice) Project coursework for the BS Data Science from IIT Madras**.
Completed in Term 4 of the Diploma Level: **Jan 2026 - May 2026**

## Overview

The **Comment Category Prediction Challenge** focuses on predicting the final category assigned to user-generated comments on an online platform.

The dataset contains information about individual comments along with various metadata, including:

* Interaction and feedback signals
* Symbolic expressions
* Topic reference indicators
* Internal system signals
* Textual, numerical, and categorical features

The objective of this project was to explore the dataset, identify meaningful patterns, and build machine learning models capable of accurately predicting the category assigned to each comment.

## Project Highlights

* Performed **extensive Exploratory Data Analysis (EDA)** to understand feature distributions, relationships, missing values, and class patterns.
* Conducted **feature analysis and preprocessing** across textual, numerical, and categorical variables.
* Used **TF-IDF** to transform textual information into numerical features.
* Experimented with multiple machine learning approaches.
* Performed **hyperparameter tuning** to improve model performance.
* Evaluated models using **Macro F1-score**, which is particularly useful for evaluating performance across multiple classes.
* Achieved a **Macro F1-score of 0.80**.

## Approach

The overall workflow consisted of the following stages:

```text
Data
  ↓
Data Cleaning & Preprocessing
  ↓
Exploratory Data Analysis
  ↓
Feature Engineering
  ↓
Text Vectorization (TF-IDF)
  ↓
Model Training
  ↓
Hyperparameter Tuning
  ↓
Model Evaluation
```

### Exploratory Data Analysis

A detailed EDA was performed to investigate:

* Feature distributions
* Missing values
* Class distribution
* Relationships between numerical and categorical features
* Text-related characteristics
* Potential correlations and predictive patterns

### Text Processing

Textual features were converted into numerical representations using **word based and character based TF-IDF (Term Frequency–Inverse Document Frequency)** from `scikit-learn`.

No dedicated deep learning or NLP deep learning frameworks were used.

### Modeling

The project focused on **traditional machine learning techniques**, combining engineered numerical/categorical features with TF-IDF-based text features.

Hyperparameter tuning was performed on XGBoost, Random Forest, Logistic Regressor, LGBM, Linear SVC and MLP to identify better-performing model configurations.

## Results

The results for the 4 best performing models are as follows:

|                   |Train F1 | Val F1 |Overfit Gap|
|LogisticRegression |  0.9179 | 0.8189 |     0.0990|
|LinearSVC          |  0.8916 | 0.8167 |     0.0750|
|MLP                |  0.8172 | 0.7889 |     0.0283|
|XGBoost            |  0.7290 | 0.7056 |     0.0234|


The Macro F1-score was used as the primary evaluation metric to account for performance across all target categories rather than allowing larger classes to dominate the evaluation.

## Technologies Used

* Python
* pandas
* NumPy
* scikit-learn, xgboost and lightgbm
* Matplotlib
* Seaborn
* Jupyter Notebook
* Kaggle

### Note on Deep Learning

This project **does not use deep learning libraries**.

For text representation, the project uses **TF-IDF from scikit-learn** rather than neural-network-based language models or deep learning frameworks.

## Repository Structure

```text
.
├── README.md
├── notebooks/
│   └── 24f2000039-notebook-t12026.ipynb
├── logs/
|   └── 24f2000039-notebook-t12026.log
├── data/
│   └── train.csv
|   └── test.csv
|   └── submission.csv
└── requirements.txt
```

## Kaggle Competition

This project was developed for the **Comment Category Prediction Challenge** on Kaggle.

The competition provides a dataset representing how an online platform processes and categorizes user-generated comments. The goal is to develop predictive models that can determine the final category associated with each comment.

## Coursework

This project was completed as part of the **MLP Project coursework**.

## Key Takeaways

Through this project, I explored the end-to-end machine learning workflow, including:

* Data exploration and visualization
* Data preprocessing
* Feature engineering
* Text representation using TF-IDF
* Multi-class classification for imbalanced classes
* Model comparison
* Hyperparameter optimization
* Evaluation using Macro F1-score

The project provided practical experience in working with a dataset containing a combination of **textual, numerical, and categorical features** and demonstrated that traditional machine learning approaches can achieve strong performance without relying on deep learning.
