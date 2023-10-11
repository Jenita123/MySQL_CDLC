```
Task: Establish a MySQL connection with Python
```

* First install the mysql-conenctor

```bash
pip install mysql-connector-python
```

```python
import mysql.connector

# Replace these values with your MySQL server information
host = "your_hostname"
user = "your_username"
password = "your_password"
database = "your_database_name"
table = "your_table_name"

# Establish a connection to the MySQL server
connection = mysql.connector.connect(
    host=host,
    user=user,
    password=password,
    database=database
)

if connection.is_connected():
    print("Connected to MySQL database")
```

# Example:
```python
import mysql.connector

# Replace these values with your MySQL server information
host = "localhost"
user = "root"
password = ""
database = "Infy"

# Establish a connection to the MySQL server
connection = mysql.connector.connect(
    host=host,
    user=user,
    password=password,
    database=database
)

if connection.is_connected():
    print("Connected to MySQL database")
```