# Task 4 – Data Storytelling & Statistical Validation

## Project: Impact of Delivery Delays on Customer Satisfaction

**Internship:** Data Analytics Internship – ApexPlanet Software Pvt Ltd  
**Task:** Task 4 – Data Storytelling & Statistical Validation  
**Dataset:** Olist E-Commerce Dataset  

---

## Project Objective

The objective of this project is to determine whether delivery delays significantly affect customer satisfaction using statistical hypothesis testing.

---

## Business Problem

Delivery performance is a key driver of customer satisfaction in e-commerce. Late deliveries can result in poor customer reviews, reduced repeat purchases, and negative brand perception.

**Key Question:**

Do late deliveries significantly reduce customer review scores?

---

## Dataset Information

Datasets used:

- `olist_orders_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_order_reviews_dataset.csv`

Total records analyzed:

- **Total delivered orders:** 96,353  
- **Late deliveries:** 6,409  
- **On-time deliveries:** 89,944  

---

## Methodology

### Data Preparation
- Filtered delivered orders
- Removed missing delivery dates
- Converted timestamps

### Feature Engineering
- Calculated actual delivery days
- Calculated estimated delivery days
- Calculated delivery delay
- Created late delivery indicator

### Data Integration
- Merged orders with review dataset

### Statistical Analysis
- Independent Sample T-Test
- Significance level: 0.05

---

## Hypothesis Testing

**Null Hypothesis (H₀):**  
There is no significant difference in review scores between late and on-time deliveries.

**Alternative Hypothesis (H₁):**  
Late deliveries have significantly lower review scores.

---

## Key Results

| Metric | Value |
|--------|-------|
| Total Orders | 96,353 |
| Late Orders | 6,409 |
| On-Time Orders | 89,944 |
| Avg Late Rating | 2.27 |
| Avg On-Time Rating | 4.29 |
| Rating Gap | 2.02 |
| P-Value | < 0.0001 |

---

## Statistical Conclusion

Since the p-value is less than 0.05, we reject the null hypothesis.

**Conclusion:**  
Late deliveries significantly reduce customer satisfaction scores.

---

## Business Insights

- Late deliveries reduce ratings by ~2 points
- Customer satisfaction depends heavily on delivery performance
- Delivery delays increase churn risk
- Logistics efficiency impacts customer retention

---

## Business Recommendations

- Improve delivery time predictions
- Optimize logistics operations
- Notify customers about delays
- Provide delay compensation policies
- Monitor delivery KPIs

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- Seaborn
- Google Colab

---

## Repository Files

| File | Description |
|------|-------------|
| Data_Storytelling.pptx | Final presentation |
| Data_Storytelling.pdf | Presentation preview |
| task4_analysis.ipynb | Analysis notebook |
| hypothesis_testing_summary.csv | Statistical summary |
| hypothesis_test_visualization.png | Visualization |

---

## Final Conclusion

This project demonstrates that delivery delays have a statistically significant negative impact on customer satisfaction. Improving delivery performance can directly improve customer ratings and overall business outcomes.

---
