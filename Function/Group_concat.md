## GROUP_CONCAT()

```sql
CREATE TABLE employees (
    department VARCHAR(50),
    name VARCHAR(50)
);

INSERT INTO employees (department, name) VALUES
    ('HR', 'Alice'),
    ('HR', 'Bob'),
    ('Engineering', 'Charlie'),
    ('Engineering', 'Dave'),
    ('Engineering', 'Eve'),
    ('Marketing', 'Frank'),
    ('Marketing', 'Grace');
```

Now, we have a table `employees` with data like this:

```
+------------+-------+
| department | name  |
+------------+-------+
| HR         | Alice |
| HR         | Bob   |
| Engineering| Charlie |
| Engineering| Dave  |
| Engineering| Eve   |
| Marketing  | Frank |
| Marketing  | Grace |
+------------+-------+
```

Create a query that concatenates the names of employees within each department:

```sql
SELECT department, GROUP_CONCAT(name ORDER BY name ASC) AS employees
FROM employees
GROUP BY department;
```

In this query:

- We select the `department` column to determine the groups.

- We use `GROUP_CONCAT(name ORDER BY name ASC)` to concatenate the `name` values within each department. The `ORDER BY` clause ensures that the names are sorted in alphabetical order within each group.

- Finally, we use `GROUP BY department` to group the rows by the `department` column.

The result of the query will be:

```
+------------+-------------------+
| department | employees         |
+------------+-------------------+
| Engineering| Charlie,Dave,Eve  |
| HR         | Alice,Bob         |
| Marketing  | Frank,Grace       |
+------------+-------------------+
```

So, the query effectively groups the employees by department and concatenates their names into a single string, separated by commas. In the "Engineering" department, we have Charlie, Dave, and Eve, and so on for the other departments.