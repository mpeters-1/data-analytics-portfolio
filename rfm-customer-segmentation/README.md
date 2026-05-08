# Customer Segmentation & Retention Analysis (RFM Model)

## Overview

This project analyzes customer purchasing behavior for a U.S.-based retail distributor using **RFM (Recency, Frequency, Monetary) segmentation** to identify high-value customers, retention patterns, and regional sales performance.

The goal of this analysis is to simulate how businesses can better understand customer behavior to improve **retention, targeted marketing, and revenue optimization strategies**.

The final output is an interactive Tableau dashboard visualizing customer segments, retention trends, product preferences, and geographic performance.

---

## Key Business Questions

- Who are the highest-value customers based on purchasing behavior?
- Which customer segments are at risk of churn or disengagement?
- How does customer value vary across regions?
- What products drive the most revenue and repeat purchases?
- How does seasonality affect customer ordering behavior?

---

## Data Cleaning & Preparation (Python)

Before performing analysis in Tableau, the dataset required preprocessing in Python to ensure data integrity and realistic transactional structure.

### Major Data Issue Identified
- Order dates and shipping dates were inconsistently recorded
- In some cases, shipping dates were **2–3 years after order dates**, which was not realistic for operational analysis

### Data Cleaning Approach
Using Python (pandas), the following transformation was applied:

- Standardized date formats
- Identified invalid or inconsistent shipping timelines
- Reconstructed shipping dates to occur within a realistic fulfillment window
- Randomized shipping dates to occur within approximately **1–14 days after order placement**
- Preserved original ordering structure while correcting temporal inconsistencies

This step ensured the dataset better reflected realistic retail operations and allowed for more accurate time-based analysis (e.g., seasonality and retention patterns).

---

## Methodology

### 1. RFM Segmentation
Customers were segmented using:

- **Recency**: Time since last purchase
- **Frequency**: Number of purchases
- **Monetary Value**: Total customer spend / gross profit

Each customer was scored and grouped into tiers to identify behavioral patterns across the customer base.

---

### 2. Customer Retention Analysis
- Defined retention as repeat purchasing behavior
- Compared retained vs non-retained customer segments
- Analyzed behavioral differences across RFM tiers

---

### 3. Regional & Product Analysis
- Identified geographic distribution of customers and revenue concentration
- Evaluated top-performing product categories
- Analyzed purchasing behavior differences across customer segments

---

### 4. Seasonality Analysis
- Evaluated quarterly purchasing trends
- Identified peak demand periods (notably Q4)
- Assessed behavior differences across customer tiers

---

## Tools & Technologies

- **Python (pandas)** – data cleaning & preprocessing  
- **Tableau** – interactive dashboards & visualization  
- **Excel** – initial data inspection  
- **RFM modeling techniques** – customer segmentation logic  

---

## Key Insights

- A small percentage of customers contribute a disproportionate share of revenue (Pareto distribution)
- “First Tier” customers show significantly higher retention rates and purchase frequency
- Q4 represents the highest concentration of purchasing activity across all segments
- Product preferences remain relatively consistent across segments, with Chocolate category items driving the highest overall demand
- Geographic concentration of revenue is clustered in a small number of high-performing regions

---

## Tableau Dashboard

The full interactive visualization is available here:

[View Interactive Tableau Dashboard](https://public.tableau.com/views/CustomerProfilesandRetentionforaUSCandyDistributor/CustomerValueMappedbyPurchasingBehavior-USCandyDistributor?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)]

---

## Project Impact

This analysis demonstrates how transactional data can be transformed into actionable business intelligence by:

- Identifying high-value customer segments
- Supporting targeted retention strategies
- Highlighting regional and seasonal revenue drivers
- Enabling data-driven marketing and operational decisions

---

## Notes

This project was developed as part of a broader data analytics portfolio focused on customer behavior modeling, business intelligence, and applied data visualization.
