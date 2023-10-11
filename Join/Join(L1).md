In SQL, a `JOIN` is used to combine rows from two or more tables based on a related column between them. It allows you to retrieve data from multiple tables in a single query by specifying how the tables are related. The result of a `JOIN` operation is a new table that combines columns from the joined tables where the specified conditions are met.

Suppose you have two tables: `students` and `courses`, and you want to retrieve a list of students and the courses they are enrolled in.

1. **Create Tables**:

   You can create the tables with the following SQL statements:

   ```sql
   CREATE TABLE students (
       student_id INT PRIMARY KEY,
       student_name VARCHAR(50)
   );

   CREATE TABLE courses (
       course_id INT PRIMARY KEY,
       course_name VARCHAR(50)
   );

   CREATE TABLE student_courses (
       student_id INT,
       course_id INT,
       FOREIGN KEY (student_id) REFERENCES students(student_id),
       FOREIGN KEY (course_id) REFERENCES courses(course_id)
   );
   ```

   In this example, the `student_courses` table acts as a junction table to establish a many-to-many relationship between students and courses.

2. **Insert Data**:

   Let's insert some sample data into the tables:

   ```sql
   -- Insert students
   INSERT INTO students (student_id, student_name)
   VALUES (1, 'Alice'),
          (2, 'Bob'),
          (3, 'Charlie');

   -- Insert courses
   INSERT INTO courses (course_id, course_name)
   VALUES (101, 'Math'),
          (102, 'Science'),
          (103, 'History');

   -- Enroll students in courses
   INSERT INTO student_courses (student_id, course_id)
   VALUES (1, 101), -- Alice in Math
          (1, 103), -- Alice in History
          (2, 102), -- Bob in Science
          (3, 101), -- Charlie in Math
          (3, 103); -- Charlie in History
   ```

3. **Perform a JOIN**:

   To retrieve a list of students and the courses they are enrolled in, you can use an `INNER JOIN` like this:

   ```sql
   SELECT students.student_name, courses.course_name
   FROM students
   INNER JOIN student_courses ON students.student_id = student_courses.student_id
   INNER JOIN courses ON student_courses.course_id = courses.course_id;
   ```

   This query combines data from the `students` and `courses` tables using the `student_courses` table as the bridge, and it selects the student names and the courses they are enrolled in.

The result of this query would be a table that shows the names of students and the courses they are enrolled in:

```
+-------------+------------+
| student_name| course_name|
+-------------+------------+
| Alice       | Math       |
| Alice       | History    |
| Bob         | Science    |
| Charlie     | Math       |
| Charlie     | History    |
+-------------+------------+
```
