# Retail Sales ETL Pipeline

##  Overview
A simple end-to-end ETL pipeline that extracts retail sales data from Excel, transforms it using Python, and stores the results in a SQLite database. Final analysis is done using SQL queries to extract KPIs like revenue, cost, and total profit.

##  Tools Used
- Python (Pandas, SQLite3)
- Excel (.xlsx input file)
- SQLite (Database storage)
- SQL (Querying KPIs)

## Steps Performed
1. Read data from an Excel file
2. Calculated new columns:
   - `Revenue` = Quantity × Price
   - `Cost` = Quantity × Cost per item
   - `Profit` = Revenue − Cost
3. Stored the cleaned data in a SQLite DB
4. Queried the database to calculate total profit by product

## Files
- `etl_pipeline.py`: Python script to run the pipeline
- `sales_data.xlsx`: Raw input data
- `sales.db`: Database generated from script
- `README.md`: Project details
- Screenshots: Proof of execution (optional)

## SQL Query Example
```sql
SELECT Product, SUM(Profit) AS Total_Profit
FROM sales_data
GROUP BY Product
ORDER BY Total_Profit DESC;

## 🔗 Excel Dashboard Link
 [View Retail Sales Analysis Excel File on OneDrive](https://1drv.ms/x/c/ed2d6b1a350e6461/EWqwr9gjiz9OlBcmrW8U2tABVlrRs1f_pMQzy4A04Kh1xQ)
