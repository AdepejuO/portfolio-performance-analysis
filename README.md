# Insurance Portfolio Performance Analysis
### Excel | Portfolio Performance Reporting 

An analysis of policy-level insurance information to understand insured value, portfolio composition, geographic concentration, and policy expiry patterns.

## 📊 Project at a Glance

| Area | Project Details |
| :--- | :--- |
| **Data Source** | `Insurance Policies Data.xlsx` (500 unique policy records) |
| **Tools** | Microsoft Excel (Workbook summary tables, charts, KPI reporting, and dashboard construction) |
| **Scope** | Policy value, geography, business type, construction type, expiry dates, and earthquake/flood risk indicators |
| **Portfolio Measures** | 500 policies &middot; $2,482,205,481 total recorded insured value &middot; 10 US states |
| **Reporting Audience** | Insurance portfolio, underwriting, risk management, and operational reporting teams |

---

## 1. Business Context & Purpose
Insurance portfolio reporting consolidates raw policy information to help leadership teams evaluate the value and mix of the insured book. Analysing geographic concentration, property characteristics, and upcoming expiries directly supports management reviews, resource planning, and renewal prioritization.

**The project structures a policy-level dataset into an operational report to answer:**
* Where is the overall insured value geographically concentrated?
* Which property and business categories account for the largest financial share?
* How are construction types distributed across the book?
* When are policies due to expire throughout the year?

---

## 2. Underlying Data & Reporting Structure
The source dataset contains one row per policy across ten distinct fields. The workbook contains dedicated reporting sheets (**Region**, **Business Type**, **Construction Type**, **Trend and KPI**, and a master **Dashboard** worksheet) built upon these core attributes:

* **Record Identifier:** `Policy` — Used to count unique policy records.
* **Time Field:** `Expiry` — Excel date field used for month-by-month expiry reporting.
* **Financial Measure:** `InsuredValue` — Recorded value, aggregated as a financial sum.
* **Segmentation:** `Region`, `State`, `Location`, `BusinessType`, `Construction`.
* **Risk Indicators:** `Earthquake` and `Flood` — Y/N flags representing geographic risk characteristics.

---

## 3. Analytical Approach & Excel Techniques

### Data Preparation & Validation
The analysis begins by establishing a structured policy table with consistent fields. The metrics reconcile policy counts and sums of insured value across all tables to confirm that the 500 records are distinct, populated, and fully balanced against the master portfolio total.

### Segment Aggregation & Calculations
The portfolio is aggregated by volume (policy count) and financial exposure (`SUM` of insured values). Segment shares are calculated by dividing segment totals by the overall portfolio metrics. Equivalent logic for these workbook summaries includes standard conditional statistical functions:
* `COUNTIF` / `COUNTIFS` — For evaluating policy volume and multi-criteria risk counts.
* `SUMIF` / `SUMIFS` — For isolating financial exposure by specific categories or regions.

### Management Information Delivery
The dashboard streamlines the path from high-level portfolio KPIs to granular segment tables. The primary horizontal distributions below illustrate the core financial concentrations identified in the workbook:

* **Insured Value by Region:** Highlights a heavy concentration in a single geographical area.
* **Five Largest Business Types:** Isolates the top property sectors driving total exposure.

---

## 4. Key Findings & Interpretation

* 📍 **Geographical Concentration:** The **East region** holds $1,826,021,818 in insured value, accounting for **73.6%** of the entire portfolio across 337 policies.
* 🏢 **Business Mix:** **Apartment** properties represent the single largest concentration at $1,158,549,996 (**46.7%** of total value), followed by **Office Buildings** at $619,820,056.
* 🏗️ **Construction Profile:** **Frame construction** is utilized in 322 out of 500 policies (**64.4%**), representing the dominant property type in the book.
* 🌆 **Urban vs. Rural:** **81.0%** of the portfolio (405 policies) is classified as urban.
* ⚠️ **Risk Indicators:** 256 policies carry an active **Earthquake flag (Y)** and 249 carry a **Flood flag (Y)**. 

> 💡 **Note on Data Interpretation:** These risk flags represent baseline environmental exposure characteristics. They do not represent claim history, financial loss records, or active incident probabilities.

---

## 5. Policy Expiry & Renewal Planning
All recorded policy expiries in this baseline dataset take place within the 2021 calendar year. Grouping the dates by month maps the upcoming operational workload for renewal teams:

* **Peak Volume:** **December** represents the highest renewal volume with 92 expiring policies, closely followed by **November** with 70.
* **Low Volume:** **July** represents the lowest operational period with 0 expirations, followed by **August** with 9.

This timeline allows managers to balance underwriting capacity ahead of peak expiration cycles.

---

## 6. Data Quality & Reporting Controls
Maintaining reliable management information depends on clear reconciliation paths back to the underlying data grain. 

* **Population Auditing:** The workbook validates that summary metrics cleanly account for all 500 distinct policies, 10 states, and the complete $2,482,205,481 portfolio value.
* **Filter Awareness & Variance:** Users should note that specific sheets isolate sub-populations. For example, the `Business Type` sheet focuses on the top five named categories (totalling $2,292,495,761) rather than all thirteen categories available in the master table ($2,482,205,481). Discrepancies like this highlight the importance of verifying denominators across reports.
* **Data Integrity Checks:** Best practices implemented include auditing for duplicate policy IDs, checking date boundaries, standardizing text labels, and enforcing uniform `Y/N` boolean flags.

---

## 7. Skills & Competencies Demonstrated
* **Data Preparation & Validation:** Verifying record completeness, identifying unique grains, and executing multi-tier metric reconciliations.
* **Excel Portfolio Analysis:** Developing segment-level aggregations, KPI summaries, and categorical distribution matrixes.
* **Performance Reporting:** Structuring policy volumes, financial exposures, category percentage shares, and time-series expiry patterns.
* **Data Visualisation:** Designing intuitive chart models and dashboard layouts optimized for leadership review.
* **Commercial Insight:** Translating raw insurance tables into actionable observations regarding risk concentration and operational peak periods.

---

## 8. Project Files & Reference Sources
* 📁 **Source Workbook:** `Insurance Policies Data.xlsx` (Contains data, dashboards, and segment worksheets)
* 📊 **Reconciliation Sheets:** Dedicated tabs for Region, Business Type, Construction Type, and Trend Analysis.
