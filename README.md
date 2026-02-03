# Healthcare Eligibility Pipeline

## Overview
This project builds a configuration-driven data pipeline that ingests eligibility files from multiple healthcare partners and outputs a unified standardized dataset.

## How to Run
1. Install dependencies:
   pip install pandas

2. Run pipeline:
   python pipeline.py

3. Output file:
   output.csv

## How to Add a New Partner
1. Add new entry in config.py:
   - file_path
   - delimiter
   - partner_code
   - column_mapping

2. No code change needed in pipeline.py

Example:
"newpartner": {
    "file_path": "data/new.csv",
    "delimiter": ";",
    "partner_code": "NEW",
    "column_mapping": {
        "id": "external_id",
        "fname": "first_name",
        "lname": "last_name",
        "dob": "dob",
        "email": "email",
        "phone": "phone"
    }
}
