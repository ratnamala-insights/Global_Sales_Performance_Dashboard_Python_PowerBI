# Sales Analytics Dashboard | Python & Power BI

## 📌 Project Overview

This project focuses on analyzing historical sales data to identify **revenue drivers, profitability patterns, and concentration risks** across markets, customers, and products. The analysis combines **Python-based exploratory data analysis (EDA)** with **Power BI dashboards** to deliver clear, decision-ready insights.

The scope of the project is intentionally aligned with the **available and reliable data**, ensuring all conclusions are fully supported by analysis and visualizations.

---

## 🎯 Business Problem Definition (Revised & Interview-Safe)

**Objective:**
Analyze sales performance and profitability patterns to understand how revenue is generated, identify high-performing market segments, and assess customer and product concentration risks.

**Key Analytical Questions Addressed:**

* Which market segment (Domestic vs International) generates higher revenue and sales volume?
* Which customers and products contribute most significantly to revenue and profit?
* How are revenue, cost, and profit distributed across transactions?
* Are profits driven primarily by high sales volume or by high-value transactions?
* Are revenue and profits concentrated among a small subset of customers or products?


## 🏢 Business Context

Sales data was originally distributed across multiple files, representing different aspects of transactional activity. This made it difficult for stakeholders to evaluate overall performance and profitability trends.

The project consolidates this data into a **centralized, analysis-ready dataset** and applies structured analysis to support business decision-making.

---

## 🧩 Data Preparation & Methodology

* Data sourced from **4 separate files**

* Key steps:

  * Data understanding and validation
  * Cleaning and standardization
  * Logical joins to create a master dataset

* Final analytical dataset:
  **`Sales_Dashboard_Final.csv`**

### Python was used for EDA to:

* Examine distributions and variability
* Identify skewness and outliers
* Understand relationships between revenue, cost, quantity, and profit
* Validate insights before dashboard design


## 📊 Key Insights from Python Analysis

### 1️⃣ Distribution Analysis (Revenue, Cost, Profit & Margin)

**What was analyzed:**

* Total Amount (Revenue)
* Quantity
* Unit Cost & Total Cost
* Gross Profit
* Profit Margin (%)

**Key Findings:**

* Revenue and profit distributions are **right-skewed**, indicating dependency on a small number of high-value transactions
* Sales quantity is more evenly distributed than revenue
* Profit margins remain within a relatively stable range, reflecting pricing discipline

**Business Interpretation:**
Revenue is largely volume-driven, but profitability is driven by select high-performing transactions.

<img width="1286" height="623" alt="image" src="https://github.com/user-attachments/assets/065d2be9-c384-4d7d-88cc-133e472da5be" />

```md
![Distribution Analysis](screenshots/distribution_overview.png)
```

---

### 2️⃣ Revenue & Profit Concentration (Pareto Analysis)

**Key Findings:**

* Approximately **20% of customers/products contribute ~80% of total revenue**
* The remaining majority contribute marginally on an individual basis

**Business Interpretation:**
The business faces concentration risk, with heavy reliance on a limited subset of customers and products.

📸 *Insert Pareto chart screenshot here*

```md
![Pareto Analysis](screenshots/pareto.png)
```

---

### 3️⃣ Market Segment Performance (Domestic vs International)

**Key Findings:**

* One market segment contributes higher sales volume
* The other contributes higher average deal value and revenue

**Business Interpretation:**
Different market segments require differentiated pricing, sales, and growth strategies.

📸 *Insert market segmentation screenshot here*

```md
![Market Segment Analysis](screenshots/market_segment.png)
```

---

### 4️⃣ Revenue vs Profit Relationship

**Key Findings:**

* High sales volume does not always translate to high profit
* Low-volume, high-value transactions often generate disproportionate profit

**Business Interpretation:**
Margin management is more critical than volume growth alone.

📸 *Insert revenue vs profit screenshot here*

```md
![Revenue vs Profit](screenshots/revenue_profit.png)
```

---

## 📈 Power BI – Business Reporting Layer

Power BI dashboards were designed to translate analytical findings into **business-consumable insights** by:

* Highlighting key KPIs
* Enabling quick comparisons across segments
* Supporting interactive filtering and drill-downs

### Visualization Mapping

| Python Analysis       | Power BI Visualization   |
| --------------------- | ------------------------ |
| Distribution Analysis | KPI Cards & Bar Charts   |
| Pareto Analysis       | Top Customers / Products |
| Market Segmentation   | Clustered Bar Charts     |
| Time-Based Trends     | Waterfall & Line Charts  |

📸 *Insert Power BI dashboard screenshot here*

```md
![Power BI Dashboard](screenshots/powerbi_dashboard.png)
```

---

## 🚀 Business Impact

* Established a **clean, consolidated dataset** for sales analysis
* Identified key revenue and profit drivers
* Highlighted customer and product concentration risks
* Enabled data-backed pricing and sales strategy discussions

---

## ✅ Key Recommendations

1. Prioritize high-margin, high-value transactions over pure volume growth
2. Protect and expand relationships with top revenue-contributing customers
3. Reduce concentration risk by developing mid-tier customers and products
4. Apply differentiated strategies for domestic and international markets
5. Use Python for analysis and Power BI for ongoing performance monitoring

---

## 🛠 Tools & Technologies

* **Python** (Pandas, Matplotlib, Seaborn) – Data preparation & EDA
* **Power BI** – Interactive dashboards & reporting
* **CSV-based analytical data model**
