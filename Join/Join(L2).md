# Types of Joins in MySQL

In MySQL, joins are used to combine rows from two or more tables based on a related column between them. There are several types of joins that can be used in MySQL, each with its own purpose. In this document, we'll explore these types of joins with examples and their corresponding outputs.


# Definition


1. **INNER JOIN:** Returns only the rows that have matching values in both tables, excluding unmatched rows.

2. **LEFT JOIN:** Retrieves all rows from the left table and the matching rows from the right table, including unmatched rows with NULL values in the right table.

3. **RIGHT JOIN:** Retrieves all rows from the right table and the matching rows from the left table, including unmatched rows with NULL values in the left table.

4. **FULL OUTER JOIN:** Combines all rows from both tables, including unmatched rows from both tables with NULL values in the opposite table.

5. **SELF JOIN:** Joins a table to itself, typically used to establish relationships within the same table.

6. **CROSS JOIN:** Generates the Cartesian product of two tables, creating a result set with all possible combinations of rows.

7. **SELF JOIN with Aggregation:** Joins a table to itself while performing an aggregation operation to find common elements between related rows.

8. **Using WHERE Clause with JOIN:** Filters the result of a join using the WHERE clause to include only rows meeting specific criteria.

9. **USING Clause:** Simplifies the join condition by specifying the common columns using the USING clause.

10. **NATURAL JOIN:** Performs an implicit join based on columns with matching names in both tables, without specifying the join condition explicitly.


# Examples


## 1. INNER JOIN: Basic Example

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  INNER JOIN Courses ON Students.StudentID = Courses.StudentID;
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Bob     | History    |
  | Charlie | Math       |

## 2. LEFT JOIN: Including Unmatched Rows (with additional data)

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  LEFT JOIN Courses ON Students.StudentID = Courses.StudentID;
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Bob     | History    |
  | Charlie | Math       |
  | David   | NULL       |  <-- David has no matching course
  | Eve     | NULL       |  <-- Eve has no matching course

## 3. RIGHT JOIN: Including Unmatched Rows (with additional data)

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  RIGHT JOIN Courses ON Students.StudentID = Courses.StudentID;
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Bob     | History    |
  | Charlie | Math       |
  | NULL    | Science    |  <-- Science has no matching student
  | NULL    | History    |  <-- History has no matching student

## 4. FULL OUTER JOIN: All Rows from Both Tables

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  FULL OUTER JOIN Courses ON Students.StudentID = Courses.StudentID;
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Bob     | History    |
  | Charlie | Math       |
  | NULL    | NULL       |

## 5. SELF JOIN: Joining a Table to Itself

- Query:
  ```sql
  SELECT A.Name, B.Name AS Friend
  FROM Students A
  INNER JOIN Students B ON A.StudentID <> B.StudentID;
  ```

- Output:
  | Name    | Friend   |
  | ------- | -------- |
  | Alice   | Bob      |
  | Alice   | Charlie  |
  | Bob     | Alice    |
  | Bob     | Charlie  |
  | Charlie | Alice    |
  | Charlie | Bob      |

## 6. CROSS JOIN: Cartesian Product

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  CROSS JOIN Courses;
  ```

- Output: (Too large to display, results in a combination of all student-course pairs)

## 7. SELF JOIN with Aggregation: Finding Friends with Common Courses

- Query:
  ```sql
  SELECT A.Name AS Student1, B.Name AS Student2, COUNT(*) AS CommonCourses
  FROM Students A
  JOIN Courses CA ON A.StudentID = CA.StudentID
  JOIN Courses CB ON CA.CourseName = CB.CourseName
  JOIN Students B ON CB.StudentID = B.StudentID
  WHERE A.StudentID < B.StudentID
  GROUP BY A.Name, B.Name;
  ```

- Output:
  | Student1 | Student2 | CommonCourses |
  | -------- | -------- | ------------- |
  | Alice    | Charlie  | 1             |

## 8. Using WHERE Clause with JOIN

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  JOIN Courses ON Students.StudentID = Courses.StudentID
  WHERE Courses.CourseName = 'Math';
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Charlie | Math       |

## 9. USING Clause: Simplifying the ON Condition

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  JOIN Courses USING (StudentID)
  WHERE Courses.CourseName = 'Math';
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Charlie | Math       |

## 10. NATURAL JOIN: Implicit Join on Common Columns

- Query:
  ```sql
  SELECT Students.Name, Courses.CourseName
  FROM Students
  NATURAL JOIN Courses;
  ```

- Output:
  | Name    | CourseName |
  | ------- | ---------- |
  | Alice   | Math       |
  | Bob     | History    |
  | Charlie | Math       |

