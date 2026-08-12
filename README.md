# QueryMart Retail Sales Database

## 📌 Project Overview

**QueryMart Retail Sales Database** is a SQL-based retail data analysis project focused on exploring and analyzing customer, product, warehouse, order, and order-item data.

The project uses **SQLite** and **Python/Pandas** to interact with the retail database and answer practical business questions using SQL queries.

The analysis covers product categories, pricing, customer information, and order-item revenue.

---

## 🎯 Objectives

The main objectives of this project are to:

* Explore the structure of a retail sales database
* Understand customer and product data
* Analyze products across different categories
* Identify high-priced products
* Calculate average order-item revenue
* Practice SQL filtering, grouping, aggregation, and sorting
* Extract useful business insights from retail data

---

## 🗄️ Database Structure

The QueryMart database contains five main tables:

| Table         | Description                                                        |
| ------------- | ------------------------------------------------------------------ |
| `customers`   | Customer details including city, age, gender, and customer segment |
| `products`    | Product information including category and unit price              |
| `warehouses`  | Warehouse-related information                                      |
| `orders`      | Customer order information                                         |
| `order_items` | Individual items within customer orders                            |

## The `customers` table contains **1,000 customer records**, while the `products` table contains **50 products** across five categories.

## 🛠️ Tools & Technologies

* **Python**
* **SQL**
* **SQLite**
* **Pandas**
* **Google Colab**
* **Jupyter Notebook**

### Python Libraries

```python
import sqlite3
import requests
import pandas as pd
```

## The notebook connects to the SQLite database and uses Pandas to execute SQL queries and display the results.

## 📊 Analysis Performed

### 1. Database Exploration

The project begins by identifying the tables available in the database:

```sql
SELECT name
FROM sqlite_master
WHERE type='table';
```

This returns:

* customers
* products
* warehouses
* orders
* order_items

### 2. Product Analysis

The project analyzes:

* Total number of products
* Number of products in each category
* Average product price by category
* Most expensive products
* Products priced above ₹10,000

There are **50 products**, with **10 products in each of the five categories**: Beauty, Electronics, Fashion, Grocery, and Home.

### 3. Customer Analysis

Customer data includes:

* Customer ID
* Customer name
* City
* Age
* Gender
* Customer segment

The dataset contains customer segments such as **Regular, Premium, and VIP**.

### 4. Revenue Analysis

The project calculates the average `net_amount` from the `order_items` table.

The notebook calculates an average order-item revenue of approximately **₹59,345.77**.

---

## 🔍 Example SQL Queries

### Count Total Products

```sql
SELECT COUNT(*)
FROM products;
```

### Products by Category

```sql
SELECT category, COUNT(*)
FROM products
GROUP BY category;
```

### Average Price by Category

```sql
SELECT
    category,
    COUNT(*),
    AVG(unit_price)
FROM products
GROUP BY category;
```

### Top 5 Most Expensive Products

```sql
SELECT *
FROM products
ORDER BY unit_price DESC
LIMIT 5;
```

### Products Above ₹10,000

```sql
SELECT *
FROM products
WHERE unit_price > 10000;
```

The notebook finds **36 products** with a unit price greater than ₹10,000.

---

## 📈 Key Findings

Some observations from the analysis include:

* The database contains **5 major tables**.
* There are **1,000 customers**.
* There are **50 products**.
* Products are divided equally across five categories, with **10 products per category**.
* Electronics has the highest average unit price among the five categories at approximately **₹26,054.82**.
* The average `net_amount` in `order_items` is approximately **₹59,345.77**.
* **36 products** have a unit price above ₹10,000.
* The highest-priced product shown in the analysis is the **Electric Kettle**, priced at approximately **₹48,498.50**.

---

## 📂 Project Structure

```text
querymart-retail-sales-analysis/
│
├── QueryMart.db
├── QueryMart_Retail_Sales.ipynb
├── README.md
└── requirements.txt
```

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/querymart-retail-sales-analysis.git
```

### 2. Install Required Libraries

```bash
pip install pandas requests
```

### 3. Open the Notebook

Open:

```text
QueryMart_Retail_Sales.ipynb
```

You can run the notebook using **Google Colab** or **Jupyter Notebook**.

### 4. Run the SQL Analysis

The notebook establishes a SQLite connection and uses Pandas to execute SQL queries against the database.

---

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

* SQL querying
* SQLite database
* Database exploration
* Data aggregation
* `GROUP BY`
* `ORDER BY`
* `WHERE`
* `COUNT()`
* `AVG()`
* Filtering
* Sorting
* Relational data analysis
* Python and Pandas
* Business-oriented data analysis

---

## 👨‍💻 Author

**Rohit Kumar Gautam**

Data Analytics | SQL | Python | Pandas | Power BI

---

## ⭐ Project Purpose

This project was created as a practical SQL and data analytics portfolio project to strengthen database querying, data exploration, and business analysis skills.
