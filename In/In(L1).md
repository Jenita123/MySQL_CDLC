The `IN` keyword in SQL is used to specify a list of values for a condition in a `WHERE` clause. It allows you to filter rows where a column's value matches any value in the list. 

### Examples

1. Retrieve employees in the Sales and Marketing departments:
```sql
SELECT * FROM employees WHERE department IN ('Sales', 'Marketing');
```

2. Get employees with specific employee IDs:
```sql
SELECT * FROM employees WHERE employee_id IN (101, 103, 105);
```

3. Find products with specific IDs from a `products` table:
```sql
SELECT * FROM products WHERE product_id IN (1, 5, 7);
```

4. Filter orders with specified order statuses:
```sql
SELECT * FROM orders WHERE order_status IN ('Shipped', 'Delivered');
```

5. Retrieve students with certain grade levels:
```sql
SELECT * FROM students WHERE grade_level IN (9, 10, 11);
```

6. Get a list of products in a specific category:
```sql
SELECT * FROM products WHERE category_id IN (2, 4, 6);
```

7. Find orders from specific customers:
```sql
SELECT * FROM orders WHERE customer_id IN (101, 103, 105);
```

8. Filter products with specific names:
```sql
SELECT * FROM products WHERE product_name IN ('Widget A', 'Widget B', 'Widget C');
```

9. Retrieve employees with specific job titles:
```sql
SELECT * FROM employees WHERE job_title IN ('Manager', 'Developer', 'Analyst');
```

10. Find customers with specific ZIP codes:
```sql
SELECT * FROM customers WHERE zip_code IN ('10001', '20003', '30005');
```
