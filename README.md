# JSON to SQL Converter

A web application that converts JSON data into properly normalized SQL Server database schemas. This tool automatically transforms complex nested JSON structures into a set of relational database tables with appropriate foreign key relationships, constraints, and optimized structure - not just a single denormalized table.

## Features

- Creates fully normalized relational database schema from nested JSON structures
- Implements proper database normalization principles (1NF, 2NF, 3NF)
- Automatically identifies and establishes parent-child relationships between tables
- Generates junction/bridge tables for many-to-many relationships in arrays
- Intelligently handles complex nested objects by creating separate related tables
- Option to rename 'id' fields to avoid conflicts with SQL Server auto-increment IDs
- Generates complete SQL scripts with both table creation (DDL) and data insertion (DML) statements
- User-friendly web interface with schema customization options

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

The application includes a built-in example that demonstrates the normalization process. It shows how complex nested JSON with users, orders, and nested properties is transformed into multiple properly normalized SQL tables with primary/foreign key relationships instead of a single denormalized table. The example demonstrates proper database design principles like avoiding data duplication and maintaining referential integrity.

## Requirements

- Python 3.6+
- Streamlit
- json_to_sql package (installed from the GitHub repository)

## Contributing

Feel free to contribute to this project or report issues on GitHub at: https://github.com/bokuwagiga/json_to_sql