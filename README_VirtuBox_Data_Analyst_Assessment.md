# VirtuBox Infotech — Data Analyst Assessment

## Project Overview
This project analyzes Superstore sales data to identify sales and profitability patterns, compare category and regional performance, and develop practical recommendations for business stakeholders.

**Primary business question:**  
How can the business improve profitability while sustaining sales performance across product categories and regions?

## Deliverables
- **Google Sheet:** `VirtuBox_Data_Analysis_Project` — business questions and hypotheses, KPI summary, key insights, and recommendations.
- **Dashboard:** `Superstore Sales and Profitability Dashboard` in Looker Studio.
- **Presentation:** `VirtuBox_Superstore_Analysis_Presentation.pptx`.
- **Data file:** `Superstore_Cleaned_50000.csv`.
- **Methodology:** This README describes the analysis workflow, assumptions, limitations, and recommended next steps.
- **Analysis code/notebook:** Add the Python/Colab notebook or script used for data preparation and calculations before submission.

> **Add your links before submitting:** Paste the Google Sheet URL and Looker Studio dashboard URL in the space below. Confirm that the assessor has permission to open them.
>
> - Google Sheet: [PASTE GOOGLE SHEET LINK]
> - Looker Studio dashboard: [PASTE DASHBOARD LINK]

## Dataset and Data Preparation
The source file was `superstore.csv`. The source dataset contains Superstore order, customer, product, shipping, sales, discount, and profit fields. The analysis uses fields such as Order Date, Region, Category, Sub-Category, Sales, Quantity, Discount, and Profit.

The working file `Superstore_Cleaned_50000.csv` contains 50,000 rows. **Important limitation:** the working dataset was expanded from the original source rather than consisting of 50,000 independently observed transactions. Therefore, results calculated from the expanded file should be treated as exploratory and should not be represented as verified real-world business totals. Before making business decisions, rerun the analysis on the original data or document precisely how rows were expanded and how duplicates were handled.

Data-quality checks should include:
- Checking missing values in important fields.
- Identifying exact duplicate rows and duplicate order/product records.
- Converting order dates and numeric columns to suitable data types.
- Checking for blank or invalid sales, discount, and profit values.
- Confirming that all dashboard and spreadsheet calculations use the same version of the data.

## Analysis Approach
The analysis is organized around these areas:

1. **KPI summary:** Total Sales, Total Profit, Profit Margin, distinct Orders, Average Discount, and records with negative profit.
2. **Product category performance:** Compare sales, profit, and profit margin by Category and Sub-Category.
3. **Regional performance:** Compare sales and profit by Region.
4. **Discount and profitability:** Review the relationship between discount levels and profit, including loss-making records.
5. **Time trends:** Examine monthly sales trends.
6. **Recommendations:** Identify areas for deeper review and possible operational improvements.

### KPI Definitions
- **Total Sales:** Sum of `Sales`.
- **Total Profit:** Sum of `Profit`.
- **Profit Margin:** `Total Profit / Total Sales × 100`, where Total Sales is non-zero.
- **Distinct Orders:** Count of unique `Order ID` values.
- **Average Discount:** Average of `Discount` across included records.
- **Negative-Profit Records:** Count of records where `Profit < 0`.

Use consistent filters, date ranges, null handling, and aggregation rules across the spreadsheet, code, and dashboard.

## Working Findings to Validate
The following are preliminary figures reported during the working analysis and must be recalculated against one clearly identified dataset version before final submission. Do not present them as independently verified until reconciled with the spreadsheet and dashboard.

- Technology was reported as the strongest category by sales and profit.
- Furniture showed a much lower reported profit margin than Technology.
- Tables and Bookcases were reported as sub-categories with substantial negative profit.
- The West region was reported as the leading region by profit.
- Higher discount bands (30%, 40%, and 50%) were associated with lower average profit in the working analysis.

The exact KPI totals and some category/sub-category values varied between working outputs. This README intentionally does not treat those values as final verified results. Reconcile them before submission.

## Recommendations
1. **Review deep-discount rules.** Investigate transactions with discounts of 30% or more and compare their profit contribution with lower-discount sales. Treat the observed relationship as an association, not proof that discounts caused losses.
2. **Investigate loss-making sub-categories.** Review pricing, costs, shipping, returns, product mix, and discounting for Tables and Bookcases before changing assortment or pricing.
3. **Learn from stronger segments.** Examine Technology and the West region to identify product, customer, pricing, or operational practices that may be transferable elsewhere.
4. **Use consistent reporting.** Align the date range, filters, distinct-order definition, and dataset version across the Google Sheet and Looker Studio dashboard.

## Dashboard
The Looker Studio dashboard is titled **Superstore Sales and Profitability Dashboard**. It was described as containing:
- KPI cards for Total Sales, Total Profit, Total Orders, and Average Discount.
- Sales by Category.
- Profit by Category.
- Sales by Region.
- Monthly Sales Trend.
- A date-range control and Region filter.

Insert the live dashboard URL near the top of this file and verify its sharing permissions before submitting.

## Limitations
- The expanded 50,000-row file is not equivalent to 50,000 independent observed transactions.
- The original dataset contains data-quality issues, including exact duplicate rows and missing values; the final treatment of these issues must be documented in the code/notebook.
- Working KPI totals and some sub-category figures were inconsistent across outputs and require reconciliation.
- Observational comparisons cannot establish causation. For example, a relationship between higher discounts and lower profit does not alone prove that discounts caused the lower profit.
- Findings should be considered exploratory until reproduced from a validated dataset.

## AI Use Disclosure
AI assistance was used to help organize the analysis, interpret reported outputs, draft recommendations, and prepare documentation and presentation materials. The dataset preparation, calculations, dashboard configuration, and final findings should be checked by the project author. Any AI-assisted text or code should be reviewed and understood before submission.

## Suggested Submission Folder
Place the following items in one clearly named folder, such as `VirtuBox_Data_Analyst_Assessment/`:

```text
VirtuBox_Data_Analyst_Assessment/
├── README.md
├── Superstore_Cleaned_50000.csv
├── analysis_notebook.ipynb  (or analysis.py)
├── VirtuBox_Superstore_Analysis_Presentation.pptx
└── links.txt  (optional: Google Sheet and dashboard URLs)
```

The Google Sheet and Looker Studio dashboard may remain online; include their URLs above if the assessment accepts links.

## Final Submission Checklist
- [ ] Add the Google Sheet URL.
- [ ] Add the Looker Studio dashboard URL.
- [ ] Ensure the assessor has viewer access to both online resources.
- [ ] Include the Python/Colab notebook or script used for calculations and data preparation.
- [ ] Reconcile KPI values and sub-category profit figures across all deliverables.
- [ ] State clearly that the 50,000-row dataset was expanded from the source.
- [ ] Check that the presentation and README do not claim unverified totals as final.
- [ ] Open each submitted file and link once before sending.
