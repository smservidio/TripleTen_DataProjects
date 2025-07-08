# 📊 Sprint 3: Business Analytics - E-commerce User Activity Project

## 🚀 Project Overview

This project simulates a real-world scenario where I was hired as a **Junior Business Analyst** at an e-commerce company. The company provided raw transaction logs, and my task was to turn them into actionable business metrics that could guide strategic decisions.

This project focused on three main analyses:
1. **Building a conversion funnel** to understand how product page views lead to purchases.
2. **Preparing cohort data and calculating retention rates** to track customer loyalty.
3. **Documenting results in an executive summary**, organizing, and formatting for a professional stakeholder report.

---

## 🛒 Business Context

### The Company
- A growing e-commerce retailer that needed to analyze user behavior on its website.

### The Challenge
- Make sense of raw event logs capturing every user interaction—page views, cart opens, and purchases.
- Provide the executive team with insights into conversion effectiveness and customer retention.

---

## 📈 Data Description

The dataset (`raw_user_activity`) contained the following columns:

| Column          | Description                                 |
|-----------------|---------------------------------------------|
| `user_id`       | Unique customer IDs                         |
| `event_type`    | User activity type (view, cart, purchase)   |
| `category_code` | Product category code                      |
| `brand`         | Brand of the product                       |
| `price`         | Price of the product in USD                 |
| `event_date`    | Date of activity (YYYY-MM-DD format)        |

---

## 🔍 Analysis Breakdown

### Part 1️⃣: Conversion Funnel
- Created a **pivot table** (`conversion_funnel`) with 3 stages:
  - Product Page Views
  - Cart Opens
  - Purchases
- Measured **unique users at each stage** to avoid double-counting.
- Calculated:
  - Overall conversion rates from page views to purchases.
  - Step-to-step conversion rates (page -> cart, cart -> purchase).

### Part 2️⃣: Preparing Data for Cohort Analysis
- Filtered out purchases to a new sheet (`purchase_activity`).
- Identified each user’s **first purchase date** to define cohorts.
- Added:
  - `event_month` and `first_purchase_month` columns (formatted as YYYY-MM).
  - `cohort_age`: number of months since first purchase.

### Part 3️⃣: Retention Analysis
- Created a `cohort_analysis` pivot table:
  - Rows: Cohorts by first purchase month (6 cohorts total).
  - Columns: Number of unique users by cohort age (0-4 months).
- Calculated **retention rates** in a `retention_rates` sheet by comparing later months to the cohort's size at age 0.

### Part 4️⃣: Executive Summary & Reporting
- Wrote an **Executive Summary** outlining:
  - Conversion funnel performance.
  - Retention rates and cohort behavior.
- Documented assumptions about data timespan, event types, and methodology (unique users, months used for cohorting, etc.).
- Organized sheets for readability:
  - Table of Contents and Executive Summary first.
  - Analytical results (funnels, retention).
  - Calculation sheets (cohorts, pivot tables).
  - Raw data last.
- Enhanced clarity with professional formatting (frozen headers, formatted dates and %s, table borders).

---

## 📊 Key Findings

- Conversion rates showed expected drop-off between views -> carts -> purchases, highlighting opportunities to optimize cart conversion.
- Retention analysis revealed declining engagement after the first month—a typical pattern for e-commerce—emphasizing the need for targeted re-engagement.

---

## 🛠 Tools & Skills Applied

- **Google Sheets (Excel-like functions)**: `VLOOKUP`, `TEXT`, `DATEDIF`, pivot tables.
- **Cohort and funnel metrics** for customer analytics.
- Data storytelling & reporting for executives.

---

📌 *This project was completed as part of a Business Analytics learning sprint to showcase analytical thinking, user funnel building, cohort retention analysis, and professional reporting skills.*

