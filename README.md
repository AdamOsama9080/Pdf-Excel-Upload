# Pdf-Excel-Upload

This Python script connects to a MySQL database and uploads two files, an Excel spreadsheet and a PDF document, then inserts them into their respective tables. It uses the `mysql-connector-python` library to interact with the MySQL database.

## Usage

1. Open the Python script in a text editor or IDE.

2. Update the database connection details:

    ```python
    mydb = mysql.connector.connect(
        host="mysql5045.site4now.net",
        user="a99555_quality",
        password="AQI@123456",
        database="db_a99555_quality"
    )
    ```

    Replace the placeholders with your actual database details.

3. Specify the file paths:

    ```python
    file_path = "test_one.xlsx"
    pdf_path = "test_one.pdf"
    ```

    Ensure that the Excel (`test_one.xlsx`) and PDF (`test_one.pdf`) files exist in the same directory as the script.

4. Run the script. It will read the files, connect to the database, and insert the data.

## Important Notes

- Make sure you have the necessary permissions to access the database and insert data.

- Always handle sensitive information (like database credentials) securely. Avoid hardcoding them directly in the script.

- This script assumes that the MySQL server is reachable and the database schema and tables (`excel_data` and `pdfs_file`) exist. If not, you may need to create them manually.

- Ensure the `mysql-connector-python` library is installed. If not, you can install it using `pip install mysql-connector-python`.

- Remember to close the database connection after use by calling `mydb.close()`.

