# breathmint (Surimi1 fork with CSV-output)

# Burp Suite XML Parser

The Burp Suite XML Parser is a Python script that allows you to parse Burp Suite XML reports and generate Excel and CSV output for further analysis and reporting. It provides a convenient way to extract and organize vulnerability data from Burp Suite's XML export format.

## Features

- Parse Burp Suite XML reports to extract vulnerability data.
- Filter vulnerabilities by risk level (severity).
- Generate Excel and CSV output for easy reporting and analysis.

## Getting Started

These instructions will help you get started with using the Burp Suite XML Parser.

### Prerequisites

Specified in requirements.txt
pip3 install -r requirements.txt

### Usage
Available command-line arguments:

- -d or --directory: Specify the directory containing Burp Suite XML files to parse.
- -f or --file: Specify a single Burp Suite XML file to parse.
- -e or --exclude: Exclude specific risk ratings (severity levels). Provide a comma-separated list (e.g., "Critical,High").
- -i or --include: Include specific risk ratings (severity levels). Provide a comma-separated list (e.g., "Medium,Low").
- -o or --output: Specify the base name of the output file(s) where parsed results will be written.
- -c or --csv: Save parsed data as a CSV file.
- -p or --product: Specify the product name for the exported data.
- -co or --customer_organization: Specify the customer organization for the exported data.
- -env or --environment: Specify the environment name (e.g., production, staging, development) for the exported data.

To parse Burp Suite XML files in a directory and generate an Excel file:
```bash
# Parse Burp Suite XML files in a directory, generate an Excel file, and specify risk ratings to exclude and include:
./breathmint.py -d /path/to/xml/files -o output_filename.xlsx -e Critical,High -i Medium,Low -co "Acme Corp" -p "Web Application" -env "Production"

# Parse a single Burp Suite XML file, generate an Excel file, and specify risk ratings to exclude and include:
./breathmint.py -f single_file.xml -o output_filename.xlsx -e Critical,High -i Medium,Low -co "Acme Corp" -p "Web Application" -env "Production"

# Parse Burp Suite XML files in a directory, generate a CSV file, and specify risk ratings to exclude and include:
./breathmint.py -d /path/to/xml/files -c output_filename.csv -e Critical,High -i Medium,Low -co "Acme Corp" -p "Web Application" -env "Production"

# Parse a single Burp Suite XML file, generate a CSV file, and specify risk ratings to exclude and include:
./breathmint.py -f single_file.xml -c output_filename.csv -e Critical,High -i Medium,Low -co "Acme Corp" -p "Web Application" -env "Production"
```

## Author
- Matthew Flick 
- Surimi1
