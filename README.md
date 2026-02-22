# kindergartenmodelling

Kindergarten Achievement Prediction Modelling

This project builds predictive models to estimate kindergarten students’ reading and mathematics test scores using demographic, classroom, and teacher-related variables. The dataset is inspired by Tennessee’s Project STAR experiment on class size and student outcomes.

Objective

The goal was to compare multiple statistical and machine learning models and identify which approach best predicts student performance while examining the trade-off between interpretability and predictive accuracy.

Dataset

~5,000 student observations

Features include class type, lunch status, teacher experience, school identifiers, demographics, and birth quarter

Target variables: reading score and math score

Methods

Exploratory Data Analysis (EDA) to understand distributions, correlations, and missing data

Data preprocessing including imputation and categorical encoding

Multi-output prediction framework implemented in Python using scikit-learn

Models evaluated using 5-fold cross-validation with mean squared error metric

Models compared:

Ordinary Least Squares

Ridge / Lasso / Elastic Net

Random Forest

Gradient Boosting Regressor

Multi-Layer Perceptron (Neural Network)

Results

Gradient Boosting Regressor achieved the lowest prediction error

~17% improvement over the baseline linear regression model

Important predictors included school identifiers, birth quarter, gender, and teacher experience
