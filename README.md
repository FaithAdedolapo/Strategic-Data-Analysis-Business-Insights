# Strategic Data Analysis and Business Insights
> *A business intelligence project analyzing Q1 sales performance across brands, customer segments, regions, and product attributes to uncover profitability drivers and support strategic decision-making.*

---

## ⚙️ Project Type Flags

- [ ] Exploratory Data Analysis (EDA)
- [ ] Dashboard / Data Visualization
- [ ] Data Cleaning / Wrangling
- [ ] End-to-End (multiple of the above)

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Repository Structure](#4-repository-structure)
5. [Data Workflow](#5-data-workflow)
6. [Data Model & Schema](#6-data-model--schema)
7. [Analysis & Metrics](#7-analysis--metrics)
8. [Key Insights](#8key-insights)
9. [Recommendations](#9-recommendations)
10. [Assumptions & Limitations](#10-assumptions--limitations)
11. [Future Enhancements](#11-future-enhancements)
12. [Deliverables](#12-deliverables)
13. [Author](#13-author)

---

## 1. Project Overview

<!--
  Write 3–5 sentences in plain language.
  Cover: context → problem → approach → outcome.
  Read it out loud. If it sounds like a form - rewrite it.

  WHAT GOOD LOOKS LIKE:
  "A mid-size retail business was seeing inconsistent revenue across
  its regional stores but couldn't identify the root cause. This project
  explored 18 months of transaction data across five regions to determine
  whether underperformance was driven by sales volume, pricing, or return
  rates. The analysis revealed that one region's gap was almost entirely
  explained by an unusually high return rate on a single product category -
  a finding invisible in the company's top-level reporting."

  WHAT TO AVOID:
  "This project analyzes sales data to find trends and insights."
  (Too vague. Could describe 10,000 projects. Describes none of them.)
-->

**Context:** A retail electronics business wanted better visibility into its sales performance and profitability across brands, regions, and customer segments. While raw sales data existed, decision-makers lacked a centralized analytical dashboard to identify performance drivers.

**Problem Statement:** The business needed to understand which products, regions, and customer segments were contributing the most to revenue and profit in order to guide marketing, inventory, and pricing strategies.

**Approach:** Sales data for Q1 2024 was cleaned and modeled in Excel and Power BI. Key business metrics such as revenue, profit, customer segmentation, and product performance were analyzed through interactive dashboards and KPI visualizations.

**Outcome:** The project produced a Power BI dashboard highlighting key performance drivers, including brand profitability, revenue trends, customer segmentation, and regional performance. Insights revealed profit concentration among specific brands and strong contributions from high-income customers.

---

## 2. Objectives

<!--
  Write objectives that are specific enough to succeed or fail.
  Use action-oriented verbs: Identify, Determine, Quantify, Build, Evaluate.

  WHAT GOOD LOOKS LIKE:
  ✅ "Determine whether customer churn rate correlates with support ticket volume."
  ✅ "Identify the top three revenue-driving product categories across all regions."
  ✅ "Build a reproducible pipeline that ingests and cleans daily sales exports."

  WHAT TO AVOID:
  ❌ "Explore the data."
  ❌ "Gain insights."
  ❌ "Understand trends."
  (These can't fail - which means they can't succeed either.)
-->

- **Primary Objective:** Determine the key drivers of revenue and profitability across products, regions, and customer segments.
- **Secondary Objective 1:** Analyze revenue trends across months in Q1 2024.
- **Secondary Objective 2:** Detect risk indicators including rising debt, transaction anomalies, and potential fraud.
- **Secondary Objective 3:** Evaluate customer segmentation (income level, gender, region) to uncover profitable target markets.

> 💡 *Every analysis decision in this project traces back to one of these objectives.*

---

## 3. Project Scope & Tools

### Scope

<!--
  WHAT GOOD LOOKS LIKE:
  In Scope: "Transaction-level data for Regions A–E, Jan 2023–Jun 2024.
             Analysis covers revenue, return rates, and product category performance."
  Out of Scope: "Customer demographics and marketing spend data were excluded -
                 demographic data was incomplete for two regions, and marketing
                 data sits in a separate system outside this engagement."

  WHAT TO AVOID:
  ❌ Leaving Out of Scope blank. This is the section that protects your credibility.
     If you don't define the fence, reviewers assume you missed things.
-->

| Dimension | Details |
|-----------|---------|
| **In Scope** | Q1 2024 retail sales data including revenue, COGS, profit, customer segmentation, and product attributes |
| **Out of Scope** | Marketing spend data, supplier costs, and operational logistics data (not included in dataset) |
| **Time Period** | January 2024 – March 2024 |
| **Granularity** | Transaction-level data aggregated for monthly, brand, and customer segmentation analysis |

### Tools & Technologies

<!--
  List only what you actually used on this project.
  This is not your skills section - it's the project's technical context.
-->

| Category | Tool(s) Used |
|----------|-------------|
| Data Storage | Excel / CSV |
| Data Processing | Excel |
| Analysis | Power BI |
| Visualization | Power BI |
| Version Control | Git / GitHub |
| Documentation | Markdown |
| Other | PowerPoint |

---

## 4. Repository Structure

```
sales-performance-dashboard/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── dashboard/
│   └── sales_dashboard.pbix
│
├── reports/
│   └── PowerBI_Capstone_Presentation.pdf
│
├── visuals/
│   └── dashboard_preview.png
│
└── README.md

```
## 5. Data Workflow

```
Sales Dataset (Excel)
        ↓
Data Cleaning & Preparation
        ↓
Data Modeling in Power BI
        ↓
Metric Creation (DAX)
        ↓
Dashboard Visualisation
        ↓
Business Insights & Recommendations

```

### Source
Retail sales dataset provided for Power BI Capstone analysis.
Format: Excel spreadsheet containing transaction-level sales data.

### Ingestion
Data imported into Power BI using the Power Query Editor.

### Data Cleaning
Standardized column naming conventions
Verified data types (dates, currency, numeric fields)
Removed duplicate records
Ensured consistent formatting across categorical variables

### Data Transformation
New calculated fields and measures were created including:
Total Sales
Total COGS
Total Profit
Profit Margin
Customer segmentation metrics

### Analysis
The analysis focused on:
Profitability by brand
Customer segmentation
Monthly revenue trends
Product attribute analysis (color)
Regional performance comparison

### Output
Final outputs include:
Interactive Power BI dashboard
Business insights presentation
Visual KPI reporting

---

## 6. Data Model & Schema

<!--
  Define your fields so that someone reading your analysis can follow along
  without digging through your code.

  WHAT GOOD LOOKS LIKE (one row example):
  | transaction_id | string | Unique identifier per sales transaction | TXN-00482 |
  | return_flag    | boolean | Whether the transaction included a return | TRUE |
  | region_code    | string | Two-letter identifier for store region | "NE" |

  WHAT TO AVOID:
  ❌ Skipping this section because "the field names are self-explanatory."
     They're not. Not to a reviewer. Not to you in six months.

  📌 FOR SQL PROJECTS: If you have multiple tables, create one block per table.
     Describe join keys and relationships here. Your ERD (Section 7) will
     visualise what this section describes in text.

  📌 FOR NON-SQL PROJECTS: Describe the shape of your dataset informally
     if a formal schema doesn't apply. Even one paragraph is more helpful than nothing.
-->

### Dataset: `Sales Data`

| Field Name | Data Type | Description | Example Value |
|------------|-----------|-------------|---------------|
| `Transaction_ID` | Integer | Unique identifier for each sales transaction | 100234 |
| `Product_Brand` | String | Brand of product sold | Apple |
| `Product_Color` | String | Product color variant | Black |
| `Region` | string | Sales region | East |
| `Customer_Gender` | String | Gender of customer | Female |
| `Income_Level` | String | Customer income category | High |
| `Sales` | Float | Total revenue generated | 45000 |
| `COGS` | Float | Cost of goods sold | 28000 |
| `Profit` | Float | Net profit from transaction | 17000 |
| `Order_Date` | Date | Date of purchase | 2024-02-14 |


> **Row count (approx.):** ~5,200 customer records
> > **Date range:** Jan 2024 – Mar 2024

---

## 7. Analysis & Metrics

<!--
  Explain what you measured and how - before you share what you found.

  WHAT GOOD LOOKS LIKE:
  Metric: "Customer Return Rate"
  Definition: "Number of transactions flagged as returns divided by total
               transactions, calculated at product-category and regional grain."
  Why It Matters: "Return rate - not sales volume - was hypothesised to
                  explain regional revenue gaps. This metric tests that hypothesis."

  WHAT TO AVOID:
  ❌ Defining a metric only in code: SUM(returns) / COUNT(transaction_id)
     That's an implementation. Write the plain-language definition here.
     Both belong in your project - the definition in the README,
     the implementation in the code.
-->

### Analytical Approach

Exploratory analysis of spending patterns, customer demographics, and risk factors; segmented data by customer type and merchant category; identified anomalies and trends.

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| `Total Salesd` | Total revenue generated from product sales | Measures overall business performance |
| `Total Profit` | Revenue minus cost of goods sold | Indicates business profitability |
| `Profit Margin` | Profit as a percentage of total sales | Evaluates operational efficiency |
| `Customer Count` | Number of unique customers | Measures market rea |
| `Revenue by Brand` | Total revenue grouped by product brand | Identifies top-performing brands |

### Methods Used

- Descriptive statistics
- Business KPI tracking
- Customer segmentation
- Comparative performance analysis
- Trend analysis across time

---

## 9. Key Insights

<!--
  Findings + implications. Not just what happened - what it means.

  WHAT GOOD LOOKS LIKE:
  ✅ "Return rates, not sales volume, explain Region A's underperformance.
      Region A's return rate on home goods was 34% - more than double the
      company average. Revenue was not lost at the point of sale; it was
      lost post-sale through refunds. This points to a fulfilment or
      product quality issue specific to that region, not a demand problem."

  WHAT TO AVOID:
  ❌ "Region A had lower revenue than other regions in Q4."
     (That's an observation. It describes what happened.
      An insight says what it means and where to look next.)

  Aim for 3–6 insights. Quality over quantity.
-->

**Insight 1: Strong overall profitability**

The company generated ₦3M in revenue and ₦932K in profit, resulting in a 31% profit margin, indicating a healthy but improvable business model.

**Insight 2: Profit concentration among key brands**

Apple and Dell contribute the largest share of total profit. This indicates strong brand demand but also creates revenue concentration risk.

**Insight 3: Balanced product color demand**

Revenue is evenly distributed across Black, Gray, and White product variants, suggesting customer preferences are evenly spread and inventory can remain balanced.

**Insight 4: Positive sales momentum**

Revenue increased steadily across Q1:
- January: ₦1.03M
- February: ₦1.04M
- March: ₦1.05M

This suggests improving sales performance and potential continued growth in Q2.

**Insight 5: High-income customers drive profitability**

High-income customers account for approximately 54% of total profit, making them the most valuable customer segment.

---

## 10. Recommendations

<!--
  Action-oriented. Addressed to a real audience.
  Tied explicitly to the insight that supports each one.

  WHAT GOOD LOOKS LIKE:
  Priority: High
  Recommendation: "Conduct a fulfilment audit for home goods deliveries
                   in Region A - specifically investigating whether returns
                   correlate with a particular warehouse, carrier, or SKU batch."
  Based On: Insight 1 - return rate anomaly in Region A
  Owner: Operations / Supply Chain team

  WHAT TO AVOID:
  ❌ "Improve the return rate."
     (Not actionable. Doesn't say who, how, or where to start.)
  ❌ "Further analysis is needed."
     (This is a placeholder, not a recommendation.)
-->

| Priority | Recommendation | Based On | Suggested Owner |
|----------|---------------|----------|-----------------|
| High | Increase marketing focus on top-performing brands such as Apple and Dell | Brand profitability insight | Marketing team |
| High | Develop premium offers and loyalty programs for high-income customers | Customer segmentation insight | Customer strategy team |
| Medium | Conduct supply chain review to reduce COGS and increase margins above 35% | Profit margin analysis | Operations team |
| Medium | Expand marketing and distribution efforts in the East region | Regional sales insight | Sales leadership |
| Low | Explore product diversification strategies for lower-performing brands | Brand performance insight | Product management |

---

## 11. Assumptions & Limitations

<!--
  WHAT GOOD LOOKS LIKE:
  Assumption: "Sales data represents all transactions for the period.
               Product costs remained stable during the analysis period."
  Limitation: "Marketing spend data was not included
               May 2025 data is partial and not directly comparable to full months.
               Customer demographic data was unavailable"

  WHAT TO AVOID:
  ❌ Leaving this section blank or writing "None known."
     Every project has limitations. Documenting them is a sign of
     analytical maturity - not a confession of failure.
-->

### Assumptions
- All transaction records were assumed to be accurate and complete.
- Profit calculations were based strictly on provided sales and COGS fields.
- Customer income categories were assumed to be correctly classified.

### Limitations
- Dataset only covers Q1 2024, limiting long-term trend analysis.
- No marketing spend data was available to correlate campaigns with sales growth.
- No marketing spend data was available to correlate campaigns with sales growth.

---

## 12. Future Enhancements

<!--
  WHAT GOOD LOOKS LIKE:
  ✅ "Automate the monthly data pull from the POS export folder using
      a scheduled Python script, replacing the current manual process."
  ✅ "Expand the return rate analysis to include carrier-level data,
      which was unavailable in this dataset but exists in the logistics system."

  WHAT TO AVOID:
  ❌ "Add a machine learning model."
     (Vague, and disconnected from the actual findings of this project.)
  ❌ Listing aspirational features that don't follow logically from the work.
-->

- [ ] Add multi-year sales data to enable long-term trend analysis
- [ ] Incorporate marketing campaign data to measure ROI
- [ ] Build predictive sales forecasting using machine learning
- [ ] Build predictive sales forecasting using machine learning

---

## 13. Deliverables

| Deliverable | Description | Location |
|-------------|-------------|----------|
| Power BI Dashboard | Interactive sales performance dashboard | /dashboard |
| Project Presentation | Capstone analysis presentatio | /reports |
| Visualizations | Exported dashboard screenshots | /visuals |

---

## 14. Author

**Faith Adedolapo**

Data Analyst | Business Analyst

- 🔗 [LinkedIn URL](https://www.linkedin.com/in/faithadedolapoolayiwola)
- 💼 [Portfolio or GitHub profile URL](https://faithadedolapo.github.io/)
- 📧 [Email](olayiwolaadefaith@gmail.com)

---

*Last updated: March 2026


