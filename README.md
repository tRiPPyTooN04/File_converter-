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

## Usage

```bash
python app.py '["orders","order_items"]'

Replace ["orders","order_items"] with the list of datasets you want to process.
