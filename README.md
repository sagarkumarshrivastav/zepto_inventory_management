📦 Zepto Inventory Management System
📌 Project Overview

The Zepto Inventory Management System is a database-driven data analytics project built using a real-world inventory dataset sourced from Kaggle. The project focuses on exploring, cleaning, and analyzing inventory data to derive meaningful business insights related to product availability, pricing, discounts, and category-wise performance.

This project demonstrates practical SQL skills including table design, data exploration, data cleaning, and solving real-life business problems using structured queries.

🗂 Dataset Information

Source: Kaggle (Zepto Inventory Dataset)

Domain: Quick Commerce / Retail Inventory

Format: CSV (imported into PostgreSQL)

Key Attributes:

SKU ID

Product Category & Name

MRP & Discounted Selling Price

Discount Percentage

Available Quantity

Product Weight

Stock Availability

🛠️ Tech Stack

Database: PostgreSQL

Language: SQL

Tool: pgAdmin / Any SQL Client

Dataset Source: Kaggle

🏗️ Database Schema
CREATE TABLE zepto(
    sku_id SERIAL PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INTEGER,
    discountedSellingPrice NUMERIC(8,2),
    weightInGms INTEGER,
    outOfStock BOOLEAN,
    quantity INTEGER
);

🔍 Data Exploration

The following exploratory operations were performed:

Total number of products in the inventory

Sampling records to understand data structure

Identification of null values across columns

Listing unique product categories

Analyzing in-stock vs out-of-stock products

Identifying duplicate product names across SKUs

🧹 Data Cleaning

Key data cleaning steps included:

Identifying and removing products with invalid pricing (MRP = 0)

Converting prices from paise to rupees

Ensuring consistency in pricing and quantity-related fields

Example:

UPDATE zepto
SET mrp = mrp / 100.0,
    discountedSellingPrice = discountedSellingPrice / 100.0;

📊 Business Problems & SQL Analysis

The project answers real-world business questions such as:

1️⃣ Top 10 Best-Value Products

Identified products offering the highest discount percentages.

2️⃣ High-MRP Products That Are Out of Stock

Found expensive products that are currently unavailable.

3️⃣ Estimated Revenue by Category

Calculated potential revenue using discounted price and available quantity.

4️⃣ Premium Products with Low Discounts

Filtered products with MRP > ₹500 and discount < 10%.

5️⃣ Categories with Highest Average Discounts

Ranked categories based on average discount percentage.

6️⃣ Best Value Products by Price per Gram

Analyzed unit pricing for products weighing over 100 grams.

7️⃣ Product Weight Classification

Grouped products into Low, Medium, and Bulk categories.

8️⃣ Total Inventory Weight by Category

Measured total inventory load per category.

📈 Key Learnings

Hands-on experience with real-world retail data

Strong understanding of SQL CRUD operations

Practical use of aggregation, filtering, grouping, and CASE statements

Business-focused analytical thinking using data

Experience with inventory and pricing analytics

🚀 Future Enhancements

Build interactive dashboards using Power BI / Tableau

Integrate Python for advanced analytics

Add time-based sales forecasting

Create a web-based inventory management interface

📌 Conclusion

This project showcases how SQL can be effectively used to manage, clean, and analyze inventory data in a fast-paced quick-commerce environment. It is ideal for demonstrating database fundamentals, analytical problem-solving, and real-world business insights.
