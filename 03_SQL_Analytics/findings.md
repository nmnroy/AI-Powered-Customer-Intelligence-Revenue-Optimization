# SQL Analytics — Key Findings
**Project:** AI-Powered Customer Intelligence & Revenue Optimization Platform  
**Analyst:** Naman Roy  
**Database:** SQLite (`olist.db`)

---

- **Market Scale:** Olist generated **R$ 15.42M in revenue** across **96,477 delivered orders** from 2016 to 2018.
- **Customer Base:** The platform served **93,357 unique individuals** (`customer_unique_id`). While 96.8% placed a single order, a high-value core of **2,997 repeat buyers** placed between 2 and 17 orders.
- **Geographic Concentration:** **São Paulo (SP)** is the dominant market engine, generating **~37.5% of total marketplace GMV** and 41.8% of order volume across Brazil's 27 federative units.
- **Logistics & Satisfaction:** Order delivery delay is the #1 driver of negative sentiment. Outlying states (Bahia, Pernambuco, Ceará) average 16–18 days delivery transit vs. SP's 8.4 days, directly driving 1-star ratings and suppressing repeat orders.
- **Payment Behavior:** **Credit cards account for 75%+ of payment volume**, with installment financing widely utilized, indicating high average order value and price sensitivity.
- **Retention Driver:** Machine learning feature importance demonstrates that **shipping freight costs and delivery delays** are the dominant predictors of customer churn (Random Forest ROC-AUC: 0.727).
