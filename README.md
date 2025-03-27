# 🛍️ Dillard’s Monthly Sales Forecasting

## Project Overview

This project aims to enhance operational efficiency and revenue at traditional department stores like **Dillard’s** by leveraging sales transaction data. We built machine learning models to **predict monthly sales** at SKU and store levels, identify key demand drivers, and analyze ROI of predictive modeling in inventory optimization.

## Approach

### 1. Data Preprocessing
- Read over 120M records from PostgreSQL
- Cleaned 5 datasets (SKU, Store, Department, Transactions, SKU-Store Info)
- Addressed data inconsistencies, missing values, duplicates, and outliers

### 2. Exploratory Data Analysis
- Analyzed trends by brand, department, state, and time
- Found holiday season peaks and high-performing brands/departments

### 3. Feature Engineering
- Selected Predictors: cost, retail price, packsize, month, color, and store state
- Standardized numeric values and one-hot encoded categorical features

### 4. Model Training
We experimented with several machine learning models, including:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **LightGBM**
- **XGBoost**

We evaluated models based on:
- **R²**
- **MSE**

### 5. Model Comparison and Evaluation

| Model           | R² Score | MSE     |
|----------------|----------|---------|
| Linear          | 0.6312   | 292.91  |
| Ridge           | 0.6312   | 292.91  |
| Lasso           | 0.6310   | 293.05  |
| **LightGBM**    | **0.7575** | **192.57** |
| XGBoost         | 0.7532   | 195.99  |

LightGBM outperformed all models and was selected for final deployment due to its accuracy and speed.


## Files Description
- **Project.ipynb**: Jupyter notebook containing the full pipeline—data preprocessing, EDA, feature engineering, modeling, and evaluation.
- **Presentation.pdf**: Final project presentation slides.
- **Report.pdf**: Final report summarizing the entire project.
- **ROI_Analysis.xlsx**: Excel workbook with detailed ROI calculations.
- **environment.yml**: Conda environment file listing all dependencies and packages used for running the notebook.
- **README.md**: Project overview and documentation.

## How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Sophiabbb/MLDS400-Dillards_Monthly_Sales_Forecasting.git
   cd MLDS400-Dillards_Monthly_Sales_Forecasting
   ```

2. Install dependencies using environment.yml: 
    ```bash
    conda env create -f environment.yml -n myenv
    ```

---

## Contributors
- Junyi Chen
- Ananya Rattan Khurana
- Fuqian Zou  
