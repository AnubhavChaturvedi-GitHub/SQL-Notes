
# **SQL Notes**

**Get started with SQL by downloading the setup here:**  
[Download MySQL](https://dev.mysql.com/downloads/installer/)  

---

## **1. Display Available Databases**
```sql
SHOW DATABASES;
```
### Output:  
| Database           |  
|--------------------|  
| information_schema |  
| mysql              |  
| performance_schema |  
| sys                |  

---

## **2. Select a Database**
```sql
USE mysql;
```

---

## **3. Show Tables in the Selected Database**
```sql
SHOW TABLES;
```
### Output:  
| Tables in mysql                       |  
|--------------------------------------|  
| columns_priv                         |  
| component                            |  
| db                                   |  
| ... *(and more)*                     |  

---

## **4. Create a Table**
```sql
CREATE TABLE STUDENTS (
  SN INT(2), 
  NAME VARCHAR(10), 
  DOB VARCHAR(10)
);
```
### Output:  
```
Query OK, 0 rows affected, 1 warning (0.02 sec)
```

---

## **5. Insert Data into the Table**
```sql
INSERT INTO STUDENTS VALUES (1, 'ANUBHAV', '08/10/2003');
```
### Output:  
```
Query OK, 1 row affected (0.01 sec)
```

---

## **6. Display Data from the Table**
```sql
SELECT * FROM STUDENTS;
```
### Output:  
| SN  | NAME    | DOB        |  
|-----|---------|------------|  
| 1   | ANUBHAV | 08/10/2003 |  

---

## **7. Delete a Row**
```sql
DELETE FROM STUDENTS WHERE SN = 3;
```
### Output:  
```
Query OK, 2 rows affected (0.01 sec)
```

---

## **8. Delete All Data in a Table**
```sql
DELETE FROM STUDENTS;
```
### Output:  
```
Query OK, 2 rows affected (0.00 sec)
Empty set (0.00 sec)
```

---

## **9. Drop a Table**
```sql
DROP TABLE STUDENTS;
```
### Output:  
```
Query OK, 0 rows affected (0.02 sec)
```

---

## **10. SQL Data Types**  
![SQL Data Types](https://github.com/user-attachments/assets/a86a07ac-a8c2-431a-9c7b-80d6ebb08653)

---

## **11. Use `WHERE` Keyword for Conditional Queries**
Example:  
```sql
SELECT * FROM collage WHERE section = "CSE";
```
### Output:  
| id  | name   | section | date       |  
|-----|--------|---------|------------|  
| 2   | Abhay  | CSE     | 01/10/2021 |  
| 3   | Shejal | CSE     | 01/10/2021 |  

---

## **12. Conditional Operators**  
![Conditional Operators](https://github.com/user-attachments/assets/23df7c1b-2fc9-4a3e-ae99-709ffa0633c7)

---

## **13. Create a Table with a Primary Key**
```sql
CREATE TABLE mydata (
  id INT PRIMARY KEY, 
  time VARCHAR(10), 
  work VARCHAR(10)
);
```

---

## **14. Keys in SQL**  
![SQL Keys](https://github.com/user-attachments/assets/2d189ebd-d597-4fad-8519-a8a9883b619e)

---

## **15. SQL Query Example - Creating and Managing Tables**

### Example:
```sql
CREATE DATABASE college;
USE college;

CREATE TABLE students (
  student_id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50),
  course VARCHAR(50)
);
```
- Creates a new database called `college` and a table `students` with `student_id` as a primary key.

---

## **16. SQL Query Example - Inserting Data**
```sql
INSERT INTO students (name, course) VALUES ('John Doe', 'Computer Science');
```
- Inserts a new record into the `students` table.

---

## **17. SQL Query Example - Updating Data**
```sql
UPDATE students SET course = 'Information Technology' WHERE student_id = 1;
```
- Updates the `course` of a student with `student_id` 1.

---

## **18. SQL Query Example - Deleting Data**
```sql
DELETE FROM students WHERE student_id = 2;
```
- Deletes the student record with `student_id` 2 from the `students` table.

---

## **19. SQL Query Example - Using `JOIN` for Multiple Tables**
```sql
SELECT students.name, courses.course_name
FROM students
JOIN courses ON students.course_id = courses.course_id;
```
- Joins two tables `students` and `courses` to fetch related data.

---

## **20. SQL Query Example - Aggregating Data**
```sql
SELECT course, COUNT(*) AS num_students
FROM students
GROUP BY course;
```
- Groups students by `course` and counts how many students are in each course.

---

## **21. SQL Query Example - Using `HAVING` for Conditional Aggregates**
```sql
SELECT course, COUNT(*) AS num_students
FROM students
GROUP BY course
HAVING COUNT(*) > 5;
```
- Filters the grouped results to show only courses with more than 5 students.

---

## **22. SQL Query Example - Sorting Data**
```sql
SELECT * FROM students ORDER BY name ASC;
```
- Orders students alphabetically by name.

---

## **23. SQL Query Example - Using `LIMIT` to Restrict Results**
```sql
SELECT * FROM students LIMIT 5;
```
- Limits the result to the first 5 records in the `students` table.

---

## **24. SQL Query Example - Using `DISTINCT` to Remove Duplicates**
```sql
SELECT DISTINCT course FROM students;
```
- Retrieves unique courses from the `students` table, removing duplicates.

---

## **25. SQL Query Example - Using `LIKE` for Pattern Matching**
```sql
SELECT * FROM students WHERE name LIKE 'J%';
```
- Finds all students whose names start with 'J'.

---

## **26. SQL Query Example - Using `IN` for Multiple Conditions**
```sql
SELECT * FROM students WHERE course IN ('Computer Science', 'Engineering');
```
- Retrieves students who are enrolled in either Computer Science or Engineering courses.

---

## **27. SQL Query Example - Using `BETWEEN` for Range Filtering**
```sql
SELECT * FROM students WHERE student_id BETWEEN 1 AND 10;
```
- Filters students whose `student_id` is between 1 and 10.

---

## **28. SQL Query Example - Using `IS NULL` for Null Values**
```sql
SELECT * FROM students WHERE course IS NULL;
```
- Retrieves students who have no course assigned (NULL values).

---

## **29. SQL Query Example - Using `ORDER BY` with `DESC` for Descending Order**
```sql
SELECT * FROM students ORDER BY student_id DESC;
```
- Orders students by `student_id` in descending order.

---

## **30. SQL Query Example - Using `INNER JOIN`**
```sql
SELECT students.name, courses.course_name
FROM students
INNER JOIN courses ON students.course_id = courses.course_id;
```
- Retrieves students' names and the corresponding course names by matching records from both tables.

---

## **31. SQL Query Example - Using `LEFT JOIN`**
```sql
SELECT students.name, courses.course_name
FROM students
LEFT JOIN courses ON students.course_id = courses.course_id;
```
- Retrieves all students and their course names, even if no matching course exists.

---

## **32. SQL Query Example - Using `RIGHT JOIN`**
```sql
SELECT students.name, courses.course_name
FROM students
RIGHT JOIN courses ON students.course_id = courses.course_id;
```
- Retrieves all courses and their corresponding students, even if no matching student exists.

---

## **33. Conclusion**
This concludes the basics of SQL queries, including table creation, data insertion, selection, and modification. The commands can be extended to more complex operations like joins, sorting, and filtering to handle large datasets.


