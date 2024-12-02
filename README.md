# SQL Notes  
> 🚀 **Quickly Set Up SQL on Your Machine**  
👉 [**Download MySQL Installer**](https://dev.mysql.com/downloads/installer/)

---

### 1️⃣ Show All Databases
```sql
SHOW DATABASES;
```
**Output:**  
| Database           |  
|--------------------|  
| information_schema |  
| mysql              |  
| performance_schema |  
| sys                |  

---

### 2️⃣ Select a Database
```sql
USE mysql;
```

---

### 3️⃣ Show Tables in the Selected Database
```sql
SHOW TABLES;
```
**Output:**  
| Tables_in_mysql |  
|-----------------|  
| columns_priv    |  
| user            |  
| ... (and more)  |  

---

### 4️⃣ Create a Table
```sql
CREATE TABLE STUDENTS (
    SN INT(2), 
    NAME VARCHAR(10), 
    DOB VARCHAR(10)
);
```
**Output:**  
```
Query OK, 0 rows affected (0.02 sec)
```

---

### 5️⃣ Insert Data into the Table
```sql
INSERT INTO STUDENTS VALUES (1, 'ANUBHAV', '08/10/2003');
```
**Output:**  
```
Query OK, 1 row affected (0.01 sec)
```

---

### 6️⃣ View All Data in the Table
```sql
SELECT * FROM STUDENTS;
```
**Output:**  
| SN | NAME    | DOB        |  
|----|---------|------------|  
| 1  | ANUBHAV | 08/10/2003 |  

---

### 7️⃣ Delete Rows Based on a Condition
```sql
DELETE FROM STUDENTS WHERE SN = 3;
```
**Output:**  
```
Query OK, 2 rows affected (0.01 sec)
```

---

### 8️⃣ Delete All Rows in a Table
```sql
DELETE FROM STUDENTS;
```

---

### 9️⃣ Drop a Table
```sql
DROP TABLE STUDENTS;
```
**Output:**  
```
Query OK, 0 rows affected (0.02 sec)
```

---

### 🔟 SQL Data Types  
| **Data Type** | **Description**       |  
|---------------|-----------------------|  
| INT           | Integer Numbers       |  
| VARCHAR(n)    | Variable-Length Text  |  
| DATE          | Dates (YYYY-MM-DD)    |  
| ...           | ...                   |  

---

### 1️⃣1️⃣ Use Conditions with `WHERE`  
#### Example: Retrieve Specific Data  
```sql
SELECT * FROM COLLAGE WHERE SECTION = 'CSE';
```
**Output:**  
| ID | NAME   | SECTION | DATE       |  
|----|--------|---------|------------|  
| 2  | Abhay  | CSE     | 01/10/2021 |  
| 3  | Shejal | CSE     | 01/10/2021 |  

---

### 1️⃣2️⃣ Conditions for Data Retrieval  
| **Condition**      | **Syntax**                 | **Example**                  |  
|---------------------|----------------------------|------------------------------|  
| Equals             | `=`                       | `id = 2`                     |  
| Not Equals         | `!=` or `<>`              | `id != 2`                    |  
| Greater/Less       | `>` or `<`                | `id > 2`                     |  
| Between            | `BETWEEN x AND y`         | `id BETWEEN 2 AND 4`         |  
| In Set             | `IN (x, y)`               | `id IN (1, 3)`               |  

---

### 1️⃣3️⃣ Create a Table with a Primary Key
```sql
CREATE TABLE MYDATA (
    ID INT PRIMARY KEY, 
    TIME VARCHAR(10), 
    WORK VARCHAR(10)
);
```

---

### 1️⃣4️⃣ Types of Keys in SQL  
| **Key Type**       | **Description**                                                                 |  
|---------------------|---------------------------------------------------------------------------------|  
| Primary Key        | Ensures uniqueness of rows                                                     |  
| Foreign Key        | Links tables                                                                   |  
| Composite Key      | Combines columns to form a unique key                                          |  

---
