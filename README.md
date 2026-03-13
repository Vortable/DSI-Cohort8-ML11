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

## Feature Engineeringris

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

# Project Risks & Limitations

While the analysis provides valuable insights, several risks and limitations should be considered.

## Data Limitations

The dataset only includes **recorded delay incidents**, which means some minor operational disruptions may not be captured. In addition, the data does not include other potentially influential variables such as:

- Weather conditions
- Passenger volume
- Special events
- Real-time train congestion

These missing factors may reduce the predictive power of the models.

## Class Imbalance

Some delay codes occur far more frequently than others. This imbalance can make it difficult for machine learning models to accurately predict rare delay categories.

To mitigate this issue, techniques such as **class weighting and category grouping** were considered.

## Model Generalization

Machine learning models trained on historical data may not fully generalize to future operational changes, such as:

- New transit infrastructure
- Changes in TTC operational procedures
- System upgrades or service expansions

Continuous retraining with updated data would be necessary for a production system.

## Interpretation Challenges

Some delay codes represent **broad operational categories**, making it difficult to distinguish precise root causes without additional contextual data.

---

# Team Task Breakdown

The project was completed through collaborative teamwork, with responsibilities divided across different stages of the machine learning pipeline.

```
1. Data Collection (by all team members)
   TTC Subway Delay Dataset

2. Data Cleaning (by Wendy Graham)
   - Handle missing values
   - Standardize delay codes
   - Remove inconsistent records

3. Exploratory Data Analysis (by Nicole Hong, Nicole Yeung)
   - Identify delay distributions
   - Detect station and time patterns

4. Feature Engineering (by Nicole Hong, Ivy Guevarra)
   - Temporal features
   - Operational variables
   - Delay statistics

5. Machine Learning Modeling (by all team members)
   - Multi-class classification
   - Model comparison

6. Model Evaluation (by Nicole Hong)
   - ROC curves
   - AUC scores
   - Feature importance analysis

7. Visualization & Dashboard (by Nicole Hong)
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
- Integrating **trLinkain schedule data**
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

> * Ivy Guevarra - Link: https://youtu.be/O6hwoKkBtJg?si=Va2pc4NVGBfABm76
> * Nicole Hong - Link: https://youtu.be/_tkG40oNVXQ
> * Nicole Yeung - Link: https://youtu.be/fxeWIs9RR8Q
> * Wendy Graham - Link: https://youtu.be/Hxuy9BrEm30
