---
layout: post
title: Predicting House Prices; MLR vs RFR
subtitle : I set out to explore whether machine learning could help us predict house prices more accurately.
tags: [ml, regression ]
author: Clifford
comments : True
---


# 🏡 Predicting House Prices: MLR vs RFR

Housing markets are notoriously complex. Prices depend on dozens of factors: location, size, condition, and sometimes even unpredictable trends. As a data science project, I set out to explore whether machine learning could help us predict house prices more accurately.


## The Dataset

I used the **King County housing dataset** (Seattle, USA), which contains **21,613 records** of house sales. Each record included features like:

* Square footage of living space
* Number of bedrooms and bathrooms
* Grade of construction
* Location details

The task: use regression models to predict house prices.


## The Approach

I compared two algorithms:

1. **Multi-Linear Regression (MLR)** – a classic baseline model assuming straight-line relationships between features and price.
2. **Random Forest Regression (RFR)** – an ensemble method combining many decision trees, capable of capturing complex patterns.

Models were trained across **10 random states**, and I evaluated them using **RMSE, MAE, MSE, and R² score**.


## Results

* **Random Forest Regression** outperformed MLR on every metric:

  * RMSE: 147,967 (vs 203,625 for MLR)
  * MAE: 76,995 (vs 114,196 for MLR)
  * R²: 0.84 (vs 0.70 for MLR)

* Why did Random Forest do better?

  * It captures **non-linear relationships** (e.g., how living space influences price differently at different ranges).
  * It accounts for **feature interactions** (like how grade + square footage together affect value).
  * It’s **robust to outliers** (expensive mansions don’t throw it off as much).


## Insights & Limitations

* **Random Forest is a strong predictor** for complex datasets like housing.
* **Multi-Linear Regression still has value** when interpretability matters (e.g., policy makers want to know which single features matter most).
* Trade-off: Random Forest is **less interpretable** and **computationally heavier**.


## Next Steps

To extend this project, I would:

* Perform **feature engineering** (create new variables like price per square foot).
* Try **dimensionality reduction** to simplify high-dimensional data.
* Explore **ensemble stacking** (combining models) for even better accuracy.


## Conclusion

Machine learning can provide powerful insights into housing markets, but choosing the right model depends on the goal. If accuracy is the target, ensemble methods like Random Forest shine. If understanding *why* prices vary is more important, linear models remain useful.

📄 You can [view the full report here](https://github.com/cliffordEmmanuel/house-prices-prediction/blob/main/Comparative_Analysis_regression_alogrithms_Report.pdf).


