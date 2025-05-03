
# 🚚 Food Delivery Time Prediction

This project aims to predict the delivery time of food orders using real-world factors like distance, delivery person’s age and ratings, and order type. Leveraging deep learning through an LSTM neural network, this solution brings predictive power to the logistics and food delivery industry.

## 📌 Overview

Accurate delivery time prediction is critical for enhancing customer satisfaction and optimizing fleet logistics. This project uses a dataset containing details of food deliveries and builds a model to predict the **time taken for delivery** based on:

- Delivery distance (calculated using the Haversine formula)
- Delivery person's age
- Delivery ratings
- Type of order and vehicle (for visual analysis)

## ✨ Key Features

- 📍 **Geospatial Distance Calculation** using Haversine formula  
- 📊 **Interactive Visualizations** with Plotly (Distance vs Time, Age vs Time, Ratings vs Time, etc.)  
- 🧠 **LSTM Neural Network** for time prediction  
- 🔍 **Exploratory Data Analysis** using Box plots and Scatter plots  
- 🧪 **Train/Test Split** for model evaluation  
- 📈 Predicts delivery time based on real-time input features

## 🔧 Tech Stack

- **Python**  
- **Pandas, NumPy** – Data manipulation  
- **Plotly** – Interactive visualizations  
- **Scikit-learn** – Data preprocessing and splitting  
- **TensorFlow/Keras** – LSTM model  
- **Jupyter/Google Colab** – Development environment

## 🧠 Model Architecture

The model uses a **2-layer LSTM network** followed by dense layers:

- LSTM (128 units) → LSTM (64 units) → Dense (25) → Dense (1)
- Loss Function: Mean Squared Error
- Optimizer: Adam
- Trained for 9 epochs

## 📊 Visualizations

- **Distance vs Time Taken**
- **Delivery Person Age vs Time Taken**
- **Ratings vs Time Taken**
- **Box Plot** by Type of Vehicle and Order

## 📥 Inputs for Prediction

The model takes the following real-time inputs:
- Age of Delivery Partner (e.g., `28`)
- Ratings from previous deliveries (e.g., `4.7`)
- Total distance in kilometers (e.g., `5.2`)

Returns the **predicted time taken in minutes**.

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/yourusername/food-delivery-time-prediction

# Install required libraries
pip install pandas numpy plotly scikit-learn tensorflow

# Run the script
python food_delivery_time_prediction.py
```

You’ll be prompted to enter inputs for Age, Rating, and Distance.

## 📁 Dataset

The dataset `deliverytime.txt` includes delivery partner details, delivery location, and timestamps. The distance is computed dynamically using latitude and longitude.

## 📌 Use Cases

- Optimize food delivery estimates
- Improve customer satisfaction
- Manage delivery resources better
- Enhance food logistics efficiency
