# 🛒 Blinkit Quick-Commerce Performance & Retention Analytics

## 📌 Project Overview
An end-to-end interactive Power BI dashboard designed to evaluate sales performance, operational delivery SLAs, and customer retention metrics for Blinkit (Quick-Commerce platform) across 5,000+ orders.

---

## 📊 Key Pages & Features

### 1. Executive Dashboard (Sales & Revenue Analysis)
- **Revenue & Orders:** Tracked Total Revenue (₹1.10Cr) and Order volumes across regions and time periods.
- **Category & Channel Breakdown:** Insights into top-performing product categories and sales channels.

### 2. Delivery SLA & Operational Performance
- **On-Time Delivery Rate (OTDR %):** Monitored average SLA compliance and delay minutes.
- **Promised vs. Actual Duration:** Evaluated operational bottlenecks using scatter plots and trend matrices.

### 3. Customer Retention & At-Risk Analysis
- **Repeat Rate % & Segmentation:** Segmented customers into *1 Single Order*, *2-5 Repeat Orders*, and *5+ Frequent Orders*.
- **At-Risk Customer Watchlist:** Formulated dynamic DAX measures (`Days Since Last Order`) with automated conditional formatting to flag churn-risk accounts (>90 days inactive).

---

## 🛠️ Key DAX Measures Formulated
- **Repeat Rate %:** `DIVIDE([Repeat Customers], [Total Customers], 0)`
- **Days Since Last Order:** `DATEDIFF(MAX(Fact_Orders[order_date]), CALCULATE(MAX(Fact_Orders[order_date]), ALL(Fact_Orders)), DAY)`
- **OTDR % (On-Time Delivery Rate):** `DIVIDE(CALCULATE(COUNT(Fact_Orders[order_id]), Fact_Orders[delivery_status] = "On Time"), COUNT(Fact_Orders[order_id]), 0)`

---

## 📁 Repository Structure
- `Blinkit_Analytics_Dashboard.pbix` — Power BI Source File
- `Screenshots/` — High-resolution visuals across all 3 dashboard pages
- `Datasets/` — Raw dataset files used for modeling and analysis 

---

## 👤 Author
**Dinesh Jangra**  
- [LinkedIn Profile](https://linkedin.com)
