# Demand Forecasting Using Machine Learning

## Overview
This project presents an end-to-end data science workflow for **product-level demand forecasting**
in a retail **environment**. The goal is to predict **daily units sold per product** using historical
sales data combined with operational and external factors such as inventory levels, pricing,
store traffic, weather conditions, and tennis events.

The project is based on a real-world use case from the **Tennis Shop**, a resort tennis 
retail store in Georgia, USA, where demand is highly seasonal and strongly influenced by
weather, guest traffic, and events.

-----

## Problem Statement
Retail managers often rely on intuition to make inventory, staffing, and promotion decisions.
Without reliable demand forecasts, this can lead to:
- Stockouts of high-demand, high-margin products
- Overstocking of slow-moving items
- Inefficient staffing during peak and low-demand periods
- Difficulty quantifying the impact of promotions, weather, and events

The objective of this project is to build a **data-driven demand forecasting system** that can
support better operational decision-making.

-----

## Data
The dataset used in this project is based on **real operational data** from the Sea Island Tennis Shop.

To protect sensitive business information, the raw dataset is **not included** in this repository.
Some numerical values were anonymized or adjusted, but the underlying patterns and trends
remain realistic.

The dataset contains **daily, product-level observations from January 2023 to June 2025** and includes:
- Sales quantity (target variable)
- Pricing and cost information
- Inventory on hand
- Store traffic
- Weather variables
- Calendar features (weekends, holidays)
- Tennis event indicators
- Product and category identifiers

-----

## Methodology
The project follows a standard data science pipeline:

1. **Data Cleaning & Preprocessing**
   - Datetime conversion and validation
   - Feature consistency checks
   - Handling of categorical variables

2. **Exploratory Data Analysis (EDA)**
   - Seasonal and weekly demand patterns
   - Revenue and margin by product category
   - Impact of weather and tennis events
   - Correlation analysis of key numeric features

3. **Feature Engineering**
   - Time-based features (year, month, day, day of week)
   - Lagged sales features (lag-1, lag-7)
   - Rolling 7-day averages
   - Promotion and traffic interaction terms
   - One-hot encoding of categorical variables

4. **Modeling**
   Three models were trained and compared using a time-based train/test split:
   - Linear Regression (baseline)
   - Random Forest Regressor
   - XGBoost Regressor

5. **Evaluation**
   Models were evaluated on 2025 data using:
   - R²
   - Mean Absolute Error (MAE)
   - Root Mean Squared Error (RMSE)

-----

## Results
XGBoost achieved the best overall performance, outperforming Linear Regression and Random Forest
in all evaluation metrics.

Key findings:
- Strong seasonality between March and July
- Weekends significantly outperform weekdays
- Weather and tennis events drive major demand spikes
- Inventory levels and recent sales momentum are among the most important predictors

-----

## Scenario Simulations
To demonstrate real-world applicability, several scenarios were simulated, including:
- Normal weekday conditions
- Promotional weekends
- Tennis events combined with promotions and warm weather

These simulations show how predicted demand can nearly **double under peak conditions** and
illustrate how managers can use forecasts to plan inventory, staffing, and promotions proactively.

-----

## Repository Structure

data/            # Dataset not included (confidential)  
figures/         # Optional exported figures (generated in notebook)  
notebooks/       # Jupyter notebook with full analysis and modeling  
reports/         # Final academic project report (PDF)

-----

## Files
- **Notebook:**  
  `notebooks/demand_forecasting_analysis.ipynb`

- **Final Project Report:**  
  `reports/Report capstone data.pdf`

-----

## Tools & Technologies
- Python
- pandas, NumPy
- scikit-learn
- XGBoost
- matplotlib, seaborn
- Jupyter Notebook

-----

## Author
**Gonzalo Tano**  
B.S. in Data Science (Computational Data Analytics)  
College of Coastal Georgia
