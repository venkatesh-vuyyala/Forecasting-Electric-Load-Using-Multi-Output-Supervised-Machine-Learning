# Forecasting Electric Load Using Multi-Output Supervised Machine Learning

[![Python](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/)

## Project Overview
Accurate short-term electric load forecasting is critical for efficient grid operation, ensuring reliability and balancing generation from conventional and renewable energy sources. This project implements a **multi-output supervised machine learning approach** to predict **3-day-ahead electricity load** using **11 years of historical generation and load data from SMARD**. The model captures interdependencies across multiple future timestamps, providing actionable insights for grid operators and energy market planning.

---

## Key Features
- **Multi-Output Forecasting**: Predicts multiple future load points simultaneously, reducing error propagation compared to recursive forecasting methods.
- **Feature Engineering**: Incorporates cyclical temporal features, history/horizon matrices, and multi-dimensional X-y pairs to improve predictive performance.
- **Modeling**: Utilizes **XGBoost** for robust, interpretable forecasts; easily extendable to LSTM or hybrid models.
- **Data Processing**: Handles large-scale time-series data, addressing missing values, duplicates, and feature scaling.
- **Visualization & Analysis**: Generates feature-importance charts and interactive dashboards to identify key drivers of load variability.

---

## Dataset
- **Source**: [SMARD](https://www.smard.de/)
- **Data Range**: 2015-01-01 to 2024-09-18
- **Granularity**: Hourly load and generation data
- **Preprocessing**: Timezone standardization (UTC), handling missing/duplicate records, scaling features

---

## Methodology
1. **Exploratory Data Analysis (EDA)**: Identify periodic patterns, trends, and data quality issues.
2. **Feature Engineering**: Create cyclical time features and transform the multivariate time-series into **X-matrix and y-vector pairs**.
3. **Model Training**: Collapse 3D training arrays into 2D for **XGBoost** training, predicting multiple timestamps simultaneously.
4. **Evaluation**: Compare forecasts against historical load, analyze feature importance, and assess predictive stability.
5. **Visualization**: Build dashboards to visualize load trends, forecast accuracy, and feature contributions.

---

## Tools & Technologies
- **Languages**: Python
- **Libraries**: XGBoost, pandas, numpy, matplotlib, seaborn, scikit-learn
- **Data Handling**: Time-series preprocessing, multi-output matrix construction
- **Visualization**: Feature importance plots, interactive dashboards

---

## Results & Impact
- Achieved **15% improvement** in predictive accuracy compared to iterative forecasting methods.
- Captured **hourly, daily, and weekly load patterns** to support operational and day-ahead market decisions.
- Framework can be extended to include **weather forecasts and renewable generation data**, enhancing grid reliability and planning.

---

## Installation
1. Clone this repository:
```bash
git clone https://github.com/venkatesh-vuyyala/Forecasting Electric Load Using Multi-Output Supervised Machine Learning.git
