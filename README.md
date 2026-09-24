# 📊 The API & Flask Project with Analytics Dashboard

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## 📌 Project Overview
This project is an end-to-end sales data processing and analytics project built with Python, Flask, and SQL Server. It features an automated ETL Data Pipeline that integrates multi-source datasets, a Flask Backend API to manage database queries, and an interactive, modern Frontend Dashboard styled with Tailwind CSS to visualize core business Key Performance Indicators (KPIs).

## 🚀 Key Features & Pipeline Architecture

### 1. Multi-Source ETL Pipeline 🔄
- **Data Extraction:** Extracts raw data from diverse sources:
  - Customer records from a local CSV file.
  - Product catalog records via an external GitHub/API URL.
  - Transactional order details from a Parquet file.
- **Data Transformation:** Merges the disparate datasets, calculates total order values (`Quantity * Unit Price`), and standardizes records.
- **Data Loading:** Cleans and loads the consolidated records into a **Microsoft SQL Server** database table named `Sales`.

### 2. Backend Server & API (Flask & Pandas) ⚙️
- Built a web application server using **Flask**.
- Connects directly to the **SQL Server** database using PyODBC/SQLAlchemy to query records from the `Sales` table.
- Utilizes **Pandas** to compute automated Key Performance Indicators (KPIs) dynamically on the backend server.

### 3. Interactive Frontend Dashboard (Tailwind CSS) 💻
- Designed an interactive, dark-themed user interface dashboard.
- Styled responsively with **Tailwind CSS** for a modern user experience.
- Dynamically renders and displays metric cards powered by the Flask backend.

## 🛠️ Technologies & Libraries Used
- **Language & Runtime:** Python 3.x
- **Data Processing:** `pandas`, `pyarrow`
- **Database:** Microsoft SQL Server, `pyodbc` / SQLAlchemy
- **Backend Framework:** `flask`
- **Frontend:** HTML5, JavaScript, Tailwind CSS

## 🗂️ Automated KPI Computations
- **Total Revenue:** Aggregate financial earnings across all orders.
- **Total Orders:** Count of unique transaction entries.
- **Average Order Value (AOV):** Mean value per placed order.
- **Total Unique Customers:** Count of distinct customer IDs.
- **Top-Selling Product:** Identification of the highest-performing product by quantity/revenue.

## 📁 Repository Structure

```text
.
├── the API task.ipynb                    # Main ETL data processing notebook
├── the api task Dashboard2.ipynb         # Flask backend server and API script
├── customers.csv                         # Local customer dataset
├── orders.parquet                        # Order transactions dataset
└── README.md                             # Project documentation