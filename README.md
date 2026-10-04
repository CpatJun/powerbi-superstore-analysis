
# Superstore Executive Profitability & Regional Dashboard

A personal Power BI portfolio project analyzing sales performance, profitability, and regional trends using the Sample Superstore dataset.

**Project Type:** Personal Portfolio Project  
**Focus:** Data Analysis, Data Modeling, DAX Measures, KPI Reporting, and Data Visualization

## Project Overview

This project uses Microsoft Power BI to analyze retail sales data and present business performance through interactive KPI cards, regional comparisons, sub-category profitability, and annual sales and profit trends.

The dashboard helps users understand business performance, identify profitable and loss-making product sub-categories, and compare results across regions.

## Business Questions

- How do sales and profit change over time?
- Which regions contribute to sales and profitability?
- Which product sub-categories generate the most profit or losses?
- How do sales and profitability change when filtering by category or order date?

## Dashboard Features

- **KPI Scorecards:** Total Sales, Total Orders, Total Profit, and Profit Margin
- **Regional Performance:** Comparison of profit, profit margin, and sales across regions
- **Sub-category Profitability:** Identification of profitable and loss-making product sub-categories
- **Sales and Profit Trends:** Annual comparison of sales and profit
- **Interactive Filters:** Category selection and order-date range

## Tools & Skills

- **Power BI:** Dashboard development and data visualization
- **DAX:** Measures and KPI calculations
- **Power Query:** Data cleaning and transformation
- **Data Modeling:** Organizing data for analysis
- **Business Analysis:** Regional performance and product profitability analysis

## DAX Measures

### Total Sales

```dax
Total Sales = SUM('Sales'[Sales])
```

### Total Profit

```dax
Total Profit = SUM('Sales'[Profit])
```

### Profit Margin %

```dax
Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
```

### Total Orders

```dax
Total Orders = DISTINCTCOUNT('Sales'[Order ID])
```

### Average Shipping Days

```dax
Avg Shipping Days =
AVERAGEX(
    'Sales',
    DATEDIFF('Sales'[Order Date], 'Sales'[Ship Date], DAY)
)
```

## Key Findings

Based on the current dashboard, the reported KPI values are approximately:

- **Total Sales:** $2.29M
- **Total Orders:** 5K
- **Total Profit:** $285.13K
- **Profit Margin:** 12.44%

These figures represent the values displayed in the current dashboard. Results may change when report filters are applied.

The sub-category profitability chart highlights differences in product profitability, including categories with negative profit. The annual trend chart supports comparisons of sales and profit over time.

## How to Explore the Project

1. Review the dashboard preview image.
2. Open the Power BI report in Power BI Desktop.
3. If a data source error occurs, update the source path to the local dataset.
4. Use the category and order-date filters to explore changes in the KPIs and charts.
5. Compare regional performance and sub-category profitability.

## Project Files

- `Project2_Executive_Profitability.pbix` — Power BI report
- `Executive_Profitability_Dashboard.pdf` — Exported dashboard report
- `dashboard_preview.JPG` — Dashboard preview image
- `Sales_Data_Cleaned.xlsx` — Cleaned sales dataset
- `README.md` — Project documentation

## Limitations

- This project uses a sample retail dataset for portfolio and educational purposes.
- Findings describe the sample data and do not represent the performance of a real company.
- KPI values may vary depending on report filters and the underlying dataset.
- Business recommendations should be based on verified results from the report.

## About

Created by **C. Pat Junlapak (Sean)** as a personal Power BI and data analytics portfolio project.

- GitHub: [CpatJun](https://github.com/CpatJun)
- Repository: [powerbi-superstore-analysis](https://github.com/CpatJun/powerbi-superstore-analysis)

