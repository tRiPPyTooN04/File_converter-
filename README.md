# Data Processing Tool

This project provides a data processing tool implemented in Python. The `app.py` script in the `MODEL-APP` folder is the main script used to run this project. It combines all the functions from the `modularised` branch into a single script for easy execution.

## Features

- Combines functions from the `modularised` branch for streamlined processing.
- Implements error handling for robust file processing.
- Utilizes environment variables for flexible file path management.

## Getting Started

To use this tool, follow these steps:

1. Clone the repository to your local machine.
2. Install the required dependencies by running `pip install -r requirements.txt`.
3. Set up the necessary environment variables (`SOURCE_BASE_DIR` and `TARGET_BASE_DIR`) for file paths.
4. Run the `app.py` script to process your files.

## Technolgies Used 

   -Programming Language | Python
   -Pandas | For Converting CSV to Dataframe and then Dataframe into JSON.


## Validation Steps

After running the data processing tool, it's important to validate whether the data in the files has been converted properly. Follow these steps to ensure the conversion was successful:

1. **Check Data Conversion:**
   - Verify that the target folder has been created and populated with JSON files.
   - Confirm that the schema structure was accurately reflected from the CSV file. You can refer to `schemas.json` for this.

2. **Compare Record Counts:**
   - Take the count of records in the CSV files and compare it to the number of records in the JSON files.

3. **Sample Code for Counting Records:**

   ```python
   import pandas as pd
   
   # Read orders JSON File using PANDAS
   orders_data_json = pd.read_json(
       'data/retail_db/orders_json/part-00000',
       lines=True
   )
   # To find count of rows
   orders_data_json.count()
   
   # Read order_items JSON File using PANDAS
   order_items_data_json = pd.read_json(
       'data/retail_db/order_items_json/part-00000',
       lines=True
   )
   # To find count of rows
   order_items_data_json.count()

## Usage

```bash
python app.py '["orders","order_items"]'

Replace ["orders","order_items"] with the list of datasets you want to process.
 
