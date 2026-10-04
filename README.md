# Superstore Executive Profitability & Regional Dashboard

A personal Power BI portfolio project exploring sales performance,
profitability, and regional trends in the Sample Superstore dataset.

> **Project type:** Personal portfolio project\
> **Focus:** Data modeling, DAX measures, KPI reporting, and interactive
> visualization

## Project Overview

This dashboard helps users explore business performance across product
categories and regions through high-level KPIs, regional comparisons,
sub-category profitability, and sales/profit trends.

## Business Questions

-   How do sales and profit change over time?
-   Which regions contribute to sales and profitability?
-   Which product sub-categories are profitable or loss-making?
-   How do results change when filtering by category or order date?
-   What does average shipping duration look like?

## Dashboard Features

-   **KPI scorecard:** Total Sales, Total Profit, Profit Margin, and
    Total Orders
-   **Regional performance:** Comparison across Central, East, South,
    and West
-   **Sub-category profitability:** Comparison of profit contributors
-   **Sales and profit trends:** Annual trend analysis
-   **Interactive filters:** Category dropdown and order-date range

## Tools & Skills

-   **Power BI** --- report and dashboard development
-   **DAX** --- KPI calculations and business measures
-   **Data modeling** --- structuring data for analysis
-   **Business analysis** --- comparing regional and product
    profitability

## DAX Measures

``` dax
Total Sales = SUM('Sales'[Sales])

Total Profit = SUM('Sales'[Profit])

Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)

Total Orders = DISTINCTCOUNT('Sales'[Order ID])

Avg Shipping Days =
AVERAGEX(
    'Sales',
    DATEDIFF('Sales'[Order Date], 'Sales'[Ship Date], DAY)
)
```

## Key Findings

The current dashboard reports:

-   **Total Profit:** \$283.03K
-   **Profit Margin:** 12.43%
-   **Total Orders:** approximately 5K

**Verify the Total Sales KPI before publishing:** the current project
description displays `$22.79bn`. Check the underlying measure, source
data, and display units in Power BI before quoting this value. This
README does not repeat that sales figure until it has been verified.

Add specific, quantified business recommendations only after confirming
them against the report and source data.

## How to Explore the Project

1.  Review the files actually included in this repository.
2.  Open the Power BI report in Power BI Desktop if a `.pbix` file is
    available.
3.  If Power BI reports a missing data source, update the source path to
    your local dataset.
4.  Use the category and order-date filters to explore how KPIs and
    visuals change.
5.  Compare regional results and sub-category profitability before
    drawing conclusions.

## Project Files

See the repository file list for the report, dataset, and supporting
assets. Update this section with exact paths after confirming which
files are committed to the repository.

## Limitations

-   This is a portfolio project using a sample retail dataset, not a
    production reporting system.
-   Findings describe the sample dataset and should not be interpreted
    as results for a real company.
-   KPI values and business recommendations should be checked against
    the report and source data before use.

## About

Created by **C.Pat Junlapak (Sean)** as a personal Power BI and data
analytics portfolio project.

-   GitHub: [CpatJun](https://github.com/CpatJun)
-   Repository:
    [powerbi-superstore-analysis](https://github.com/CpatJun/powerbi-superstore-analysis)
