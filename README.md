# Sales-Inventory-Analysis-ARIMA-Forecast-


## 📌 Project Overview  
Retailers often face challenges in **balancing sales and inventory**. Too little stock leads to **lost sales**, while overstocking increases **holding costs**.  

This project demonstrates how a **Data Analyst** can use **Python, SQL, and Power BI** to design an end-to-end solution:  
- Create & manage **synthetic retail data** (>20k rows)  
- Perform **ETL (Extract-Transform-Load)** using Python & SQL  
- Handle **unclean data** and prepare cleaning pipelines  
- Build **Power BI dashboards** to provide insights  

---

## 🎯 Key Business Questions to Solve  
1. 📦 Which products are **fast-moving** and which are **slow-moving**?  
2. 💰 What is the **sales trend** (daily, weekly, monthly)?  
3. 🏬 Which **stores/regions** are underperforming?  
4. 🔄 What is the **stock turnover ratio** by product category?  
5. ⏳ How many days of stock are available before **stockout**?  
6. 📈 Can we predict **next month’s demand** for top products?  

---

## 🗂 Project Roadmap  

### **1. Data Creation (Synthetic Dataset)**  
- Create **transaction-level retail data** with >20,000 records using Python.  
- Columns include:  
  - `TransactionID`  
  - `Date`  
  - `StoreID`  
  - `ProductID`  
  - `Category`  
  - `Quantity`  
  - `UnitPrice`  
  - `TotalAmount`  
  - `StockOnHand`  
  - `Supplier`  

- Introduce **unclean data scenarios**:  
  - Missing values (`NULL` in Quantity, Price)  
  - Duplicates (same transaction multiple times)  
  - Wrong data types (string in Quantity)  
  - Outliers (negative sales, extremely high price)  

📌 **Script:** Python script will generate & export CSV → loaded into SQL DB.  

---

### **2. ETL Pipeline (Python ↔ SQL)**  
- **Extract:** Load CSV into Python (Pandas).  
- **Transform:**  
  - Handle missing values (impute / drop)  
  - Fix data types (string → numeric)  
  - Remove duplicates  
  - Identify outliers (Z-score, IQR)  
- **Load:**  
  - Push cleaned dataset into SQL (PostgreSQL/MySQL).  
  - Create staging & final tables.  

📌 Deliverables:  
- Python ETL script (`etl_pipeline.py`)  
- SQL schema & table creation script  

---

### **3. Data Cleaning & Validation**  
Examples of **unclean → cleaned scenarios**:  
- ❌ Quantity = `"abc"` → ✅ Converted to `0`  
- ❌ Negative Sales = `-10` → ✅ Converted to `NULL` and flagged as error  
- ❌ Duplicate Transactions → ✅ Removed  
- ❌ Missing Price → ✅ Imputed using average category price  

📌 Deliverables:  
- Jupyter Notebook: `data_cleaning.ipynb`  
- Before & After snapshots (for README screenshots)  

---

### **4. SQL Analysis**  
Run SQL queries for insights:  
- **Top 10 best-selling products**  
- **Stockout risk products** (`StockOnHand < avg_weekly_sales`)  
- **Store performance** by sales & inventory turnover  
- **Monthly sales trend**  

📌 Deliverables:  
- SQL scripts (`queries.sql`)  
- Sample query results in README  

---

### **5. Power BI Dashboard**  
Create a dashboard with visuals:  
- 📊 Sales trend (line chart by date)  
- 🏷️ Top-selling products (bar chart)  
- 🏬 Store performance map/heatmap  
- 📦 Inventory turnover ratio (card visual)  
- ⚠️ Low-stock alerts (table with conditional formatting)  
- 🔮 Demand forecast (line chart with Python model output)  

📌 Deliverables:  
- PBIX file (`Sales_Inventory_Dashboard.pbix`)  
- Screenshots in README  

---

## 📂 Repository Structure  
