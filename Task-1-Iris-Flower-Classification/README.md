# Task 1 – Iris Flower Classification

## Data Science Internship

**Internship Organization:** Oasis Infobyte (OIBSIP)  
**Task:** Task 1 – Iris Flower Classification  
**Author:** Rramandeip Singh

---

##  Project Overview

This project was completed as part of my Data Science Internship with Oasis Infobyte.

The objective of this task is to build a machine learning classification model that can identify the species of an Iris flower based on its sepal and petal measurements.

The Iris dataset contains measurements of three different Iris flower species:

- Setosa
- Versicolor
- Virginica

In this project, Exploratory Data Analysis (EDA) was performed to understand the dataset, followed by data preprocessing, feature scaling, model training, evaluation, and prediction.

Two classification algorithms were implemented and compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)

---

##  Objective

The main objectives of this project are:

1. Load and understand the Iris dataset.
2. Convert the dataset into a Pandas DataFrame.
3. Convert numerical species labels into meaningful species names.
4. Perform Exploratory Data Analysis (EDA).
5. Analyze feature relationships and distributions.
6. Split the dataset into training and testing sets.
7. Standardize the numerical features.
8. Train Logistic Regression and KNN classification models.
9. Evaluate both models using accuracy, classification reports, and confusion matrices.
10. Compare the performance of the models.
11. Use the trained model to predict the species of a new Iris flower.

---

##  Dataset

The Iris dataset is a commonly used dataset for machine learning classification.

It contains:

- **150 observations**
- **4 numerical features**
- **3 target classes**

### Features

| Feature | Description |
|---|---|
| Sepal Length | Length of the sepal in centimeters |
| Sepal Width | Width of the sepal in centimeters |
| Petal Length | Length of the petal in centimeters |
| Petal Width | Width of the petal in centimeters |

### Target Classes

- Setosa
- Versicolor
- Virginica

Each species contains 50 observations, making the dataset balanced across the three classes.

---

## 🛠️ Technologies and Libraries

The project was developed using Python and Jupyter Notebook.

### Programming Language

- Python

### Libraries

- Pandas – Data manipulation and analysis
- NumPy – Numerical operations
- Matplotlib – Data visualization
- Seaborn – Statistical visualization
- Scikit-learn – Machine learning and evaluation

### Machine Learning Algorithms

- Logistic Regression
- K-Nearest Neighbors (KNN)

---

##  Project Workflow

The project follows the following workflow:

```text
Iris Dataset
     ↓
Data Loading
     ↓
DataFrame Creation
     ↓
Species Label Conversion
     ↓
Exploratory Data Analysis
     ↓
Data Visualization
     ↓
Feature Selection
     ↓
Train-Test Split (80/20)
     ↓
Feature Scaling
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Model Comparison
     ↓
Final Prediction
