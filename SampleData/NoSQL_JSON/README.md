# NoSQL_JSON: MongoDB Sample Datasets
This folder contains **JSON datasets** used for testing **MongoDB** queries.

## JSON Datasets
| Dataset Name                   | Description |
|---------------------------------|-------------|
| **lottery_expenditures.json**   | Data on lottery expenditures, potentially including spending patterns, state-wise statistics, and demographic insights. |
| **phones.json**                 | Contains mobile phone details, including brand, model, price, and specifications such as display, battery, and connectivity features. |
| **spongebob_characters.json**   | Character dataset from the SpongeBob SquarePants universe, including details like name, occupation, residence, and notable appearances. |

### How ChatDB Uses These Datasets
ChatDB **does not require an actual MongoDB database**. It loads CSV files into **dataframes** and processes NoSQL queries in-memory.

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
