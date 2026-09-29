# 📊 E-Commerce Customer Lifecycle & Operational Churn Analysis

## 📌 Executive Summary
An end-to-end data analytics project uncovering customer retention patterns, purchasing behaviors, and operational delivery bottlenecks across 100K+ real-world marketplace orders (Olist dataset). Using Google BigQuery SQL and Python, this analysis delivers an automated RFM segmentation model and actionable retention strategies to drive repeat purchases.

---

## 🎯 Business Problem & Objectives
- **The Challenge:** While customer acquisition is steady, repeat purchase rates remain low. The business lacked visibility into high-value customer segments and how fulfillment delays directly harm customer lifetime value.
- **Objectives:**
  1. Build a monthly Cohort Retention Matrix to measure true customer stickiness.
  2. Implement an automated RFM model to classify customers for targeted CRM campaigns.
  3. Quantify the operational threshold where delivery delays trigger negative reviews and churn.

---

## 🛠 Tech Stack & Repository Structure
- **Data Warehouse:** Google BigQuery (Standard SQL)
- **Techniques:** Window Functions (`NTILE`, `ROW_NUMBER`, `DENSE_RANK`), Multi-layer CTEs, Cohort Matrices
- **Exploratory Data Analysis & Viz:** Python (Pandas, Matplotlib, Seaborn)
- **Project Structure:**
  - `/sql`: Queries for data hygiene, cohort retention, and RFM scoring.
  - `/notebooks`: Statistical distributions, cohort heatmaps, and churn correlation models.
  - `/docs`: Business insights report and executive slide summary.

---

## 🔍 Key Findings
1. **Low Baseline Retention:** Overall 3-month retention stands at ~3.4%, signaling that the marketplace acts primarily as a transactional discovery platform rather than an ongoing ecosystem.
2. **The 80/20 Rule in Action:** The top 8% of customers (Champions segment) account for 31% of total gross merchandise value (GMV).
3. **The Shipping Tipping Point:** Orders delivered even 1 day past the estimated delivery date show an 84% drop in CSAT (1-star reviews surge from 4% to 58%), virtually eliminating repeat transaction likelihood.

---

## 💡 Strategic & Operational Recommendations
1. **Targeted Re-engagement for "At Risk":** Launch automated win-back discount campaigns specifically targeting customers in RFM buckets (R ≤ 2, F ≥ 3).
2. **Proactive Fulfillment Alerts:** Automate proactive compensation vouchers (e.g., free shipping on next purchase) the moment a shipment flags an unavoidable carrier delay, mitigating 1-star churn.
3. **VIP Loyalty Layer:** Establish dedicated customer support routing for the top RFM deciles to protect high-LTV revenue.

---

## 🚀 How to Replicate
1. Clone the repository.
2. Run SQL scripts in `/sql` against the Olist public dataset in BigQuery.
3. Execute `analysis_notebook.ipynb` to generate the cohort heatmap and visualizations.
