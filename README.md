# DSI-Cohort8-ML11
# TTC Subway Delay Prediction  
---

## Project Overview

This project analyzes TTC subway delay data (2022–2025) to predict delay duration and identify high-delay incidents.  

Our goal is to improve transit reliability by building predictive models that support TTC operations, service planning, and data-driven decision-making.
---

## Intended Audience

This project is designed for:

- Operational Managers  
- Team Leads  
- Service Planning Teams  
---

## Business Motivation

Transit delays impact rider satisfaction, operational efficiency, and city mobility.

By predicting delay duration and identifying high-delay incidents, this project aims to:

- Improve operational response planning
- Identify high-risk stations, times, and delay causes
- Enhance overall transit reliability

---

## Dataset

**Dataset:** TTC Subway Delay Dataset  
**Time Range:** 2022 – 2025  

### Key Variables

#### Feature Variables
- `Min Delay` (Delay duration in minutes)
- Month / Year / Seasons (Derived from date)
- Different Times of the Day (Derived from time)
- Station
- Line
- Direction

#### Target Variable
- Cause of Delay

---

## Business Questions

1. What factors contribute most to significant delays?
2. Can we classify whether a delay will exceed 5 minutes (high-delay incident)?

---

## Data Cleaning & Preprocessing Strategy

### Handling Missing Values
- “Vehicle” column contains missing values
- “Bound” column frequently contains missing or placeholder values (e.g., “XXXXX”)
- Strategy:
  - Impute where appropriate
  - Remove unusable rows
  - Treat missing values as a separate category if necessary

### Data Consistency Issues
- Spelling errors
- Inconsistent naming (e.g., line names)
- Strategy:
  - Standardize categorical values
  - Clean and normalize text fields

### Outlier Handling
- Extreme delays exist (e.g., 716 minutes)
- Remove delays greater than 60 minutes to focus on realistic operational scenarios

### Modeling Focus
- Focus on delays greater than 5 minutes
- Emphasis on origin station and direction

---

## Analysis Approach

### Classification (Primary ML Focus)

**Objective:** Predict high-delay incidents (> 5 minutes)

- Binary target creation
- Address class imbalance
- Models:
   TBC

---

## Risks & Uncertainties

- Missing or inconsistent categorical data
- Potential bias from removing extreme outliers
- Bound column largely missing

Mitigation:
- Robust validation strategy
- Clear documentation of assumptions

---

## Project Timeline

**Project Deadline:** Sunday, March 8  
**Machine Learning Focus:** Classification

| Date | Task | Owner |
|------|------|-------|
| 2021–2025 | Reviewing Data | All |
| Thursday, Feb 26 | Document Business Objectives / Project Plan | All |
| Saturday, Feb 28 | Data Cleaning | Wendy |
| Monday, March 2 | Data Preprocessing - Time & Day Categories | Nicole H |
| Tuesday, March 3 | EDA / Feature Engineering| Nicole H / Ivy |
| TBD | ML Development (Train/Test) | All |
| TBD | Model Selection | All |
| TBD | GitHub Documentation | Nicole Y / Ivy |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Git / GitHub
- Jupyter Notebook

---

## Project Showcase

At the end of the project, we will present:

- Business motivation
- Data exploration insights
- Model performance comparison
- Key recommendations
- Future improvements
