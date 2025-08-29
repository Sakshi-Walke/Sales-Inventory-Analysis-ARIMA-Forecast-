# Sales & Inventory Analysis Dashboard  

## Project Overview  
Retailers often face challenges in balancing sales and inventory. Too little stock leads to lost sales, while overstocking increases holding costs.  

This project demonstrates how a Data Analyst can use Python, SQL, and Power BI to design an end-to-end solution:  
- Create and manage synthetic retail data (>20k rows)  
- Perform ETL (Extract-Transform-Load) using Python and SQL  
- Handle unclean data and prepare cleaning pipelines  
- Build Power BI dashboards to provide insights  

---

## Key Business Questions to Solve  
1. Which products are fast-moving and which are slow-moving?  
2. What is the sales trend (daily, weekly, monthly)?  
3. Which stores/regions are underperforming?  
4. What is the stock turnover ratio by product category?  
5. How many days of stock are available before stockout?  
6. Can we predict next month’s demand for top products?  

---

## Project Roadmap  

### 1. Data Creation (Synthetic Dataset)  
- Create transaction-level retail data with more than 20,000 records using Python.  
- Columns include:  
  - TransactionID  
  - Date  
  - StoreID  
  - ProductID  
  - Category  
  - Quantity  
  - UnitPrice  
  - TotalAmount  
  - StockOnHand  
  - Supplier  

- Introduce unclean data scenarios:  
  - Missing values (NULL in Quantity, Price)  
  - Duplicates (same transaction multiple times)  
  - Wrong data types (string in Quantity)  
  - Outliers (negative sales, extremely high price)  


Trend Identification

“Detected seasonal patterns, showing an expected 18% sales increase during festive months compared to the average.”
