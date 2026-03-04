# Task 1: Data Immersion and Data Wrangling

## Project
**E-commerce Order Fulfillment Efficiency**

This task focuses on preparing a clean and analysis-ready dataset from a real-world e-commerce transactional dataset. The goal of this phase is to ensure that the data accurately represents completed order fulfillment cycles and can support downstream analysis of delivery efficiency.

---

## Dataset

The dataset used in this project is the **Olist Brazilian E-commerce Dataset**, which contains transactional and logistics data for online orders.

The dataset includes multiple timestamps representing different stages of the order lifecycle, such as:

- Order purchase time
- Order approval time
- Carrier dispatch time
- Final customer delivery time

These timestamps allow reconstruction of the full fulfillment pipeline from purchase to delivery.

---

## Objectives of Task 1

The primary objective of this phase was to transform raw operational data into a **clean and structured dataset** suitable for analytical investigation.

Key goals included:

- Understanding the structure of the dataset
- Identifying lifecycle timestamps
- Handling incomplete order records
- Preparing the data for time-based performance analysis

---

## Data Cleaning Steps

The following data preparation steps were performed:

1. Standardized timestamp fields into proper datetime format.
2. Filtered the dataset to retain only **delivered orders** to ensure complete fulfillment lifecycle data.
3. Removed records with missing customer delivery timestamps.
4. Ensured the dataset was suitable for duration-based calculations.

---

## Feature Engineering

Three analytical features were created to enable operational analysis of the fulfillment pipeline:

### delivery_days
Represents the total time between order placement and final customer delivery.

delivery_days = order_delivered_customer_date - order_purchase_timestamp


### shipping_days
Represents the time between order placement and carrier dispatch.


shipping_days = order_delivered_carrier_date - order_purchase_timestamp


### approval_delay
Represents the delay between order placement and payment/system approval.


approval_delay = order_approved_at - order_purchase_timestamp


These features allow the delivery lifecycle to be decomposed into operational stages.

---

## Files in This Folder

| File | Description |
|-----|-------------|
| cleaned_orders_dataset.csv | Cleaned dataset used for analysis |
| data_dictionary.xlsx | Definitions and explanations of dataset columns |
| data_cleaning_summary.docx | Documentation of data cleaning steps |


---

## Outcome

The result of this phase is a **clean, analysis-ready dataset** that accurately represents completed order fulfillment cycles. This dataset forms the foundation for further exploratory analysis and operational insights in the next stages of the project.

---
