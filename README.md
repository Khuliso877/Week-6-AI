Smart Agriculture Simulation System
AI + IoT Crop Yield Prediction

A complete simulation environment for sensor data generation, feature engineering, and AI-based yield prediction.

📌 Overview

This project implements a Smart Agriculture Simulation System that mimics real-world IoT-based farming.
It simulates sensor data for multiple farm plots, aggregates the readings into season-level features, and trains a machine learning model to predict crop yield.

This provides a realistic digital-twin environment for experimenting with:

IoT sensor networks
Feature engineering
AI-driven yield prediction
Model evaluation and explainability
The system is fully runnable in Google Colab.

🚀 Features
1. IoT Sensor Simulation

The notebook generates realistic daily readings for each farm plot, including:
Soil moisture (10 cm, 30 cm)
Soil temperature
Air temperature
Air humidity
Rainfall
Solar radiation
NDVI (vegetation index)

2. Feature Engineering

Season-level (per-plot) features are computed automatically:
Mean, min, max soil moisture
Cumulative rainfall
Average NDVI, maximum NDVI
Average temperatures and humidity
Soil & plot quality metrics
Synthetic crop growth indicators
These are fed into a supervised learning model.

3. Machine Learning — Yield Prediction

An XGBoost Regressor predicts final crop yield (tons per hectare).

Outputs include:
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)
R² Score
Scatter plot: predicted vs actual
Feature importance (top contributing factors)

4. Synthetic Ground Truth Generation

A “hidden” yield formula is used to generate realistic yield labels.
Model accuracy reflects how well it learns this underlying crop-yield function.

5. Example Inference Pipeline

The project demonstrates how new incoming seasonal data can be fed into the model for real-time or post-season predictions.
Static plot attributes: soil quality, irrigation efficiency, yield potential
Sensor values follow environmental patterns, seasonal curves, and random events (rain, cloud cover).
