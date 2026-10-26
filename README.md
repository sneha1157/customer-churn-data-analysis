# EdVyro Data Analytics — Task 2: Business KPI Dashboard

## Deliverables
- `Business_KPI_Dashboard.html` — interactive browser dashboard with KPI cards, charts, and filters.
- `customer_churn_cleaned.csv` — cleaned CSV with standardized snake_case column names.
- `customer_churn_analysis.xlsx` — workbook containing cleaned data, KPI summary, data-quality checks, and category breakdowns.
- `customer_churn_sample (3).csv` — original input dataset (keep only if you are allowed to redistribute it).

## How to view the dashboard
1. Download `Business_KPI_Dashboard.html`.
2. Open it in Chrome or Edge while connected to the internet.
3. Use the Contract Type, Tenure Group, and Payment Method filters. KPI cards and charts update together.

## KPI definitions
- Churn rate = churned customers / filtered customers.
- Retention rate = retained customers / filtered customers.
- Monthly revenue at risk (proxy) = sum of monthly charges for churned customers in the filtered data.
- Average tenure = mean tenure in months for filtered customers.

## Important limitations
This is a small synthetic dataset of 15 records. Treat the charts as an illustrative analysis, not as statistically reliable generalizations. Revenue at risk is a monthly-charge proxy, not lifetime revenue. The HTML dashboard uses Plotly from a CDN and therefore needs an internet connection.

## Publishing / submission
GitHub can host the HTML file via GitHub Pages if the repository is configured for Pages. Upload the HTML, cleaned CSV, workbook, and this README. Then enable Pages in the repository settings and submit the resulting public page URL if the task permits public hosting. Do not publish private or sensitive data.
