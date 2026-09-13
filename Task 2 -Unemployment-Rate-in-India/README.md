# Data Science Task 2 — Unemployment Analysis with Python

## Project Overview

This project analyzes unemployment data in India using Python. The analysis focuses on understanding unemployment trends across different states, regions, and months, with particular attention to the impact of the COVID-19 lockdown period.

The project uses data analysis and visualization techniques to identify patterns, compare unemployment rates, and understand relationships between unemployment, employment, and labour participation.

---

## Objectives

The main objectives of this project are:

- Analyze unemployment rates across Indian states.
- Examine unemployment trends over time.
- Compare unemployment rates across different regions.
- Analyze the impact of the COVID-19 lockdown on unemployment.
- Examine the relationship between unemployment, employment, and labour participation.
- Identify states and regions with higher unemployment rates.
- Present findings using appropriate data visualizations.

---

## Dataset

The dataset used in this project is:

**Unemployment_Rate_upto_11_2020.csv**

The dataset contains unemployment-related observations from India covering the year 2020.

### Main Variables

| Variable | Description |
|---|---|
| States | Name of the Indian state |
| Date | Date of the observation |
| Frequency | Frequency of the observation |
| Estimated Unemployment Rate | Estimated unemployment rate (%) |
| Estimated Employed | Estimated number of employed people |
| Estimated Labour Participation Rate | Labour participation rate (%) |
| Region | Geographic region |
| longitude | Longitude of the state |
| latitude | Latitude of the state |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Jupyter Notebook

---

## Data Preparation

The following data preparation steps were performed:

1. Loaded the CSV dataset using Pandas.
2. Inspected the dataset structure and columns.
3. Cleaned column names.
4. Renamed columns where necessary for easier analysis.
5. Converted the `Date` column into datetime format.
6. Checked data types.
7. Checked for missing values.
8. Checked for duplicate rows.
9. Created additional month-related information for time-series analysis.

---

## Exploratory Data Analysis

The project includes several exploratory analyses and visualizations.

### 1. Dataset Overview

The dataset was examined to understand:

- Number of rows and columns
- Column names
- Data types
- Dataset structure

The dataset contains **267 observations and 9 original columns**.

---

### 2. Missing Values

Missing values were checked across all columns.

The analysis found:

**Total missing values: 0**

Therefore, no missing-value treatment was required.

---

### 3. Duplicate Records

Duplicate rows were also checked.

**Total duplicate rows: 0**

This indicates that no duplicate observations were identified in the dataset.

---

### 4. Descriptive Statistics

Descriptive statistics were calculated for the numerical variables.

The analysis examined:

- Mean
- Standard deviation
- Minimum
- Maximum
- Quartiles

The unemployment rate showed considerable variation across the observations, with some observations having substantially higher unemployment rates than the overall average.

---

## Data Visualizations

The project contains several visualizations to understand unemployment patterns.

### Unemployment Rate Distribution

A histogram was created to examine the distribution of unemployment rates.

The distribution is concentrated toward lower unemployment-rate values, while a smaller number of observations show substantially higher unemployment rates.

---

### State-Level Unemployment Analysis

Average unemployment rates were calculated for individual states.

This allows states with relatively lower and higher average unemployment rates to be compared.

---

### Regional Analysis

Average unemployment rates were calculated for the major regions:

- North
- Northeast
- East
- West
- South

This provides a geographic comparison of unemployment patterns.

---

### Time-Series Analysis

Unemployment rates were examined across the months of 2020.

The time-series analysis helps identify changes in unemployment over the study period and highlights the substantial changes observed during the COVID-19 period.

---

## COVID-19 Lockdown Impact Analysis

A specific analysis was performed to compare unemployment rates before and after the COVID-19 lockdown period.

The unemployment rate before and after the lockdown was calculated for individual states.

The percentage change in unemployment was then calculated to identify states experiencing larger changes.

The results show that the impact of the lockdown was not uniform across all states.

Some states experienced substantially larger increases in unemployment compared with others.

---

## Correlation Analysis

A correlation matrix was created for:

- Estimated Unemployment Rate
- Estimated Employed
- Estimated Labour Participation Rate

The analysis produced the following approximate correlations:

| Variables | Correlation |
|---|---:|
| Unemployment Rate vs Estimated Employed | -0.25 |
| Unemployment Rate vs Labour Participation Rate | -0.07 |
| Estimated Employed vs Labour Participation Rate | -0.05 |

The strongest relationship among these variables was the negative relationship between unemployment rate and estimated employment.

---

## Key Findings

The major findings from the analysis are:

- The dataset contains unemployment observations from multiple Indian states during 2020.
- Unemployment rates vary considerably across states and over time.
- The unemployment-rate distribution is concentrated toward lower values but contains several high-rate observations.
- Geographic differences can be observed in unemployment levels across Indian regions.
- The COVID-19 lockdown period was associated with substantial changes in unemployment in several states.
- The impact of the lockdown varied from state to state.
- The correlation analysis shows a negative relationship between unemployment rate and estimated employment.
- The dataset contained no missing values or duplicate rows after the data-quality checks.

---

## Conclusion

This project analyzed unemployment patterns in India using Python, Pandas, and data visualization techniques.

The analysis included data cleaning, exploratory data analysis, descriptive statistics, state-level analysis, regional analysis, time-series analysis, COVID-19 lockdown impact analysis, and correlation analysis.

The results demonstrate that unemployment varied considerably across Indian states and over time. The COVID-19 period produced noticeable changes in unemployment, although the magnitude of change differed between states.

Overall, this project demonstrates how Python-based data analysis and visualization can be used to explore real-world unemployment data and identify meaningful patterns and trends.

---

## Project Files

```text
Task-2-Unemployment-Analysis/
│
├── Unemployment_Rate_Analysis.ipynb
├── Unemployment_Rate_Analysis.pdf
├── Unemployment_Rate_upto_11_2020.csv
└── README.md
