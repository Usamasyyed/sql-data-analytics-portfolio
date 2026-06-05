# SQL Data Analytics Portfolio Project

This repository showcases a SQL Server analytics workflow built around a sales data warehouse. The project covers database setup, exploratory analysis, business KPI development, customer segmentation, product performance analysis, and reporting views.

## Project Overview

The project uses a simple star-schema style analytics layer:

- `gold.dim_customers`: customer profile attributes such as country, gender, marital status, and birthdate.
- `gold.dim_products`: product catalog attributes such as category, subcategory, product line, and cost.
- `gold.fact_sales`: order-level sales facts including order dates, revenue, quantity, and price.

The SQL scripts move from foundational exploration to analysis-ready reporting views. They are organized so the project can be reviewed step by step or used as a reference for common business analytics patterns in SQL.

## Repository Structure

```text
.
├── datasets/
│   ├── DataWarehouseAnalytics.bak
│   └── flat-files/
│       ├── dim_customers.csv
│       ├── dim_products.csv
│       └── fact_sales.csv
├── reports/
│   └── sql-data-analytics-report.pdf
├── scripts/
│   ├── 00_init_database.sql
│   ├── 01_database_exploration.sql
│   ├── ...
│   ├── 12_report_customers.sql
│   └── 13_report_products.sql
├── LICENSE
└── README.md
```

## Analysis Areas

- Database and schema creation for a SQL Server analytics database.
- Dimension exploration for countries, categories, subcategories, and product lines.
- Date range analysis for customer birthdates and order history.
- Measures and KPI exploration for sales, orders, quantity, products, and customers.
- Magnitude analysis by geography, gender, category, and customer.
- Ranking analysis for top and bottom products and customers.
- Change-over-time and cumulative trend analysis.
- Product and customer segmentation using revenue, lifespan, and behavioral metrics.
- Reporting views for customer-level and product-level analytics.

## Skills Demonstrated

- SQL Server database setup and schema design.
- Data loading with `BULK INSERT`.
- Joins across fact and dimension tables.
- Aggregations and KPI calculation.
- Window functions for ranking and performance comparisons.
- Time-series analysis with `DATETRUNC`, `FORMAT`, and cumulative totals.
- Customer segmentation using `CASE` expressions.
- Reporting view creation with common table expressions.
- Analytics documentation for a portfolio-ready repository.

## How To Use

1. Open SQL Server Management Studio or Azure Data Studio.
2. Update the file paths in `scripts/00_init_database.sql` if your local clone is not stored under `C:\sql\sql-data-analytics-portfolio`.
3. Run `scripts/00_init_database.sql` to create and load the `DataWarehouseAnalytics` database.
4. Run the exploration and analysis scripts in numerical order.
5. Run `scripts/12_report_customers.sql` and `scripts/13_report_products.sql` to create reusable reporting views.

> Warning: `scripts/00_init_database.sql` drops and recreates the `DataWarehouseAnalytics` database if it already exists.

## Key Deliverables

- SQL scripts for end-to-end data analytics practice.
- Customer reporting view with customer segment, recency, average order value, and monthly spend metrics.
- Product reporting view with product segment, average selling price, average order revenue, and monthly revenue metrics.
- Short portfolio report available at `reports/sql-data-analytics-report.pdf`.

## License

This project is distributed under the MIT License. The original license notice is preserved in `LICENSE`.
