

# California Housing: End-to-End Price Prediction Pipeline

This repository contains a comprehensive machine learning project focused on predicting median house values in California. The goal was to build a complete pipeline, moving from raw data processing to model evaluation.

## Project Motivation
While my background is primarily in the R ecosystem for statistical analysis, I am currently expanding my technical repertoire into Python. This project serves as a practical application of machine learning fundamentals (specifically regression) using the Scikit-Learn framework.

## Methodology
The project follows a structured data science workflow to ensure model reliability and reproducibility.

* **Data Stratification:** I utilized Stratified Shuffle Split to ensure the training and test sets maintained a representative distribution of median income, preventing sampling bias.
* **Exploratory Data Analysis:** I conducted a geospatial analysis to identify price clusters and calculated correlation matrices to determine which features, such as proximity to the ocean, had the most significant impact on value.
* **Feature Engineering:** I developed custom transformers to handle missing values and create derived attributes like rooms-per-household, which improved the model's predictive power over raw census data.
* **Model Selection:** I benchmarked multiple algorithms, including Linear Regression and Random Forest Regressors, to evaluate the trade-offs between underfitting and overfitting.

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Scikit-Learn
* **Environment:** Google Colab

## Current Status and Results
The initial Random Forest model significantly outperformed the Linear Regression baseline. I am currently in the process of fine-tuning hyperparameters via GridSearchCV to optimize the Root Mean Squared Error (RMSE).

## Lessons Learned
One of the key findings during the data exploration phase was a cap on the median house value at $500,000. This quirk in the dataset requires careful handling to ensure the model does not learn a false ceiling for prices. This project highlighted the importance of thorough data cleaning and the impact that even a few derived features can have on model accuracy.
