# edufin-portfolio-health-analysis
# EduFin Loan Portfolio Health Analysis 📊💼

## 📌 Project Overview
This project contains a comprehensive portfolio risk investigation for **EduFin**, an educational fintech lender experiencing a sudden portfolio-wide quality crisis[cite: 2]. Using **Databricks SQL**, this analysis translates raw operational loan data into executive-level financial insights, establishing a definitive baseline of risk exposure and automating health classification metrics to guide strategic C-suite decision-making[cite: 2].

The core investigation was completed as part of the **"Portfolio Investigation with Databricks"** bootcamp led by **Viresh Gendle**.

---

## 🏢 Business Objective & Problem Statement
Management and board members at EduFin became aware of an emerging credit crisis but lacked quantified visibility into its scale and depth[cite: 2]. The goal of this analysis is to answer critical macro-level financial questions[cite: 2]:
1. **Distribution:** Is the issue localized to specific cohorts or is it a portfolio-wide systemic crisis?
2. **Scale:** What is the actual monetary scale of operations, and does a known ₹12 Cr discrepancy pose an existential threat to company liquidity?
3. **Portfolio at Risk (PAR):** How much capital is currently locked up in actual defaults vs. early-stage payment stress pipelines?
4. **Classification:** What is the automated risk classification of the portfolio based on credit thresholds?

---

## 📊 Core Data Scale Metrics
The analysis was performed on a dataset containing **5,000 active and historical loan records** mapping back to **3,000 unique customers**:
* **Total Portfolio Value:** `₹204.82 Crores`
* **Average Loan Ticket Size:** `₹4.10 Lakhs`

---

## 🔍 Investigation Breakdown & Queries

### 1. Portfolio Status Distribution (Query 1A)
Establishes the structural baseline by breaking down loan frequencies and percentages across all recorded statuses.
* **Insight:** The combined volume of distressed loans significantly exceeded acceptable tolerances, proving the issue is systemic rather than localized.

### 2. Operational & Value Scale (Query 1B)
Determines operational scale in Crores and Lakhs to contextualize the severity of outstanding capital stress.
* **Insight:** Shows that the average loan size is moderate, meaning the crisis is driven by high-frequency failures across the entire portfolio rather than single-customer concentration risk.

### 3. Credit Risk & Forward Pipeline Metrics (Query 1C)
Calculates actual Default Percentages and Portfolio-at-Risk (PAR) rates to model future default migrations.
* **Insight:** Outlined a heavy pipeline of overdue accounts poised to slide into immediate default without swift collections intervention.

### 4. Financial Impact Conversion (Query 1D)
Translates operational loan counts into real financial impact, quantifying exactly how many Crores are locked in non-performing assets.
* **Insight:** Discovered that **₹35.18 Crores** of capital is actively exposed to stress, representing a massive **17.18%** of total business assets.

### 5. Automated Executive Dashboard (Query 1E)
Consolidates all metrics into a single-row, executive-ready view utilizing programmatic `CASE WHEN` logic to output an automated company health status (`HEALTHY` / `MODERATE RISK` / `HIGH RISK` / `CRITICAL`) based on asset quality.

---

## 📈 Key Findings & Executive Summary

| Loan Status | Loan Count | Count % | Financial Value (Cr) | Portfolio Value % | Risk Category |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Active** | 3,965 | 79.30% | ₹162.41 Cr | 79.29% | Healthy |
| **Defaulted** | 590 | 11.80% | ₹24.24 Cr | 11.83% | At Risk (Capital Loss) |
| **Overdue** | 273 | 5.46% | ₹10.94 Cr | 5.34% | At Risk (Pipeline Stress) |
| **Closed** | 172 | 3.44% | ₹7.24 Cr | 3.53% | Healthy |

* **Automated Portfolio Health Classification:** `HIGH RISK`
* **Portfolio-at-Risk (PAR) Rate:** **17.26%** (Combined Defaulted + Overdue)

### 🚨 Strategic Recommendations for Leadership
1. **Immediate Credit Freeze/Tightening:** Instantly adjust underwriting criteria and tighten credit scoring algorithms for applicant segments reflecting high default profiles.
2. **Accelerated Collection Taskforce:** Deploy dedicated recovery teams specifically targeting the **₹10.94 Crores** sitting in the volatile `Overdue` bracket to prevent imminent migration into hard defaults.
3. **Capital Adequacy Review:** Inform risk committees of the active **11.80%** capital write-off rate to evaluate current provision reserves against overall liquidity requirements.

---

## 🛠️ Repository Files & Structure
* **`Portfolio Health.ipynb`**: The exported Jupyter notebook containing the interactive analytical narrative, data validation checkpoints, and full production-ready SQL scripts executed in Databricks[cite: 2].
* **`Portfolio Health.dbc`**: The native Databricks Archive file containing the original platform-ready source code, formatting, and dashboard metadata[cite: 1].
* **`loans.csv`**: The underlying portfolio dataset utilized throughout the analytics lifecycle.

---

## 🚀 Technical Skills Demonstrated
* **Databricks Environment Optimization:** Managing multi-cell script notebooks, leveraging platform native visualizations, and structuring enterprise SQL pipelines[cite: 2].
* **Advanced Databricks SQL:** Utilizing window functions (`SUM() OVER ()`), conditional aggregations (`COUNT(CASE WHEN...)`), and dynamic risk banding expressions.
* **Risk Analytics & Financial Modeling:** Programmatically calculating Portfolio-at-Risk (PAR) metrics, asset health trends, and micro/macro scale exposure ratios.

---
*Special thanks to **Viresh Gendle** for providing the architectural frameworks, guidance, and domain knowledge required to execute this fintech investigation.*
