

# 🚕 Ride Price Estimation System

**Mini Machine Learning Project – Semester One**

## 📌 Project Overview

This project presents an end-to-end machine learning system designed to estimate the price of a ride based on trip and contextual information. The goal of the project is not to build a perfect pricing model, but to demonstrate practical machine learning thinking: how to frame a real-world problem, design a dataset, prepare data, train models, evaluate results, and reflect on limitations and ethical concerns.

The project follows the complete machine learning workflow taught in Semester One and emphasizes reasoning, interpretability, and clarity over model complexity.

---

## 🧠 Problem Statement

Ride prices are influenced by several factors such as trip distance, duration, traffic conditions, time of day, weather, and rider demand. These factors interact in non-linear and sometimes unpredictable ways, making it difficult to define accurate pricing using fixed rules.

This project frames ride price estimation as a **supervised machine learning problem**, where a model learns pricing patterns from historical ride data and uses those patterns to estimate prices for new, unseen rides.

---

## 🎯 Learning Objectives

By completing this project, the following machine learning competencies are demonstrated:

* Framing a real-world problem as a machine learning task
* Designing a dataset with meaningful numerical and categorical features
* Applying the full machine learning workflow
* Building and evaluating both regression and classification models
* Communicating results clearly through code, visualizations, and explanations

---

## 📊 Dataset Description

The dataset used in this project was **synthetically created** to simulate realistic ride-hailing scenarios. All values were generated based on logical assumptions about how ride pricing works in practice.

* **Number of rows:** 150+
* **Target variable:** `ride_price` (continuous)
* **Feature types:** Numerical and categorical

### Features Used and Justification

* **distance_km**
  Longer distances naturally increase fuel usage and driver time, leading to higher prices.

* **duration_min**
  Ride duration captures time-based pricing, especially in slow traffic conditions.

* **time_of_day**
  Prices often vary depending on whether a ride occurs during peak or off-peak hours.

* **traffic_level**
  Heavier traffic increases trip time and operational cost.

* **weather_condition**
  Poor weather conditions can increase prices due to higher risk and reduced driver availability.

* **demand_level**
  High demand is commonly associated with surge pricing mechanisms.

* **fuel_price**
  Fuel cost affects operational expenses and indirectly influences ride pricing.

**Feature considered but not included:**
Gender was intentionally excluded because it is ethically inappropriate and should not influence ride pricing decisions.

---

## 🔄 Machine Learning Workflow

The notebook follows a structured machine learning pipeline:

1. **Problem Framing & ML Justification**
   Defining why machine learning is suitable for this task.

2. **Data Exploration & Understanding**
   Inspecting the dataset, checking for missing values, inconsistent labels, outliers, and visualizing raw data.

3. **Data Cleaning & Feature Engineering**
   Handling missing values, encoding categorical variables, scaling numerical features, and treating outliers.

4. **Regression Model: Ride Price Prediction**
   Training a Linear Regression model to predict continuous ride prices and evaluating its performance.

5. **Classification Model: High-Cost vs Low-Cost Ride**
   Creating a binary target and training a Logistic Regression model, evaluated using accuracy and a confusion matrix.

6. **Model Evaluation & Comparison**
   Comparing regression and classification results and identifying the most influential features.

7. **Ethical & Practical Reflection**
   Discussing potential risks, biases, and limitations of the system.

---

## 🤖 Models Used

### Linear Regression

Used to predict continuous ride prices. Evaluation metrics include:

* Mean Absolute Error (MAE)
* R² score

### Logistic Regression

Used to classify rides as **high-cost** or **low-cost**. Evaluation metrics include:

* Accuracy
* Confusion Matrix

These models were chosen because they are interpretable and aligned with methods taught in Semester One.

---

## 📈 Key Findings

* Distance and demand level were the most influential features affecting ride price
* Data quality significantly impacted model performance
* Simple models were able to learn meaningful pricing behavior
* Classification results depended heavily on how the price threshold was defined

---

## ⚖️ Ethical and Practical Considerations

* **Potential unfair pricing:** Surge pricing during high demand may disadvantage certain users
* **Real-world risk:** Over-reliance on automated pricing without human oversight
* **Dataset limitation:** Synthetic data may not fully capture real-world complexity

---

## ▶️ How to Run the Notebook

1. Clone this repository
2. Open `notebook/ride_price_model.ipynb` in Jupyter Notebook or Google Colab
3. Ensure required Python libraries are installed (`pandas`, `numpy`, `matplotlib`, `scikit-learn`)
4. Run all cells from top to bottom

---

## 📁 Repository Structure

```
ride-price-ml/
│── data/
│   └── rides.csv
│── notebook/
│   └── ride_price_model.ipynb
│── README.md
```

---


