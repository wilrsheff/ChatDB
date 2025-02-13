# NoSQL_JSON: MongoDB Sample Datasets
This folder contains **JSON datasets** used for testing **MongoDB** queries.

### JSON Datasets
| Dataset Name   | Description |
|---------------|-------------|
| `phones.json`  | Contains mobile phone details (`brand`, `model`, `price`, `features`) |
| `users.json`   | User information dataset with fields like `name`, `age`, `location`, `purchases` |

### How to Load JSON Data into MongoDB
1. **Start MongoDB:**
   ```bash
   mongod --dbpath /path/to/your/mongodb/data
2. Import a JSON file into MongoDB:
   mongoimport --db ChatDB --collection phones --file filename.json --jsonArray

   (Replace "filename" with desired sample dataset file)

### Example NoSQL Query
Find the average price of phones per brand:
{
  "$group": { "_id": "$phone_brand", "average_price": { "$avg": "$price" } }
}
