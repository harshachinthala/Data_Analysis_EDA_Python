<div align="center">
  <h1>📊 Exploratory Data Analysis & Feature Engineering</h1>
  <p>A hands-on data analysis project where I explored, cleaned, and found important patterns in different real-world datasets using Python.</p>
</div>

### 🧠 Tech Stack & Skills
![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Pandas](https://img.shields.io/badge/Data_Manipulation-Pandas-150458?logo=pandas)
![NumPy](https://img.shields.io/badge/Numerical_Computing-NumPy-013243?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Visualization-Matplotlib-11557c)
![Seaborn](https://img.shields.io/badge/Visualization-Seaborn-4c6e91?logo=databricks)
![Plotly](https://img.shields.io/badge/Interactive_Visualization-Plotly-3f4f75?logo=plotly)
![Folium](https://img.shields.io/badge/Geospatial-Folium-77B829)
![SciPy](https://img.shields.io/badge/Statistics-SciPy-8CAAEE?logo=scipy)
![Scikit-Learn](https://img.shields.io/badge/Machine_Learning-Scikit_Learn-F7931E?logo=scikit-learn)
![Statsmodels](https://img.shields.io/badge/Statistical_Models-Statsmodels-green)
![Prophet](https://img.shields.io/badge/Forecasting-Prophet-blue)

## 📊 Project Overview

This repository contains a comprehensive set of data analysis exercises designed to tackle varying levels of complexity—from simple descriptive statistics to advanced feature engineering, time-series anomaly detection, forecasting, and interactive data visualizations. 

### 🟢 Foundation Data Exploration (Easy)
1. **Simple Histogram Analysis (`student_scores.csv`)**
   - Assessed distribution symmetry, central tendencies (mean vs. median), and dataset range to evaluate exam difficulty.
2. **Basic Box Plot Comparison (`employee_salaries.csv`)**
   - Compared salary distributions across departments, identified overlaps, and performed IQR-based outlier detection.
3. **Simple Scatter Plot Relationship (`house_simple.csv`)**
   - Calculated Pearson correlation coefficient ($r = 0.826$) and linear regression to model the impact of square footage on house prices.

### 🟡 Advanced Distributions & Time Series (Medium)
4. **Multi-Variable Distribution Analysis (`customer_transactions.csv`)**
   - Evaluated extreme skewness in transaction amounts (Skew: 8.35).
   - Applied and compared Log and Square Root transformations to normalize data for predictive modeling.
5. **Time Series Pattern Detection (`daily_sales.csv`)**
   - Calculated 7-day and 30-day moving averages.
   - Detected seasonality (weekend spikes, holiday surges) and statistically flagged anomalies (sales > 2 standard deviations).

### 🔴 End-to-End EDA & Feature Engineering (Hard)
6. **Complete EDA with Feature Engineering (`credit_risk.csv`)**
   - **Data Profiling:** Handled missing data (median/mode imputation) and class imbalance.
   - **Bivariate Analysis:** Identified multicollinearity using Variance Inflation Factor (VIF) and analyzed feature-target correlations.
   - **Feature Engineering:** Created derived features including `debt_income_ratio`, `credit_utilization`, missing value indicators, and interaction terms.
   - **Data Preprocessing:** Handled outliers via capping (Winsorization), performed One-Hot Encoding for categorical variables, and scaled numerical features using `StandardScaler`.
   - **Insights:** Identified `credit_score`, `debt`, `interest_rate`, `loan_amount`, and `income` as the top 5 features driving loan default predictions.

### 🟣 Time Series Forecasting & Interactive Dashboards (Advanced)
7. **Time Series Decomposition & Forecasting (`Class_5_Assignment_Final.ipynb`)**
   - **Decomposition:** Applied both Classical and STL (Seasonal and Trend decomposition using Loess) decomposition to extract trend, seasonal, and residual components. Proved STL's robustness against anomalies.
   - **Forecasting:** Built predictive models spanning 90 days using Holt-Winters Exponential Smoothing, SARIMA, and Facebook Prophet. Generated comprehensive uncertainty bands (80% and 95% confidence intervals) through bootstrapping and residual simulations.
   - **Validation:** Validated models using hold-out datasets evaluating Mean Absolute Error (MAE), RMSE, and MAPE metrics.
8. **Interactive Plotly Dashboards (`Class_5_Assignment_Final.ipynb`)**
   - Designed interactive analytical dashboards equipped with range sliders, seasonal isolation views, index-based comparison metrics, and interactive aggregation dropdowns.

### 🔵 Geospatial & Flow Analysis
9. **Choropleth Maps & Sankey Diagrams (`In_Class6_Assignment.ipynb`)**
   - **Geospatial Mapping:** Implemented dynamic Choropleth maps using Folium for spatial data representation augmented with Pandas dataframe integration and interactive tooltips.
   - **Flow Visualization:** Constructed geographic and abstract flow Sankey diagrams employing Plotly to track variable movements and relational volumes.

## ⚙️ Key Methodologies
- **Time Series Analysis:** Classical & STL Decomposition, Moving Averages, Seasonality Adjustment, Residual Diagnostic plotting.
- **Forecasting Models:** SARIMA, Holt-Winters Exponential Smoothing, Facebook Prophet.
- **Outlier Handling:** IQR (Interquartile Range) Method, Winsorization, and Z-score anomaly detection.
- **Machine Learning Preparation:** Transformations (Log/Sqrt), VIF checks, Z-score standardization, One-Hot Encoding.
- **Interactive Visualization:** Plotly Dashboards, customized Range Sliders, Geospatial Mapping (Folium Choropleth), Sankey Flow Diagrams.

## 📁 Repository Structure
```
├── README.md                      # Project Documentation
├── Group_Assignment_4.ipynb       # Foundation & Advanced EDA Notebook
├── Class_5_Assignment_Final.ipynb # Time Series Forecasting & Dashboard Notebook
├── In_Class6_Assignment.ipynb     # Geospatial Maps & Sankey Flows Notebook
├── Class 6_in Class Assignment.pdf# Associated assignment instructions
├── final_processed_dataset.csv    # Output: Cleaned and engineered dataset
├── data/                          # Dataset directory (if applicable)
│   ├── student_scores.csv
│   ├── employee_salaries.csv
│   ├── house_simple.csv
│   ├── customer_transactions.csv
│   ├── daily_sales.csv
│   └── credit_risk.csv
```

## 🚀 Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harshachinthala/Comprehensive-EDA-Python.git
   cd Comprehensive-EDA-Python
   ```

2. **Install required dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels plotly folium prophet
   ```

3. **Run the Analysis:**
   - Launch Jupyter Notebook or Jupyter Lab:
     ```bash
     jupyter notebook
     ```
   - Execute notebooks iteratively based on your area of interest (e.g., `Group_Assignment_4.ipynb`, `Class_5_Assignment_Final.ipynb`, `In_Class6_Assignment.ipynb`).

## 📝 Key Insights & Outcomes
- **Robust Outlier Management:** Instead of deletion, Winsorization and flag creation preserved the integrity of real-world financial data anomalies (like high-value customer transactions).
- **Time Series Insights:** Analyzing seasonality confirmed distinct weekend and holiday-driven sales spikes within the transaction pipelines.
- **Forecasting Precision:** Integrating Facebook Prophet alongside SARIMA provided dynamic, seasonally-aware predictions with deeply quantified uncertainty intervals, demonstrating high resiliency properly fitting unscaled sales data.
- **Enhanced Data Accessibility:** Incorporating customized Plotly dashboards permitted rapid drilling into datasets by stakeholders through custom aggregation and time-slicing features.
- **Spatial Awareness:** Deploying Folium and Sankey maps uncovered hidden geographical flows, effectively transitioning abstract relational volumes into highly interpretable maps.
