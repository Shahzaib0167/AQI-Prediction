Air Quality Index (AQI) Prediction Pipeline

This project implements a complete end-to-end Data Science pipeline to predict the Air Quality Index (AQI) based on atmospheric and environmental factors. By leveraging advanced machine learning techniques and time-series feature engineering, the model provides accurate forecasts to help monitor environmental safety.



🚀 Project Overview

Predicting air quality is a complex regression problem. This project focuses on processing raw environmental data—specifically PM2.5, Temperature, and Humidity—and transforming it into a robust predictive model.



Key Features

Data Cleaning \& Robustness: Handled missing values, duplicates, and implemented IQR Capping (Winsorization) to manage outliers without losing data integrity.



Advanced Feature Engineering: \* Extracted time-based components (Month, Day, Hour).



Applied Cyclical Encoding (Sine/Cosine transforms) to capture the periodic nature of seasonal and daily atmospheric changes.



Time-Series Validation: Used TimeSeriesSplit for cross-validation to respect the temporal order of data, preventing data leakage.



Optimized Modeling: Performed a comparative analysis of multiple models, selecting a Tuned Gradient Boosting Regressor as the final estimator.



Hyperparameter Tuning: Utilized GridSearchCV to fine-tune model parameters for maximum accuracy.



🛠️ Tech Stack

Language: Python 3.x



Data Manipulation: Pandas, NumPy



Visualization: Matplotlib, Seaborn



Machine Learning: Scikit-Learn



Model Persistence: Joblib



📊 Methodology

1\. Data Preprocessing

Sanity checks for data types and range.



Feature engineering of lag variables and rolling averages to capture trends.



Scaling and normalization where required for linear baselines.



2\. Exploratory Data Analysis (EDA)

Correlation heatmaps to identify key predictors (e.g., the high impact of PM2.5 on AQI).



Distribution plots to identify skewness in environmental variables.



3\. Modeling \& Evaluation

The model was evaluated based on Mean Absolute Error (MAE) and R-Squared (R²). The final Gradient Boosting model was chosen for its ability to handle non-linear relationships in environmental data.

