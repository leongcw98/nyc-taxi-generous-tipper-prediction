# Predicting Generous Tippers for NYC Taxis

## Project Overview

This project focuses on developing a machine learning model to predict which New York City taxi passengers are likely to give generous tips (20% or more). The aim is to help taxi drivers target high-value passengers and potentially increase their earnings.

## Objective

Build a predictive model that identifies passengers likely to give generous tips, thereby aiding taxi drivers in maximizing their overall earnings.

## Dataset

The dataset contains information on NYC taxi rides, including trip details, fares, and tipping behavior. The data has been cleaned and preprocessed to prepare it for modeling.

## Methodology

### 1. Data Cleaning

- Handled missing values
- Addressed outliers
- Removed irrelevant features

### 2. Feature Engineering

Engineered features to improve model performance, including:
- `VendorID`
- `Predicted_fare`
- `Mean_duration`
- `Mean_distance`
- Additional features such as trip distance categories and fare amount ratios

### 3. Model Training

Trained and evaluated the following classifiers:
- **Random Forest Classifier**
- **XGBoost Classifier**

### 4. Hyperparameter Tuning

Optimized model performance using GridSearchCV to find the best hyperparameters.

### 5. Model Evaluation

Models were evaluated based on F1 score, accuracy, precision, and recall. The Random Forest model demonstrated slightly better performance than the XGBoost model.

## Results Summary

- **Random Forest Model**:
  - F1 Score: ~0.7235
  - Accuracy: ~0.6865
  - Correctly identified ~78% of actual responders, which is 48% better than random guessing.

- **XGBoost Model**:
  - Slightly lower F1 Score compared to the Random Forest model.

### Feature Importance

Key features identified by the Random Forest model include:
- `VendorID`
- `Predicted_fare`
- `Mean_duration`
- `Mean_distance`

`VendorID` was particularly notable, suggesting that different vendors attract varying tipping behaviors.

## Conclusions

- **Model Recommendation**: The Random Forest model is effective, with an F1 score of 0.7235. It is recommended for testing with a select group of taxi drivers to gather practical feedback.
  
- **Model Insights**: The Random Forest algorithm, while effective, lacks transparency in how features influence tipping. Further investigation into the impact of `VendorID` is warranted.

## Future Model Suggestions

- **Granular Data**: Collect more detailed data on drivers and passengers, including past tipping behavior.
- **Cluster Analysis**: Use K-means clustering to analyze data clusters and derive additional insights.

## Next Steps

1. **Consultation**: Share the model results with the New York City Taxi and Limousine Commission and recommend using the model as an indicator of potential tip amounts.
2. **Data Expansion**: Acquire additional data to further enhance model accuracy and effectiveness.
