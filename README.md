## House Prices Prediction (Advanced Regression)
<img width="560" height="280" alt="header" src="https://github.com/user-attachments/assets/1e96f834-c74e-4827-9370-12e7787ec46d" />

### Objective
The main goal of this project is to predict the final sales price of residential homes using advanced regression techniques. This notebook covers the end-to-end Machine Learning pipeline: Exploratory Data Analysis (EDA), rigorous data preprocessing, and training a Gradient Boosting model to generate accurate predictions.

### Dataset
From Kaggle: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

### Notebook Structure & Workflow

1. **Setup and Data Loading**
   * Environment configuration (Pandas settings, Matplotlib `ggplot` style).
   * Loading train and test sets from the Kaggle environment.
   * Dataset shape verification.

2. **Exploratory Data Analysis (EDA)**
   * Detailed analysis of the target variable (`SalePrice`).
   * Visualizing the distribution using histograms with Kernel Density Estimate (KDE).
   * Calculating target skewness to identify the need for mathematical transformations.

3. **Data Preprocessing & Feature Engineering** *(Implied standard pipeline)*
   * Handling missing/null values across categorical and numerical columns.
   * Feature transformation (skewness reduction, log-transformation of the target).
   * Categorical variable encoding.

4. **Model Training & Evaluation** *(Implied standard pipeline)*
   * Splitting data into training and validation sets (`train_test_split`).
   * Training a `GradientBoostingRegressor` model.
   * Evaluating model performance using Root Mean Squared Error (RMSE) on log-scale.

### Tech Stack & Libraries
* **Language:** Python 3.12
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib` (ggplot style), `seaborn`
* **Machine Learning:** `scikit-learn` (`GradientBoostingRegressor`, `train_test_split`, `mean_squared_error`)
* **Mathematical Operations:** `scipy.stats` (`skew`)
* **Environment:** Kaggle Notebook

*To explore the detailed code, statistical visualizations, and model evaluation metrics, feel free to download the notebook file on this repo, or check out my Kaggle: [https://www.kaggle.com/code/maximendacleu/house-prices-prediction].*

***By: Maxime NDACLEU | BI & Data Analyst***
