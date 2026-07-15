# Business Recommendations
**Project:** AI-Powered Customer Intelligence & Revenue Optimization  
**Dataset:** Brazilian Olist E-Commerce  
**Analyst:** Divyansh Aggarwal

---

## Context

After analyzing 96,000+ orders, segmenting customers using RFM, 
building a churn prediction model, and studying cohort retention — 
one thing became very clear.

Olist doesn't have an acquisition problem. It has a retention problem.

Almost every customer buys once and never comes back. The five 
recommendations below are directly tied to findings from the analysis 
— not generic advice.

---

## Recommendation 1 — Fix Retention Before Spending on Acquisition

**What the data showed:**  
Cohort analysis revealed near-zero retention after month 1 across 
every single cohort going back two years. This isn't seasonal — 
it's structural.

**What to do:**  
Launch a 3-touch post-purchase email sequence for every new customer:
- Day 7 — ask for a review while the experience is fresh
- Day 30 — send a personalized recommendation based on what they bought
- Day 60 — offer 10% off their next order with a clear expiry date

**Why this works:**  
The customer already trusts the platform — they bought once. 
Converting them to a repeat buyer costs a fraction of acquiring 
someone new. Even a 5% improvement in repeat purchase rate across 
96,000 customers means thousands of additional orders.

---

## Recommendation 2 — Double Down on São Paulo, Then Expand

**What the data showed:**  
São Paulo drives approximately 40% of total revenue despite being 
one of 26 states. The gap between SP and the next state (Rio de 
Janeiro) is enormous.

**What to do:**  
Conduct a deep audit of what's driving SP performance — seller 
density, logistics speed, marketing channels. Then build the same 
infrastructure systematically in Rio de Janeiro and Minas Gerais.

**Why this works:**  
The demand clearly exists in other states. The gap is supply-side — 
fewer sellers, slower delivery, less marketing presence. Fix the 
supply and the revenue follows.

---

## Recommendation 3 — Protect Champions at All Costs

**What the data showed:**  
RFM analysis identified a Champions segment with CLV approximately 
15 times higher than the Lost segment. Losing even a handful of 
Champions has an outsized revenue impact.

**What to do:**  
Create a VIP program exclusively for Champions — priority delivery, 
dedicated customer support line, early access to new product 
categories, and loyalty rewards.

**Why this works:**  
Champions already love the platform. A VIP program reinforces that 
relationship and makes switching to a competitor feel like a 
significant downgrade in experience.

---

## Recommendation 4 — Fix Late Deliveries in Problem States

**What the data showed:**  
Delivery delay analysis showed Bahia, Pernambuco and Ceará averaging 
16-18 days delivery time compared to São Paulo's 8.4 days. Late 
deliveries and 1-star reviews are directly correlated throughout 
the dataset.

**What to do:**  
Audit logistics partners in the three worst-performing states. 
Set stricter SLAs with penalties for consistent delays. Test 
alternative carriers where delays are chronic.

**Expected impact:**  
A 20% reduction in late deliveries in these states would 
meaningfully lift review scores and customer retention in 
those regions.

---

## Recommendation 5 — Re-engage Customers at 60 Days, Not 180

**What the data showed:**  
The churn prediction model found Recency is the strongest predictor 
of churn by a significant margin. Customers who cross 90 days of 
inactivity rarely return after reaching 180 days.

**What to do:**  
Change the re-engagement trigger from "customer has churned" to 
"customer is about to churn." Flag every customer at 60 days of 
inactivity automatically and send a personalized campaign immediately.

**Why this works:**  
Win-back campaigns targeting already-churned customers cost 5 times 
more and convert at a fraction of the rate. Catching customers 
before they're fully gone is both cheaper and more effective.

---

## Summary

| Priority | Recommendation | Expected Impact |
|----------|---------------|-----------------|
| 1 | Post-purchase retention campaign | Highest ROI — low cost, high upside |
| 2 | SP playbook expansion to RJ & MG | Geographic revenue growth |
| 3 | Champions VIP program | Protect highest-value segment |
| 4 | Fix late deliveries in BA/PE/CE | Improve reviews and retention |
| 5 | Re-engage at 60-day mark | Reduce churn before point of no return |

---

*All recommendations are grounded in specific data findings from 
SQL analysis, RFM segmentation, cohort retention study and 
churn prediction model.