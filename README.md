# Regional Sales Growth Analysis

An Excel-based analysis of how sales changed by region between 2023 and 2024, with a written report.


## Workbook contents

- **KPI Summary**: the original summary sheet, unchanged.
- **Regional Growth**: annual growth by region, quarterly sales by region, quarter-over-quarter growth, and a line chart. Every number is a live formula.
- **Sales Data**: the original 3,000 order records (columns A to T), plus two added columns:
  - `2023 Orders` (column U) and `2024 Orders` (column V) show each Order ID under its order year and are blank otherwise.

## Method

1. Order dates are stored as text (`MM/DD/YYYY`), so the year is read from the last four characters and the quarter from the month.
2. Sales are summed per region and year with `SUMIFS`, and per region and quarter with `SUMPRODUCT`.
3. Dollar change = 2024 sales minus 2023 sales.
4. Growth rate = 2024 sales / 2023 sales - 1.
5. Quarter-over-quarter growth = a quarter's sales / the previous quarter's sales - 1.

Growth is measured on **Sales ($)** only.

## Key results

| Region | 2023 | 2024 | Growth |
|---|---|---|---|
| Central | $287,690 | $252,222 | -12.3% |
| East | $316,137 | $353,274 | +11.7% |
| North | $334,991 | $250,288 | -25.3% |
| South | $332,873 | $337,294 | +1.3% |
| West | $337,125 | $339,115 | +0.6% |
| **Total** | **$1,608,815** | **$1,532,193** | **-4.8%** |

## Limitations

- Only two years of data, so this shows a comparison, not a long-run trend.
- Quarterly growth rates are volatile because each quarter is compared with a single other quarter.
- The data shows what changed, not why.
- Profit, discounts and order counts by region were not analyzed.

## How to use the workbook

Open `Sales_Data_by_Year.xlsx` and go to the **Regional Growth** sheet. Click any number to see its formula. The years and quarters shown in blue are labels the formulas read, so they can be changed. The formulas cover rows 2 to 3001 of Sales Data, so extend the ranges if you add more rows.
