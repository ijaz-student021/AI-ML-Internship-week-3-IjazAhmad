# AIML Internship Week 3 — House Price Analysis

## Project Overview

This project is part of the AI/ML Internship Week 3 task, focused on Data Visualization and Feature Engineering. The project uses the House Prices dataset to analyze housing features, create professional visualizations, engineer meaningful features, apply encoding and scaling techniques, treat skewed distributions, and prepare a machine learning-ready dataset.

The main goal of this project is to understand which factors affect house sale prices and prepare clean, useful features for future machine learning models.

## Dataset

Dataset used: House Prices — Advanced Regression Techniques

Main file used: `data/raw/train.csv`

Target column: `SalePrice`

The dataset contains housing information such as living area, overall quality, basement size, garage capacity, year built, neighborhood, kitchen quality, and sale price.

## Project Structure

AIML-INTERNSHIP-WEEK3-IJAZAHMAD/

data/
raw/
train.csv
test.csv
sample_submission.csv
data_description.txt

processed/
house_prices_processed.csv

notebook/
week3_house_price_analysis.ipynb

outputs/
figures/
week3_dashboard.png
week3_fe_pipeline.png
w3_time_trend.png
w3_pairplot.png
w3_facetgrid.png

reports/
step1_dataset_summary.txt
step7_feature_creation_summary.txt
step9_encoding_strategy.csv
step12_skewness_report.csv
week3_written_report.txt

README.md
internship-week3.docx

## Tools and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Scikit-learn
* Jupyter Notebook
* VS Code

## Main Tasks Completed

## Part A — Data Visualization

* Loaded and inspected the House Prices dataset
* Created SalePrice distribution charts before and after log transformation
* Created GrLivArea box plot and violin plot
* Built a multi-variable scatter plot using GrLivArea, SalePrice, OverallQual, and GarageCars
* Created time-based trend analysis using YearBuilt decades
* Built neighborhood boxplots and correlation heatmaps
* Created advanced Seaborn pair plot and FacetGrid visualizations

## Part B — Feature Engineering and Encoding

Created 8 engineered features:

* TotalSF
* TotalBaths
* HouseAge
* RemodelAge
* HasRemodeled
* QualCond
* PricePerSF
* IsNewHouse

Applied encoding strategies:

* Label encoding for ordinal quality columns
* One-hot encoding for nominal low-cardinality columns
* Frequency encoding for high-cardinality columns
* Dropped weak or highly missing columns

## Part C — Scaling, Skewness, and Feature Selection

* Compared StandardScaler, MinMaxScaler, and RobustScaler
* Detected skewed numerical features
* Applied log transformation using np.log1p()
* Compared SalePrice transformations using log, square-root, and Box-Cox
* Selected important features using correlation, variance threshold, and multicollinearity checks

## Part D — Dashboard and Final Report

Created two final project outputs:

* outputs/figures/week3_dashboard.png
* outputs/figures/week3_fe_pipeline.png

The final dashboard includes:

* SalePrice distribution before and after log transformation
* TotalSF vs SalePrice scatter plot
* Top 15 feature importance chart
* SalePrice by OverallQual boxplot
* Correlation heatmap
* Scaling comparison chart

The feature engineering infographic includes:

* Features created
* Encoding decisions
* Skewness treatment
* Final selected feature set

## Key Findings

1. OverallQual is one of the strongest predictors of SalePrice.
2. Larger living area and total square footage usually increase house price.
3. SalePrice is highly right-skewed, and log transformation improves its distribution.
4. Neighborhood has a strong impact on property value.
5. Engineered features like TotalSF, TotalBaths, and QualCond improve the predictive quality of the dataset.

## Top Engineered Features

## TotalSF

Combines basement, first floor, and second floor area to represent total property size.

## TotalBaths

Creates a weighted count of bathrooms, giving full bathrooms more importance than half bathrooms.

## QualCond

Combines overall quality and overall condition to capture both construction quality and current property condition.

## Final Output Files

Important output files:

* outputs/figures/week3_dashboard.png
* outputs/figures/week3_fe_pipeline.png
* data/processed/house_prices_processed.csv
* outputs/reports/week3_written_report.txt

## How to Run This Project

1. Open the project folder in VS Code or Jupyter Notebook.
2. Make sure the dataset files are inside `data/raw/`.
3. Open the notebook `notebook/week3_house_price_analysis.ipynb`.
4. Run all cells from top to bottom.
5. Check generated outputs in `outputs/figures/`, `outputs/reports/`, and `data/processed/`.

## Future Work

In the next phase, this processed dataset can be used to train machine learning regression models such as Linear Regression, Ridge Regression, Random Forest Regressor, Gradient Boosting, and XGBoost.

The model performance can be evaluated using RMSE, MAE, and R² score.

## Author

Ijaz Ahmad

BS Computer Science Student

AI/ML Internship — Week 3
