# SELECT queries

In MySQL, you can perform SELECT queries to retrieve data from a database. You can select different data types by specifying the columns you want to retrieve in your query. Here's a basic example of a SELECT query with different data types:

Assuming you have a table named "example_table" with the following columns:

- id (integer)
- name (string)
- age (integer)
- salary (decimal)
- is_active (boolean)

You can write a SELECT query to retrieve data from this table as follows:

```sql
SELECT id, name, age, salary, is_active
FROM example_table;
```

In this query:

- `id` and `age` are of integer data types.
- `name` is of string data type.
- `salary` is of decimal data type.
- `is_active` is of boolean data type.

This query will retrieve all rows from the "example_table" and include the values of each column in the result, preserving their respective data types.


# Examples:


1. Basic SELECT:

   This query selects all columns from a table named "employees."

   ```sql
   SELECT * FROM employees;
   ```

2. Select Specific Columns:

   You can select specific columns from a table:

   ```sql
   SELECT first_name, last_name, email FROM employees;
   ```

3. Alias Columns:

   You can give columns aliases for more readable output:

   ```sql
   SELECT first_name AS "First Name", last_name AS "Last Name" FROM employees;
   ```

4. Using WHERE Clause:

   To filter results, use the WHERE clause:

   ```sql
   SELECT * FROM employees WHERE department = 'HR';
   ```

5. Ordering Results:

   You can sort results using the ORDER BY clause:

   ```sql
   SELECT * FROM employees ORDER BY hire_date DESC;
   ```

6. Limiting Results:

   To limit the number of rows returned, use the LIMIT clause:

   ```sql
   SELECT * FROM products LIMIT 10;
   ```

7. Aggregating Data:

   You can use aggregate functions like SUM, COUNT, AVG, etc.:

   ```sql
   SELECT department, AVG(salary) AS avg_salary FROM employees GROUP BY department;
   ```

8. Joining Tables:

   To retrieve data from multiple tables, use JOIN clauses:

   ```sql
   SELECT employees.first_name, departments.department_name
   FROM employees
   JOIN departments ON employees.department_id = departments.department_id;
   ```

9. Using Subqueries:

   You can use subqueries to retrieve data based on the result of another query:

   ```sql
   SELECT first_name, last_name
   FROM employees
   WHERE department_id IN (SELECT department_id FROM departments WHERE location = 'New York');
   ```
