
# Executive Profitability & Regional Dashboard (Power BI)

## 📌 Project Overview
This Power BI project provides a comprehensive executive summary of sales performance, profitability trends, and regional dynamics for the Superstore dataset. It is designed to assist stakeholders and business leaders in quickly identifying top-performing product categories, key regional drivers, and underlying profitability challenges.

![Dashboard Preview](dashboard_preview.png)

---

## 🔑 Key Features & Highlights

1. **KPI Scorecard**:
   - **Total Sales**: `$22.79bn`
   - **Total Profit**: `$283.03K`
   - **Profit Margin %**: `12.43%`
   - **Total Orders**: `5K`

2. **Regional Performance Matrix**:
   - Evaluates performance across Central, East, South, and West regions.
   - Highlights regional breakdown with custom DAX calculations and concise data formatting (`Billions`).

3. **Sub-Category Profitability Analysis**:
   - Horizontal bar chart with explicit Data Labels identifying high-margin categories (Copiers, Phones) vs. loss-leading categories (Tables, Bookcases).

4. **Sales & Profit Trend**:
   - Dual-axis Line and Clustered Column chart visualizing annual sales growth against profit movement over time (2014–2017).

5. **Interactive Controls**:
   - Dynamic **Category Dropdown** and **Order Date Range Slider** for seamlessly slicing business performance across dimensions.

---

## 🛠️ Data Model & DAX Measures

### Data Table: `Sales`

The dashboard utilizes custom Data Analysis Expressions (DAX) to deliver business metrics:

```dax
// Total Sales Calculation
Total Sales = SUM('Sales'[Sales])

// Total Profit Calculation
Total Profit = SUM('Sales'[Profit])

// Profit Margin Percentage
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

// Total Unique Orders
Total Orders = DISTINCTCOUNT('Sales'[Order ID])

// Average Shipping Duration (Days)
Avg Shipping Days = AVERAGEX('Sales', DATEDIFF('Sales'[Order Date], 'Sales'[Ship Date], DAY))
