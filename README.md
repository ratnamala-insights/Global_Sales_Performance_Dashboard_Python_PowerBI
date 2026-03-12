# Sales Analytics Dashboard (Python + Power BI)

## Project Overview

This project demonstrates an **end-to-end sales analytics workflow**, starting from raw data stored across multiple files and transforming it into **business-ready insights and dashboards**. The focus of the project is to analyze **sales distribution, profitability behavior, revenue concentration, lead effectiveness, and month-over-month growth**, strictly based on analyses and visualizations that were actually performed.

---

## Business Context

The business generates transactional sales data across customers, products, industries, and time periods. Initially, this data was fragmented across multiple files, making it difficult for stakeholders to:

* Understand revenue and profit distribution
* Identify concentration risk across industries
* Evaluate lead quality effectiveness
* Monitor revenue growth trends over time

This project consolidates the data into a single analytical dataset and applies structured analysis to support data-driven decision-making.

---

## Business Questions Answered


1. How are sales, cost, quantity, and profit distributed across transactions?
2. How variable are sales and profitability metrics, and are there significant outliers?
3. Is industry revenue concentrated among a small number of industries?
4. Does lead score effectively predict deal value?
5. How is revenue growing month-over-month?

---

## Data Preparation & Methodology

* Data sourced from **4 separate CSV files** representing different parts of the sales lifecycle

* Steps performed:

  * Data inspection and understanding
  * Cleaning and standardization
  * Logical joins to create a master dataset

* Final analytical dataset:

  ```
  Sales_Dashboard_Final.csv
  ```

### Tools Used by Phase

* **Python** → Exploratory Data Analysis (EDA)
* **Power BI** → Business reporting and interactive dashboards

---

## Insights from Python Analysis

### 1. Distribution Analysis – Histograms

**Visuals Created (6 Histograms):**

* Total Amount
* Quantity
* Unit Cost
* Total Cost
* Gross Profit
* Profit Margin %

<img width="1270" height="623" alt="image" src="https://github.com/user-attachments/assets/9c17da16-d17a-4fda-a4a9-46cd20282a29" />

`![Histogram Distribution](screenshots/histogram_distribution.png)`

**Quantitative Observations:**

* Majority of transactions are clustered at lower values
* All monetary metrics show right-skewed distributions
* A small number of high-value transactions act as outliers

**Business Insight:**
Sales volume is high at lower transaction values, while revenue and profit are influenced by fewer high-value deals.

**Actions:**

* Identify and monitor high-value transactions
* Avoid evaluating performance using averages alone

---

### 2. Variability & Outlier Analysis – Box Plots

**Visuals Created (6 Box Plots):**

* Total Amount
* Quantity
* Unit Cost
* Total Cost
* Gross Profit
* Profit Margin %

<img width="1285" height="620" alt="image" src="https://github.com/user-attachments/assets/e3790551-0e39-461a-94f0-cd8118a98ffc" />

`![Box Plot Analysis](screenshots/box_plot_distribution.png)`

**Observations:**

* Wide interquartile ranges indicate high variability
* Presence of extreme outliers across revenue and profit metrics
* Median values are significantly lower than maximum values

**Business Insight:**
Pricing, cost, and profitability are inconsistent across transactions, increasing financial risk.

**Actions:**

* Review pricing and discounting practices
* Analyze extreme outliers for risk or best-practice identification

---

### 3. Industry Revenue Concentration – Pareto Analysis

**Visual Created:**

* Pareto chart using **Industry vs Total Amount**

<img width="1114" height="580" alt="image" src="https://github.com/user-attachments/assets/06c9e80c-d36f-4d4f-8f5b-c8f09757981d" />

`![Industry Pareto](screenshots/industry_pareto.png)`

**Observations:**

* A small subset of industries contributes the majority of total revenue
* Clear 80/20-style concentration pattern observed

**Business Insight:**
Revenue dependency is concentrated across limited industries, increasing exposure to industry-specific risks.

**Actions:**

* Strengthen relationships with high-performing industries
* Diversify revenue streams across emerging industries

---

### 4. Lead Effectiveness Analysis – Scatter Plot

**Visual Created:**

* Scatter plot of **Lead Score vs Total Amount**

<img width="1141" height="661" alt="image" src="https://github.com/user-attachments/assets/530a5451-b0e8-413a-851b-04c4e8fd02c7" />

`![Lead Score vs Revenue](screenshots/lead_score_vs_revenue.png)`

**Observations:**

* Weak or no correlation between lead score and deal value
* High and low deal values occur across all lead score ranges

**Business Insight:**
Current lead scoring does not reliably predict deal value.

**Actions:**

* Re-evaluate lead scoring logic
* Incorporate historical revenue signals into lead qualification

---

### 5. Month-over-Month (MoM) Revenue Growth Analysis

**Visual Created:**

* Line chart showing **MoM Revenue Growth %**

<img width="1110" height="609" alt="image" src="https://github.com/user-attachments/assets/84bc469b-7e19-437b-906d-1d31ebc47fd6" />

`![MoM Revenue Growth](screenshots/mom_revenue_growth.png)`

**Observations:**

* Revenue growth fluctuates month-to-month
* Periods of growth and decline are clearly visible

**Business Insight:**
Revenue performance is non-linear and influenced by time-based factors such as seasonality or campaigns.

**Actions:**

* Use MoM trends for proactive performance monitoring
* Investigate recurring decline periods

---

## Power BI Reporting Layer

Power BI was used to convert Python-based insights into **decision-ready dashboards**.

**Purpose of Power BI Visuals:**

* High-level KPI monitoring
* Interactive filtering and drill-downs
* Faster business interpretation

<img width="1164" height="651" alt="image" src="https://github.com/user-attachments/assets/818092ef-c5fa-466c-a615-feb66d199ca3" />

`![Power BI Dashboard](screenshots/powerbi_dashboard.png)`

---

## Business Impact

* Created a consolidated analytical dataset

* Identified:

  * Distribution and variability of sales and profit
  * Industry-level revenue concentration risk
  * Lead scoring effectiveness gaps
  * Revenue growth volatility

---

## Key Takeaways

Significant Revenue Volatility: The Month-on-Month (MoM) revenue analysis revealed high volatility, with a maximum growth peak of +30.07% and a sharp decline of -29.35%.

Takeaway: The business is currently susceptible to extreme seasonal or cyclical swings. Marketing and Sales must implement a "bridge strategy" for low-performance months (like February) to stabilize cash flow.

Pareto Concentration (80/20 Rule): Approximately 80% of total revenue ($13.09B) is generated by just 3 key industries: Pharma, Energy, and Petrochemicals.

Takeaway: These are the "Engine" industries. Strategic focus should be on retaining these high-value accounts while diversifying into secondary sectors to reduce dependency risk.

Lead Scoring Precision: Scatter plot analysis showed that 75% of deals exceeding $10M originated from leads with a score of 80 or higher.

Takeaway: The current lead scoring model is a high-accuracy predictor of revenue. Sales teams should be mandated to prioritize "High Score" leads first, as they represent the highest ROI on effort.

Industry Profitability Variance: While Pharma leads in volume, the Bar-in-Bar and Box Plot analysis showed that the Energy sector maintains a 5.4% higher average profit margin.

Takeaway: Revenue is a vanity metric; profit is sanity. The company should pivot its "Aggressive Growth" strategy toward Energy products to improve overall net bottom-line margins.

Customer Tier Dependency: The Top 5 Companies contribute nearly 45% of the total annual revenue, yet represent less than 1% of the total customer base.

Takeaway: This represents a high "Churn Risk." A dedicated Key Account Management (KAM) program is required for these top 5 entities to ensure long-term revenue security.



---

## Tools & Technologies

* **Python:** Pandas, Matplotlib, Seaborn – EDA & analysis
* **Power BI:** Interactive dashboards
* **CSV:** Analytical data model

---
