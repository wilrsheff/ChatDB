# SQL_CSV: MySQL Sample Datasets
This folder contains **CSV datasets** that are used for **SQL query generation** in ChatDB.

## CSV Datasets
| Dataset Name              | Description |
|---------------------------|-------------|
| **books.csv**             | Contains book details including title, author, price, and genre. |
| **e-commerce_sales.csv**  | Transactional sales data for an e-commerce store, including product category, sales amount, and date. |
| **smartphones_sales.csv** | Sales data specifically for smartphones, covering brand, model, sales figures, and pricing. |
  
### How ChatDB Uses These Datasets
ChatDB **does not require an actual MySQL database**. It loads CSV files into **dataframes** and processes SQL queries in-memory.

### Running SQL Queries in ChatDB
1. **Ensure dependencies are installed:**
   ```bash
   pip install pandas sqlalchemy sqlite3
2. Run ChatDB and load a CSV dataset:
   python chatdb.py --dataset SampleData/SQL_CSV/books.csv
3. Example Query in ChatDB:
   - User Input: “Find the number of books per genre.”
   - Generated SQL Query: SELECT genre, COUNT(*) FROM books GROUP BY genre;

**No MySQL database is needed—ChatDB processes CSV files via Python.**
