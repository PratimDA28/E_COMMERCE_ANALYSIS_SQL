# 🛍️ E-Commerce Data Analysis Using SQL

## 📑 Overview
This project demonstrates how to use **SQL** to solve real-world **business challenges** in an e-commerce environment. The queries and procedures in this project answer key questions related to **sales, customer behavior, inventory management, revenue analysis, and operational performance**.

---

## 🗂️ Project Structure

### 1️⃣ Database Setup
- Created the `AMAZON_db` database.
- Designed and normalized relational tables to reflect e-commerce business operations.

### 2️⃣ Data Import
- Inserted sample but realistic data across all tables to simulate actual business activity.

### 3️⃣ Data Cleaning
- Removed nulls where necessary and enforced data integrity for accurate analysis.

### 4️⃣ Business Problems Solved
- Addressed **15 real-world scenarios** using advanced SQL queries and stored procedures.

---

## 🖼️ Entity Relationship Diagram (ERD)
Visual representation of how all tables are connected to form the database.

📌 _[Insert ERD image or link here]_  

---

## 🚀 Project Highlights

| Business Problem | Description |
|------------------|-------------|
| 🔝 Top Selling Products | Identify top-selling products by total sales value |
| 💰 Revenue by Category | Calculate revenue per category and its percentage contribution |
| 📦 Average Order Value | For customers with >5 orders |
| 📅 Monthly Sales Trend | Track month-wise sales for the past year |
| 🙋‍♂️ Customers with No Purchases | Find users who registered but didn’t order |
| 📉 Least Selling Category by State | Identify weak-performing categories by location |
| 🏆 Customer Lifetime Value | Rank users by overall spending |
| 🚨 Inventory Stock Alerts | Alert for products below stock threshold |
| ⏳ Shipping Delays | Orders shipped 3+ days after placement |
| ✅ Payment Success Rates | % of successful payments vs total |
| 🧑‍💼 Top Performing Sellers | Rank sellers by sales |
| 🧮 Product Profit Margin | Rank products by (Price - COGS) |
| 🔁 Most Returned Products | Highest return count per product |
| 💤 Inactive Sellers | No sales in last 6 months |
| 🔁 Stored Procedure for Sales | Automatically update inventory after sale |

---

## 🧠 Learning Outcomes

- 🧩 Mastered joins, aggregations, window functions & subqueries.
- 📈 Analyzed business KPIs and sales trends effectively.
- 🛠️ Wrote a stored procedure to automate stock update.
- 🧾 Derived meaningful insights for **inventory**, **revenue**, and **customer management**.

---

## 🧱 Database Schema

### 1. `category`
Stores product categories.
| Column | Type | Description |
|--------|------|-------------|
| category_id | INT (PK) | Unique ID |
| category_name | VARCHAR(20) | Name of category |

### 2. `customers`
| Column | Type | Description |
|--------|------|-------------|
| customer_id | INT (PK) | Unique ID |
| first_name | VARCHAR(20) | First name |
| last_name | VARCHAR(20) | Last name |
| state | VARCHAR(20) | State of residence |

### 3. `sellers`
| Column | Type | Description |
|--------|------|-------------|
| seller_id | INT (PK) | Unique ID |
| seller_name | VARCHAR(25) | Seller's name |
| origin | VARCHAR(10) | Origin location |

### 4. `products`
| Column | Type | Description |
|--------|------|-------------|
| product_id | INT (PK) | Unique ID |
| product_name | VARCHAR(50) | Name |
| price | FLOAT | Selling price |
| cogs | FLOAT | Cost of goods sold |
| category_id | INT (FK) | Linked to `category` |

### 5. `orders`
| Column | Type | Description |
|--------|------|-------------|
| order_id | INT (PK) | Unique ID |
| order_date | DATE | Date of order |
| customer_id | INT (FK) | Linked to `customers` |
| seller_id | INT (FK) | Linked to `sellers` |
| order_status | VARCHAR(15) | Status (e.g., completed, pending) |

### 6. `order_items`
| Column | Type | Description |
|--------|------|-------------|
| order_item_id | INT (PK) | Unique ID |
| order_id | INT (FK) | Linked to `orders` |
| product_id | INT (FK) | Linked to `products` |
| quantity | INT | No. of units |
| price_per_unit | FLOAT | Unit price |

### 7. `payments`
| Column | Type | Description |
|--------|------|-------------|
| payment_id | INT (PK) | Unique ID |
| order_id | INT (FK) | Linked to `orders` |
| payment_date | DATE | Date of payment |
| payment_status | VARCHAR(20) | Status |

### 8. `shippings`
| Column | Type | Description |
|--------|------|-------------|
| shipping_id | INT (PK) | Unique ID |
| order_id | INT (FK) | Linked to `orders` |
| shipping_date | DATE | Shipped date |
| return_date | DATE | Returned date (if any) |
| shipping_providers | VARCHAR(15) | Provider name |
| delivery_status | VARCHAR(15) | Delivery status |

### 9. `inventory`
| Column | Type | Description |
|--------|------|-------------|
| inventory_id | INT (PK) | Unique ID |
| product_id | INT (FK) | Linked to `products` |
| stock | INT | Units in stock |
| warehouse_id | INT | Warehouse ID |
| last_stock_date | DATE | Last update date |

---

## ⚙️ Technologies Used

- SQL (PostgreSQL / MySQL compatible syntax)
- Stored Procedures
- Data Modeling & Relational Design
- Git & GitHub for version control

---

## 📂 Want to Explore More?

Check out the full project, download the SQL files, and run them in your SQL environment!

🧠 Ideal for:  
- Beginners practicing SQL queries  
- Analysts looking to work with real-world e-commerce data  
- Portfolio enhancement for job seekers

---

## 📬 Connect with Me

- 💼 [LinkedIn](https://www.linkedin.com/in/your-profile)
- 📧 [Email](mailto:your.email@example.com)
- 📊 Portfolio: [YourWebsite.com](https://yourwebsite.com)

---

> **Note**: All data used in this project is sample data for educational purposes only.

