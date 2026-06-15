# 🍕 Pizza Sales Analysis — SQL Project

## 📌 Project Overview

This project analyzes a full year of pizza sales data to uncover revenue trends, customer ordering patterns, and product performance — simulating the workflow of a data analyst in the food & beverage industry. The analysis covers everything from basic aggregations to advanced window functions and cumulative revenue tracking.

---

## 📂 Dataset

| Property | Details |
|----------|---------|
| **Period** | January 2015 — December 2015 |
| **Total Orders** | 21,350 |
| **Total Revenue** | $817,860.05 |
| **Pizza Types** | 32 |
| **Categories** | Classic, Supreme, Chicken, Veggie |
| **Sizes** | S, M, L, XL, XXL |
| **Tables** | orders, order_details, pizzas, pizza_types |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **MySQL** | Database setup and all analysis queries |
| **MySQL Workbench** | Query execution |

---

## 🗂️ Project Structure

```
pizza-sales-analysis/
├── orders.csv                  # Order date and time data
├── order_details.csv           # Pizza quantities per order
├── pizzas.csv                  # Pizza sizes and prices
├── pizza_types.csv             # Pizza names, categories, ingredients
├── pizza_analysis.sql          # Full SQL script
└── README.md
```

---

## 🔄 Workflow

### Database Setup
- Created `pizza_db` database with 4 normalized tables
- Defined primary keys and relationships across orders, order_details, pizzas and pizza_types

### Basic Analysis
- Total orders placed and revenue generated
- Highest-priced pizza identification
- Most common pizza size ordered
- Top 5 most ordered pizza types by quantity

### Intermediate Analysis
- Total quantity ordered by pizza category
- Order distribution by hour of the day
- Category-wise pizza count
- Average pizzas ordered per day

### Advanced Analysis
- Top 3 pizzas by revenue
- Percentage revenue contribution by category
- Cumulative revenue over time using window functions
- Top 3 pizzas per category using RANK() and partitioning

---

## 💡 Key Findings

1. **Classic category leads revenue at $220,053** — closely followed by Supreme ($208,197), Chicken ($195,919) and Veggie ($193,690). Revenue is remarkably balanced across all 4 categories, with no single category dominating.

2. **Large size is the most popular** with 18,526 orders — accounting for nearly double the Small (14,137) and XL/XXL combined, suggesting customers prefer sharing-sized pizzas.

3. **The Classic Deluxe Pizza is the bestseller** with 2,453 units sold, followed by Barbecue Chicken (2,432) and Hawaiian (2,422) — top 5 are tightly competitive with under 100 units separating them.

4. **Average of 138 pizzas sold per day** throughout the year — with clear peak hours identifiable from hourly distribution, useful for staffing and kitchen planning.

5. **The Greek XXL is the most expensive pizza at $35.95** — XL and XXL sizes have very low uptake (544 and 28 orders respectively), suggesting premium sizing may need better promotion or pricing adjustment.

---

## 🚀 How to Run

1. Create the database and tables using the `CREATE TABLE` statements in `pizza_analysis.sql`
2. Import the 4 CSV files into their respective tables via MySQL Workbench
3. Execute the queries section by section

---
