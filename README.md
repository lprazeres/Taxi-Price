Taxi Fare Price Prediction

Project Overview

This project aims to build a machine learning model to predict taxi trip prices based on trip data. The focus is on data cleaning, statistical feature analysis, and regression modeling to achieve reliable fare estimates.

Data Cleaning and Imputation

Missing values in numerical features were imputed using the median.

Missing values in categorical features were imputed using the mode.

Imputation strategies were validated using model performance metrics such as RMSE and R² to ensure minimal bias.

Statistical Analysis

Categorical Variables

For categorical variables with two groups and sample sizes larger than 30, an independent t-test was applied.

For categorical variables with more than two groups, normality of the target variable distribution within groups was tested using the Shapiro-Wilk test.

Since the data did not meet normality assumptions, the Kruskal-Wallis test was used as a non-parametric alternative to ANOVA.

Results showed no significant influence of categorical variables on taxi fare prices.

Numerical Variables

A multiple linear regression was performed to assess the statistical significance of numerical features.

Four numerical variables were found statistically significant predictors of the fare price:

Trip_Distance_km

Per_Km_Rate

Per_Minute_Rate

Trip_Duration_Minutes

Interpretation of coefficients considered both magnitude and statistical significance (p-values).

Machine Learning Modeling

Models evaluated:

Linear Regression

Random Forest Regressor

Gradient Boosting Regressor

Models were compared using MAE, RMSE, and R² metrics.

The Random Forest Regressor showed the best performance, balancing accuracy and variance explanation.

Tools and Libraries
Python

Pandas, NumPy

Scikit-learn

Statsmodels

SciPy

How to Use

Preprocess and clean your dataset with imputation.

Perform feature significance testing using the provided statistical tests.

Train regression models and evaluate performance metrics.

Use the best-performing model to predict taxi fares given new input data.
