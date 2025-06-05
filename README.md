ETL Extract Lab
Name: Iranzi InnocentStudent ID: 670513  
Description
This project is a take-home lab for DSA 2040A - Lab 3 (US 2025), focused on practicing the Extraction phase of the ETL (Extract, Transform, Load) process. The goal is to demonstrate Full Extraction and Incremental Extraction using a synthetic sales dataset. The project is implemented in a Jupyter Notebook (etl_extract.ipynb), which includes code to:

Generate a Dataset: Create a realistic sales dataset (custom_data.csv) with 100+ records, including columns for transaction ID, date, customer ID, product, and amount.
Full Extraction: Extract all records from the dataset into a pandas DataFrame.
Incremental Extraction: Extract only new records based on a timestamp stored in last_extraction.txt.
Test Incremental Extraction: Simulate new data by appending records and verify that incremental extraction processes only the new records.
Documentation: Provide clear explanations of each step using Markdown cells in the notebook.

The project is organized in a folder named ETL_Extract_IranziInnocent_670513, which contains all required files and is uploaded to a public GitHub repository for submission.
Tools Used

Python: Programming language used to write the ETL code.
pandas: Python library for data manipulation and extraction.
Jupyter Notebook: Interactive environment for coding and documenting the project.
Git/GitHub: Version control and repository hosting for project submission.
random and datetime: Python libraries used to generate synthetic data.

Project Structure
The project folder (ETL_Extract_IranziInnocent_670513) contains the following files:

etl_extract.ipynb: Jupyter Notebook with all code and documentation for dataset generation, full extraction, incremental extraction, and testing.
custom_data.csv: Synthetic sales dataset with 100+ records.
last_extraction.txt: Text file to store the timestamp of the last extraction for incremental extraction.
.gitignore: File to exclude unnecessary files (e.g., __pycache__, .ipynb_checkpoints) from the Git repository.
README.md: This file, explaining the project and how to run it.

How to Reproduce
To run this project on your computer, follow these steps:

Install Python:

Download and install Python (version 3.11 or later) from python.org.
Ensure you check “Add Python to PATH” during installation.
Verify installation by running in a terminal:python --version




Install Required Libraries:

Install Jupyter Notebook and pandas using pip:pip install jupyter pandas




Clone the Repository:

Install Git from git-scm.com if not already installed.
Clone this repository to your computer:git clone https://github.com/yourusername/ETL_Extract_IranziInnocent_670513.git

(Replace yourusername with your GitHub username.)


Navigate to the Project Folder:

Change to the project directory:cd ETL_Extract_IranziInnocent_670513




Launch Jupyter Notebook:

Start Jupyter:jupyter notebook


This opens a browser window showing the project folder.


Run the Notebook:

Open etl_extract.ipynb in the Jupyter interface.
Click “Kernel” > “Restart & Run All” to execute all cells in order.
The notebook will:
Generate custom_data.csv (if not already present).
Perform full extraction, displaying all records.
Perform incremental extraction, extracting records after the timestamp in last_extraction.txt.
Add new records and re-run incremental extraction to demonstrate functionality.





Data Source
The dataset (custom_data.csv) is a synthetic sales dataset generated using Python’s pandas, random, and datetime libraries. It contains 100 initial records, with 5 additional records added for testing incremental extraction. Each record includes:

transaction_id: Unique identifier (1 to 105).
date: Transaction date (from Jan 1, 2025, to April 5, 2025).
customer_id: Random customer ID (1000–9999).
product: Product name (Laptop, Phone, Tablet, or Headphones).
amount: Transaction amount ($50–$1000, rounded to 2 decimal places).

The dataset meets the task requirement of having at least 50 realistic records, simulating a sales transaction log.
Implementation Details
1. Dataset Generation

The notebook generates a synthetic dataset with 100 records using Python’s random library for realistic values and datetime for dates between January 1, 2025, and approximately March 31, 2025.
The dataset is saved as custom_data.csv in the project folder.

2. Full Extraction

The notebook uses pandas.read_csv to load all records from custom_data.csv into a DataFrame.
It displays the first 5 rows and the total number of records (100 initially) to verify the extraction.

3. Incremental Extraction

The notebook reads the last extraction timestamp from last_extraction.txt.
If the file is empty or missing, it uses a default date (January 1, 2020) to ensure all records are extracted initially.
It filters records with a date later than the last extraction timestamp using pandas.
The extracted records are displayed, and the latest date is written to last_extraction.txt for the next extraction.

4. Testing Incremental Extraction

The notebook appends 5 new records to custom_data.csv with dates in April 2025.
Incremental extraction is re-run, demonstrating that only the new records are extracted based on the updated timestamp in last_extraction.txt.

5. Documentation

The notebook includes Markdown cells explaining each section: introduction, setup, dataset generation, full extraction, incremental extraction, testing, and conclusion.
Code comments clarify the purpose of each code block.

Notes

The project is designed to be reproducible on any system with Python, pandas, and Jupyter installed.
The notebook handles errors gracefully (e.g., missing last_extraction.txt) to ensure robust execution.
All code is commented and documented for clarity, as required by the task.
The repository is public, as specified, to allow access for grading.

For any issues running the project, please contact Iranzi Innocent or check the GitHub repository for updates.
