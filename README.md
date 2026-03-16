# 🛒 Walmart Sales Data Analysis Project

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange?logo=mysql)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green?logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A beginner-friendly end-to-end data analysis project using **Python** and **MySQL** on Walmart's retail sales data. This project covers data cleaning, database integration, and answering real business questions using SQL.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Project Workflow](#project-workflow)
- [Business Questions Solved](#business-questions-solved)
- [How to Run This Project](#how-to-run-this-project)
- [Project Structure](#project-structure)
- [Key Learnings](#key-learnings)
- [Connect With Me](#connect-with-me)

---

## 📖 About the Project

This project analyzes Walmart's sales transactions to uncover patterns in customer behavior, sales performance, and profitability. It is designed as a **beginner portfolio project** to demonstrate skills in:

- Data cleaning with **Python (Pandas)**
- Loading data into a **MySQL** database using SQLAlchemy
- Writing **SQL queries** to answer business questions

---

## 📊 Dataset

| Property        | Details                          |
|-----------------|----------------------------------|
| Source          | Walmart Sales Dataset (CSV)      |
| Total Records   | ~10,000 transactions             |
| Time Period     | 2019 – 2023                      |
| Cities Covered  | Multiple cities across Texas, USA|

### Columns in the Dataset

| Column           | Description                              |
|------------------|------------------------------------------|
| `invoice_id`     | Unique transaction ID                    |
| `branch`         | Walmart branch code                      |
| `city`           | City where the branch is located         |
| `category`       | Product category                         |
| `unit_price`     | Price per item                           |
| `quantity`       | Number of items purchased                |
| `date`           | Date of transaction                      |
| `time`           | Time of transaction                      |
| `payment_method` | Cash / Ewallet / Credit Card             |
| `rating`         | Customer rating (1–10)                   |
| `profit_margin`  | Profit margin percentage                 |
| `total`          | Total transaction value                  |

**Product Categories:** Health & Beauty, Electronic Accessories, Home & Lifestyle, Sports & Travel, Food & Beverages, Fashion Accessories

---

## 🛠️ Tech Stack

| Tool          | Purpose                            |
|---------------|------------------------------------|
| Python 3.8+   | Data cleaning & preprocessing      |
| Pandas        | Data manipulation                  |
| MySQL 8.0     | Data storage & querying            |
| SQLAlchemy    | Python ↔ MySQL connection          |
| PyMySQL       | MySQL adapter for Python           |
| Jupyter Notebook | Interactive development        |

---

## 🔄 Project Workflow

```
Raw CSV Data
     ↓
Python (Pandas) — Data Cleaning
     ↓
MySQL Database — Data Loading via SQLAlchemy
     ↓
SQL Queries — Business Analysis
     ↓
Insights & Conclusions
```

### Step 1 — Data Cleaning (Python)
- Loaded raw `Walmart.csv` using Pandas
- Removed duplicate records
- Handled missing/null values
- Fixed data types (dates, prices)
- Added a computed `total` column (`unit_price × quantity`)
- Saved cleaned data as `cleaned_walmart.csv`

### Step 2 — Load Data into MySQL
- Created a MySQL database `walmart_db`
- Used **SQLAlchemy** + **PyMySQL** to push the cleaned DataFrame directly into MySQL
- Verified data with basic SQL checks

### Step 3 — SQL Analysis
- Wrote 9 business-focused SQL queries
- Used concepts like `GROUP BY`, `RANK()`, `CASE WHEN`, `CTEs`, and `Window Functions`

---

## 💼 Business Questions Solved

| # | Question |
|---|----------|
| Q1 | What are the different payment methods, number of transactions, and quantity sold per method? |
| Q2 | Which category has the highest average rating in each branch? |
| Q3 | What is the busiest day of the week for each branch? |
| Q4 | What is the total quantity of items sold per payment method? |
| Q5 | What are the average, min, and max ratings for each category in each city? |
| Q6 | Which product category generates the highest total profit? |
| Q7 | What is the most preferred payment method for each branch? |
| Q8 | How are sales distributed across Morning, Afternoon, and Evening shifts? |
| Q9 | Which 5 branches had the highest revenue decline from 2022 to 2023? |

---

## ▶️ How to Run This Project

### Prerequisites
Make sure you have the following installed:
- Python 3.8+
- MySQL Server
- Jupyter Notebook

### 1. Clone this Repository
```bash
git clone https://github.com/your-username/walmart-sales-analysis.git
cd walmart-sales-analysis
```

### 2. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 3. Set Up MySQL Database
Open MySQL and run:
```sql
CREATE DATABASE walmart_db;
```

### 4. Run the Jupyter Notebook
```bash
jupyter notebook project.ipynb
```
> Update the MySQL connection string in the notebook with your own username and password.

### 5. Run SQL Queries
Open `walmart_sql_queries.sql` in MySQL Workbench and execute the queries on the `walmart_db` database.

---

## 📁 Project Structure

```
walmart-sales-analysis/
│
├── Walmart.csv                  # Raw dataset
├── cleaned_walmart.csv          # Cleaned dataset (output of notebook)
├── project.ipynb                # Jupyter Notebook (cleaning + DB loading)
├── walmart_sql_queries.sql      # All SQL business queries
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## 📚 Key Learnings

- How to clean real-world messy data using **Pandas**
- How to connect Python to **MySQL** using SQLAlchemy
- Writing advanced SQL queries using **Window Functions** and **CTEs**
- Breaking down business problems into analytical queries
- End-to-end project workflow from raw data to insights

