🚕 Ride Price Estimation System (Mini Machine Learning Project)
Project Overview

This project implements an end-to-end machine learning system to estimate ride prices based on trip and contextual factors such as distance, duration, traffic conditions, weather, and demand level. The main goal is to demonstrate the full machine learning workflow, from dataset design to model evaluation and reflection, rather than maximizing prediction accuracy.

Problem Statement

Ride prices are influenced by multiple interacting factors that are difficult to model using fixed rules. This project frames ride price estimation as a supervised machine learning problem, allowing models to learn pricing patterns directly from data and make predictions for unseen ride scenarios.

Dataset Description

The dataset used in this project was synthetically created to simulate realistic ride-hailing scenarios.

Number of rows: 150+

Target variable: ride_price (continuous)

Feature types: Numerical and categorical

Features Used and Justification

distance_km: Longer distances generally increase ride cost

duration_min: Time-based component of pricing

time_of_day: Peak hours tend to have higher prices

traffic_level: Heavy traffic increases ride cost

weather_condition: Poor weather can raise prices due to higher risk

demand_level: High demand often leads to surge pricing

fuel_price: Higher fuel prices increase operational costs

Feature considered but not included:
Price of fuel was considered as an external real-time factor but was excluded to keep the dataset simple and because it does not vary significantly per individual ride in short time periods.

Machine Learning Workflow

The notebook follows the standard machine learning pipeline taught in Semester One:

Problem framing and ML justification

Data exploration and visualization

Data cleaning and feature engineering

Linear Regression for ride price prediction

Logistic Regression for high-cost vs low-cost classification

Model evaluation and comparison

Ethical and practical reflection

Models Used

Linear Regression: Predicts continuous ride prices

Logistic Regression: Classifies rides as high-cost or low-cost

Evaluation metrics include Mean Absolute Error (MAE), R² score, accuracy, and confusion matrix.

Key Findings

Distance and demand level were the most influential features

Data quality had a strong impact on both regression and classification performance

Even simple models can capture meaningful pricing behavior

Ethical and Practical Considerations

Potential unfair pricing during high-demand periods

Risk of overpricing during emergencies or bad weather

Synthetic data limits real-world generalization

How to Run the Notebook

Clone the repository

Open notebook/ride_price_model.ipynb in Jupyter Notebook or Google Colab

Ensure required Python libraries are installed

Run the notebook cells sequentially from top to bottom

Repository Structure
ride-price-ml/
│── data/
│   └── rides.csv
│── notebook/
│   └── ride_price_model.ipynb
│── README.md