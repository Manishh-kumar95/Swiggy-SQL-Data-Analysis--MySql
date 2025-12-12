# 🍔 Swiggy SQL Data Analysis Case Study

![SQL](https://img.shields.io/badge/Language-SQL-blue?style=for-the-badge&logo=mysql)
![Data Analysis](https://img.shields.io/badge/Domain-Food_Delivery-orange?style=for-the-badge)
![Swiggy](https://img.shields.io/badge/Focus-Business_Insights-red?style=for-the-badge)

## 🎯 Project Overview
This project analyzes a relational dataset from **Swiggy**, India's leading food delivery platform. The goal was to derive actionable insights into customer behavior, restaurant performance, and delivery partner efficiency using advanced SQL queries.

## 🗂️ Dataset Schema
The analysis connects information from multiple tables:
* **Customers:** User details and location (City).
* **Orders:** Transactional data including order dates and amounts.
* **Restaurants:** Partner details, ratings, and locations.
* **Delivery Partners:** Performance metrics and delivery assignments.

---

## 💻 Key Business Problems Solved (SQL)
I designed 13 specific SQL queries to answer critical business questions:

### 1. Customer Insights & Segmentation
* **Active vs. Inactive Users:** Identified customers who have never placed an order (`IS NULL`) vs. frequent users (`COUNT > 1`).
* **Loyalty Analysis:** Found consistent customers who placed orders on exactly 3 different days using `COUNT(DISTINCT date)`.
* **City-Wise Analysis:** Analyzed customer ordering patterns specifically in major metros like **Mumbai** and **Delhi**.

### 2. Restaurant Performance
* **Revenue Generation:** Calculated total revenue per restaurant using `SUM(total_amount)` and `GROUP BY`.
* **Rating Analysis:** Identified the **Top 5 Restaurants** with the highest average ratings (`ORDER BY rating DESC LIMIT 5`).
* **Average Ratings:** Computed city-wide average restaurant ratings to benchmark performance.

### 3. Delivery Partner Efficiency
* **Workload Analysis:** Identified delivery partners who completed more than 1 delivery.
* **Customer Reach:** Found the delivery partner who served the *most unique customers* using `COUNT(DISTINCT customer_id)`.

### 4. Advanced Logic (Self Joins)
* **Customer Overlap:** Used a **Self Join** on the Orders and Customers tables to identify pairs of customers from the same city who ordered from the same restaurant but on different dates.

---

## 🛠️ Technical Skills Demonstrated
* **Joins:** Inner Join, Left Join, and Self Join to connect 4+ tables.
* **Aggregations:** `COUNT`, `SUM`, `AVG` for metric calculation.
* **Filtering & Logic:** `HAVING` clauses, `BETWEEN`, `DATEDIFF` (for identifying recent orders in the last 30 days).
* **Data Cleaning:** Handling `NULL` values in order history.

---

## ✅ Conclusion
This analysis provides a granular view of the Swiggy ecosystem, helping stakeholders understand:
1.  **Customer Retention:** Who are the high-value users?
2.  **Partner Performance:** Which restaurants and delivery partners are driving the business?
3.  **Operational Efficiency:** Where are the gaps in service?

---
