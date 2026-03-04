# 📦 Task 2 — Exploratory Data Analysis & Business Intelligence
### E-Commerce Order Fulfillment Efficiency | Olist Brazilian E-Commerce Dataset

---

## 🎯 Objective
Uncover patterns, trends, and relationships within the order fulfillment lifecycle. 
Answer 7 key operational business questions using SQL and Python-based EDA to identify where fulfillment breaks down and why.

---

## 📊 Dataset
**Source:** Olist Brazilian E-Commerce Public Dataset (Kaggle)  
**Scope:** 96,315 completed (delivered) orders | 2016–2018  
**Files Used:**
- `olist_orders_dataset.csv` — Core lifecycle timestamps
- `olist_order_items_dataset.csv` — Order to product/seller mapping
- `olist_products_dataset.csv` — Product category data
- `olist_sellers_dataset.csv` — Seller location data
- `olist_customers_dataset.csv` — Customer location data
- `product_category_name_translation.csv` — Portuguese → English

---

## 🔍 Analysis Structure

### Phase 1 — Descriptive Statistics & Univariate Analysis
- Summary statistics for delivery_days, shipping_days, approval_delay
- Distribution histograms with mean/median overlays
- Box plots with outlier quantification
- On-Time vs Late delivery breakdown + deviation from estimate

### Phase 2 — SQL Business Intelligence 
| # | Question | Method |
|---|---|---|
| Q1 | Which states have worst delivery performance? | GROUP BY + JOIN |
| Q2 | Which product categories take longest? | Multi-table JOIN |
| Q3 | What is the monthly delivery trend? | STRFTIME + aggregation |
| Q4 | Which sellers have highest late delivery rate? | HAVING + subquery |
| Q5 | How does approval delay vary by weekday? | CASE + STRFTIME |
| Q6 | How accurate are delivery estimates over time? | Deviation analysis |
| Q7 | Which fulfillment stage drives delivery time? | Correlation analysis |

### Phase 3 — Static KPI Dashboard Mock-up
Proposed operational dashboard with 5 core KPIs for an e-commerce operations manager.

---

## 🎯 Key Findings

### Finding 1 — Last-Mile is the Bottleneck
Last-mile delivery (carrier → customer) has **r = 0.928** correlation with total delivery time. 
This single stage explains 92.8% of all delivery time variance. 
Approval delay has r = 0.080 — virtually zero impact.

### Finding 2 — Estimation Padding Strategy
Olist delivers an average of **12.3 days earlier** than the estimated delivery date. 
This padding artificially inflates the on-time rate to 91.9%.
As order volumes scaled through 2018, this buffer shrank — directly causing late rate spikes.

### Finding 3 — The Feb/Mar 2018 Crisis
Late delivery rate spiked to **21.36% in March 2018** without a corresponding volume spike. 
This suggests an external disruption — possible carrier strike or infrastructure failure.

### Finding 4 — Geographic Concentration
State **AM averages 26.4 days** delivery. State **AL has 23.9% late rate**.
13 of the 15 worst-performing sellers are located in São Paulo (SP).

### Finding 5 — Weekend Approval Gap
Orders placed on weekends face **29% slower approval** than weekday orders.
23% of Sunday orders take more than 1 full day just to be approved.

---

## 📈 KPI Dashboard Preview
> Full interactive dashboard coming in Task 3

| KPI | Value | Target |
|---|---|---|
| On-Time Delivery Rate | 91.9% | 95% |
| Avg Fulfillment Time | 12.6 days | — |
| Avg Carrier Handoff | 3.2 days | — |
| Estimation Buffer | −12.3 days | — |
| Late Delivery Orders | 7,827 (8.1%) | <5% |

---
