
# OIBSIP Task 3 - Car Price Prediction with Machine Learning

## Project Overview

This project was completed as part of the **Oasis Infobyte Data Science Internship (OIBSIP)**.

The aim of this project is to predict the selling price of used cars using machine learning. The dataset contains information such as the car's present price, manufacturing year, kilometers driven, fuel type, seller type, transmission, and number of previous owners.

The project includes data analysis, visualization, feature engineering, data preprocessing, machine learning model training, and model evaluation.

## Objective

The main objective of this project is to build a machine learning model that can predict the selling price of a used car based on the available vehicle information.

The project focuses on:

- Understanding the car price dataset
- Checking and preparing the data
- Exploring relationships between different variables and selling price
- Creating a new feature for car age
- Preparing categorical data for machine learning
- Training different regression models
- Comparing model performance
- Selecting the best-performing model

## Dataset

The dataset contains **301 records** and the following variables:

| Column | Description |
|---|---|
| Car_Name | Name of the car |
| Year | Manufacturing year of the car |
| Selling_Price | Selling price of the used car |
| Present_Price | Present price of the car |
| Kms_Driven | Number of kilometers driven |
| Fuel_Type | Fuel type of the car |
| Seller_Type | Type of seller |
| Transmission | Transmission type |
| Owner | Number of previous owners |

A new feature called **Car_Age** was created from the `Year` column to represent the age of the vehicle.

## Tools and Technologies

The project was completed using:

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Steps

### 1. Loading the Dataset

The car dataset was loaded using Pandas and the initial records were reviewed to understand the structure of the data.

### 2. Dataset Overview

The dataset was examined using information about its rows, columns, data types, and basic statistics.

Missing values and duplicate records were also checked.

### 3. Exploratory Data Analysis

Different visualizations were created to understand the relationship between car features and selling price.

The analysis included:

- Selling Price distribution
- Present Price vs Selling Price
- Year vs Selling Price
- Kilometers Driven vs Selling Price
- Average Selling Price by Fuel Type
- Average Selling Price by Transmission

### 4. Feature Engineering

A new feature called `Car_Age` was created using the manufacturing year.

This was done to give the machine learning models information about how old each car is.

### 5. Feature and Target Selection

`Selling_Price` was selected as the target variable.

The following features were used for prediction:

- Present_Price
- Kms_Driven
- Fuel_Type
- Seller_Type
- Transmission
- Owner
- Car_Age

### 6. Train-Test Split

The dataset was divided into training and testing sets.

- **80%** of the data was used for training
- **20%** was used for testing

### 7. Data Preprocessing

Categorical variables such as fuel type, seller type, and transmission were converted into numerical values using **One-Hot Encoding**.

A preprocessing pipeline was used so that the same transformations could be applied consistently during model training and prediction.

## Machine Learning Models

Three regression models were trained and compared:

### Linear Regression

Linear Regression was used as a baseline model for predicting the selling price of the cars.

### Decision Tree Regression

Decision Tree Regression was used to capture non-linear relationships between the car features and selling price.

### Random Forest Regression

Random Forest Regression was also tested to compare its performance with Linear Regression and Decision Tree Regression.

## Model Evaluation

The models were evaluated using four metrics:

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **R² (R-squared)**

Lower MAE, MSE, and RMSE indicate lower prediction error, while a higher R² indicates better model performance.

## Model Results

The models produced the following results on the test data:

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Linear Regression | 1.472892 | 6.370753 | 2.524035 | 0.752815 |
| Decision Tree | **1.081174** | **2.525526** | **1.589343** | **0.796096** |
| Random Forest | 1.461091 | 12.005822 | 3.464493 | 0.534175 |

## Best Performing Model

Based on the test results, **Decision Tree Regression** performed the best among the three models.

The Decision Tree achieved:

- **MAE:** 1.081174
- **MSE:** 2.525526
- **RMSE:** 1.589343
- **R²:** 0.796096

The R² score of approximately **0.796** means that the model explains about **79.6% of the variation in selling prices** in the test dataset.

It also had the lowest MAE and RMSE among the three models tested.

## Key Findings

Some of the main observations from the analysis were:

- Present Price showed a clear positive relationship with Selling Price.
- Newer cars generally tended to have higher selling prices.
- Cars with higher kilometers driven generally tended to have lower selling prices.
- Diesel cars had the highest average selling price among the fuel types in this dataset.
- Automatic cars had a higher average selling price than manual cars.
- Decision Tree Regression performed better than the other two models based on the test results.
- The Decision Tree model achieved an R² score of approximately 0.796.

## Conclusion

This project showed how machine learning can be used to estimate the selling price of used cars.

The project covered the complete process from exploring the dataset to preparing the data, creating useful features, training different regression models, and evaluating their performance.

Among the three models tested, **Decision Tree Regression gave the best results** on the test dataset, with an R² score of approximately **0.796**.

The analysis also showed that factors such as present price, car age, kilometers driven, fuel type, transmission, seller type, and previous ownership can provide useful information for predicting used-car prices.

However, actual car prices can also depend on other factors that are not included in this dataset, such as the condition of the vehicle, location, service history, and market demand.

