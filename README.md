
# **Forecasting Air Pollutant Trends from NPRI Data**

## **Overview**
This project focuses on forecasting air pollutant trends using data from the **National Pollutant Release Inventory (NPRI)**. The goal is to leverage historical emissions data to predict future trends, providing insights that support **policy decisions**, **environmental planning**, and **public health protection**.

---

## **Table of Contents**
1. #project-objective
2. [Dataset Description](#dataset-description)
3. [Project Workflow](#project-workflow)
4. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
5. [Modeling Approach](#modeling-approach)
6. [Performance Evaluation](#performance-evaluation)
7. #forecast-results
8. [Insights & Recommendations](#insights--recommendations)
9. [Technologies Used](#technologies-used)
10. #how-to-run-the-project
11. [Future Improvements](#future-improvements)
12. [Contributors](#contributors)

---

## **Project Objective**
- **Why Forecasting Matters:**
  - Supports **policy decisions** for emission control.
  - Protects **public health** by anticipating pollutant risks early.
- **Scope:**
  - Forecast trends for six major pollutants reported in NPRI.
  - Provide actionable insights for environmental stakeholders.

---

## **Dataset Description**
- **Source:** [NPRI Official Site](https://www.canada.ca/en/environment-climate-change/services/national-pollutant-release-inventory.html)
- **Coverage:** 2000–2022
- **Size:** ~737,516 records, 28 columns
- **Key Features:**
  - Emissions to **Air**, **Water**, **Land**
  - Facility and company characteristics
  - Estimation methods
- **Challenges:**
  - Missing values
  - Reporting inconsistencies
  - Sparse facility-level data
- **Pollutants in Scope:**
  - SO₂, CO, VOCs, NOₓ, PM2.5, PM10

---

## **Project Workflow**
1. **Data Cleaning**
   - Handle missing values and inconsistencies.
2. **Feature Engineering**
   - Create lag variables, moving averages, and trend terms.
3. **Exploratory Data Analysis**
   - Identify patterns, trends, and anomalies.
4. **Manual Forecast**
   - Baseline using average yearly change.
5. **Modeling**
   - Linear Regression, Ridge, and Lasso.
6. **Evaluation**
   - Metrics: RMSE, MAPE, R².
7. **Insights & Recommendations**
   - Actionable findings for stakeholders.

---

## **Exploratory Data Analysis (EDA)**
- **Key Observations:**
  - SO₂ and CO show steady decline.
  - VOC and PM spikes between 2017–2019 (linked to wildfires).
- **Visualizations:**
  - Multi-line charts for pollutant trends.
  - Annotated spikes for external events.

---

## **Modeling Approach**
- **Baseline Model:** Linear Regression with time-based features.
- **Regularization Models:** Ridge and Lasso to improve stability and reduce overfitting.
- **Features Used:**
  - Year index
  - Lag variables (lag_1, lag_2, lag_3)
  - Moving averages (MA_3yr)
  - Trend term
- **Validation Strategy:**
  - **Walk-forward validation** to mimic real-world forecasting.
- **Why Ridge & Lasso Helped:**
  - Reduced overfitting.
  - Handled multicollinearity among lag features.
  - Lasso performed feature selection for interpretability.

---

## **Performance Evaluation**
- **Metrics:**
  - RMSE, MAPE, R²
- **Results:**
  - SO₂ performed best (R² ≈ 0.42).
  - VOC and PM had negative R² due to volatility.
- **Disclaimer:** Forecasts are indicative only—interpret with caution.

---

## **Forecast Results**
- **SO₂ & CO:** Continue downward trend.
- **VOC & NOₓ:** Historical spikes, but forecasts suggest stability.
- **PM2.5:** Reliable predictions.
- **PM10:** Weak performance—needs improvement.

---

## **Insights & Recommendations**
- Monitor volatile pollutants (VOC, PM).
- Integrate external factors (wildfires, industrial activity).
- Explore advanced time-series models (ARIMA, Prophet, LSTM).
- Policy implication: **Data-driven decisions for emission control**.

---

## **Technologies Used**
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
- **Environment:** Jupyter Notebook

---
