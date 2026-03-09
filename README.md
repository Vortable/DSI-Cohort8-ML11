# DSI-Cohort8-ML11
# TTC Subway Delay Analysis & Prediction

## Purpose & Overview

Subway delays significantly impact service reliability and passenger experience within the Toronto Transit Commission (TTC) network. Identifying the root causes of delays in real time is difficult due to the complex interactions between operational, environmental, and human factors.

This project analyzes historical TTC subway delay incidents and applies machine learning techniques to uncover patterns and predict delay causes. The objective is to transform historical operational data into actionable insights that support better transit management and service reliability.

The dataset includes over 20,000 delay incidents recorded between 2021 and 2026, containing information such as:

- Date and time of incident
- Subway station
- Line and direction
- Delay duration
- Operational delay codes

By combining data analysis, feature engineering, and machine learning models, this project identifies key factors contributing to subway delays and provides insights that can improve transit operations.

---

## Goals & Objectives

### Operational Goals

The project aims to support transit operators by enabling data-driven operational decisions.

Key goals include:

- Identify the primary causes of subway delays
- Understand when and where delays occur most frequently
- Detect patterns across stations, lines, and time periods
- Provide insights that support faster response and better resource allocation

### Analytical Goals

From a machine learning perspective, the project aims to:

- Predict delay categories based on operational conditions
- Identify important predictive variables
- Evaluate different machine learning models for delay prediction

Key analytical questions include:

- What factors contribute most to significant delays?
- Which stations experience the highest frequency of incidents?
- How do time-of-day and operational conditions influence delays?

---

## Dataset Description

The dataset contains TTC subway delay incidents from 2021 to 2026.

Total observations analyzed: **20,316 delay events**

Main variables include:

### Temporal Information
- Year
- Month
- Time category (Early AM, AM Peak, Midday, PM Peak, Evening)

### Operational Information
- Station
- Subway line
- Travel direction (bound)

### Delay Statistics
- Min delay 
- Min gap between trains

These variables provide the operational context needed to analyze transit service disruptions.

---

## Techniques & Technologies

### Programming Tools

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### Machine Learning Models Tested

Several classification algorithms were evaluated:

- XGBoost
- LightGBM
- CatBoost
- Random Forest
- K-Nearest Neighbors (KNN)
- Neural Network (MLP)
- Logistic Regression
- Naive Bayes

Among these models, **XGBoost achieved the best predictive performance** for classifying delay categories.

---

## Feature Engineering

Several features were engineered to improve model performance.

### Numerical Features
- hour
- hour_sin (cyclical time representation)
- month_num
- year
- min_delay
- min_gap
- station_freq

### Categorical Features
- time_category
- delay_category
- line
- bound

Feature importance analysis showed that **station-related variables and time-based characteristics are the most influential predictors of delay causes**.

---

## Key Findings

### Time Patterns

Exploratory Data Analysis shows that:

- Delays tend to be higher during **PM Peak and Midday periods**
- **Weekend delays are higher on average**
- Typical delay duration ranges from **5 to 10 minutes**, with occasional extreme outliers

### Station-Level Patterns

Delay incidents vary significantly across the TTC network.

Examples include:

- **Bloor Station** experiencing higher security-related incidents
- **Finch Station** showing more operator-related delays
- **St George and Spadina** reporting higher medical incidents

These patterns suggest that **passenger activity and station infrastructure influence delay frequency**.

### Major Causes of Delays

Key operational delay categories include:

- Security incidents
- Mechanical failures
- Infrastructure issues
- Operator-related incidents

---

## Model Performance

Multiple machine learning models were evaluated using classification metrics.

Example AUC results:

| Model | AUC |
|------|------|
| XGBoost | 0.770 |
| LightGBM | 0.768 |
| CatBoost | 0.756 |
| Random Forest | 0.753 |
| KNN | 0.730 |
| Neural Network | 0.738 |
| Logistic Regression | 0.642 |
| Naive Bayes | 0.628 |

XGBoost achieved the strongest performance in predicting TTC delay patterns.

---

## Analytics Dashboard

An analytics dashboard was developed to summarize operational insights.

Key metrics include:

- Total delay incidents analyzed: **20,316**
- Average delay duration: **11.44 minutes**
- High delay incidents: **5% of events**
- Overall on-time performance: **93%**

Dashboard features allow users to filter by:

- Subway line
- Station
- Date range
- Incident category

This enables transit planners to explore delay patterns interactively.

---

## Project Workflow

```
1. Data Collection
   TTC Subway Delay Dataset

2. Data Cleaning
   - Handle missing values
   - Standardize delay codes
   - Remove inconsistent records

3. Exploratory Data Analysis
   - Identify delay distributions
   - Detect station and time patterns

4. Feature Engineering
   - Temporal features
   - Operational variables
   - Delay statistics

5. Machine Learning Modeling
   - Multi-class classification
   - Model comparison

6. Model Evaluation
   - ROC curves
   - AUC scores
   - Feature importance analysis

7. Visualization & Dashboard
```

---

## Installation

Install required Python packages:

```
pip install pandas numpy matplotlib seaborn scikit-learn xgboost catboost lightgbm
```

---

## Running the Project

Run the notebooks in the following order:

```
1_data_cleaning_final.ipynb
2_eda_nicoleh.ipynb
3_feature_engineering_nicoleh.ipynb
4_baseline_model_development_nicoleh.ipynb
```

---

## Future Improvements

Potential future enhancements include:

- Incorporating **weather data**
- Integrating **train schedule data**
- Developing **real-time delay prediction systems**
- Deploying models for **live transit monitoring dashboards**

These improvements could help transit agencies move from historical analysis toward **real-time operational intelligence**.

---

## Contributors

DSI Cohort 8 – Machine Learning Project - Group ML11
Wendy Graham, 
Ivy Guevarra,  
Nicole Hong, 
Nicole Yeung

## Video (Reflection)

Ivy Guevarra- Link: https://youtu.be/O6hwoKkBtJg?si=Va2pc4NVGBfABm76