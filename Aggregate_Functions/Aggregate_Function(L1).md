# Aggregate_Function

1. **COUNT()**: Counts the number of rows in a group.

   Example: Count the number of employees in a department.
   ```sql
   SELECT department, COUNT(*) as employee_count
   FROM employees
   GROUP BY department;
   ```

2. **SUM()**: Calculates the sum of a numeric column in a group.

   Example: Calculate the total sales for each product.
   ```sql
   SELECT product_name, SUM(sales) as total_sales
   FROM sales_data
   GROUP BY product_name;
   ```

3. **AVG()**: Computes the average of a numeric column in a group.

   Example: Find the average salary in a company.
   ```sql
   SELECT AVG(salary) as average_salary
   FROM employees;
   ```

4. **MAX()**: Retrieves the maximum value in a group.

   Example: Find the highest temperature in a city over a period.
   ```sql
   SELECT city, MAX(temperature) as highest_temperature
   FROM weather_data
   GROUP BY city;
   ```

5. **MIN()**: Retrieves the minimum value in a group.

   Example: Find the lowest score in a test for each subject.
   ```sql
   SELECT subject, MIN(score) as lowest_score
   FROM test_scores
   GROUP BY subject;
   ```

6. **SUM()**: Calculates the total value of a column in a group.

   Example: Calculate the total expenses for each category.
   ```sql
   SELECT category, SUM(expense) as total_expense
   FROM expenses
   GROUP BY category;
   ```

7. **GROUP_CONCAT()**: Concatenates values from a column into a single string within a group.

   Example: Get a list of all employees in each department.
   ```sql
   SELECT department, GROUP_CONCAT(employee_name) as employees_list
   FROM employees
   GROUP BY department;
   ```