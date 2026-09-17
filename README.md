# E-Commerce Sales Analysis – Power BI

## 📌 Project Overview

This project focuses on transforming, cleaning, merging, and modeling e-commerce sales data using **Microsoft Power BI** and **Power Query**.

The project demonstrates data transformation techniques, custom and conditional columns, data merging, Group By operations, data quality checks, and relationship creation between tables.

---

## 🎯 Objectives

- Import and transform e-commerce datasets using Power Query
- Clean and prepare data for analysis
- Create a Location column using City and State
- Calculate Profit Margin
- Create Profit Status categories
- Merge Order data with Order Details
- Check missing values and duplicates
- Sort and filter the transformed data
- Perform Group By operations
- Create relationships between tables
- Prepare a structured Power BI data model

---

## 📂 Dataset Files

The project uses the following CSV files:

1. **List of Orders.csv**
2. **Order Details.csv**
3. **Sales target.csv**

---

## 🔄 Data Transformation

The following transformations were performed using Power Query:

### List of Orders

- Restricted the dataset to the first 500 rows
- Converted `Order Date` to Date format
- Applied Proper Case to `CustomerName`
- Merged `City` and `State` into a new `Location` column

Example:

`Chennai, Tamil Nadu`

### Order Details

- Converted `Amount` to Fixed Decimal Number
- Created a custom column:

`Profit Margin = Profit / Amount`

- Created a conditional column:

| Profit Condition | Profit Status |
|---|---|
| Profit < 0 | Loss |
| Profit = 0 | Break-Even |
| Profit > 0 | Profit |

### Orders Data

- Merged `List of Orders` with `Order Details` using `Order ID`
- Expanded the required Order Details columns
- Checked for missing values
- Checked for duplicate records
- Sorted `Order Date` in descending order
- Applied a State filter for Tamil Nadu as part of the transformation check

### Group By Operations

#### Order Details Group By

Grouped by:

`Sub-Category`

Calculated:

`Total Amount`

using the Sum operation.

#### Sales Target Group By

Grouped by:

`Month of Order Date`

Calculated:

`Total Target`

using the Sum operation.

---

## 🔗 Data Modeling

The Power BI model contains the following main tables:

- `List of Orders`
- `Order Details`
- `Orders Data`
- `Sales target`
- `Order Details Group By`
- `Sales Target Group By`

The required relationships include:

### Relationship 1

`List of Orders[Order ID]`

↕

`Order Details[Order ID]`

### Relationship 2

`Order Details[Category]`

↕

`Sales target[Category]`

The relationships were created in Power BI Model View as part of the data modeling process.

---

## 🛠️ Tools Used

- Microsoft Power BI Desktop
- Power Query
- CSV datasets
- Microsoft Word

---

## 📸 Project Documentation

The project includes screenshots documenting:

1. List of Orders – Initial Data
2. Location Merge – City, State
3. Profit Margin & Profit Status
4. Orders Data – Merge & Expand
5. Missing Values & Duplicate Check
6. Sort by Order Date & State Filter
7. Order Details – Total Amount by Sub-Category
8. Sales Target – Total Target by Month
9. Data Modeling – Relationships

---

## 📁 Project Structure

```text
E-Commerce Sales Analysis/
│
├── E-Commerce_Sales_Analysis_PowerBI.pbix
├── E-Commerce_Sales_Analysis_Report.docx
├── List of Orders.csv
├── Order Details.csv
├── Sales target.csv
├── README.md
│
└── Screenshots/
    ├── Screenshot 1
    ├── Screenshot 2
    ├── Screenshot 3
    ├── Screenshot 4
    ├── Screenshot 5
    ├── Screenshot 6
    ├── Screenshot 7
    ├── Screenshot 8
    └── Screenshot 9
