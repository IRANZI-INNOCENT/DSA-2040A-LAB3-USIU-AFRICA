# ETL Extract Lab  
**Name:** Iranzi Innocent  
**Student ID:** 670xxx  

## Description
This project is a take-home lab for **DSA 2040A - Lab 3 (US 2025)** focused on practicing the **Extraction** phase of the ETL (Extract, Transform, Load) process. It demonstrates **Full Extraction** and **Incremental Extraction** using a synthetic sales dataset.

The implementation is provided in a Jupyter Notebook (`etl_extract.ipynb`) and includes code to:

- **Generate a Dataset:** Create a realistic sales dataset (`custom_data.csv`) with 100+ records, including transaction ID, date, customer ID, product, and amount.
- **Full Extraction:** Load all records from the dataset into a pandas DataFrame.
- **Incremental Extraction:** Extract only new records using a timestamp stored in `last_extraction.txt`.
- **Test Incremental Extraction:** Simulate new data by appending records and verify that only new entries are extracted.
- **Documentation:** Provide step-by-step explanations using Markdown cells in the notebook.

All project files are organized in a folder named `ETL_Extract` and hosted on a public GitHub repository for submission.

## Tools Used
- **Python**: Core programming language.
- **pandas**: For data manipulation and extraction.
- **Jupyter Notebook**: For interactive code development and documentation.
- **Git/GitHub**: For version control and project submission.
- **random, datetime**: For synthetic data generation.

## Project Structure

ETL\_Extract\_xxxx\xxxxx/
├── etl\_extract.ipynb           # Main Jupyter Notebook
├── custom\_data.csv             # Synthetic sales dataset
├── last\_extraction.txt         # Tracks last extraction timestamp
├── .gitignore                  # Excludes unnecessary files from Git
└── README.md                   # Project overview and instructions


## How to Reproduce

### 1. Install Python
Download and install Python 3.11 or later from [python.org](https://www.python.org/).  
Ensure you check **“Add Python to PATH”** during installation.

Verify installation:

python --version

### 2. Install Required Libraries

Use pip to install dependencies:

pip install jupyter pandas

### 3. Clone the Repository

Ensure Git is installed from [git-scm.com](https://git-scm.com/). After cloning;


### 4. Navigate to the Project Folder

cd your project directory


### 5. Launch Jupyter Notebook

jupyter notebook

This will open a browser window with the project directory.

### 6. Run the Notebook

* Open `etl_extract.ipynb`.
* Click `Kernel > Restart & Run All` to execute all cells.

The notebook will:

* Generate `custom_data.csv` if not present.
* Perform full extraction and display all records.
* Perform incremental extraction using `last_extraction.txt`.
* Append new records and re-run incremental extraction.

## Data Source

The `custom_data.csv` file is a **synthetic dataset** created using Python’s `pandas`, `random`, and `datetime` libraries.

Each record includes:

* `transaction_id`: Unique ID (1 to 105)
* `date`: Date (from Jan 1, 2025 to Apr 5, 2025)
* `customer_id`: Random value between 1000–9999
* `product`: One of `Laptop`, `Phone`, `Tablet`, or `Headphones`
* `amount`: Value between \$50 and \$1000 (rounded to 2 decimal places)

This dataset simulates a sales transaction log with over 50 realistic records.

## Implementation Details

### 1. Dataset Generation

* Uses `random` and `datetime` to create 100 initial records.
* Saves dataset to `custom_data.csv`.

### 2. Full Extraction

* Reads all data using `pandas.read_csv()`.
* Displays first few rows and total record count.

### 3. Incremental Extraction

* Reads last timestamp from `last_extraction.txt`.
* Uses default of Jan 1, 2020 if file is missing.
* Filters and extracts only newer records.
* Updates `last_extraction.txt` with latest date.

### 4. Testing Incremental Extraction

* Appends 5 new records with April 2025 dates.
* Re-runs incremental extraction to verify only new records are picked up.

### 5. Documentation

* Clear Markdown explanations for each step.
* Code is well-commented for clarity.

## Notes

* Designed to run on any system with Python, pandas, and Jupyter installed.
* Handles errors like missing `last_extraction.txt`.
* Repository is public as required for grading.

