# 📊 Tailwind Traders — Power BI Sales & Profit Analytics

> **Microsoft Power BI Data Analyst Professional Certificate — Capstone Project**

An end-to-end Business Intelligence project built in **Microsoft Power BI** to analyze Tailwind Traders' global sales and profitability, standardize international financial data into USD, and provide decision-makers with interactive sales, profit, and executive-level reporting.

---

## 👔 Executive Dashboard

The final solution consolidates key sales and profitability metrics into a single **Executive Dashboard**, providing management with a high-level view of business performance.

![Tailwind Traders Executive Dashboard](Executive_dashboard.png)

The dashboard brings together key indicators across:

- Sales performance
- Net and gross revenue
- Profitability
- Product performance
- Geographic performance
- Customer loyalty
- Inventory
- Sales and profit-margin trends

This creates two levels of business intelligence:

**Detailed Reports → Analyst / Operational Analysis**

**Executive Dashboard → Management Performance Monitoring**

---

## 🎯 Business Problem

Tailwind Traders operates across multiple international markets and requires a consolidated view of its **sales and financial performance**.

The business needs to understand:

- How sales are performing across countries and products
- Which products generate the most revenue
- How sales and profitability change over time
- How customer loyalty differs across markets
- How much inventory is available
- Whether financial performance is improving or declining
- When critical revenue metrics fall below defined thresholds

A further analytical challenge is that international transactions involve different currencies, making direct financial comparison difficult.

The objective of this project was therefore to develop a Power BI solution that transforms raw operational data into **standardized, decision-ready business intelligence**.

---

## 💡 Solution Overview

I developed an end-to-end analytics workflow covering:

**Data Preparation → Data Transformation → Data Modeling → DAX → Sales Analysis → Profit Analysis → Executive Dashboard → Mobile Reporting → Automated Monitoring**

The final solution consists of:

- 📈 **Sales Overview Report**
- 💰 **Profit Overview Report**
- 👔 **Executive Dashboard**
- 📱 **Mobile-optimized dashboard**
- 🚨 **KPI alert**
- 📧 **Scheduled report subscriptions**

---

## 🛠️ Technology Stack

| Technology | Application |
|---|---|
| **Microsoft Excel** | Initial sales-data preparation and revenue calculations |
| **Power Query** | Data cleaning, transformation, validation, and type configuration |
| **Python / Pandas** | Preparation of historical currency-exchange data |
| **Power BI Desktop** | Data modeling, DAX calculations, analysis, and report development |
| **DAX** | Financial KPIs, time intelligence, and statistical calculations |
| **Power BI Service** | Publishing, executive dashboard, mobile view, alerts, and subscriptions |

---

# 🔄 Analytics Workflow

## 1. Data Preparation — Excel

Prepared the initial sales dataset before loading it into Power BI.

Calculated key transaction-level financial fields including:

- **Gross Revenue**
- **Total Tax**
- **Net Revenue**

### Business Logic

```text
Gross Revenue = Gross Product Price × Quantity Purchased

Total Tax = Tax Per Product × Quantity Purchased

Net Revenue = Gross Revenue − Total Tax
```

These calculations established core financial metrics for downstream analysis.

---

## 2. Data Cleaning & Transformation — Power Query

Imported and configured multiple datasets including:

- Sales
- Purchases
- Countries
- Historical Exchange Rates

Performed data-quality and transformation tasks including:

- Correcting column data types
- Reviewing column quality and distributions
- Profiling numerical fields
- Validating records
- Filtering returned purchases to retain relevant transactions
- Preparing datasets for relational modeling

These steps helped ensure that downstream calculations and visualizations were based on consistent, analysis-ready data.

---

## 3. Currency Data Preparation — Python

Used **Python with Pandas** to transform historical currency-exchange information into a structured dataset that could be integrated into the Power BI model.

The exchange-rate data supported analysis across currencies including:

- USD
- GBP
- EUR
- AED
- AUD

This enabled international sales and financial metrics to be standardized into **US dollars for comparable global reporting**.

---

# 🧩 Data Modeling

Designed a relational Power BI model connecting sales, purchases, countries, exchange-rate information, calendar data, and USD-standardized sales calculations.

![Tailwind Traders Power BI Data Model](model_view.png)

Key modeling work included:

- Configuring table relationships and cardinality
- Establishing appropriate filter relationships
- Creating a dedicated **Calendar Table**
- Building a calculated **Sales in USD** table
- Connecting country information with exchange-rate data
- Supporting time-intelligence analysis through the calendar dimension

### Why the Data Model Matters

The model allows sales, purchases, geography, currency, and time to work together so that stakeholders can investigate questions such as:

> Which products generate the most revenue in USD?

> How does profitability change over time?

> How does business performance differ between countries?

---

# 🌍 Standardizing Global Sales to USD

Created a calculated **Sales in USD** table using DAX and related exchange-rate information.

The model generated standardized financial fields including:

- **Gross Revenue USD**
- **Net Revenue USD**
- **Total Tax USD**

This allowed Tailwind Traders' international performance to be compared using a common reporting currency.

---

# 🧮 DAX & Business Metrics

Created DAX measures to convert transactional data into decision-oriented KPIs.

Key calculations included:

### Yearly Profit Margin

Evaluates profitability relative to net revenue and supports annual financial-performance monitoring.

### Quarterly Profit

Uses time intelligence to evaluate profit performance within the relevant quarter.

### Year-to-Date Profit

Tracks cumulative profit performance from the beginning of the year through the current reporting period.

### Median Sales

Measures the middle sales value and provides an alternative view of typical sales performance that is less influenced by extreme values.

I also used **Power BI Performance Analyzer** to review report performance and evaluate DAX query execution.

---

# 📈 Sales Overview

The **Sales Overview** was designed to support sales and operational decision-making across products, countries, customer loyalty, inventory, and time.

![Tailwind Traders Sales Overview](Sales_Overview.png)

### Key KPIs

- **Stock:** 14K
- **Quantity Purchased:** 152
- **Median Sales:** $222.50
- **Yearly Profit Margin:** 107.72%

### Analysis Included

#### Loyalty Points by Country

Evaluates customer loyalty across international markets and helps identify geographic differences in customer engagement.

#### Quantity Sold by Product

Compares product demand and identifies higher- and lower-volume products.

#### Median Sales Distribution by Country

Compares typical sales performance geographically.

#### Median Sales Over Time

Tracks changes in sales performance and highlights trends or unusual periods that may require further investigation.

#### Country Filtering

Allows users to interactively analyze performance for individual markets including:

- France
- UK
- USA
- Australia
- UAE

---

# 💰 Profit Overview

The **Profit Overview** focuses on financial performance, revenue contribution, profitability, geographic comparison, and changes over time.

![Tailwind Traders Profit Overview](Profit_Overview.png)

### Key KPIs

- **YTD Profit:** 107.80%
- **Net Revenue:** $13.89K
- **Gross Revenue:** $390

### Analysis Included

#### Net Revenue by Product

Ranks products according to their contribution to net revenue.

#### Yearly Profit Margin by Country

Compares profitability across geographic markets.

#### Yearly Profit Margin Over Time

Tracks profitability trends and highlights periods of unusual performance.

#### Date Filtering

Allows stakeholders to investigate financial performance across selected reporting periods.

---

# 🔎 Business Questions Addressed

The solution enables stakeholders to investigate questions such as:

1. Which products have the strongest sales demand?
2. Which products contribute the most net revenue?
3. How are median sales changing over time?
4. How does profitability vary between countries?
5. Which markets demonstrate stronger customer loyalty?
6. What is the current inventory position?
7. How is year-to-date profitability performing?
8. Are there unusual changes in sales or profit trends?
9. Has gross revenue fallen below the defined business threshold?

---

# 📊 Dashboard Observations

Based on the completed capstone dataset and reports:

- The **UK recorded the highest loyalty points (315)**, followed by the **USA (305)**.
- The **Modular Sofa Set** generated the highest displayed net revenue at approximately **$928**.
- Median sales were **$222.50**.
- Net revenue was approximately **$13.89K**.
- Geographic profit-margin distribution was relatively balanced across the five analyzed countries.
- Sales and profit time-series visuals revealed noticeable fluctuations that could be investigated further by product, country, and reporting period.

> **Note:** These observations describe the educational capstone dataset and should not be interpreted as results from a real commercial deployment.

---

## 📱 Mobile-Optimized Analytics

The Executive Dashboard was optimized for mobile consumption in Power BI Service, enabling stakeholders to monitor key sales and profitability metrics on mobile devices.

The mobile layout prioritizes key KPIs and business visuals for a streamlined experience on smaller screens.

### 🎥 Power BI Mobile Dashboard Demo

▶️ **[Watch the Mobile Dashboard Demo](Tailwind_Traders_Mobile_Dashboard_Demo.mp4)**

The demo shows the Tailwind Traders Executive Dashboard running in the Power BI mobile experience, demonstrating mobile-optimized access to key sales and profitability insights.

---

# 🚨 Proactive KPI Monitoring

Configured a Power BI data alert for **Gross Revenue**.

### Business Rule

```text
Gross Revenue < $400 → Trigger Alert
```

Instead of requiring stakeholders to continuously monitor the dashboard, Power BI can notify them when revenue falls below the defined threshold.

This introduces **exception-based performance monitoring** into the BI solution.

---

# 📧 Automated Report Distribution

Configured weekly subscriptions for:

- **Sales Overview**
- **Profit Overview**

Subscriptions provide stakeholders with recurring access to updated business-performance information without requiring them to manually check the reports.

Together, these Power BI Service capabilities support:

**Dashboard → Visibility**

**Mobile View → Accessibility**

**Alerts → Exception Monitoring**

**Subscriptions → Recurring Information Delivery**

---

# 💼 Skills Demonstrated

### Business Intelligence

- KPI development
- Sales analytics
- Profitability analysis
- Executive reporting
- Business performance monitoring
- Stakeholder-focused dashboard design

### Data Preparation

- Microsoft Excel
- Power Query
- Data profiling
- Data-quality validation
- Data transformation

### Data Modeling

- Relational modeling
- Table relationships
- Calendar dimensions
- Currency standardization
- Calculated tables

### Analytics

- DAX
- Time intelligence
- Median analysis
- Revenue analysis
- Profitability analysis

### Reporting & Deployment

- Power BI Desktop
- Power BI Service
- Interactive reports
- Executive dashboards
- Mobile layouts
- Performance Analyzer
- Data alerts
- Report subscriptions

### Programming

- Python
- Pandas

---

# 📁 Repository Structure

Countries.xlsx
Executive_dashboard.png
Profit_Overview.png
Purchases.xlsx
README.md
Sales_Overview.png
Tailwind Traders Report.pbix
Tailwind-Traders-Sales.xlsx
Tailwind_Traders_Mobile_Dashboard_Demo.mp4
model_view.png

---

# 🎓 Project Context

This project was completed as part of the **Microsoft Power BI Data Analyst Professional Certificate Capstone**.

The capstone uses a scenario-based business environment to demonstrate the practical application of:

**Data Preparation → Transformation → Modeling → DAX → Visualization → Reporting → Dashboarding → Monitoring**

**Tailwind Traders is the capstone business scenario. This repository represents an educational project and proof of applied learning rather than professional employment or client work.**

---

# 🚀 Key Takeaway

This project strengthened my understanding that **Business Intelligence is not simply about creating visualizations**.

A complete BI workflow connects:

**Business Requirements → Reliable Data → Data Model → Business Metrics → Analysis → Visualization → Executive Communication → Monitoring → Decision Support**

The project demonstrates my ability to translate defined business requirements into a structured Power BI analytics solution while considering both the technical data workflow and the way business stakeholders consume information.

---

## 👤 Connect With Me

I'm continuing to build practical **Data Analytics and Business Intelligence projects** focused on solving business problems using **SQL, Python, Power BI, Excel, and modern analytics workflows**.

- 💼 **LinkedIn:** [Usman Ali](https://www.linkedin.com/in/usmanali9999/)
- 💻 **GitHub:** [usmanali9999](https://github.com/usmanali9999)
---

⭐ If you found this project interesting, feel free to explore my other data analytics projects on GitHub or connect with me on LinkedIn.
