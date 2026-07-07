## House Prices Prediction (Advanced Regression)
<img width="560" height="280" alt="header" src="https://github.com/user-attachments/assets/1e96f834-c74e-4827-9370-12e7787ec46d" />

### Objective
The main goal of this project is to predict the final sales price of residential homes using advanced regression techniques. This notebook covers the end-to-end Machine Learning pipeline: Exploratory Data Analysis (EDA), data preprocessing, and training a Gradient Boosting model to generate accurate predictions.

### Dataset
From [Kaggle](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques). You can also find the files in this repo: test.csv, train.csv, and data_description.txt.

### Notebook Structure & Workflow
1. **Setup and Data Loading:** Import libraries and load train/test datasets.
2. **Exploratory Data Analysis (EDA):** Analyze the distribution and skewness of the target variable (`SalePrice`).
3. **Data Preprocessing:** Handle missing values, encode categorical features, and apply log transformation.
4. **Modeling:** Train a `GradientBoostingRegressor` and evaluate performance.
5. **Feature Importance:** Identify the most influential predictors.
6. **Prediction & Submission:** Generate final predictions and prepare the Kaggle submission file.

## Key Insights & Feature Importance
- The target variable `SalePrice` is right-skewed. A **log transformation** was applied to normalize it and improve model performance.
- The model achieved a **Validation RMSE of 0.1362** (on log scale), which corresponds to an average prediction error of approximately **13%**.
- **Top 10 Most Important Features** (according to the Gradient Boosting model):

| Rank | Feature          | Description |
|------|------------------|-----------|
| 1    | **OverallQual**  | Overall material and finish quality of the house (dominant feature) |
| 2    | **GrLivArea**    | Above grade (ground) living area |
| 3    | **TotalBsmtSF**  | Total square feet of basement area |
| 4    | **GarageCars**   | Size of garage in car capacity |
| 5    | **1stFlrSF**     | First floor square feet |
| 6    | **GarageArea**   | Size of garage |
| 7    | **YearBuilt**    | Original construction date |
| 8    | **FullBath**     | Full bathrooms above grade |
| 9    | **YearRemodAdd** | Remodel date |
| 10   | **TotRmsAbvGrd** | Total rooms above grade |

**Key takeaway**: House **quality** and **size** (especially living area and basement) are the strongest drivers of price.

## Strategic Recommendations
Based on the analysis, here are practical recommendations:
- **Prioritize quality improvements** (kitchen, bathrooms, finishes) — they have the highest return on investment.
- **Increase livable space** (`GrLivArea`, `1stFlrSF`) when possible.
- **Invest in garage and basement** — both significantly impact valuation.
- Consider **feature interactions** (e.g. Quality × Size) for future model improvements.
- Always apply **log transformation** on right-skewed price targets in real estate modeling.
- For production use, explore model stacking or ensemble techniques to push performance further.

## Tech Stack & Libraries

* **Language:** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

* **Data Manipulation:** ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

* **Visualization:** ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat) ![Seaborn](https://img.shields.io/badge/Seaborn-5B8DB8?style=flat)

* **Machine Learning:** ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white) (`GradientBoostingRegressor`)

* **Evaluation:** ![RMSE](https://img.shields.io/badge/RMSE-Evaluation-blue?style=flat)

* **Environment:** ![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-F37626?style=flat&logo=jupyter&logoColor=white) ![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)

---
*To explore the detailed code, feel free to download the notebook file on this repo, or check out my [Kaggle](https://www.kaggle.com/code/maximendacleu/house-prices-prediction).*
