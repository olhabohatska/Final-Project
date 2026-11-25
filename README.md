# Customer Retention, Monetization, and Churn Risk Analysis in B2B SaaS

An end-to-end Business Intelligence and data analytics case study exploring revenue generation, seat utilization, customer activity, payment health, and churn drivers across **50,000 B2B SaaS customer accounts**.

## Executive Snapshot
* **Dataset:** 50,000 customer records and 18 features (`MP_Synthetics_50000_Rows.csv`)
* **Total MRR:** 33,267,908
* **Overall Churn Rate:** 1.83%
* **Churned MRR:** 396,040 (1.19% of total portfolio MRR)
* **Stack:** Python (`pandas`, `NumPy`, `Matplotlib`, `Seaborn`), Google Colab, GitHub

## Project Workflow
1. **Data Loading & Audit:** Loaded the raw dataset and verified structural integrity (50,000 rows, 18 columns, 0 missing values, 0 duplicate rows).
2. **Data Cleaning & Feature Engineering:**
   * Parsed `Signup_Date` and `Last_Active_Date` into `datetime64[ns]`.
   * Cleaned `Feature_Adoption_Rate` into numeric `Feature_Adoption_Rate_Num`.
   * Mapped `Churn_Risk_Score` (`Low`, `Medium`, `High`) into an ordered category (`Churn_Risk_Level`) and numeric scale (`Churn_Risk_Score_Num`).
   * Engineered `Seat_Utilization`, `Tenure_Days`, `Days_Since_Active`, and `Churned_MRR`.
3. **Business Questions (Q1–Q10):** Analyzed MRR and churn by billing cycle and plan tier, top countries and industries, company size segments, seat utilization, payment status and inactivity windows, account manager distribution, monthly signup trends, tenure cohorts, risk scoring with support load, and overall revenue at risk.
4. **Pivot Tables & Visualizations:** Built multi-dimensional summary pivot tables and five unified consulting-style charts (`Bar`, `Horizontal Bar`, `Line`, `Boxplot`, and `Heatmap`).
5. **Executive Summary & Recommendations:** Synthesized key findings into actionable retention, onboarding, payment recovery, and expansion recommendations.

## Key Findings & Recommendations
* **High-Value vs. High-Churn Segments:** `Enterprise` leads total MRR (~16.39M `Monthly` and ~8.82M `Annual`) with low churn (1.01%–1.36%), whereas `Starter` holds the largest customer count (30,008 accounts) and highest churn (2.24%–2.30%), alongside smaller company tiers (`1-10` and `11-50`).
* **Early Warning Signals:** `Failed` payments (14.49% churn), inactivity beyond 30 days (`31-90 days` and `90+ days` at 100.00% churn), and elevated `Churn_Risk_Level` (`Medium` at 37.00%, `High` at 64.71%, paired with higher 30-day support tickets and lower feature adoption) highlight clear intervention points.
* **Actionable Next Steps:** Automate pre-30-day re-engagement and payment recovery workflows, improve `Starter` onboarding and seat right-sizing, expand high-utilization (`90%+`) `Pro` and `Enterprise` accounts, and monitor `Churned_MRR` continuously.

## Repository Structure
* `B2B_saas_churn_BI_analysis.ipynb` — Full Google Colab analysis notebook with code, tables, charts, and documentation.
* `README.md` — Project overview and key takeaways.
