**Step 1: Create a Table**

Let's create a basic table called "Employee" with the following columns:

- EmployeeID (an integer representing a unique identifier for each employee)
- FirstName (a string representing the employee's first name)
- LastName (a string representing the employee's last name)
- Department (a string representing the department the employee belongs to)
- Salary (a numeric value representing the employee's salary)

```sql
CREATE TABLE Employee (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Department VARCHAR(50),
    Salary DECIMAL(10, 2)
);
```

**Step 2: Insert Values**

Now, let's insert some sample data into the Employee table:

```sql
INSERT INTO Employee (EmployeeID, FirstName, LastName, Department, Salary)
VALUES
    (1, 'John', 'Doe', 'HR', 50000.00),
    (2, 'Jane', 'Smith', 'IT', 60000.00),
    (3, 'Alice', 'Johnson', 'Sales', 55000.00),
    (4, 'Bob', 'Brown', 'Finance', 62000.00);
```

Now, you have a basic Employee table with some sample data.

**Step 3: Create a View**

A view in a relational database is a virtual table that is based on the result of a SELECT query. It allows you to simplify complex queries, provide a security layer by limiting access to specific columns, and present data in a more user-friendly way without modifying the underlying table structure.

Let's create a view that selects the first and last names of employees in the HR department:

```sql
CREATE VIEW HR_Employees AS
SELECT FirstName, LastName
FROM Employee
WHERE Department = 'HR';
```

In this example, we've created a view called "HR_Employees" that includes only the first and last names of employees in the HR department. It does not store any data itself but provides a dynamic and up-to-date result set based on the original Employee table.

Now, you can query this view just like a regular table:

```sql
SELECT * FROM HR_Employees;
```

This will give you a result set with the first and last names of HR department employees from the Employee table without having to write the WHERE clause every time you need this information.

**Conclusion**
A view in a relational database is a virtual table created from the result of a SELECT query. It simplifies data access, enhances security, and provides a convenient way to work with specific subsets of data from one or more underlying tables.