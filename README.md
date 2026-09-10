# Databricks Sales Analytics Project

This repository contains a complete sales analytics project built with Databricks, demonstrating data cleansing, transformation, and analysis workflows.

## Project Overview

This project analyzes sales data to provide insights into:
- Total sales revenue and order metrics
- Product category performance
- Regional sales distribution
- Sales channel effectiveness
- Customer behavior patterns
- Monthly sales trends

## Repository Contents

### 1. Data_Import_and_Cleansing.ipynb
This notebook handles the ETL (Extract, Transform, Load) process:
- Data import and initial exploration
- Handling missing values and data quality issues
- Removing duplicates based on TransactionID
- Standardizing categorical data (ProductCategory formatting)
- Filtering invalid records (negative quantities/prices)
- Calculating derived metrics (SalesAmount)
- Creating the gold_sales table for analytics

### 2. Sales_Dashboard.ipynb
This notebook contains SQL queries for dashboard visualizations and analytics:
- Key metrics: Total Sales, Orders, Units Sold, Average Order Value
- Monthly sales trends analysis
- Sales breakdown by Product Category, Region, and Channel
- Top 10 products by sales performance
- Comprehensive data exploration queries

### 3. Sales_Perfomance_Dashboard.lvdash.json
The Databricks AI/BI Lakeview Dashboard configuration file with:
- **Overview Page**: Key metrics (Total Sales, Orders, Units Sold, Average Order Value) and visualizations showing sales trends by month, product category, region, and channel
- **Customer & Behavioral Analytics Page**: Customer insights including unique customers, average items per order, discount analysis, and behavioral patterns
- **Global Filters Page**: Interactive filters for dynamic data exploration

To use this dashboard:
1. Import the `.lvdash.json` file into your Databricks workspace
2. Connect it to your `gold_sales` table
3. The dashboard will automatically render with all visualizations

## Data Model

The `gold_sales` table includes:
- **TransactionID**: Unique identifier for each transaction
- **TransactionDate**: Date of the transaction
- **CustomerID**: Customer identifier
- **ProductID**: Product identifier
- **ProductCategory**: Category (Electronics, Office, Home, Accessories)
- **ProductName**: Name of the product
- **Quantity**: Number of units sold
- **UnitPrice**: Price per unit
- **Discount**: Discount applied (0-1)
- **SalesAmount**: Calculated total sales amount
- **PaymentMethod**: Payment method used
- **StoreRegion**: Regional location
- **SalesChannel**: Online or Store
- **CustomerType**: New or Existing customer
- **OrderStatus**: Status of the order

## Technologies Used

- **Databricks**: Cloud data platform
- **Apache Spark (PySpark)**: Distributed data processing
- **SQL**: Data analysis and querying
- **Delta Lake**: Data storage and management
- **Lakeview**: Interactive dashboards and visualizations

## Getting Started

1. Import the notebooks into your Databricks workspace
2. Ensure you have access to the source sales data
3. Run `Data_Import_and_Cleansing.ipynb` to create the gold_sales table
4. Run queries in `Sales_Dashboard.ipynb` to analyze the data
5. Import `Sales_Perfomance_Dashboard.lvdash.json` to view the interactive dashboard

## Dashboard Features

The Sales Performance Dashboard includes:
- **Interactive visualizations**: Charts and graphs for exploring sales data
- **Key performance indicators**: Real-time metrics tracking
- **Multi-page layout**: Organized views for different analytical perspectives
- **Filters**: Dynamic filtering capabilities for focused analysis

## Author

Olwethu Boqwana

## Date

Created: September 2026
