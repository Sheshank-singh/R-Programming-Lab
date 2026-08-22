# Experiment 03 — Multi-Source Retail Sales Data Integration and Analysis

## Domain
Retail Analytics

## Objective

The objective of this experiment is to perform end-to-end retail data
processing using the UCI Online Retail dataset.

The supplied dataset is provided as a single Excel file. To simulate a
multi-source retail environment, the dataset is logically separated into
three data sources:

- Transaction Data
- Product Data
- Customer Data

These logical sources are cleaned, integrated using `dplyr` joins, analyzed
for sales and customer performance, and finally stored in a SQLite database.

## Dataset

**UCI Online Retail Dataset**

The dataset contains retail transaction information including:

- InvoiceNo
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- CustomerID
- Country

## Tasks Performed

### Task 1 — Import and Clean

- Imported the Excel dataset using `readxl`
- Checked dataset dimensions and structure
- Identified missing values
- Removed duplicate records
- Removed invalid quantities
- Removed invalid unit prices
- Created logical transaction, product and customer datasets
- Calculated Revenue = Quantity × UnitPrice

### Task 2 — Data Integration

The logical datasets were integrated using:

- `left_join()` on `StockCode`
- `left_join()` on `CustomerID`

Unmatched product and customer records were also identified.

### Task 3 — Sales and Customer Analysis

The analysis includes:

- Total sales revenue
- Top 5 products by revenue
- Top 5 countries by revenue
- Top 5 customers by purchase value
- Customer value segmentation
- High-performing and underperforming markets

Customer segments:

- Low Value
- Medium Value
- High Value
- Premium

The segmentation thresholds are determined using quartiles of customer
purchase values and implemented using `case_when()`.

### Task 4 — SQLite Database

The final integrated dataset is stored in:

`retail_sales.db`

Table:

`retail_sales`

SQL queries are executed from R to obtain:

- Top 5 customers by revenue
- Revenue by country
- Overall retail performance

## Technologies

- R
- dplyr
- readxl
- tidyr
- DBI
- RSQLite
- ggplot2
- SQL
- SQLite

## Deliverables

- R Markdown notebook
- PDF report
- SQLite database
- Business insights
