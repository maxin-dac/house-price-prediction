# 🏡 House Prices Prediction (Advanced Regression Techniques)

## Project Objective
The primary goal of this project is to predict the final sales price (`SalePrice`) of residential homes using advanced regression techniques. This repository contains an end-to-end Machine Learning pipeline that transforms raw housing attributes into highly accurate pricing predictions, uncovering the underlying economic drivers of real estate valuation.

## Dataset & Context
The dataset is sourced from [Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques). 
For convenience, all essential files are also available directly in this repository:
* `train.csv` – The training set (1,460 observations with 81 features).
* `test.csv` – The test set (to generate final predictions).
* `data_description.txt` – Full text description of each feature.

## Notebook Structure & Workflow

The project is structured into a logical, sequential data science workflow:

1. **Setup & Data Loading:** Initializing the environment, importing specialized libraries, and loading datasets.
2. **Exploratory Data Analysis (EDA):** Investigating target distribution, uncovering feature correlations, and identifying data skewness.
3. **Advanced Data Preprocessing:** 
   * Handling high-cardinality missing values (e.g., `PoolQC`, `Alley`, `Fence`).
   * Categorical feature encoding and feature scaling.
   * Applying **Log/Box-Cox transformations** to stabilize variance and normalize distributions.
4. **Model Training & Tuning:** Implementing a robust `GradientBoostingRegressor` to capture non-linear interactions.
5. **Feature Importance Analysis:** Extracting and visualizing the most influential predictors driving house prices.
6. **Prediction & Submission:** Generating final predictions and formatting the Kaggle submission file.

## Key Insights & Model Performance

### Model Metrics
* **Target Variable:** `SalePrice` (Right-skewed, successfully normalized via Log Transformation).
* **Validation Score:** **RMSE of 0.1362** (on log scale), representing an average prediction error of approximately **13%** on unseen data.

### Top 10 Most Important Features
According to our trained Gradient Boosting model, property value is predominantly driven by **Quality** and **Size**:

| Rank | Feature | Description | Impact Type |
| :---: | :--- | :--- | :--- |
| **1** | `OverallQual` | Overall material and finish quality of the house | **Dominant Feature** |
| **2** | `GrLivArea` | Above grade (ground) living area square feet | Size / Space |
| **3** | `TotalBsmtSF` | Total square feet of basement area | Size / Space |
| **4** | `GarageCars` | Size of garage in car capacity | Utility |
| **5** | `1stFlrSF` | First floor square feet | Size / Space |
| **6** | `GarageArea` | Size of garage in square feet | Utility |
| **7** | `YearBuilt` | Original construction date | Age / Modernity |
| **8** | `FullBath` | Full bathrooms above grade | Utility |
| **9** | `YearRemodAdd` | Remodel date (indicates recent upgrades) | Age / Modernity |
| **10** | `TotRmsAbvGrd` | Total rooms above grade (excluding bathrooms) | Size / Space |

## Tech Stack

* **Language:** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
* **Environment:** ![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-F37626?style=flat&logo=jupyter&logoColor=white) ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)
* **Data Manipulation:** ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
* **Data Visualization:** ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat) ![Seaborn](https://img.shields.io/badge/Seaborn-5B8DB8?style=flat)
* **Machine Learning:** ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white) (`GradientBoostingRegressor`)

---

## Explore the Notebook
Want to see the code behind these insights? 
* Clone this repo and run the local Jupyter Notebook.
* Download the pdf file on this repo.
* Check out the interactive, up-to-date version directly on [Kaggle](https://www.kaggle.com/code/maximendacleu/house-prices-prediction).
