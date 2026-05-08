# Energy Reliability Case Study

## Problem Statement
Energy providers experience recurring outages, but it is unclear which providers and failure types contribute most to system-wide losses.

---

## Objective
Identify key drivers of energy outages and quantify the providers responsible for the highest operational risk.

---

## Tools Used
- SQL (CTEs, CASE statements, window functions)
- Python (data processing in Jupyter Notebook)
- Tableau (dashboard visualization)

---

## Methodology

- Analyzed 1,500+ outage events across 18 utility providers
- Standardized outage duration using JULIANDAY calculations
- Categorized providers based on frequency and duration of outages
- Aggregated risk exposure across providers and time periods

---

## Key Findings

- 23% year-over-year increase in forced outages
- 34% of total energy loss driven by unplanned disruptions
- Top 3 providers accounted for 47% of all outage-related losses
- Certain facilities consistently exceeded 1.5-day average downtime thresholds

---

## Business Insight

Results suggest that targeted infrastructure improvements at a small subset of providers could significantly reduce system-wide reliability issues.

---

## Output

- Tableau dashboard included in repository
- SQL analysis scripts available in notebook
