# Predictive Maintenance using Machine Learning

## Project Overview

This project develops a predictive maintenance system using machine learning techniques to classify component failures based on machine telemetry, error logs, maintenance history, and machine metadata.

The goal is to predict the type of component failure (comp1, comp2, comp3, comp4) by analyzing machine behavior in the period leading up to a failure event.

## Business Problem

Unexpected equipment failures can lead to increased downtime, loss of productivity, higher maintenance costs, and operational inefficiencies. Predictive maintenance aims to detect failure patterns early and enable proactive maintenance actions before breakdowns occur.

## Dataset

Microsoft Azure Predictive Maintenance Dataset

Data Sources:
- Telemetry
- Errors
- Failures
- Maintenance
- Machines

## Exploratory Data Analysis

### Error Analysis
- Error5 showed the strongest association with failures.
- Error2 and Error3 frequently occurred before failures.

### Telemetry Analysis
- Comp1 -> Elevated Voltage
- Comp2 -> Reduced Rotation
- Comp3 -> Elevated Pressure
- Comp4 -> Elevated Vibration

### Maintenance Analysis
- Maintenance timing contributed minimal predictive information.

### Machine Metadata Analysis
- Comp4 failures were concentrated among older machines.

## Feature Engineering

Error Features:
- error_count_24h
- error1_count_24h
- error2_count_24h
- error3_count_24h
- error4_count_24h
- error5_count_24h

Telemetry Features:
- mean_voltage_24h
- mean_rotation_24h
- mean_pressure_24h
- mean_vibration_24h

Maintenance Features:
- days_since_maintenance

Machine Features:
- age
- model

## Models Evaluated

### Decision Tree
- Accuracy: 88%

### Random Forest
- Accuracy: 89%

## Random Forest Feature Importance

Top predictors:
- mean_rotation_24h
- mean_voltage_24h
- mean_vibration_24h
- error5_count_24h
- error2_count_24h
- mean_pressure_24h

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

## Future Improvements

- Hyperparameter tuning
- XGBoost implementation
- Streamlit deployment
- SHAP explainability

## Results Summary

- Built an end-to-end predictive maintenance pipeline.
- Engineered features from telemetry, maintenance and error history.
- Achieved 89% accuracy using Random Forest.
