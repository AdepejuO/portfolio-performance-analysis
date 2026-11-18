``# INSURANCE PORTFOLIO PERFORMANCE ANALYSIS

Excel-based analysis of policy distribution, insured exposure, coverage indicators, premiums and paid losses for 2021 Policy Dataset

## 1 | Business context and analytical objective

This project examines a 500-policy insurance dataset to show where insured value is concentrated, how the portfolio is distributed, coverage indicators, and how collected premiums compare with recorded paid losses. The aim is to turn policy-level information into clear management reporting that can support portfolio performance monitoring.

## 2 | Project at a Glance

| Area | Project overview |
| :--- | :--- |
| **Business focus** | Insurance portfolio performance, insured-value exposure, coverage distribution, claims experience and policy expiry analysis. |
| **Tools** | Microsoft Excel – Excel Tables, formulas, PivotTables, Pivot Charts, calculated fields and dashboard reporting. |
| **Data structure** | 500 insurance policy records containing insured values, premiums, losses paid, business types, construction types, geographical regions, policy expiry dates, and flood and earthquake coverage indicators. |
| **Key metrics and KPIs** | Policy count, total insured value, total premiums, total losses paid, paid-loss ratio, coverage distribution and exposure concentration. |
| **Currency** | Pound sterling (GBP, £) – all financial values, including insured values, premiums and losses paid, are reported in pounds. |
| **Reporting scope** | Analysis of 500 policies, including regional and business-type comparisons, coverage combinations, financial performance and historical policy expiry patterns. |
| **Analysis Period** | 2021 (January–December) – analysis of 500 insurance policies with expiry dates within the 2021 calendar year. |
| **Output** | Interactive Excel dashboard with Pivot Table summaries, charts and KPI reporting to support portfolio monitoring, risk assessment and management decision-making. |

## 3 | Business questions

| Question | Analytical output |
| :--- | :--- |
| Where is the insured exposure concentrated? | Policy count and insured value by region, state and location. |
| Which types of business and construction account for the largest exposure? | Exposure distribution by business type, construction and combined category. |
| How are earthquake and flood indicators distributed? | Counts and insured values for both, either or neither indicator. |
| How do premium and paid-loss results compare across groups? | Premium, paid losses and portfolio paid-loss ratio, segmented by region or construction. |
| When do policies expire? | Monthly policy counts for the 2021 expiry period. |
| Which individual policies warrant closer review? | Largest insured values and unusually high individual paid-loss ratios. |

## 4 | Metrics and KPIs

| Measure | Definition / interpretation | Recorded value |
| :--- | :--- | :--- |
| **Policy count** | Distinct policy identifiers in the source table. | 500 |
| **Total insured value** | Sum of Insured Value; a measure of stated exposure, not claim cost. | 2,482,205,481 |
| **Average insured value** | Total insured value ÷ 500 policies. | 4,964,411 |
| **Premium** | Sum of recorded premium across policies. | 11,315,760.90 |
| **Paid loss** | Sum of populated Loss Paid amounts; blanks are not independently verified as zero. | 7,249,785.94 |
| **Portfolio paid-loss ratio** | Sum of recorded paid losses ÷ sum of premium (not the mean policy ratio). | 64.07% |
| **Coverage distribution** | Share of policy count or insured value by coverage category. | See section 6 |
| **Top 10 exposure share** | Sum of the ten largest policy insured values ÷ total portfolio insured value. | 14.0% (£347.4m) |
| **Expiry trend** | Monthly count of policy expiry dates in 2021. | December: 92 policies |

## 5 | Data sources, structure and preparation

The source is an Excel table containing one row per policy and fields for policy identifier, expiry date, location, state, reporting region, insured value, construction, business type, earthquake indicator, flood indicator, premium and loss paid. The workbook includes supporting analysis tabs for region, coverage, business type, construction, expiry trends and KPIs.

Three calculated columns extend the source table: Loss Ratio (paid loss ÷ premium), Exposure Combination (business type joined to construction) and Coverage Category (both, earthquake only, flood only or neither). This creates consistent reporting groups without changing the underlying policy records.

### Excel methods demonstrated

| Technique / function | Purpose |
| :--- | :--- |
| **Excel Table and structured references** | Keep formulas linked to policy-level columns and support summaries. |
| **IF and AND** | Classify the two Y/N coverage indicators into mutually exclusive groups. |
| **Text concatenation (&)** | Combine business type and construction for exposure comparisons. |
| **Division** | Calculate policy-level paid-loss-to-premium ratios. |
| **PivotTables / distinct count** | Summarise policy count, insured value, premium, loss paid and distinct states. |
| **GETPIVOTDATA** | Pull PivotTable summary values into KPI and coverage reporting areas. |
| **PivotCharts and dashboard charts** | Present regional, coverage, construction and expiry patterns visually. |

## 6 | Analysis and Findings

### Exposure by region

The East region accounts for approximately 73.6% of total insured value, indicating high concentration in one reporting region. The remaining values are 18.9% Midwest, 5.6% Northeast and 2.0% Central.

<img width="269" height="144" alt="Exposure By Region" src="https://github.com/user-attachments/assets/c7d41c2b-6aa2-4d54-a67d-139d793dfed8" />


### Coverage mix and concentration

The coverage combination chart compares four mutually exclusive groups: both flood and earthquake, earthquake only, flood only, and neither. Comparing policy counts with total insured value shows where exposure is concentrated, rather than relying on policy volume alone.

**Key finding — coverage combination.** Although 47% of policies (235 of 500) have both flood and earthquake coverage indicators, they account for approximately 73.6% of the portfolio’s total insured value. In contrast, 46% of policies (230 of 500) have neither indicator and account for 21.6% of insured value.

**Management implication.** Higher-value policies are disproportionately represented in the group with both coverage types. This makes the combined-coverage segment particularly important when reviewing insured-value concentration and potential exposure. Management can use the breakdown to prioritise further analysis by location, construction type and business category.

<img width="305" height="146" alt="Coverage Combination" src="https://github.com/user-attachments/assets/2c1cfaa2-9318-4c80-b351-d2a47e12d72b" />

### Premium and Loss Comparisons

The overall paid-loss ratio is 64.1%. Regional comparisons show material differences: approximately 60.3% East, 45.1% Midwest, 6.5% Central and 201.3% Northeast. The Northeast result indicates recorded paid losses exceeding premium within that group; which indicates a need for further investigation.

### Top 10 Policy Exposures

**Key finding.** The ten largest policies have a combined insured value of £347.4 million, accounting for approximately 14.0% of the £2.48 billion portfolio. The largest individual policy, Policy 100275 in Wisconsin, has an insured value of approximately £53.4 million.

<img width="326" height="164" alt="Top 10 Exposures" src="https://github.com/user-attachments/assets/03e74a2a-60a0-4955-b1b9-fc573dd341dd" />

**Management implication.** Individual high-value policies contribute materially to total portfolio exposure. A relatively small number of policies therefore warrant closer examination alongside the wider regional and coverage concentration analysis.

### Policy Expiry

December has the highest recorded count (92), followed by November (70). KPI cards at the top of a dashboard allow users to read portfolio totals before exploring the breakdowns.

<img width="268" height="145" alt="Policy Expiry" src="https://github.com/user-attachments/assets/fc6067ce-7348-4823-9f2d-cf1048e47c28" />


## 7 | How the analysis answered the business questions

| Business question | What the analysis established | Potential management use |
| :--- | :--- | :--- |
| **Exposure concentration** | East has 73.6% of insured value; apartment and frame categories also dominate. | Monitor exposure and review the balance of the portfolio. |
| **Coverage distribution** | 47% of policies have both flood and earthquake cover and represent 73.6% of the total insured value. While 46% of policies have neither but account for 21.6% of insured value. Implication is that Higher-value policies are disproportionately represented with both coverage types. | Investigate the concentration of higher insured values among policies with both coverage indicators. |
| **Premium and paid losses** | Overall paid-loss ratio is 64.1%, with strong regional variation. | Select regions and policies for further loss-data and underwriting review. |
| **Expiry distribution** | December has 92 historical 2021 expiries. | Use the understanding of expiry distribution to support renewal planning. |
| **Large individual exposures** | The ten largest policies account for £347.4m (14.0%) of insured value. Policy 100275 in Wisconsin is largest at £53.4m. | Review underwriting limits, risk characteristics and geographical concentration of large individual exposures, particularly where several high-value exposures occur in the same area or share similar construction or coverage characteristics. |

## 8 | Data quality assurance and validation

| Test | Approach | Excel Method | Documented result |
| :--- | :--- | :--- | :--- |
| **Uniqueness** | Compare total rows with distinct policy IDs; investigate repeated IDs before counting policies. | Validated primary key uniqueness by comparing total rows against distinct Policy IDs using `COUNT` and `COUNT(UNIQUE(...))` | 500 rows and 500 unique policy identifiers. |
| **Completeness** | Check policy ID, premium, insured value, region and flood/earthquake fields for blanks. | Count blank cells (e.g. Insured Value and Premium) using `COUNTBLANK` or `COUNTIF`. | No blanks reported in those fields. |
| **Completeness (Group Totals)** | Sum group counts and compare with the portfolio count of 500. | Used Pivot summaries | Regions: 337 East + 108 Midwest + 34 Northeast + 21 Central = 500. Coverage groups: 235 both + 230 neither + 21 earthquake only + 14 flood only = 500. |
| **Consistency** | Recalculate sums from the policy table; compare with PivotTable and KPI outputs. | Used Pivot summaries | Insured value £2,482,205,481; premium £11,315,760.90; populated paid losses £7,249,785.94. |
| **Validity** | Review negative or unusual insured values and premiums | Use `COUNTIF` to flag insured values or premiums `<= 0` | There were no negative or unusual values |
| **Validity (Date Range)** | Confirm Expiry column contain valid dates, and all records fall between 1 Jan and 31 Dec 2021 | Used The `MIN` and `MAX` formula to determine the earliest and latest dates. | The date was between 02/01/2021 and 31/12/2021 |

## 9 | Skills and competencies demonstrated

* Data preparation and calculated fields
* Excel structured tables
* `IF`/`AND` logic
* PivotTables and Pivot Charts
* KPI definition and aggregation
* Distinct-count and reconciliation checks
* Segmented portfolio analysis
* Clear visual selection

### Project materials

* **Project file:** `Insurance Policies Data 2.1.xlsx`
