# 🛒 AI-Powered Customer Intelligence & Revenue Optimization Platform

> **End-to-end data analytics project** transforming raw e-commerce data into
> actionable business intelligence — from SQL queries to machine learning to
> an interactive executive dashboard.

**Dataset:** Brazilian Olist E-Commerce (100k+ real orders, 2016–2018)  
**Tools:** Python · SQL · Machine Learning · Plotly · Git

---

## 📖 The Story Behind This Project

When I first loaded the Olist dataset, the numbers looked healthy on the
surface — R$ 15.4 million in revenue, 96,000+ orders delivered. But when
I dug deeper, something stood out immediately.

**The total orders and total unique customers were almost identical.**

That means nearly every customer bought once and never came back. For a
growing marketplace, that's not just a retention problem — it's an
existential one. This project became my attempt to understand exactly why
that's happening, who the most valuable customers are, and what the
business can do about it.

---

## 🔍 Key Findings

---

## 📸 Project Showcase

### 🖥️ Executive Summary Dashboard
![Executive Summary](11_Screenshots/04_PowerBI/page1_executive_summary.png) 

---

### 🧠 Customer Intelligence Dashboard
![Customer Intelligence](11_Screenshots/04_PowerBI/page2_customer_intelligence.png)

---

### 🛍️ Product & Sales Dashboard
![Product & Sales](11_Screenshots/04_PowerBI/page3_product_sales.png)

---

### 🚚 Delivery & Operations Dashboard
![Delivery & Operations](11_Screenshots/04_PowerBI/page4_delivery_operations.png)

---

### 🎯 RFM Customer Segmentation
![RFM Segments](11_Screenshots/02_Python/rfm_segments.png)

---

### 🤖 Churn Prediction — Feature Importance
![Churn Feature Importance](11_Screenshots/03_Machine_Learning/churn_feature_importance.png)

---

### 📈 EDA — Monthly Revenue Trend
![Monthly Revenue](11_Screenshots/02_Python/eda_states.png)

---

**Five things that stood out from the data:**

- São Paulo alone drives **~40% of total revenue** across 26 states —
  the geographic concentration is striking and shapes every strategic decision

- **Cohort retention drops to near-zero after month 1** — and this pattern
  holds across every single cohort going back two years, confirming it's
  structural, not seasonal

- **Champions segment has 15× higher CLV** than Lost customers — a small
  group of power buyers is carrying a disproportionate share of revenue

- **Recency is the #1 churn predictor** — customers who haven't purchased
  recently are almost certainly gone, and the model confirms it with high
  confidence

- **Late deliveries and 1-star reviews are directly correlated** — Bahia,
  Pernambuco and Ceará have the worst delivery times and the worst review
  scores in the entire dataset

---

## 🏗️ Project Architecture

```
Phase 1  →  Data Cleaning          Clean 7 raw datasets for analysis
Phase 2  →  SQL Analytics          Answer 8 business questions using SQL
Phase 3  →  Feature Engineering    Build delivery, revenue & customer features
Phase 4  →  Exploratory Analysis   Visualize patterns with business context
Phase 5  →  Customer Intelligence  RFM segmentation + CLV + Cohort analysis
Phase 6  →  Churn Prediction       ML model to identify at-risk customers
Phase 7  →  Interactive Dashboard  4-page dashboard with live filters
Phase 8  →  Recommendations        5 data-driven business actions
```

---

## 📊 What Was Built

### Data Cleaning
Cleaned all 7 Olist tables — handled missing delivery dates (business
decision: kept them since they belong to cancelled orders), removed
duplicates, converted date columns, and exported clean CSVs for
downstream analysis.

### SQL Analytics
Built a SQLite database and wrote 8 business-focused queries covering
monthly revenue trends, geographic performance, top product categories,
delivery performance, customer satisfaction by category, and payment
behavior. Used JOINs, CTEs, Window Functions and aggregations.

### Feature Engineering
Created 15+ new features from raw data:
- **Delivery features** — delivery days, delivery delay, is_late flag
- **Time features** — order year, month, quarter, day of week, is_weekend
- **Revenue features** — order value, basket size, avg item price
- **Customer features** — tenure days, days since last purchase

### Exploratory Data Analysis
Six charts, each answering a specific business question — monthly revenue
trend, top states by revenue, best product categories, review score
distribution, delivery delay distribution, and payment method breakdown.
Every chart includes a business insight explaining what the finding means.

### Customer Intelligence

**RFM Segmentation** — scored all 96,000+ customers on Recency,
Frequency and Monetary dimensions (1–5 scale) and grouped them into
six actionable segments:

| Segment | Count | Strategy |
|---------|-------|----------|
| Champions | 4,182 | Reward and protect |
| Loyal Customers | 9,870 | Upsell and engage |
| Potential Loyalists | 16,280 | Nurture and convert |
| New Customers | 5,614 | Onboard carefully |
| At Risk | 21,940 | Re-engage urgently |
| Lost | 38,591 | Low-cost win-back only |

**CLV Analysis** — Champions average CLV is 15× higher than Lost
customers. Every retention dollar spent on Champions has far higher
ROI than spending the same on win-back campaigns for Lost customers.

**Cohort Retention** — built a full retention heatmap across 12 monthly
cohorts. Every cohort drops to near-zero retention after month 1.
The business is entirely dependent on new customer acquisition —
expensive and unsustainable.

### Churn Prediction

Trained a Random Forest classifier to predict which customers are at
churn risk (defined as 180+ days of inactivity).

| Metric | Result |
|--------|--------|
| Model | Random Forest (100 estimators) |
| Churn Definition | 180+ days inactive |
| Top Feature | Recency (by significant margin) |
| Output | Churn probability score per customer |

Feature importance confirmed that **Recency dominates** — a customer
who hasn't bought recently is the clearest signal of churn. The model
outputs probability scores (not just binary predictions) so the business
can tier its response by risk level.

### Interactive Dashboard

4-page dashboard built with Plotly — opens in any browser, no
installation needed. Every filter updates all charts and KPIs in
real time.

**Page 1 — Executive Summary**
Revenue, orders, customers, AOV — with year and state filters

**Page 2 — Customer Intelligence**
RFM segments, CLV by segment, cohort retention heatmap —
with segment filter

**Page 3 — Product & Sales**
Top categories, payment methods, review scores —
with category filter that changes both charts simultaneously

**Page 4 — Delivery & Operations**
On-time rate, delivery days by state, delay distribution —
with state filter that reshapes every chart and all KPIs

```
📂 08_PowerBI/01_Dashboard/olist_dashboard.html
   → Open in any browser to explore
```

---

## 💡 Business Recommendations

### 1 — Launch a Post-Purchase Retention Campaign
**Finding:** Cohort retention drops to near-zero after month 1 across
every cohort. The platform acquires customers effectively but loses
almost all of them after a single transaction.

**Action:** 3-touch email sequence after every first purchase —
Day 7 review request, Day 30 personalized recommendation, Day 60
discount offer with expiry date.

**Why it works:** The customer already trusts the platform. Converting
even 5% of first-time buyers to repeat buyers means thousands of
additional orders from the existing base.

---

### 2 — Replicate the São Paulo Playbook in New States
**Finding:** SP contributes ~40% of total revenue despite being one
of 26 states. Rio de Janeiro and Minas Gerais have large populations
but significantly lower revenue contribution.

**Action:** Audit what's driving SP performance — seller density,
logistics partnerships, marketing spend — and build the same
infrastructure systematically in RJ and MG.

---

### 3 — Build a VIP Program for Champions
**Finding:** Champions CLV is 15× higher than Lost customers.
Losing even a small number of them has an outsized revenue impact.

**Action:** Priority delivery, dedicated support, early product access,
loyalty rewards — exclusively for the Champions segment identified
through RFM analysis.

---

### 4 — Fix Deliveries in Problem States
**Finding:** Bahia, Pernambuco and Ceará average 16–18 days delivery
time vs São Paulo's 8.4 days. Late deliveries and 1-star reviews are
directly correlated throughout the dataset.

**Action:** Audit logistics partners in these three states. Set stricter
SLAs with clear penalties. Test alternative carriers where delays are
chronic.

---

### 5 — Re-engage Customers at 60 Days, Not 180
**Finding:** Churn model shows customers crossing 90 days of inactivity
rarely return after 180 days. By the time they're "churned" the window
has already closed.

**Action:** Trigger automated re-engagement at the 60-day inactivity
mark — not after 180. Win-back campaigns at 180+ days cost 5× more
and convert at a fraction of the rate.

---

## 🛠️ Tech Stack

| Tool | Version | Used For |
|------|---------|----------|
| Python | 3.13 | Core analysis language |
| Pandas | Latest | Data manipulation |
| NumPy | Latest | Numerical operations |
| Matplotlib & Seaborn | Latest | Static visualizations |
| Scikit-learn | Latest | Churn prediction ML model |
| SQLite | Built-in | SQL analytics database |
| Plotly | Latest | Interactive dashboard |
| Git & GitHub | Latest | Version control |
| Jupyter Notebook | Latest | Analysis environment |
| VS Code | Latest | Development environment |

---

## 📂 Project Structure

```
Intelligent-Customer-Analytics-Suite/
│
├── 02_Data/
│   ├── 01_Raw_Data/          — Original Olist CSV files
│   ├── 02_Cleaned_Data/      — 7 cleaned datasets
│   └── 03_Processed_Data/    — Featured + RFM + Churn outputs
│
├── 04_SQL_Analytics/
│   ├── 01_Database/          — SQLite setup + 8 business queries
│   └── findings.md           — SQL phase key findings
│
├── 05_Analytics/
│   ├── 01_Notebooks/         — Feature Engineering + EDA notebooks
│   └── 03_Visualizations/    — All exported charts
│
├── 06_Customer_Intelligence/
│   ├── 01_RFM_Analysis/      — RFM scoring and segmentation
│   ├── 02_CLV_Analysis/      — Customer Lifetime Value by segment
│   └── 03_Cohort_Analysis/   — Monthly cohort retention heatmap
│
├── 07_Machine_Learning/
│   ├── 02_Models/            — Churn prediction notebook
│   ├── 03_Evaluation/        — Confusion matrix + feature importance
│   └── 04_Predictions/       — Churn probability scores per customer
│
├── 08_PowerBI/
│   └── 01_Dashboard/         — olist_dashboard.html (open in browser)
│
├── 09_Reports/
│   └── 02_Business_Report/   — Business_Recommendations.md
│
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/divyanshaggarwal/Intelligent-Customer-Analytics-Suite.git

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn plotly

# 3. Run notebooks in order
#    03_Data_Cleaning → SQL → Feature_Engineering → EDA
#    → RFM → CLV → Cohort → Churn_Prediction

# 4. Open dashboard
#    Open 08_PowerBI/01_Dashboard/olist_dashboard.html in any browser
```

---

## 👤 About

**Divyansh Aggarwal**  
Aspiring Data Analyst | Python · SQL · Machine Learning · Plotly

I built this project to demonstrate what end-to-end analytical thinking
looks like in practice — starting from a raw dataset and a business
problem, not just a clean CSV and a pre-defined question.

If you're a recruiter and want to discuss any part of this project,
I'd genuinely enjoy that conversation.

## 📬 Contact
 **Email:** divyanshaggarwal840@gmail.com
 **LinkedIn:** [Divyansh Aggarwal](https://www.linkedin.com/in/divyansh-aggarwal-2a54a8280)
 **GitHub:** [divyanshaggarwal69](https://github.com/divyanshaggarwal69)