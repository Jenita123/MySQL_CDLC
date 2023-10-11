## Keywords in MySQL:

1. ADD
2. ALL
3. ALTER
4. ANALYZE
5. AND
6. AS
7. ASC
8. AUTO_INCREMENT
9. BETWEEN
10. BY
11. CASCADE
12. CASE
13. CHANGE
14. CHAR
15. CHECK
16. COLLATE
17. COLUMN
18. CONSTRAINT
19. CREATE
20. CROSS
21. DATABASE
22. DATE
23. DECIMAL
24. DEFAULT
25. DELETE
26. DESC
27. DISTINCT
28. DROP
29. ELSE
30. ENUM
31. EXISTS
32. FALSE
33. FOREIGN
34. FROM
35. FULL
36. GROUP
37. HAVING
38. IF
39. IGNORE
40. IN
41. INDEX
42. INNER
43. INSERT
44. INT
45. INTO
46. IS
47. JOIN
48. KEY
49. LEFT
50. LIKE
51. LIMIT
52. MATCH
53. NOT
54. NULL
55. ON
56. OPTION
57. OR
58. ORDER
59. OUTER
60. PRIMARY
61. REFERENCES
62. RIGHT
63. SELECT
64. SET
65. SMALLINT
66. TABLE
67. TEMPORARY
68. TEXT
69. THEN
70. TIMESTAMP
71. TRUE
72. UNION
73. UNIQUE
74. UNSIGNED
75. UPDATE
76. USE
77. VALUES
78. VARCHAR
79. VIEW
80. WHEN
81. WHERE
82. WHILE
83. WITH

## Meaning

1. ADD: Used to add columns or constraints to a table.
2. ALL: Specifies that a condition should be true for all values in a subquery.
3. ALTER: Modifies the structure of an existing table.
4. ANALYZE: Analyzes and updates index statistics for optimization.
5. AND: A logical operator for combining multiple conditions in a query.
6. AS: Renames a column or table with an alias.
7. ASC: Sorts query results in ascending order.
8. AUTO_INCREMENT: Automatically increments the value of a column, typically used for generating unique IDs.
9. BETWEEN: Tests whether a value falls within a specified range.
10. BY: Used in GROUP BY clause to group rows by a specified column.
11. CASCADE: Specifies that changes to a table should propagate to related tables.
12. CASE: Provides conditional logic within a query.
13. CHANGE: Modifies the name or data type of a column in an existing table.
14. CHAR: Defines a fixed-length character string data type.
15. CHECK: Adds a constraint to enforce data validation rules.
16. COLLATE: Specifies a collation (sorting and comparison rules) for character data.
17. COLUMN: Represents a single data field within a table.
18. CONSTRAINT: Enforces rules for data integrity within a table.
19. CREATE: Used to create a new table, database, or other database objects.
20. CROSS: Performs a Cartesian product of two tables.
21. DATABASE: Specifies the database to be used in the query.
22. DATE: Represents date data.
23. DECIMAL: Defines a fixed-point numeric data type.
24. DEFAULT: Sets a default value for a column.
25. DELETE: Removes rows from a table.
26. DESC: Sorts query results in descending order.
27. DISTINCT: Filters duplicate values in query results.
28. DROP: Deletes a table, database, or other database objects.
29. ELSE: Provides an alternative condition in a CASE statement.
30. ENUM: Defines a column with a set of permissible values.
31. EXISTS: Checks for the existence of rows in a subquery.
32. FALSE: Represents a Boolean false value.
33. FOREIGN: Defines a foreign key relationship between tables.
34. FROM: Specifies the source tables in a query.
35. FULL: Performs a full outer join between two tables.
36. GROUP: Groups rows for aggregate functions.
37. HAVING: Filters rows after grouping in a query.
38. IF: Implements conditional logic within a query.
39. IGNORE: Ignores duplicate key errors in INSERT statements.
40. IN: Tests whether a value is within a set of specified values.
41. INDEX: Creates an index on one or more columns for faster data retrieval.
42. INNER: Performs an inner join between two tables.
43. INSERT: Adds new rows to a table.
44. INT: Defines a 32-bit integer data type.
45. INTO: Specifies the target table for INSERT statements.
46. IS: Tests for equality or null values in a query.
47. JOIN: Combines rows from multiple tables based on a related column.
48. KEY: Defines an index or primary key constraint.
49. LEFT: Performs a left outer join between two tables.
50. LIKE: Compares a column value to a pattern using wildcards.
51. LIMIT: Specifies the maximum number of rows to retrieve.
52. MATCH: Performs full-text search against a column's values.
53. NOT: Negates a condition in a query.
54. NULL: Represents a missing or unknown value.
55. ON: Specifies join conditions or filter conditions in a query.
56. OPTION: Used in combination with optimizer hints.
57. OR: A logical operator for combining multiple conditions in a query.
58. ORDER: Sorts query results.
59. OUTER: Performs an outer join between two tables.
60. PRIMARY: Defines the primary key for a table.
61. REFERENCES: Establishes a referential integrity relationship.
62. RIGHT: Performs a right outer join between two tables.
63. SELECT: Retrieves data from one or more tables.
64. SET: Assigns values to variables within a query.
65. SMALLINT: Defines a 16-bit integer data type.
66. TABLE: Represents a structured data container.
67. TEMPORARY: Creates a temporary table.
68. TEXT: Defines a variable-length character string data type.
69. THEN: Specifies the action in a CASE statement.
70. TIMESTAMP: Stores date and time data.
71. TRUE: Represents a Boolean true value.
72. UNION: Combines the result sets of two or more SELECT statements.
73. UNIQUE: Enforces uniqueness of values in a column.
74. UNSIGNED: Specifies that a numeric column can only contain non-negative values.
75. UPDATE: Modifies existing rows in a table.
76. USE: Specifies the default database for the current session.
77. VALUES: Inserts data into a table.
78. VARCHAR: Defines a variable-length character string data type.
79. VIEW: Creates a virtual table based on a query's result.
80. WHEN: Specifies conditions for CASE statements.
81. WHERE: Filters rows in a query based on a condition.
82. WHILE: Implements a loop in a stored procedure or function.
83. WITH: Defines common table expressions (CTEs) for complex queries.

## Syntax

1. ADD:
   ```sql
   ALTER TABLE table_name ADD column_name datatype;
   ```

2. ALL:
   ```sql
   SELECT * FROM table_name WHERE column_name > ALL (SELECT other_column FROM another_table);
   ```

3. ALTER:
   ```sql
   ALTER TABLE table_name MODIFY column_name new_datatype;
   ```

4. ANALYZE:
   ```sql
   ANALYZE TABLE table_name;
   ```

5. AND:
   ```sql
   SELECT * FROM table_name WHERE condition1 AND condition2;
   ```

6. AS:
   ```sql
   SELECT column_name AS alias_name FROM table_name;
   ```

7. ASC:
   ```sql
   SELECT * FROM table_name ORDER BY column_name ASC;
   ```

8. AUTO_INCREMENT:
   ```sql
   CREATE TABLE table_name (id INT AUTO_INCREMENT PRIMARY KEY, name VARCHAR(255));
   ```

9. BETWEEN:
   ```sql
   SELECT * FROM table_name WHERE column_name BETWEEN value1 AND value2;
   ```

10. BY:
    ```sql
    SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
    ```

11. CASCADE:
    ```sql
    ALTER TABLE table_name ADD FOREIGN KEY (column_name) REFERENCES other_table(other_column) ON DELETE CASCADE;
    ```

12. CASE:
    ```sql
    SELECT column_name,
           CASE
               WHEN condition1 THEN 'Result1'
               WHEN condition2 THEN 'Result2'
               ELSE 'Result3'
           END
    FROM table_name;
    ```

13. CHANGE:
    ```sql
    ALTER TABLE table_name CHANGE old_column_name new_column_name datatype;
    ```

14. CHAR:
    ```sql
    CREATE TABLE table_name (id INT, name CHAR(50));
    ```

15. CHECK:
    ```sql
    CREATE TABLE table_name (id INT, age INT CHECK (age >= 18));
    ```

16. COLLATE:
    ```sql
    SELECT column_name FROM table_name WHERE column_name COLLATE utf8_general_ci = 'value';
    ```

17. COLUMN:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50), age INT);
    ```

18. CONSTRAINT:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50), CONSTRAINT pk_id PRIMARY KEY (id));
    ```

19. CREATE:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50));
    ```

20. CROSS:
    ```sql
    SELECT * FROM table1 CROSS JOIN table2;
    ```

21. DATABASE:
    ```sql
    CREATE DATABASE database_name;
    ```

22. DATE:
    ```sql
    SELECT column_name FROM table_name WHERE DATE(date_column) = '2023-10-11';
    ```

23. DECIMAL:
    ```sql
    CREATE TABLE table_name (id INT, price DECIMAL(10, 2));
    ```

24. DEFAULT:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50) DEFAULT 'John');
    ```

25. DELETE:
    ```sql
    DELETE FROM table_name WHERE condition;
    ```

26. DESC:
    ```sql
    SELECT * FROM table_name ORDER BY column_name DESC;
    ```

27. DISTINCT:
    ```sql
    SELECT DISTINCT column_name FROM table_name;
    ```

28. DROP:
    ```sql
    DROP TABLE table_name;
    ```

29. ELSE:
    ```sql
    SELECT column_name,
           CASE
               WHEN condition1 THEN 'Result1'
               ELSE 'Result2'
           END
    FROM table_name;
    ```

30. ENUM:
    ```sql
    CREATE TABLE table_name (id INT, gender ENUM('Male', 'Female'));
    ```

31. EXISTS:
    ```sql
    SELECT column_name FROM table_name WHERE EXISTS (SELECT * FROM another_table WHERE condition);
    ```

32. FALSE:
    ```sql
    SELECT * FROM table_name WHERE condition = FALSE;
    ```

33. FOREIGN:
    ```sql
    CREATE TABLE table_name (id INT, other_id INT, FOREIGN KEY (other_id) REFERENCES other_table(id));
    ```

34. FROM:
    ```sql
    SELECT column_name FROM table_name;
    ```

35. FULL:
    ```sql
    SELECT * FROM table1 FULL JOIN table2 ON table1.column_name = table2.column_name;
    ```

36. GROUP:
    ```sql
    SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
    ```

37. HAVING:
    ```sql
    SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > 1;
    ```

38. IF:
    ```sql
    SELECT column_name,
           IF(condition, 'Result1', 'Result2') AS result
    FROM table_name;
    ```

39. IGNORE:
    ```sql
    INSERT IGNORE INTO table_name (id, name) VALUES (1, 'John');
    ```

40. IN:
    ```sql
    SELECT column_name FROM table_name WHERE column_name IN ('value1', 'value2', 'value3');
    ```

41. INDEX:
    ```sql
    CREATE INDEX index_name ON table_name (column1, column2);
    ```

42. INNER:
    ```sql
    SELECT * FROM table1 INNER JOIN table2 ON table1.column_name = table2.column_name;
    ```

43. INSERT:
    ```sql
    INSERT INTO table_name (column1, column2) VALUES ('value1', 'value2');
    ```

44. INT:
    ```sql
    CREATE TABLE table_name (id INT, age INT);
    ```

45. INTO:
    ```sql
    INSERT INTO table_name (column1, column2) VALUES ('value1', 'value2');
    ```

46. IS:
    ```sql
    SELECT column_name FROM table_name WHERE column_name IS NULL;
    ```

47. JOIN:
    ```sql
    SELECT * FROM table1 JOIN table2 ON table1.column_name = table2.column_name;
    ```

48. KEY:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50), PRIMARY KEY (id));
    ```

49. LEFT:
    ```sql
    SELECT * FROM table1 LEFT JOIN table2 ON table1.column_name = table2.column_name;
    ```

50. LIKE:
    ```sql
    SELECT column_name FROM table_name WHERE column_name LIKE 'pattern%';
    ```

51. LIMIT:
    ```sql
    SELECT * FROM table_name LIMIT 10;
    ```

52. MATCH:
    ```sql
    SELECT column_name FROM table_name WHERE column_name MATCH 'search_term';
    ```

53. NOT:
    ```sql
    SELECT * FROM table_name WHERE NOT condition;
    ```

54. NULL:
    ```sql
    SELECT * FROM table_name WHERE column_name IS NULL;
    ```

55. ON:
    ```sql
    SELECT * FROM table1 JOIN table2 ON table1.column_name = table2.column_name;
    ```

56. OPTION:
    ```sql
   

 SELECT * FROM table_name OPTION (OPTIMIZE FOR UNKNOWN);
    ```

57. OR:
    ```sql
    SELECT * FROM table_name WHERE condition1 OR condition2;
    ```

58. ORDER:
    ```sql
    SELECT * FROM table_name ORDER BY column_name;
    ```

59. OUTER:
    ```sql
    SELECT * FROM table1 FULL JOIN table2 ON table1.column_name = table2.column_name;
    ```

60. PRIMARY:
    ```sql
    CREATE TABLE table_name (id INT PRIMARY KEY, name VARCHAR(50));
    ```

61. REFERENCES:
    ```sql
    CREATE TABLE table_name (id INT, other_id INT, FOREIGN KEY (other_id) REFERENCES other_table(id));
    ```

62. RIGHT:
    ```sql
    SELECT * FROM table1 RIGHT JOIN table2 ON table1.column_name = table2.column_name;
    ```

63. SELECT:
    ```sql
    SELECT column1, column2 FROM table_name;
    ```

64. SET:
    ```sql
    UPDATE table_name SET column_name = 'new_value' WHERE condition;
    ```

65. SMALLINT:
    ```sql
    CREATE TABLE table_name (id INT, count SMALLINT);
    ```

66. TABLE:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(50));
    ```

67. TEMPORARY:
    ```sql
    CREATE TEMPORARY TABLE temp_table (id INT, name VARCHAR(50));
    ```

68. TEXT:
    ```sql
    CREATE TABLE table_name (id INT, description TEXT);
    ```

69. THEN:
    ```sql
    SELECT column_name,
           CASE
               WHEN condition1 THEN 'Result1'
               WHEN condition2 THEN 'Result2'
               ELSE 'Result3'
           END
    FROM table_name;
    ```

70. TIMESTAMP:
    ```sql
    CREATE TABLE table_name (id INT, timestamp_column TIMESTAMP);
    ```

71. TRUE:
    ```sql
    SELECT * FROM table_name WHERE condition = TRUE;
    ```

72. UNION:
    ```sql
    SELECT column1 FROM table1 UNION SELECT column2 FROM table2;
    ```

73. UNIQUE:
    ```sql
    CREATE TABLE table_name (id INT, email VARCHAR(255) UNIQUE);
    ```

74. UNSIGNED:
    ```sql
    CREATE TABLE table_name (id INT UNSIGNED, value INT);
    ```

75. UPDATE:
    ```sql
    UPDATE table_name SET column_name = 'new_value' WHERE condition;
    ```

76. USE:
    ```sql
    USE database_name;
    ```

77. VALUES:
    ```sql
    INSERT INTO table_name (column1, column2) VALUES ('value1', 'value2');
    ```

78. VARCHAR:
    ```sql
    CREATE TABLE table_name (id INT, name VARCHAR(255));
    ```

79. VIEW:
    ```sql
    CREATE VIEW view_name AS SELECT column1, column2 FROM table_name;
    ```

80. WHEN:
    ```sql
    SELECT column_name,
           CASE
               WHEN condition1 THEN 'Result1'
               ELSE 'Result2'
           END
    FROM table_name;
    ```

81. WHERE:
    ```sql
    SELECT * FROM table_name WHERE condition;
    ```

82. WHILE:
    ```sql
    WHILE condition DO
       -- statements
    END WHILE;
    ```

83. WITH:
    ```sql
    WITH cte_name AS (SELECT column1, column2 FROM table_name)
    SELECT * FROM cte_name;
    ```
