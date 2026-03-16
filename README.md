# Salary Prediction using Machine Learning

## Overview

This project predicts the expected salary (CTC) of applicants based on their profile details using a machine learning model. A Random Forest Regressor is trained on historical applicant data to identify patterns between factors such as experience, education level, and existing offers, and estimate a reasonable salary expectation.

## Data Preprocessing

Several preprocessing steps were performed to improve model performance:

* **Dimensionality Reduction:** Removed columns that act as identifiers or add noise, such as `IDX`, `Applicant_ID`, passing year fields, location fields, and university information.
* **Handling Missing Values:** Missing categorical values were replaced with `"Unknown"`.
* **Binary Encoding:** The `Inhand_Offer` column was converted into numerical form (`Yes = 1`, `No = 0`).
* **Categorical Encoding:** Text-based features were converted into numerical values using `LabelEncoder`.

## Model

The project uses a Random Forest Regressor, an ensemble learning algorithm that combines multiple decision trees to produce stable and accurate predictions.

* Algorithm: Random Forest Regressor
* Number of Estimators: 100
* Train/Test Split: 80% training and 20% testing

## Performance

The model achieved strong performance during evaluation.

* **R² Score:** 0.9996, indicating that the model explains almost all variance in salary values.
* **RMSE:** 23,568.23, meaning predictions deviate on average by around 23k from the actual salary.

Despite a few larger differences in individual predictions, the percentage error remains low relative to overall salary values.

## Prediction Function

A helper function `predict_salary(input_data)` is included in the project. It allows users to provide applicant attributes and obtain a predicted salary estimate based on the trained model.

## Technologies Used

* Python 3.x
* Pandas
* NumPy
* Scikit-Learn

Key Scikit-Learn modules used include `RandomForestRegressor`, `LabelEncoder`, `train_test_split`, `mean_squared_error`, and `r2_score`.

## Dataset

The dataset used in this project is **expected_ctc.csv**, which contains historical applicant information such as experience, education level, location, and existing job offers.

## Development Environment

The project was developed using Visual Studio Code with the Python and Jupyter extensions, running Python 3.10 or later.

## Author

Alien Lakshmi C
B.Tech Computer Science and Engineering
Amrita University
