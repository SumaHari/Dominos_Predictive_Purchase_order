# 🍕 Dominos - Predictive Purchase Order System

This project builds a **predictive purchase order system** for a pizza chain using historical sales data. The goal is to forecast **pizza sales quantities** for the upcoming week using **Facebook Prophet**, and then automatically generate a **purchase order of required ingredients** based on predicted sales volumes.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Folder Structure](#folder-structure)
- [Setup Instructions](#setup-instructions)
- [How It Works](#how-it-works)
- [Results](#results)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## 📊 Project Overview

**Industry Domain:** Food Service  
**Problem Type:** Forecasting + Recommendation System  
**Primary Objective:**  
To forecast pizza sales (quantity) for the next 7 days using Facebook Prophet and generate a weekly ingredient-level **purchase order**.

---

## ✨ Key Features

- Data parsing and cleaning from raw CSV files  
- Time series aggregation of pizza orders per day  
- Forecasting pizza sales quantity using Facebook Prophet  
- Generating next-week forecasts and calculating ingredient needs  
- Visualizations: sales trends, forecasts, and purchase orders  
- Robust handling of NaT values, zero sales, and missing ingredient mappings

---

## 🛠 Tech Stack

- **Python**: Core programming language
- **Pandas**: Data cleaning & manipulation
- **Matplotlib & Seaborn**: Data visualization
- **Facebook Prophet**: Time series forecasting
- **Datetime**: Handling time-based features
- **Jupyter Notebook / VS Code**: Development environment

---

## 📁 Folder Structure
dominos-predictive-order/
│
├── data/ # Historical order data
│ ├── orders.csv # Main sales data
│ ├── pizza_ingredients.csv # Pizza to ingredients map
│ └── pizza_types.csv # Pizza categories/types
│
├── dominos_forecast.py # Main executable Python script
├── README.md # Project documentation (this file)
├── requirements.txt # List of Python dependencies
└── plots/ # Output visualizations (optional)
How It Works
Data Preprocessing

Converts order timestamps into proper datetime format

Filters invalid rows (e.g., NaT values)

Aggregates quantity sold by day

Time Series Forecasting

Trains a Facebook Prophet model on daily quantity sold

Forecasts quantity for the next 7 days

Visualizes actual vs predicted sales and seasonal components

Ingredient Demand Estimation

Calculates historical pizza-type proportions

Distributes forecasted pizza quantities by proportion

Multiplies by per-pizza ingredient requirements to estimate total ingredient needs

Generates purchase order and visualizes it as a horizontal bar chart

✅ Results
Forecast Accuracy: Reported using MAPE (Mean Absolute Percentage Error)

Final Output:

Forecast table for next 7 days

DataFrame of required ingredients with rounded quantity (in KG)

Purchase Order Barplot (sorted by quantity)

🚀 Future Enhancements
Use LSTM or other deep learning models for forecasting

Include price-based optimization for bulk purchasing

Handle multiple stores or regions

Add Streamlit interface for live forecasts and reports

📝 License
This project is licensed under the MIT License.




