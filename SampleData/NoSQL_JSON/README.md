# NoSQL_JSON: MongoDB Sample Datasets
This folder contains **JSON datasets** used for testing **MongoDB** queries.

### JSON Datasets
| Dataset Name   | Description |
|---------------|-------------|
| `phones.json`  | Contains mobile phone details (`brand`, `model`, `price`, `features`) |
| `users.json`   | User information dataset with fields like `name`, `age`, `location`, `purchases` |

### How ChatDB Uses These Datasets
ChatDB processes these JSON files **without needing a MongoDB server**. It reads and queries JSON data dynamically using **Python's `pymongo` and `json` libraries**.

### Running NoSQL Queries in ChatDB
1. **Ensure dependencies are installed:**
   ```bash
   pip install pymongo pandas
2. Run ChatDB and load a JSON dataset:
   python chatdb.py --dataset SampleData/NoSQL_JSON/filename.json

   (Replace filename with desired JSON dataset name or path to your own dataset)
3. Example Query in ChatDB:
   - User Input: “Get the average price of phones per brand.”
   - Generated MongoDB Query: {"$group": { "_id": "$phone_brand", "average_price": { "$avg": "$price" } }}
   
**No actual MongoDB instance is required—ChatDB processes JSON files directly.**
