# -ecommerce-sql-project-Public-Create
E-Commerce Database built with MySQL - 7 normalized tables, 1000+ records, 7 FK relationships | Data Analyst Project
# E-Commerce Database Management System | MySQL
> A complete 3NF normalized relational database for an E-Commerce platform with 7 tables and 5000+ records.

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Workbench](https://img.shields.io/badge/MySQL_Workbench-00758F?style=for-the-badge&logo=mysql&logoColor=white)
![Records](https://img.shields.io/badge/Records-5000+-blue)
![Tables](https://img.shields.io/badge/Tables-7-orange)

## 📸 Preview
MySQL Workbench Result Grid + ER Diagram (Attach your 2 screenshots here)

## 📊 Project Overview
Designed an end-to-end E-Commerce database `ecommerce_db` to simulate real-world business workflow:
**Customer → Product Browsing → Order → Payment → Review**

This project demonstrates strong fundamentals in Database Design, Normalization, and Analytical Querying - essential for Data Analyst roles.

## 🗂️ Database Schema - 7 Tables

### 1. `categories` (12 records)
Product category master table.
- `category_id` (PK), `category_name`, `description`

### 2. `customers` (800 records)
Customer master with location details.
- `customer_id` (PK), `customer_name`, `email` (UQ), `phone`, `address`, `city`, `state`, `pincode`

### 3. `products` (600 records)
Inventory table linked to categories.
- `product_id` (PK), `category_id` (FK), `product_name`, `price`, `stock_quantity`, `status`

### 4. `orders` (1000 records)
Order transaction header.
- `order_id` (PK), `customer_id` (FK), `order_date`, `order_status`, `total_amount`

### 5. `order_items` (1300 records)
Many-to-Many bridge between Orders & Products.
- `item_id` (PK), `order_id` (FK), `product_id` (FK), `quantity`, `unit_price`

### 6. `payments` (900 records)
Payment details for each order.
- `payment_id` (PK), `order_id` (FK), `amount`, `payment_method` (UPI/COD/Card), `payment_status`, `payment_date`

### 7. `reviews` (388 records)
<img width="1600" height="1141" alt="image" src="https://github.com/user-attachments/assets/763c09fa-c877-4685-8a0c-3dafc890ee6d" />

- `review_id` (PK), `product_id` (FK), `customer_id` (FK), `rating` (1-5), `review_text`

**Total Records: 5000**

## 🔗 ER Diagram & Relationships (1:N)
