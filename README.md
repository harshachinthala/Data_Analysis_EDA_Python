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
![SciPy](https://img.shields.io/badge/Statistics-SciPy-8CAAEE?logo=scipy)
![Scikit-Learn](https://img.shields.io/badge/Machine_Learning-Scikit_Learn-F7931E?logo=scikit-learn)
![Statsmodels](https://img.shields.io/badge/Statistical_Models-Statsmodels-green)

## 📊 Project Overview

This repository contains a comprehensive set of data analysis exercises designed to tackle varying levels of complexity—from simple descriptive statistics to advanced feature engineering and time-series anomaly detection. 

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

## ⚙️ Key Methodologies
- **Outlier Handling:** IQR (Interquartile Range) Method, Winsorization, and Z-score anomaly detection.
- **Transformations:** Logarithmic and Square Root transformations for right-skewed variables.
- **Multicollinearity Checks:** Variance Inflation Factor (VIF) analysis.
- **Feature Importance:** Extracted using `RandomForestClassifier`.
- **Scaling & Encoding:** Z-score standardization and One-Hot Encoding for machine learning readiness.

## 📁 Repository Structure
```
├── README.md                      # Project Documentation
├── Group_Assignment_4.ipynb       # Main Jupyter Notebook
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
   pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels
   ```

3. **Run the Analysis:**
   - Launch Jupyter Notebook or Jupyter Lab:
     ```bash
     jupyter notebook Group_Assignment_4.ipynb
     ```
   - Execute the cells sequentially to reproduce the visualizations and final processed datasets.

## 📝 Key Insights & Outcomes
- **Data Normalization proves critical:** Log transformations effectively neutralized high skewness in financial transaction data, preserving extreme values without distorting baseline models.
- **Feature Engineering boosts separability:** Creating features like `debt_income_ratio` provided higher predictive power than raw variables individually.
- **Robust Outlier Management:** Instead of deletion, Winsorization and flag creation preserved the integrity of real-world financial data anomalies (like high-value customer transactions).
- **Time Series Insights:** Analyzing seasonality confirmed distinct weekend and holiday-driven sales spikes within the transaction pipelines.
