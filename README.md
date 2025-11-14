# Diligent_cursor_task

# Healthcare Data Project

This project contains healthcare data management scripts for creating a SQLite database from CSV files and querying the data.

## Project Structure

```
Diligent-Cursor-task/
├── data_healthcare/          # CSV data files
│   ├── patients.csv
│   ├── doctors.csv
│   ├── appointments.csv
│   ├── treatments.csv
│   └── billing.csv
├── ingest_healthcare_data.py  # Script to load CSVs into SQLite
├── execute_healthcare_query.py # Script to run the join query
├── view_tables.py             # Script to view individual tables
├── healthcare_join.sql        # SQL join query
├── healthcare.db              # SQLite database (created after ingestion)
├── requirements.txt           # Python dependencies
├── HOW_TO_VIEW_RESULTS.md     # Guide on viewing results
└── REQUIREMENTS_CHECKLIST.md  # Requirements verification

```

## Quick Start

### 1. Set up environment

```bash
# Navigate to project folder
cd Diligent-Cursor-task

# Create virtual environment (if not already created)
python3 -m venv venv

# Activate virtual environment
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Load data into database

```bash
python ingest_healthcare_data.py
```

### 3. View results

```bash
# View joined query results (recommended)
python execute_healthcare_query.py

# View individual tables
python view_tables.py list
python view_tables.py patients
python view_tables.py doctors
```

## Files Description

- **ingest_healthcare_data.py** - Creates SQLite database and loads CSV data
- **execute_healthcare_query.py** - Executes the join query and displays results
- **view_tables.py** - Views individual database tables
- **healthcare_join.sql** - SQL query that joins all 5 tables
- **healthcare.db** - SQLite database containing all healthcare data
- **data_healthcare/** - Folder containing all CSV data files
- **requirements.txt** - Python package dependencies (pandas)

## Data Files

- **patients.csv** - 15 patient records
- **doctors.csv** - 10 doctor records
- **appointments.csv** - 18 appointment records
- **treatments.csv** - 18 treatment records
- **billing.csv** - 18 billing records

All IDs are properly linked across files (foreign key relationships).

## Usage Notes

- All scripts use relative paths, so run them from the `Diligent-Cursor-task` folder
- The database will be created in the same folder as the scripts
- CSV files are read from the `data_healthcare` folder
- Foreign key relationships are validated during ingestion

# Diligent_cursor_task
