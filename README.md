# 📊 The API & Flask projcet with Analytics Dashboard

An end-to-end sales data processing and analytics project consisting of an ETL Data Pipeline, a Flask Backend API, and an interactive Frontend Dashboard.

---

## 📌 Project Components

The repository is structured into three main components:

1. **`The API & Flask projcet` (ETL Data Pipeline)**:
   - A data pipeline script / Jupyter Notebook that extracts data from multiple sources:
     - Customer data from a local CSV file.
     - Product data from a GitHub URL.
     - Order data from a Parquet file.
   - Merges the datasets and calculates the total order value (`Quantity * Unit Price`).
   - Cleans and loads the consolidated records into a **SQL Server** database table named `Sales`.

2. **`Analytics Dashboard ` (Backend Server - Flask)**:
   - A web application built with **Flask**.
   - Connects to the **SQL Server** database to query records from the `Sales` table.
   - Uses **Pandas** to calculate Key Performance Indicators (KPIs) and serve them to the frontend.

3. **`index` / `index.html` (Frontend Dashboard)**:
   - An interactive, dark-themed user interface dashboard.
   - Styled with **Tailwind CSS**.
   - Dynamically displays KPI metric cards powered by the Flask backend.

---

## 🚀 Key Features

- **Multi-Source Data Integration**: Native handling of CSV, Parquet files, and external GitHub/API resources.
- **Automated KPI Computation**:
  - Total Revenue
  - Total Orders
  - Average Order Value (AOV)
  - Total Unique Customers
  - Top-Selling Product
- **Modern UI**: Clean, responsive, dark-mode analytics interface powered by Tailwind CSS.

---

## 🛠️ Tech Stack

- **Language & Runtime**: Python 3.x
- **Data Processing**: Pandas, PyArrow
- **Database**: Microsoft SQL Server, PyODBC / SQLAlchemy
- **Backend Framework**: Flask
- **Frontend**: HTML5, JavaScript, Tailwind CSS

---

## ⚙️ Setup & Installation

### 1️⃣ Prerequisites
- Install [Python 3.8+](https://www.python.org/)
- Microsoft SQL Server instance running locally or remotely
- Install required Python dependencies:
  ```bash
  pip install pandas flask sqlalchemy pyodbc pyarrow requests