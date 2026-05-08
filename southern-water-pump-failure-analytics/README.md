# Southern Water Corp – Pump Operations Workforce & Reliability Case Study

## Overview

This project is a data-driven case study conducted for Southern Water Corp to analyze pump system performance, workforce-linked operational variables, and failure behavior using Python.  

The objective is to move beyond traditional spreadsheet-based analysis and demonstrate how Python can be used to:
- Rapidly explore operational datasets
- Identify patterns in workforce and environmental conditions
- Detect anomalies and outliers in sensor data
- Build statistical models to predict pump failure
- Translate raw operational data into actionable business insight

Rather than treating this as a technical exercise, this project is framed as a **customer workforce and operations reliability study**, where the goal is to understand how operational roles, system conditions, and performance metrics relate to pump failures.

---

## Business Context

Southern Water Corp operates critical pump infrastructure where downtime directly impacts service reliability and operational cost.  

Each record in the dataset reflects a snapshot of:
- Operational conditions (flow, speed, torque, efficiency)
- Environmental context (temperature)
- System outcomes (pump failure or normal operation)
- Derived variability measures (rolling standard deviation dataset)

This analysis helps answer:
- What conditions are associated with pump failure?
- Which operational variables show the strongest relationship with breakdowns?
- Can variability (instability) in system behavior better explain failures than raw measurements?
- How accurately can we model pump failure using observed conditions?

---

## Dataset Description

Two datasets are used:

### 1. Raw Pump Operations Data (`DF_Raw_Data.csv`)
Contains real-time operational metrics:
- Volumetric Flow Meter readings
- Pump Speed (RPM)
- Pump Torque
- Ambient Temperature
- Horse Power
- Pump Efficiency
- Pump Failure indicator (0 = normal, 1 = failure)

### 2. Rolling Standard Deviation Data (`DF_Rolling_Stdev.csv`)
Contains smoothed variability signals derived from the raw system behavior, used to capture instability trends over time.

---

## Tools & Libraries Used

- Python 3
- Pandas – data manipulation
- NumPy – numerical operations
- Matplotlib – visualization
- Seaborn – statistical visualizations
- Statsmodels – regression modeling

---

## Methodology

### 1. Data Exploration & Cleaning
- Imported raw and rolling standard deviation datasets
- Explored structure using `.info()` and `.describe()`
- Compared distribution differences between raw vs variability data

---

### 2. Data Visualization
- Box plots to identify distribution spread and outliers
- Line plots to observe system behavior over time
- Comparative visualizations for:
  - Pump failure vs normal operation
  - High vs low efficiency conditions

---

### 3. Workforce & Operational Segmentation Analysis
- Filtered datasets by:
  - Pump failure status (0 vs 1)
  - Operational conditions
- Compared behavior patterns across system states

---

### 4. Outlier Detection
- Applied Interquartile Range (IQR) method:
  - Q1 and Q3 quantiles calculated
  - Upper and lower bounds defined
- Identified and removed extreme values
- Evaluated impact of outlier removal on dataset integrity

---

### 5. Feature-Level Trend Analysis
- Iterated through each numerical variable
- Visualized relationship between:
  - Operational variables
  - Pump failure state
- Used dual-axis plots to compare scale differences

---

### 6. Correlation Analysis
- Built correlation matrices using `.corr()`
- Generated heatmaps using Seaborn
- Identified strongest relationships with pump failure

Key insight:
- No single variable strongly predicts failure in raw data
- Stronger structure emerges in variability (stdev) dataset

---

### 7. Predictive Modeling (OLS Regression)

Two models were built:

#### Model 1: Raw Data Regression
- Moderate explanatory power (low R²)
- Weak predictive relationship overall

#### Model 2: Rolling Standard Deviation Regression
- Strong predictive improvement (high R² ~ 0.77+)
- Indicates system instability is more predictive than raw values

---

## Key Findings

### 1. System Variability Matters More Than Raw Values
Rolling standard deviation features significantly outperform raw metrics in explaining pump failure.

---

### 2. Strongest Predictors of Pump Failure
Across models, the most influential variables include:
- Horse Power
- Pump Efficiency
- Volumetric Flow (especially Meter 2)
- Pump Speed and Torque (secondary influence)

---

### 3. Failure Is a Multivariate Condition
Pump failure is not driven by a single metric, but by a combination of:
- Mechanical load
- Efficiency degradation
- Flow inconsistency
- System instability over time

---

### 4. Variability Signals Improve Predictability
The rolling standard deviation dataset provides:
- Higher R² values
- Stronger regression coefficients
- Better model stability

This suggests that **instability is more predictive than absolute readings**.

---

## Business Implications

For Southern Water Corp operations teams:

- Monitoring **system variability** may be more effective than monitoring raw sensor values alone
- Predictive maintenance models should prioritize:
  - Fluctuation patterns
  - Rolling metrics
  - Efficiency drift
- Workforce and operational scheduling could be optimized around:
  - High-risk operating conditions
  - Identified instability thresholds

---

## Conclusion

This case study demonstrates how Python can be used to transform raw operational data into actionable insights for infrastructure reliability and workforce-driven system performance.

Key takeaway:
> Pump failures are best understood not through static measurements, but through **patterns of change and instability over time**.
