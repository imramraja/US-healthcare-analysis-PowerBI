# U.S. Healthcare Industry Dynamics (2019–2020)

## Table of Contents

[Project Overview](#project-overview) •
[Key Features](#key-features) •
[Highlights](#highlights) •
[Insights](#insights) •
[ER Diagram](#er-diagram) •
[Live Dashboard](#live-dashboard) •
[Conclusion](#conclusion)

---

## Project Overview

This project delivers a metric-driven analysis of U.S. healthcare operational and financial data across 2019–2020. The objective was to engineer a structured analytical system capable of measuring hospital performance, patient cost behavior, provider-level revenue concentration, and expense volatility under a consistent relational framework.

Rather than producing a descriptive report, the implementation focuses on building a performance monitoring layer on top of transactional healthcare datasets. Metrics are modeled to answer operational questions around throughput balance, financial dependency, cost concentration, and structural expense patterns.

The resulting dashboard operates as a decision-support interface backed by a formally defined data model and defensible KPI logic.

---

## Key Features

- **Star-Schema Data Modeling**  
  Designed and implemented a relational model separating fact tables (admissions, expenses, provider transactions) from conformed dimension tables (hospital, patient, provider, calendar). Relationships were defined to preserve one-to-many integrity and prevent aggregation anomalies.

- **Advanced DAX Metric Engineering**  
  Constructed calculated measures using DAX to handle:
  - Context-aware admission-to-discharge ratios  
  - Segment-level cost averages  
  - Revenue distribution and concentration metrics  
  - Time-intelligence calculations (MoM, YoY variance)  
  - Dynamic KPI recalculations under slicer context  

- **Filter Context Control & Model Integrity**  
  Designed measures to behave predictably across cross-filter interactions, avoiding double counting and context leakage.

- **Functional Dashboard Segmentation**  
  Structured report pages by business domain: operations, patient analytics, financial distribution, and expense monitoring to align visualization with functional responsibility areas.

---

## Highlights

- **Executive Summary Layer**  
  Centralized KPI board consolidating admission flow, discharge alignment, revenue metrics, and expense aggregates to provide immediate macro-level system visibility.

- **Operational Flow Assessment**  
  Evaluated hospital throughput efficiency by comparing admission volume against discharge completion trends to detect utilization imbalance and operational variance.

- **Cost Segmentation & Treatment Analytics**  
  Analyzed cost allocation across demographic and treatment categories to identify concentration and variability patterns within patient cohorts.

- **Provider Revenue Concentration Analysis**  
  Quantified financial distribution across providers to evaluate revenue dependency and identify disproportionate exposure.

- **Expense Volatility & Structural Trend Monitoring**  
  Modeled monthly expense aggregation to detect recurring patterns, cyclical behavior, and structural cost shifts rather than isolated deviations.

- **Formal Data Architecture (ER Model)**  
  Implemented a controlled relational schema to ensure metric reproducibility and eliminate ambiguity in aggregation logic.

---

## Insights

| Executive Summary | Hospital Insights |
|-------------|-------------|
| ![executive_summary](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/executive_summary.jpg) | ![hospital_insights](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/hospital_insights.jpg) |
| System-wide activity shows measurable shifts in admission volume and cost distribution across the two-year window, indicating structural rather than random variance. | Facility-level comparison highlights variability in discharge alignment and operational throughput efficiency. |

---

| Patient Outcome Analysis | Healthcare Provider Metrics |
|-------------|-------------|
| ![patient_outcome_analysis](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/patient_outcome_analysis.jpg) | ![healthcare_provider_metrics](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/healthcare_provider_metrics.jpg) |
| Treatment distribution and demographic segmentation reveal cost concentration patterns that differ across patient categories. | Revenue mapping shows financial concentration across select providers, highlighting dependency risk and performance imbalance. |

---

| Monthly Expenses Trends | 
|--------------------------|
| ![monthly_expenses_trends](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/monthly_expenses_trends.jpg) | 
| Expense analysis demonstrates recurring monthly volatility patterns, indicating structured cost cycles rather than isolated anomalies. |

---

## ER Diagram

Below is the Entity Relationship Diagram representing the underlying analytical model:

![ER_Diagram](https://github.com/imramraja/1.US-healthcare-analysis-PowerBI/blob/main/assets/er_diagram.png)

The model follows a controlled star-schema design:

- Fact tables capturing transactional healthcare activity  
- Dimension tables standardizing hospital, provider, patient, and calendar attributes  
- Explicit one-to-many relationships ensuring deterministic aggregation  
- Time dimension enabling consistent period-over-period evaluation  

This modeling approach ensures:

- Deterministic KPI computation  
- Stable filter propagation  
- Elimination of ambiguous joins  
- Scalability for additional analytical layers  

---

## Live Dashboard

Interactive Power BI Report:

🔗 https://app.powerbi.com/links/x_BEXo8_4A?ctid=a2e8c89e-7534-4ccf-b1fa-00c12005cb9d&pbi_source=linkShare&bookmarkGuid=ef4fde42-5ed7-4a3a-b773-200d74946dec

---

## Conclusion

This implementation reflects applied analytical engineering rather than dashboard assembly. The project demonstrates:

- Formal relational modeling  
- Context-aware DAX metric construction  
- Controlled aggregation logic  
- Functional dashboard segmentation aligned with business domains  

The output is a performance monitoring framework capable of supporting structured healthcare operational and financial evaluation under consistent metric governance.
