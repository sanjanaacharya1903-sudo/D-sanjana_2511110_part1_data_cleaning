# Retail Data Cleaning and Validation

## Problem Summary

This project cleans a retail order dataset exported from multiple
systems and prepares it for business analysis.

## Dataset Description

-   Order-level retail sales data
-   932 records
-   Customer, product, sales, shipping and payment information

## Tools Used

-   Microsoft Excel
-   Pivot Tables
-   Formulas (TRIM, IF, IFERROR, PROPER, SUBSTITUTE, YEAR, MONTH)
-   Data Validation

## Cleaning Steps

1.  Preserved raw data.
2.  Standardized text fields.
3.  Cleaned dates.
4.  Filled missing Region/Ship Mode with Unknown.
5.  Filled valid missing discounts with 0.
6.  Flagged invalid discounts.
7.  Identified duplicates.
8.  Added calculated columns.
9.  Generated pivot summaries.

## Business Rules

-   Missing Region → Unknown
-   Missing Ship Mode → Unknown
-   Missing Discount → 0 (when applicable)
-   Negative/invalid discounts flagged
-   Cancelled and failed-payment orders excluded from completed sales
    summaries
-   Refunded orders summarized separately

## Data Quality Summary

-   Missing values identified and handled.
-   Duplicate records reviewed.
-   Invalid shipping records flagged.
-   Calculation mismatches checked.

## Pivot Reports

-   Sales & Profit by Region
-   Sales & Profit by Category/Sub-category
-   Order Count by Ship Mode
-   Profit Margin by Segment
-   Monthly Sales Trend
-   Refunded/Cancelled/Failed Orders by Region

## Key Business Insights

-   Regional performance can be compared using cleaned sales.
-   Product categories contribute differently to profit.
-   Shipping performance can be monitored using delay days.
-   Refunds and failed payments are isolated from completed sales.

## Assumptions

Business rules supplied in the assignment were followed.

## Limitations

No external master data was available for validation.

## Screenshots Included

-   raw_data_preview.png
-   cleaned_data_preview.png
-   pivot_summary_1.png
-   pivot_summary_2.png
