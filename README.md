# Deutsche Bahn Delays Analysis with Advanced Methods

This project analyzes train punctuality at Tübingen Hauptbahnhof using one year of operational data. By combining exploratory data analysis (EDA), machine learning, and explainable AI techniques, the goal is to understand delay patterns, identify critical factors, and build predictive models for operational improvement.

## Project Overview

* Objective: Analyze train delays and predict delay duration & critical delays.

* Data: One-year operational dataset including train schedules, delays, and service types.

* Tools & Libraries: Python, Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, CatBoost, SHAP.

* Models Implemented:

  Random Forest (Regression & Classification)

  XGBoost (Regression & Classification)

  LightGBM (Regression & Classification)

  CatBoost (Regression & Classification)

## Features & Engineering

* Cyclical Time Features: Hour of the day encoded as sine and cosine to preserve continuity.

* Categorical Encoding: Train types encoded with one-hot encoding.

* Target Variables:

  `delay_in_min` → Regression target

  `critical_delay` (delay > 5 min) → Classification target

* Data Cleanup: Removed helper and irrelevant columns for modeling.

## Model Performance Summary
**Model	      MAE (Regression)	RMSE (Regression)	Classification Accuracy	F1-score (critical delay)**
Random Forest	2.41	            5.39	0.87	0.46

XGBoost	      2.43	5.38	0.86	0.42

LightGBM	      2.48	5.50	0.86	0.44

CatBoost	      2.31	5.90	0.86	0.42

* Models successfully capture structural delay patterns.

* Classification models struggle with critical delays due to inherent unpredictability.

## Explainability with SHAP

* Global Feature Importance: Identified key factors influencing delays.

* Individual Prediction Analysis: SHAP values provide insight into why specific delays occur.

* Operational Insights: Peak hours, service type, and route interactions are the main drivers of delays.

## Key Takeaways

* Most delays are minor, but peak-hour and service-specific patterns significantly influence performance.

* Predictive models perform consistently across algorithms, highlighting structural factors over model choice.

* SHAP explainability supports actionable operational improvements.

* Integrating external factors (weather, technical issues, passenger volume) could enhance predictions.
