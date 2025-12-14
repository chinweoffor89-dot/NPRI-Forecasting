Forecasting Air Pollutant Trends from NPRI Data
Overview
This project focuses on forecasting air pollutant trends using data from the National Pollutant Release Inventory (NPRI). The goal is to leverage historical emissions data to predict future trends, providing insights that support policy decisions, environmental planning, and public health protection.

Table of Contents

#project-objective
#dataset-description
#project-workflow
#exploratory-data-analysis-eda
#modeling-approach
#performance-evaluation
#forecast-results
#insights--recommendations
#technologies-used
#how-to-run-the-project
#future-improvements
#contributors


Project Objective

Why Forecasting Matters:

Supports policy decisions for emission control.
Protects public health by anticipating pollutant risks early.


Scope:

Forecast trends for six major pollutants reported in NPRI.
Provide actionable insights for environmental stakeholders.




Dataset Description

Source: https://www.canada.ca/en/environment-climate-change/services/national-pollutant-release-inventory.html
Coverage: 2000–2022
Size: ~737,516 records, 28 columns
Key Features:

Emissions to Air, Water, Land
Facility and company characteristics
Estimation methods


Challenges:

Missing values
Reporting inconsistencies
Sparse facility-level data


Pollutants in Scope:

SO₂, CO, VOCs, NOₓ, PM2.5, PM10




Project Workflow

Data Cleaning

Handle missing values and inconsistencies.


Feature Engineering

Create lag variables, moving averages, and trend terms.


Exploratory Data Analysis

Identify patterns, trends, and anomalies.


Manual Forecast

Baseline using average yearly change.


Modeling

Linear Regression, Ridge, and Lasso.


Evaluation

Metrics: RMSE, MAPE, R².


Insights & Recommendations

Actionable findings for stakeholders.




Exploratory Data Analysis (EDA)

Key Observations:

SO₂ and CO show steady decline.
VOC and PM spikes between 2017–2019 (linked to wildfires).


Visualizations:

Multi-line charts for pollutant trends.
Annotated spikes for external events.




Modeling Approach

Baseline Model: Linear Regression with time-based features.
Regularization Models: Ridge and Lasso to improve stability and reduce overfitting.
Features Used:

Year index
Lag variables (lag_1, lag_2, lag_3)
Moving averages (MA_3yr)
Trend term


Validation Strategy:

Walk-forward validation to mimic real-world forecasting.


Why Ridge & Lasso Helped:

Reduced overfitting.
Handled multicollinearity among lag features.
Lasso performed feature selection for interpretability.




Performance Evaluation

Metrics:

RMSE, MAPE, R²


Results:

SO₂ performed best (R² ≈ 0.42).
VOC and PM had negative R² due to volatility.


Disclaimer: Forecasts are indicative only—interpret with caution.


Forecast Results

SO₂ & CO: Continue downward trend.
VOC & NOₓ: Historical spikes, but forecasts suggest stability.
PM2.5: Reliable predictions.
PM10: Weak performance—needs improvement.


Insights & Recommendations

Monitor volatile pollutants (VOC, PM).
Integrate external factors (wildfires, industrial activity).
Explore advanced time-series models (ARIMA, Prophet, LSTM).
Policy implication: Data-driven decisions for emission control.


Technologies Used

Language: Python
Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
Environment: Jupyter Notebook


How to Run the Project

Clone the repository:
Shellgit clone https://github.com/<your-username>/NPRI-Forecasting.gitShow more lines

Navigate to the project directory:
Shellcd NPRI-ForecastingShow more lines

Install dependencies:
Shellpip install -r requirements.txtShow more lines

Run the notebook:
Shelljupyter notebookShow more lines



Future Improvements

Incorporate external datasets (wildfire data, industrial output).
Apply advanced forecasting models (Prophet, LSTM).
Automate data updates for real-time predictions.


Contributors

Anthonia Offor
Ayomide Tubi
Miriam Obiajuru
Nike Ndukwe

