# SQL_CSV: MySQL Sample Datasets
This folder contains **CSV datasets** that are used for **SQL query generation** in ChatDB.

### CSV Datasets
| Dataset Name  | Description |
|--------------|-------------|
| `books.csv`  | Contains book details (`title`, `author`, `price`, `genre`) |
| `sales.csv`  | Transactional sales data (`product_id`, `category`, `sales_amount`, `date`) |

### How to Load CSV Data into MySQL
1. **Start MySQL:**
   ```bash
   mysql -u your_username -p
  
### How ChatDB Uses These Datasets
ChatDB **does not require an actual MySQL database**. It loads CSV files into **Pandas DataFrames** and processes SQL queries in-memory.

### Running SQL Queries in ChatDB
1. **Ensure dependencies are installed:**
   ```bash
   pip install pandas sqlalchemy sqlite3
2. Run ChatDB and load a CSV dataset:
   python chatdb.py --dataset SampleData/SQL_CSV/books.csv
3.	Example Query in ChatDB:
   - User Input: “Find the number of books per genre.”
	- Generated SQL Query: SELECT genre, COUNT(*) FROM books GROUP BY genre;

**No MySQL database is needed—ChatDB processes CSV files via Python.**
