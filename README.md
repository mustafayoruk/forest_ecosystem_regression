# Forest Ecosystem Analysis & Prediction Model

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Statsmodels](https://img.shields.io/badge/Statsmodels-OLS-orange.svg)
![Data Science](https://img.shields.io/badge/Machine_Learning-Linear_Regression-brightgreen.svg)

## Project Overview
This project aims to analyze the relationship between **Total Forest Area** (in hectares) and the **Growing Stock** (wood volume in cubic meters) in Turkey from 1973 to 2024. Using statistical modeling, this repository demonstrates an end-to-end data processing and linear regression pipeline.

The goal is to determine how accurately we can predict the total growing stock simply by observing the expansion of forest lands.

## Dataset
The dataset consists of historical records regarding forest area and growing stock. 
* **Independent Variable (X):** `ForestArea_Hectare` 
* **Dependent Variable (Y):** `GrowingStock_m3`

> **Note:** The raw data was provided in an unstructured Excel format. A custom Python parsing script was developed to extract, clean, and merge the relevant yearly totals.

## Technologies Used
* **Pandas:** Data extraction, manipulation, and merging.
* **NumPy:** Mathematical operations.
* **Statsmodels:** Building the OLS (Ordinary Least Squares) model and conducting statistical assumption tests.
* **Scikit-Learn:** Calculating RMSE and MAE error metrics.
* **SciPy:** Performing normality tests.

## Model Performance & Results
The Simple Linear Regression model achieved exceptional explanatory power:

* **R-Squared:** 0.9644 (96.4% of the variance in growing stock is explained by the forest area).
* **Adjusted R-Squared:** 0.9614
* **RMSE:** ~46.2 Million m³

### Statistical Assumption Checks
As a best practice, the underlying assumptions of the linear model were tested:
1. **Normality of Residuals:** Passed (Shapiro-Wilk p-value: 0.4463)
2. **Homoscedasticity:** Warning (Breusch-Pagan p-value: 0.0389) indicating a slight presence of heteroscedasticity.
3. **Autocorrelation:** Warning (Durbin-Watson: 0.7318) indicating expected time-series autocorrelation.

## Practical Use Case
For every **1 hectare** increase in forest land, the model predicts an average increase of approximately **239.96 cubic meters** in growing stock. This insight can be utilized by forestry departments for strategic planning and budgeting.

## How to Run
1. Clone this repository: `git clone https://github.com/YourUsername/YourRepoName.git`
2. Ensure you have the required libraries installed: `pip install pandas numpy statsmodels scikit-learn scipy openpyxl`
3. Open `forest_ecosystem_regression.ipynb` in Jupyter Notebook or Google Colab and run the cells.

**Author:** [Mustafa YÖRÜK]  
*Statistics Student @ Hacettepe University*
