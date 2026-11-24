# AI-Powered Customer Intelligence & Revenue Optimization Platform
**Project Charter & Business Requirements**  
**Analyst:** Naman Roy  

---

## 1. Business Problem
E-commerce marketplaces generate massive transactional, logistics, and review datasets daily. However, without systematic analytical modeling, businesses struggle to identify top-tier customer lifetime value, combat high acquisition-to-churn drop-offs, and diagnose delivery friction points.

The primary objective of this project is to convert raw marketplace transaction logs into strategic intelligence through exploratory data analysis, SQL analytics, RFM customer segmentation, cohort retention tracking, predictive machine learning churn modeling, and an interactive executive web dashboard.

---

## 2. Business Objectives
- **Customer Segmentation:** Profile customers along Recency, Frequency, and Monetary (RFM) vectors using persistent individual identities (`customer_unique_id`).
- **Revenue Driver Analysis:** Uncover regional and categorical GMV concentration (e.g., São Paulo dominance).
- **Logistics & Satisfaction:** Quantify the statistical impact of delivery transit delays on customer review scores and repeat order propensity.
- **Predictive Churn Risk:** Engineer behavioral features to predict customer lapse probabilities before the point of no return.
- **Executive Visualizations:** Provide stakeholders with responsive, interactive dashboards for dynamic scenario filtering and KPI monitoring.

---

## 3. Core Business KPIs
- **Total Gross Merchandise Value (GMV):** R$ 15.42M
- **Delivered Order Volume:** 96,477 orders
- **Unique Customer Base:** 93,357 unique buyers
- **Average Order Value (AOV):** R$ 160.99
- **Repeat Buyer Ratio:** 3.2% (2,997 multi-order buyers)
- **On-Time Delivery Rate:** 93.2%
- **Average Review Rating:** 4.14 / 5.00 Stars
- **Customer Churn Rate (>180 Days Inactivity):** 59.8%

---

## 4. Analytical Tech Stack
- **Core Analytics & Modeling:** Python 3.13, Pandas, NumPy, Scikit-Learn
- **Relational Database:** SQLite (`olist.db`) with CTEs, Window Functions (`DENSE_RANK`), and aggregations
- **Data Visualization & Presentation:** Plotly.js, Matplotlib, Seaborn, HTML5 / CSS3 Responsive Dashboard
- **Machine Learning:** Random Forest Classifier (Stratified K-Fold / Train-Test Split, ROC-AUC Evaluation)
- **Version Control & Development:** Git, GitHub, Jupyter Notebook, VS Code
