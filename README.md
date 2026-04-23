# 📊 Retail Profitability & Inventory Optimization Analysis

End-to-end Business Analyst project demonstrating **data analysis, SQL insights, process thinking, and executive dashboard storytelling** using industry-standard tools.

---

# 📑 Table of Contents

* [📌 Project Overview](#-project-overview)
* [❗ Problem Statement](#-problem-statement)
* [🎯 Objectives](#-objectives)
* [🔄 Process Flow](#-process-flow-ba-approach)
* [📄 Business Requirement Document (BRD)](#-business-requirement-document-brd)
* [📊 Dataset](#-dataset)
* [📈 Dashboard](#-dashboard)
* [🧠 SQL Analysis](#-sql-analysis)
* [📌 Requirements Traceability Matrix (RTM)](#-requirements-traceability-matrix-rtm)
* [🧩 Agile Project Management (Jira)](#-agile-project-management-jira)
* [🔁 End-to-End Analysis Performed](#-end-to-end-analysis-performed)
* [📊 Key Insights](#-key-insights)
* [💡 Business Recommendations](#-business-recommendations)
* [🛠 Tools Used](#-tools-used)
* [🚀 Outcome](#-outcome)

---

# 📌 Project Overview

This project focuses on analyzing **retail sales and profitability data** to identify revenue leakage and optimize business performance.

The analysis highlights how **discount strategies, product categories, and regional performance** impact profitability, similar to large-scale retail environments like Walmart.

An executive-level dashboard is developed to support **data-driven decision-making**.

---

# ❗ Problem Statement

Despite strong sales performance, the business is experiencing:

* Low profitability in certain product categories
* Losses driven by excessive discounting
* Regional performance inconsistencies
* Lack of visibility into key performance drivers

---

# 🎯 Objectives

* Identify profit leakage across categories and products
* Analyze discount impact on profit margins
* Evaluate regional performance
* Enable executive-level decision making
* Provide actionable business recommendations

---

# 🔄 Process Flow (BA Approach)

1. Data Collection
2. Data Cleaning & Transformation
3. Data Analysis (SQL + Dashboard)
4. Insight Generation
5. Dashboard Development
6. Business Recommendations

---

# 📄 Business Requirement Document (BRD)

## Objective

Improve profitability by identifying loss-making areas and optimizing pricing strategies.

## Scope

* Sales & Profit Analysis
* Discount Impact
* Regional Performance

## Key Requirements

### Business Requirements

* Identify high and low-performing categories
* Analyze discount vs profit relationship
* Provide executive dashboard

### Functional Requirements

* Calculate sales, profit, and margin
* Visualize category, region, and product insights

[BRD DOCUMENT](https://github.com/manilpatel010-hub/Sales-and-Profitability-Analysis/blob/main/BRD%20for%20Retail%20sales.docx)

---

# 📊 Dataset

* Superstore Dataset (~10K records)
* Fields include:

  * Sales, Profit, Discount
  * Category, Sub-Category
  * Region, State

 [DATASET](https://github.com/manilpatel010-hub/Sales-and-Profitability-Analysis/blob/main/retail_data.csv)

---

# 📈 Dashboard

## Page 1: Executive Summary

* KPI Cards (Sales, Profit, Margin)
* Category Performance
* Regional Profit Analysis
* Loss-Making Sub-Categories

[DASHBOARD 1](https://github.com/manilpatel010-hub/Sales-and-Profitability-Analysis/blob/main/Power%20BI/Dashboard%201.png)


## Page 2: Root Cause Analysis

* Discount vs Profit
* State-Level Sales
* Monthly Trends
* Product Performance

📎 `/dashboard/Retail_Dashboard.pbix`

---

# 🧠 SQL Analysis

The following SQL queries were used to validate insights and support business recommendations:

## 1. Category Performance

```sql
SELECT Category,
       SUM(Sales) AS Total_Sales,
       SUM(Profit) AS Total_Profit,
       ROUND(SUM(Profit)/SUM(Sales),2) AS Profit_Margin
FROM superstore
GROUP BY Category;
```

## 2. Loss-Making Sub-Categories

```sql
SELECT Sub_Category,
       SUM(Profit) AS Total_Profit
FROM superstore
GROUP BY Sub_Category
HAVING SUM(Profit) < 0;
```

## 3. Discount Impact

```sql
SELECT Discount,
       AVG(Profit) AS Avg_Profit
FROM superstore
GROUP BY Discount;
```

## 4. Regional Performance

```sql
SELECT Region,
       SUM(Sales) AS Total_Sales,
       SUM(Profit) AS Total_Profit
FROM superstore
GROUP BY Region;
```

## 5. Top & Worst Products

```sql
SELECT Product_Name,
       SUM(Profit) AS Total_Profit
FROM superstore
GROUP BY Product_Name
ORDER BY Total_Profit DESC;
```

---

# 📌 Requirements Traceability Matrix (RTM)

| Requirement | Description                   | User Story | Test Case |
| ----------- | ----------------------------- | ---------- | --------- |
| BR-01       | Category Performance Analysis | US-01      | TC-01     |
| BR-02       | Discount Impact Analysis      | US-02      | TC-02     |
| BR-03       | Regional Performance Analysis | US-03      | TC-03     |
| BR-04       | Product Profitability         | US-04      | TC-04     |

---

# 🧩 Agile Project Management (Jira)

* Epic: Retail Profitability Optimization
* User Stories defined for analysis and dashboard
* Sprint-based execution
* Task tracking

📎 `/docs/JIRA_User_Stories.md`

---

# 🔁 End-to-End Analysis Performed

* Requirement gathering
* Data analysis using SQL
* Dashboard development
* Insight generation
* Business recommendations

---

# 📊 Key Insights

* Furniture category has high sales but low profit
* Tables and Bookcases are major loss drivers
* High discounts reduce profitability
* Central region underperforms
* Few products drive majority of revenue

---

# 💡 Business Recommendations

* Optimize discount strategy
* Re-evaluate loss-making products
* Focus on high-margin categories
* Improve regional strategy
* Implement data-driven pricing

---

# 🛠 Tools Used

* Power BI
* SQL
* Excel
* Jira
* draw.io
* GitHub

---

# 🚀 Outcome

This project demonstrates:

* Business analysis thinking
* SQL and data analysis skills
* Dashboard storytelling
* Ability to convert data into decisions

---
