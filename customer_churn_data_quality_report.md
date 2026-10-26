# Customer Churn — Data Quality and Exploratory Analysis

## 1. Objective
Audit and clean the supplied synthetic customer churn dataset, summarize its quality, and describe initial churn patterns. This is descriptive analysis, not a predictive model.

## 2. Dataset overview
- Records: 15
- Fields: 11
- Churned customers (`Churn = Yes`): 7 (46.7%)
- Non-churned customers (`Churn = No`): 8 (53.3%)

**Schema note:** The task's screenshot guide describes six fields (`customer_id`, `tenure_months`, `monthly_charge`, `support_tickets`, `contract_type`, `churned`), but the uploaded CSV contains 11 differently named fields: `CustomerID`, `Gender`, `Age`, `TenureMonths`, `SubscriptionType`, `MonthlyCharges`, `TotalCharges`, `ContractType`, `SupportTickets`, `PaymentMethod`, and `Churn`. This report analyzes the actual uploaded CSV and preserves its fields, with column names standardized in the cleaned output. Confirm with the internship provider whether this is the intended dataset.

## 3. Data-quality checks
- Missing cells: 0
- Duplicate full rows: 0
- Duplicate customer IDs: 0
- Negative ages, tenure values, monthly charges, or support-ticket counts: 0
- Total charges consistency: all records satisfy `TotalCharges = MonthlyCharges × TenureMonths` to two decimal places.
- Outliers: no values were removed automatically. Because the dataset contains only 15 records, unusual values should be reviewed with business context rather than assumed to be errors.

## 4. Cleaning actions
1. Standardized column names to lowercase snake_case (for example, `CustomerID` → `customer_id`).
2. Preserved all 15 rows because no duplicate, missing, or clearly invalid values were detected in the checks above.
3. Kept original category values and numeric values unchanged.
4. Added a cleaning log and validation checks in the accompanying workbook.

## 5. Initial exploratory findings
- Overall churn rate: 7/15 = 46.7%.
- Contract type:
  - Month-to-Month: 7 customers, 7 churned, observed churn rate 100%.
  - One Year: 4 customers, 0 churned, observed churn rate 0%.
  - Two Year: 4 customers, 0 churned, observed churn rate 0%.
- Subscription type:
  - Basic: 5 churned out of 7 (71.4%).
  - Pro: 2 churned out of 4 (50.0%).
  - Enterprise: 0 churned out of 4 (0%).
- Average tenure: churned customers 7.0 months; non-churned customers 29.1 months.
- Average support tickets: churned customers 4.29; non-churned customers 1.00.

## 6. Recommendation
**Audience:** The subscription retention team.  
**Decision:** As a first, small pilot, prioritize reviewing month-to-month customers with several recent support tickets and short tenure for a helpful retention check-in.  
**Supporting metrics:** In this sample, all 7 month-to-month customers churned; churned customers averaged 4.29 support tickets versus 1.00 among non-churned customers, and had average tenure of 7.0 months versus 29.1 months.  
**Uncertainty:** The dataset has only 15 synthetic records, and these are descriptive associations, not proof that contract type or support tickets cause churn. The 100% rate in a group of 7 should not be generalized to real customers.  
**Next measurement:** Test a retention outreach pilot and track contact rate, response rate, subsequent churn rate, and an appropriate comparison group over a defined period.

## 7. Files
- `customer_churn_cleaned.csv`: cleaned data with standardized column names.
- `customer_churn_analysis.xlsx`: cleaned data, quality checks, summary statistics, churn breakdowns, and cleaning log.

