# Gold Layer — Business Analytics

## Objective
Derive transaction-level revenue and create business-oriented analytical datasets.

## Analytics produced
- Monthly Sales Analytics
- Product Performance Analytics
- Country Performance Analytics and Average Order Value
- Customer Analytics and ranking
- Top five products by country (ties can produce more than five rows)
- Month-over-Month Revenue Growth
- Customer Retention and Repeat Purchase Analytics
- Customer Segmentation
- Consolidated Business KPI Table

## Transaction metric
Line-level revenue is calculated as `Quantity × Price` in Gold.

## KPI examples
Total revenue, total quantity, invoice count, identified customer count, Average Order Value, average revenue per customer, average orders per customer, one-time buyers, repeat buyers, repeat-purchase rate and repeat-customer revenue.

Customer-level analyses exclude NULL Customer_ID where a customer identity is required; unidentified sales remain included in overall sales reporting.

## Persisted tables
Gold tables are persisted under `workspace.ecommerce` using Delta, including:
- `gold_monthly_sales`
- `gold_product_performance`
- `gold_country_performance`
- `gold_customer_analytics`
- `gold_top5_products_country`
- `gold_mom_revenue`
- `gold_customer_retention`
- `gold_customer_segmentation`
- `gold_business_kpi`

## Notebook
`notebooks/03_Gold_Final_Table.ipynb`
