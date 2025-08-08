# JSON to SQL Converter

A web application that converts JSON data into SQL Server table creation and insertion scripts. This tool automatically normalizes nested JSON structures into relational database tables with proper relationships.

## Features

- Converts nested JSON structures to normalized SQL Server tables
- Automatically creates relationship tables for arrays
- Option to rename 'id' fields to avoid conflicts with SQL Server auto-increment IDs
- Generates complete SQL scripts with both table creation and data insertion statements
- User-friendly web interface with customization options

## Installation

1. Clone this repository or download the source code
2. Install the required dependencies:

```bash
pip install streamlit
pip install git+https://github.com/bokuwagiga/json_to_sql.git
```

## Usage

1. Run the Streamlit application:

```bash
streamlit run json_to_sql_web_app.py
```

2. Open your web browser and navigate to the provided URL (typically http://localhost:8501)

3. Paste your JSON data in the text area, configure the options, and click "Generate SQL"

4. Copy the generated SQL script or download it for use in SQL Server

## Configuration Options

- **Root table name**: The name for the main table
- **Schema name**: Database schema to use for the tables
- **Rename 'id' fields**: Option to rename JSON 'id' fields to 'original_id' to avoid conflicts with SQL Server's auto-increment IDs

## Example

The application includes a built-in example that demonstrates how nested JSON with users and orders is converted to properly normalized SQL tables with relationships.

## Requirements

- Python 3.6+
- Streamlit
- json_to_sql package (installed from the GitHub repository)

## Contributing

Feel free to contribute to this project or report issues on GitHub at: https://github.com/bokuwagiga/json_to_sql