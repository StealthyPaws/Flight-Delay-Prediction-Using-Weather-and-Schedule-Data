# Flight Delay Prediction Using Weather and Schedule Data

This repository predicts flight departure delays by analyzing flight and weather data. The solution involves data integration, feature engineering, exploratory data analysis, classification, regression, and model optimization. Predictions are formatted for Kaggle competition submission.

---

## Objective

To build a machine learning pipeline to predict flight departure delays using:
- Train and test flight data
- Weather data

---

## Data Sources

- Flight schedule and actual performance (train and test sets)
- Weather data joined on relevant time and location fields

---

## Phase 1: Data Preprocessing & Feature Engineering

### 1. Data Integration
- Merge flight and weather datasets on date and location.

### 2. Data Cleaning & Transformation
- Handle missing values
- Convert time fields into datetime format

### 3. Feature Engineering
- Compute delay duration
- Extract weather features (e.g., temperature, wind speed)
- Generate temporal features:
  - Day of the week
  - Hour of the day
  - Month

---

## Phase 2: Exploratory Data Analysis

### 1. Visual Analysis
- Histograms of delay durations
- Delay trends by hour, day, and month
- Category-wise delay patterns by airline and airport

### 2. Correlation Analysis
- Visualizations exploring relationships between:
  - Weather features and delay
  - Flight features and delay

### 3. Dataset Comparison
- Evaluate consistency between training and test sets

---

## Phase 3: Predictive Modeling

### 1. Binary Classification
- On-time vs delayed
- Evaluation: accuracy, precision, recall, F1, confusion matrix

### 2. Multi-Class Classification
- Delay categories:
  - No Delay (0 min)
  - Short Delay (<45 min)
  - Moderate Delay (45–175 min)
  - Long Delay (>175 min)
- Evaluation: multi-class metrics including class-wise analysis

### 3. Regression
- Predict exact delay duration
- Metrics: MAE, RMSE
- Cross-validation for evaluation

---

## Phase 4: Model Optimization & Evaluation

- Hyperparameter tuning using grid search/random search
- k-fold cross-validation for robustness
- Comparative analysis of classifiers and regressors

---

## Phase 5: Test Predictions

- Predict departure delays on test data using trained models
- Format outputs for Kaggle submission:
  - Classification: labels as "on-time", "delayed", etc. (not numeric)
  - Regression: predicted delay time

