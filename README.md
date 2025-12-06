# Corporate Expense Fraud Detection System 🕵️‍♂️📊

**Portfolio Project: Forensic Data Analytics**

## 📖 Executive Summary
This project simulates a forensic audit of corporate procurement data to identify fraud, waste, and abuse. Using a **Rule-Based Detection Engine** and **Statistical Modeling**, I built a system that autonomously flags high-risk transactions.

**Key Results:**
* **Structuring Detected:** Identified "Split Payments" used to bypass approval limits.
* **Conflict of Interest:** Caught "Ghost Vendors" via address matching algorithms.
* **Statistical Anomalies:** Implemented **Benford's Law** to catch unnatural expense reporting.
* **Risk Scoring:** Developed a weighted scoring model (0-100) to prioritize audits for the CFO.

## 🛠️ Tech Stack
* **Python:** Pandas, NumPy (Data Processing), Faker (Synthetic Data Generation).
* **SQL (SQLite):** Complex Window Functions (`LAG`, `LEAD`), Joins, CTEs.
* **Forensic Math:** Benford's Law Analysis, Haversine Formula (Geospatial Distance).
* **Visualization:** Matplotlib, Seaborn.

## 🔍 The Investigation Pipeline

### 1. Data Simulation
Generated a synthetic dataset of **50 Employees, 100 Vendors, and 1,000+ Transactions** with specific fraud patterns injected (Ground Truth).

### 2. SQL "Red Flag" Analysis
* **Split Payments:** Used SQL Window Functions to find identical payments < 24 hours apart.
* **Weekend Spend:** Filtered for high-value transactions processed on Saturdays/Sundays.

### 3. Statistical & Geospatial Analysis
* **Benford's Law:** Analyzed leading digit distribution to find unnatural number patterns.
* **Geospatial Risk:** Calculated Haversine distance to flag vendors located <2km from employees.

### 4. The Risk Scoring Engine
Aggregated all findings into a composite **Risk Score**.
* Ghost Vendor: +100 pts
* Split Payment: +40 pts
* Weekend Spend: +20 pts

## 📊 Executive Dashboard
*(Note: Upload your dashboard screenshot here)*
The final output is a prioritized "Hit List" of employees requiring immediate audit.

## 🚀 How to Run
1.  Install dependencies: `pip install -r requirements.txt`
2.  Run the Jupyter Notebook to generate data and perform the audit.