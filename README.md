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
