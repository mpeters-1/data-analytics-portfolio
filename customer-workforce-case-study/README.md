# Workforce Demographics & Income Insights Analysis (U.S. Census Data)

## Project Overview

This project explores workforce demographic and occupational patterns using structured U.S. Census data to uncover how education level, job role, and employment characteristics relate to income outcomes.

The goal of this analysis is to simulate a **real-world workforce analytics scenario**, where HR teams or policy analysts may want to understand:
- Which job roles are most common in different workforce segments
- How education level relates to income distribution
- Which roles are most associated with higher earning potential

This project demonstrates practical skills in **data cleaning, feature selection, exploratory data analysis, and business-focused data visualization using Python (Pandas + Matplotlib).**

---

## Business Context

Organizations and workforce planners often need to answer questions such as:
- Which job categories are associated with higher earning populations?
- How do education levels influence income distribution across roles?
- Are there clear workforce segments that over-index in high-income brackets?

This analysis focuses on a subset of census attributes to simulate a simplified workforce intelligence dashboard.

---

## Tools & Libraries

- Python 3
- Pandas (data manipulation)
- Matplotlib (data visualization)

---

## Dataset

The dataset is derived from structured census records and includes demographic and employment attributes such as:

- Employment Type
- Education Level
- Marital Status
- Job Role
- Family Status
- Ethnicity
- Gender
- Country
- Income Level (<=50K or >50K)

---

## Key Analytical Steps

### 1. Feature Selection & Filtering
Selected relevant workforce attributes for focused analysis:
- Employment Type
- Education Level
- Job Role
- Income Level
- Demographic attributes (gender, ethnicity, country)

This step ensures analysis is scoped to meaningful workforce signals.

---

### 2. Data Standardization
Renamed raw census columns into business-friendly labels:

- `State-gov` → Employment Type  
- `Bachelors` → Degree Status  
- `Never-married` → Marriage Status  
- `Adm-clerical` → Job Role  
- `Not-in-family` → Family Role  
- `White` → Ethnicity  
- `Male` → Gender  
- `United-States` → Country  
- `<=50K` → Earnings  

This improves interpretability for stakeholders.

---

### 3. Workforce Composition Analysis
A frequency distribution of job roles was generated to understand workforce structure across occupations.

Output:
- Bar chart showing distribution of job roles (ascending order)

This highlights the most and least common occupational categories in the dataset.

---

### 4. Income Segmentation by Job Role (High School Graduates)
The dataset was segmented to isolate:
- High school graduates earning ≤50K
- High school graduates earning >50K (U.S. only)

This allows comparison of job role distribution across income bands.

Output:
- Two comparative bar charts showing job role distribution across income groups

---

### 5. Income Proportion Analysis
A normalized distribution was calculated to identify:
> Which job roles are most overrepresented among high earners (>50K)

This helps highlight occupational categories associated with stronger earning potential.
