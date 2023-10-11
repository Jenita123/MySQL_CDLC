In SQL, `ON` is used specifically to define the conditions for combining rows from two or more tables when performing JOIN operations. Here's a simple definition:

**Definition:** The `ON` keyword in SQL is used to specify the conditions under which rows from different tables should be matched and combined when performing JOIN operations.

So, ON is mainly associated with JOIN clauses and is used to establish the relationship between tables by defining the criteria for row matching between those tables. It doesn't have a standalone purpose or function beyond this context. 

## Example:

Suppose you have two tables, `orders` and `customers`, and you want to retrieve a list of orders along with the customer information for each order. To do this, you would join the `orders` and `customers` tables based on a common key, which is typically a customer ID. Here's an example:

```sql
SELECT orders.order_id, orders.order_date, customers.customer_name
FROM orders
JOIN customers ON orders.customer_id = customers.customer_id;
```

In this example:

- We start with the `SELECT` statement to specify the columns we want to retrieve from the combined result.
- We specify the source table, which is `orders`.
- We use the `JOIN` keyword to indicate that we want to perform a join operation.
- We specify the target table, which is `customers`.
- The `ON` keyword is used to define the join condition, indicating that the join should occur when the `customer_id` column in the `orders` table matches the `customer_id` column in the `customers` table.
