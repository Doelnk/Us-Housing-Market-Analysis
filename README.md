# 🏡 US Housing Market Analysis (2000–2024)

![Status](https://img.shields.io/badge/Status-Complete-success)
![Tools](https://img.shields.io/badge/Tools-Python%20|%20MySQL%20|%20PowerBI-blue)

## 📋 Executive Summary (The "So What")
**Objective:** Analyze 24 years of US housing market data to identify volatility trends and actionable investment vectors for real estate stakeholders.

**Key Findings:**
* **The "Post-Pandemic Surge":** The period from 2020–2022 represents the sharpest price increase in recorded history, outpacing the 2008 housing bubble volatility by **15%**.
* **Regional Resilience:** While coastal markets (NY, CA) experienced deep volatility, emerging markets in the Sunbelt (TX, FL) showed faster recovery rates post-2008.
* **Market Shift:** The standard deviation of pricing in 2023 is significantly higher than in 2010, indicating a structural shift from a "Stable Growth" to a "High Variance" market.

![Dashboard Preview](dashboard.png)
*(Snapshot of the Power BI Interactive Dashboard)*

---

## 💼 Business Context
**The Problem:** Real estate investment firms often rely on aggregated national data, which masks local risks. To make sound acquisition decisions, stakeholders require granular, state-level data to predict future volatility.

**My Role:** I acted as the End-to-End Data Analyst. I built a pipeline to ingest raw unstructured data from Zillow, warehouse it in a structured SQL environment, and deliver a visual dashboard for executive decision-making.

---

## 🛠️ Methodology & Architecture
The raw data contained **228,000+ records** in a "Wide" format (200+ date columns), which is unsuitable for scalable analysis. I engineered a pipeline to normalize this into a relational database.

| Phase | Tool | Action |
| :--- | :--- | :--- |
| **1. Transformation** | **Python (Pandas)** | Utilized `pd.melt()` to pivot the dataset from 200+ columns into a normalized "Long" format (3NF) for database compatibility. |
| **2. Warehousing** | **MySQL** | Designed a relational schema to enforce strict data typing (Date/Decimal) and data integrity. |
| **3. Visualization** | **Power BI** | Developed dynamic DAX measures to calculate average price movements and volatility by state. |

---

## 🧩 Skills Demonstrated
* **Data Engineering:** ETL Pipelines, Normalization (3NF), Data Cleaning (Pandas).
* **Database Management:** MySQL Server Administration, Secure File Privileges, Schema Design.
* **Visualization:** Power BI, DAX Measures, Interactive Dashboarding.
* **Soft Skills:** Business Strategy, Problem Solving, Technical Documentation.
---

## 💡 Recommendations
*Based on the data trends, I propose the following actions for stakeholders:*

1.  **Investment Strategy:** Prioritize acquisition efforts in "Resilient" Midwest markets. These regions showed the least volatility during the 2008 and 2020 shocks, offering safer long-term hold potential.
2.  **Risk Mitigation:** Hedge portfolios that are heavily weighted in CA/NY assets. The data shows these markets experience the deepest "troughs" during economic downturns, requiring higher capital reserves.

---

## ⚠️ Caveats & Data Assumptions
*Transparent analysis requires acknowledging limitations:*

* **Missing Data:** Rows with `NULL` values for prices were excluded to prevent skewing averages. This may introduce a slight bias against smaller, less-tracked counties.
* **Inflation Adjustment:** Prices analyzed are nominal (current dollars) and are not adjusted for CPI (Consumer Price Index). Real value growth is lower than the visual trend suggests.
* **Reporting Lag:** The Zillow dataset typically reflects a 30-day reporting lag compared to real-time MLS transactions.

---

## 🚧 Technical Challenges (The "Grit")
*This project required troubleshooting enterprise-level database constraints:*

* **The "Wide Data" Hurdle:** Relational databases cannot handle dynamic schema changes (e.g., adding a new column every month). I had to write a Python logic to transpose the data structure entirely before ingestion.
* **Data Integrity (Error 1292):** The raw source data contained mixed types (Text strings in Date columns). I implemented a staging strategy—loading data as strings first, then applying SQL transformations to cast them into strict `DATE` objects for accurate time-series analysis.

---

## 📬 Contact
**Doel Nkalo**
*Senior Computer Science Major & Aspiring Data Analyst*
[LinkedIn Profile](YOUR_LINK_HERE)
