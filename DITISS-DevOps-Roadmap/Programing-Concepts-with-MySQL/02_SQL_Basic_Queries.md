Below is a **complete MySQL Lab Assignment** with **step-by-step commands**, suitable for **practice, exams, or lab records**.

---

# **Lab Assignment: MySQL User, Database, Tables, and Data Management**

---

## **1. Create a MySQL User**

### **Step 1: Login as root**

```sql
mysql -u root -p
```

### **Step 2: Create a New User**

```sql
CREATE USER 'lab_user'@'localhost' IDENTIFIED BY 'lab_password';
```

### **Step 3: Grant Privileges**

```sql
GRANT ALL PRIVILEGES ON lab_db.* TO 'lab_user'@'localhost';
FLUSH PRIVILEGES;
```

### **Verify User**

```sql
SELECT user, host FROM mysql.user;
```

---

## **2. Create a Database**

```sql
CREATE DATABASE lab_db;
```

### **Use the Database**

```sql
USE lab_db;
```

---

## **3. Create Tables**

### **Table 1: Students**

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    email VARCHAR(100),
    age INT
);
```

### **Table 2: Courses**

```sql
CREATE TABLE courses (
    course_id INT PRIMARY KEY AUTO_INCREMENT,
    course_name VARCHAR(50),
    duration INT
);
```

---

## **4. Insert Data into Tables**

### **Insert Data into Students**

```sql
INSERT INTO students (name, email, age) VALUES
('Alice', 'alice@gmail.com', 20),
('Bob', 'bob@gmail.com', 22),
('Charlie', 'charlie@gmail.com', 21);
```

### **Insert Data into Courses**

```sql
INSERT INTO courses (course_name, duration) VALUES
('Database Systems', 6),
('Web Development', 4);
```

### **View Data**

```sql
SELECT * FROM students;
SELECT * FROM courses;
```

---

## **5. Modify a Table**

### **Add a New Column**

```sql
ALTER TABLE students
ADD phone VARCHAR(15);
```

### **Modify Column Data Type**

```sql
ALTER TABLE students
MODIFY age SMALLINT;
```

### **Rename a Column**

```sql
ALTER TABLE students
CHANGE phone contact_number VARCHAR(15);
```

---

## **6. Delete Table Data**

### **Delete Specific Record**

```sql
DELETE FROM students WHERE student_id = 3;
```

### **Delete All Records (Table Structure Remains)**

```sql
TRUNCATE TABLE courses;
```

---

## **7. Drop a Table**

```sql
DROP TABLE courses;
```

---

## **8. Drop the Database**

⚠️ **Warning: This deletes all tables and data permanently**

```sql
DROP DATABASE lab_db;
```

### **Safe Drop**

```sql
DROP DATABASE IF EXISTS lab_db;
```

---

## **9. Lab Assignment Summary**

| Task             | Command Used           |
| ---------------- | ---------------------- |
| Create user      | `CREATE USER`          |
| Grant privileges | `GRANT ALL PRIVILEGES` |
| Create database  | `CREATE DATABASE`      |
| Create table     | `CREATE TABLE`         |
| Insert data      | `INSERT INTO`          |
| Modify table     | `ALTER TABLE`          |
| Delete records   | `DELETE / TRUNCATE`    |
| Drop table       | `DROP TABLE`           |
| Drop database    | `DROP DATABASE`        |

---

## ✅ **Outcome**

* Successfully created a MySQL user
* Created a database and tables
* Inserted and modified data
* Deleted tables and database

---

Just let me know 👍

