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

To parse Burp Suite XML files in a directory and generate an Excel file:
```bash
./burp_suite_xml_parser.py -d /path/to/xml/files -o output_filename.xlsx
```
To parse a single Burp Suite XML file and generate an Excel file:
```bash
./burp_suite_xml_parser.py -f single_file.xml -o output_filename.xlsx
```
To specify risk ratings to exclude or include:
```bash
./burp_suite_xml_parser.py -d /path/to/xml/files -o output_filename.xlsx -e Critical,High -i Medium,Low
```
To save parsed data as a CSV file:
```bash
./burp_suite_xml_parser.py -d /path/to/xml/files -c output_filename.csv
```

## Author
Matthew Flick 
Surimi1
