# E-Commerce Sales & Customer Analytics Dashboard

## Project Overview

The **E-Commerce Sales & Customer Analytics Dashboard** is a Power BI-based business intelligence project developed to analyze e-commerce sales, product performance, customer behavior, geographical performance, and order and delivery operations.

The project transforms raw e-commerce data into meaningful KPIs, interactive visualizations, and business insights to support data-driven decision-making.

## Objectives

- Analyze overall sales and revenue performance.
- Identify high-performing products, categories, and brands.
- Understand customer behavior and purchasing patterns.
- Analyze sales and order performance across states and cities.
- Monitor order status, cancellations, returns, payment methods, and delivery performance.
- Provide interactive dashboards for business analysis and decision-making.

## Datasets

| Dataset | Records | Description |
|---|---:|---|
| Sales | 250,000 | Order, sales, pricing, payment, status, delivery, and location information |
| Products | 2,000 | Product, category, brand, pricing, discount, stock, and rating information |
| Customers | 40,000 | Customer, demographic, location, registration, tier, order, and spending information |
| Dim_Date | — | Date, year, quarter, month, and year-month information |

## Data Assessment & Cleaning

The datasets were assessed before modelling and dashboard development.

Main checks included:

- Missing and null values
- Duplicate records
- Data types
- Inconsistent categorical values
- Date fields
- Key fields such as `Order_ID`, `Customer_ID`, and `Product_ID`
- Data consistency and relationship suitability

Data cleaning and transformation were performed to prepare the datasets for reliable analysis.

> **Note:** A duplicate `Order_ID` does not necessarily represent a duplicate transaction because one order can contain multiple products.

## Data Model

The project uses a **star-schema approach**.

### Tables

- **Sales** – Central fact table containing transactional data.
- **Products** – Product dimension.
- **Customers** – Customer dimension.
- **Dim_Date** – Date dimension.

### Main Relationships

```text
Customers (1) ─────── (*) Sales
Products  (1) ─────── (*) Sales
Dim_Date  (1) ─────── (*) Sales
```

## Key KPIs

- Total Sales
- Total Orders
- Total Quantity Sold
- Total Customers
- Average Order Value
- Sales Growth %
- Total Discount
- Cancellation Rate
- Return Rate
- Average Delivery Days
- Average Customer Spending
- Average Orders per Customer
- Total Products
- Average Product Rating

## Dashboard Pages

### 1. Sales Overview
Provides an overall view of sales performance, orders, quantity sold, customers, sales trends, categories, payment modes, and order status.

### 2. Product & Category Analysis
Analyzes product, category, and brand performance using sales, quantity, ratings, and discount information.

### 3. Customer Analysis
Analyzes customer segments, spending, order frequency, age groups, gender, and top customers.

### 4. Geographical Analysis
Analyzes sales, orders, and quantity sold across different states and cities.

### 5. Order & Delivery Analysis
Monitors order status, cancellations, returns, payment methods, and delivery performance.

## Key Business Insights

- The dashboard provides an overall view of e-commerce sales and order performance.
- Customer analysis helps identify valuable customer segments and purchasing patterns.
- Product and category analysis helps identify high-performing products and categories.
- Geographical analysis highlights differences in sales and order performance across locations.
- Order and delivery analysis helps monitor cancellations, returns, and delivery performance.
- Discount analysis can help evaluate the relationship between discounts and sales.

## Recommendations

- Focus on high-performing products and categories.
- Improve customer retention through loyalty strategies.
- Reduce order cancellations and returns.
- Improve delivery performance in locations with longer delivery times.
- Optimize discounts and promotional strategies.
- Monitor key KPIs regularly for better decision-making.

## Limitations

- The project uses only the available sales, product, and customer datasets.
- The dashboard does not provide real-time data.
- Detailed reasons for cancellations and returns are not available.
- Detailed delivery and courier information is not included.
- The project does not include sales forecasting or predictive analysis.
- External factors such as competitors and market trends are not considered.

## Tools & Technologies

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **CSV datasets**

## Project Structure

```text
E-Commerce-Sales-Customer-Analytics/
│
├── Data/
│   ├── sales.csv
│   ├── products.csv
│   └── customers.csv
│
├── PowerBI/
│   └── E-Commerce Sales & Customer Analytics Dashboard.pbix
│
├── Documentation/
│   ├── BRD
│   ├── FRD
│   ├── Dataset Assessment
│   ├── Testing Checklist
│   └── Analysis Report
│
└── README.md
```

## Conclusion

This project demonstrates how Power BI can be used to transform e-commerce data into an interactive analytical solution. The dashboard provides insights into sales, products, customers, geographical performance, and order and delivery operations, helping stakeholders make data-driven business decisions.
