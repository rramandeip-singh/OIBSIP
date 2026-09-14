# OIBSIP Task 3 - Car Price Prediction with Machine Learning

## Project Overview

This project was completed as **Task 3** of the **Oasis Infobyte Data Science Internship (OIBSIP)**.

The goal of this project is to predict the selling price of used cars using machine learning. The analysis uses information such as present price, kilometers driven, fuel type, seller type, transmission, ownership, car age, and car brand/model information.

The project covers data cleaning, exploratory data analysis, feature engineering, preprocessing, model training, model evaluation, and feature importance analysis.

## Objective

The main objective of this project is to build a regression model that can predict the selling price of a used car based on the available vehicle information.

The project focuses on:

- Understanding the dataset
- Checking and preparing the data
- Exploring relationships between vehicle features and selling price
- Creating useful features such as car age and car brand/model prefix
- Encoding categorical variables
- Training different regression models
- Comparing model performance
- Identifying the best-performing model
- Understanding feature importance

## Dataset

The dataset contains information about **301 original records** and the following variables:

| Column | Description |
|---|---|
| `Car_Name` | Name of the car |
| `Year` | Manufacturing year |
| `Selling_Price` | Selling price of the used car |
| `Present_Price` | Present price of the car |
| `Kms_Driven` | Number of kilometers driven |
| `Fuel_Type` | Fuel type of the car |
| `Seller_Type` | Type of seller |
| `Transmission` | Transmission type |
| `Owner` | Number of previous owners |

Two additional features were created during the analysis:

- `Car_Age` - calculated from the manufacturing year
- `Car_Brand` - extracted from the car name as a simple brand/model prefix

Two duplicate records were removed during data preparation, leaving **299 records for the final analysis**.

## Tools and Technologies

The project was completed using:

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

The project followed these steps:

1. Load the car price dataset.
2. Inspect the dataset shape, columns, and data types.
3. Check for missing values.
4. Check for and remove duplicate records.
5. Review descriptive statistics and categorical variables.
6. Explore the distribution of selling prices.
7. Analyse the relationship between present price and selling price.
8. Analyse year and kilometers driven in relation to selling price.
9. Compare selling prices across fuel types and transmission types.
10. Create the `Car_Age` feature.
11. Extract the `Car_Brand` feature from `Car_Name`.
12. Create a correlation heatmap for numerical variables.
13. Select features and target variable.
14. Split the data into training and testing sets using an 80/20 split.
15. Apply One-Hot Encoding to categorical features.
16. Train Linear Regression, Decision Tree Regression, and Random Forest Regression models.
17. Evaluate the models using MAE, RMSE, and R².
18. Select the best-performing model.
19. Analyse feature importance for the best tree-based model.
20. Compare actual and predicted selling prices.

## Exploratory Data Analysis

### Selling Price Distribution

The selling price distribution shows that most cars are concentrated in the lower price range, while a smaller number of vehicles have considerably higher selling prices.

### Present Price vs Selling Price

A clear positive relationship was observed between present price and selling price. Cars with higher present prices generally have higher selling prices.

### Year vs Selling Price

Newer cars generally tend to have higher selling prices, although the selling price varies between individual vehicles.

### Kilometers Driven vs Selling Price

Cars with higher kilometers driven generally tend to have lower selling prices. However, the relationship is not consistent for every vehicle.

### Selling Price by Fuel Type

A box plot was used to compare the distribution of selling prices across Petrol, Diesel, and CNG vehicles.

The average selling prices in the dataset were approximately:

| Fuel Type | Average Selling Price |
|---|---:|
| Diesel | 10.10 |
| Petrol | 3.26 |
| CNG | 3.10 |

Diesel vehicles had the highest average selling price among the fuel types in this dataset.

### Selling Price by Transmission

The average selling prices were approximately:

| Transmission | Average Selling Price |
|---|---:|
| Automatic | 9.07 |
| Manual | 3.92 |

Automatic cars had a higher average selling price than manual cars in this dataset.

## Feature Engineering

### Car Age

A `Car_Age` feature was created from the `Year` column.

This provides the models with a direct measure of how old each vehicle is.

### Car Brand / Model Prefix

A `Car_Brand` feature was extracted from the first part of the `Car_Name` column.

This provides additional categorical information about the vehicle while keeping the original car name available in the dataset.

## Correlation Analysis

A correlation heatmap was created to examine relationships between the numerical variables.

The analysis showed that **Present Price has a strong positive relationship with Selling Price**, while variables such as Car Age and Kilometers Driven show negative relationships with selling price.

## Data Preprocessing

The following features were used for machine learning:

- `Present_Price`
- `Kms_Driven`
- `Fuel_Type`
- `Seller_Type`
- `Transmission`
- `Owner`
- `Car_Age`
- `Car_Brand`

The target variable was:

- `Selling_Price`

Categorical variables were converted into numerical features using **One-Hot Encoding**.

The dataset was divided into:

- **80% training data**
- **20% testing data**

A `random_state` of 42 was used for reproducibility.

## Machine Learning Models

Three regression models were trained and compared.

### 1. Linear Regression

Linear Regression was used as a baseline model for predicting car selling prices.

### 2. Decision Tree Regression

Decision Tree Regression was used to capture non-linear relationships between vehicle features and selling price.

### 3. Random Forest Regression

Random Forest Regression was used as another tree-based model to compare its performance with Linear Regression and Decision Tree Regression.

## Model Evaluation

The models were evaluated using:

- **MAE (Mean Absolute Error)** - measures the average absolute difference between actual and predicted prices.
- **RMSE (Root Mean Squared Error)** - measures prediction error while giving more weight to larger errors.
- **R² (R-squared)** - measures how well the model explains the variation in selling prices.

For MAE and RMSE, lower values indicate lower prediction error. For R², a higher value indicates better model performance.

## Model Results

The models produced the following results on the test data:

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Linear Regression | 1.348138 | 5.707221 | 2.388979 | 0.778560 |
| **Decision Tree** | **0.999118** | **3.928858** | **1.982135** | **0.847561** |
| Random Forest | 1.420197 | 11.989887 | 3.462642 | 0.534794 |

## Best Performing Model

Based on the test results, **Decision Tree Regression** was the best-performing model among the three models tested.

Its results were:

- **MAE:** 0.999118
- **MSE:** 3.928858
- **RMSE:** 1.982135
- **R²:** 0.847561

The R² score of approximately **0.848** means that the model explains about **84.8% of the variation in selling prices** in the test dataset.

The Decision Tree also achieved the lowest MAE and RMSE among the three models.

## Feature Importance

Feature importance was examined using the best-performing Decision Tree model.

The top features included:

| Feature | Importance |
|---|---:|
| Present Price | 0.872172 |
| Car Age | 0.069445 |
| Car Brand - Land | 0.045938 |
| Fuel Type - Diesel | 0.004294 |
| Car Brand - Corolla | 0.002663 |
| Kms Driven | 0.002050 |

The results show that **Present Price was by far the most important feature** in the Decision Tree model. Car Age was the second most important feature, followed by selected car brand/model categories.

## Key Findings

- Present Price showed a clear positive relationship with Selling Price.
- Newer cars generally tended to have higher selling prices.
- Higher kilometers driven generally tended to be associated with lower selling prices.
- Diesel cars had the highest average selling price among the fuel types.
- Automatic cars had a higher average selling price than manual cars.
- Decision Tree Regression performed better than Linear Regression and Random Forest Regression on the test data.
- The Decision Tree achieved an R² score of approximately **0.848**.
- Present Price was the most important feature in the Decision Tree model, followed by Car Age and selected car brand/model categories.

## Conclusion

This project demonstrated how machine learning can be used to predict the selling price of used cars.

The project covered the complete workflow, including data inspection, duplicate checking, exploratory data analysis, feature engineering, categorical encoding, train-test splitting, regression modelling, model evaluation, and feature importance analysis.

Three regression models were tested: Linear Regression, Decision Tree Regression, and Random Forest Regression. Among them, **Decision Tree Regression performed the best**, achieving an R² score of approximately **0.848**, with an MAE of approximately **0.999** and an RMSE of approximately **1.982**.

The feature importance analysis showed that **Present Price was the strongest predictor** in the Decision Tree model, followed by Car Age and selected car brand/model categories.

Overall, the results show that machine learning can provide useful estimates of used-car selling prices. However, real-world selling prices can also depend on factors that are not included in this dataset, such as vehicle condition, service history, location, and market demand.

## Project Structure

```text
Task-3 - Car Prediction/
│
├── README.md
├── Car_Price_Prediction.ipynb
├── Car_Price_Prediction.pdf
├── car data.csv
│
└── Screenshots/
    ├── Load Dataset & Dataset overview.png
    ├── Stats & Variable Analysis.png
    ├── Selling Price.png
    ├── Present Vs Selling price.png
    ├── Year Vs Selling Price.png
    ├── Kilometers Vs selling Price.png
    ├── Train Split & Data Preprocessing.png
    ├── Linear Regression, Random Forest & Decision Tree.png
    ├── Model evaluation.png
    └── Feature Importance.png
```

## Author

**Rramandeip Singh**

Data Science Intern  
**Oasis Infobyte (OIBSIP)**

## Task

**OIBSIP Data Science Internship - Task 3**

**Car Price Prediction with Machine Learning**
