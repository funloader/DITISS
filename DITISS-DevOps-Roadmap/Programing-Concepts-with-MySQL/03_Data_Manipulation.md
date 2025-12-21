Below is a **clear, lab-ready explanation of MySQL SELECT queries**, covering **SELECT, WHERE, ORDER BY, and basic JOINs**, with **syntax and examples**.

---

# **MySQL Data Retrieval (SELECT, WHERE, ORDER BY, JOIN)**

---

## **1. Writing SELECT Statements to Fetch Data**

### **Basic Syntax**

```sql
SELECT column1, column2
FROM table_name;
```

### **Select All Columns**

```sql
SELECT * FROM students;
```

### **Select Specific Columns**

```sql
SELECT name, email
FROM students;
```

---

## **2. Using WHERE Clause for Filtering Data**

The `WHERE` clause filters rows based on conditions.

### **Syntax**

```sql
SELECT column1, column2
FROM table_name
WHERE condition;
```

### **Examples**

#### **Filter by Age**

```sql
SELECT * FROM students
WHERE age > 20;
```

#### **Filter Using AND**

```sql
SELECT * FROM students
WHERE age > 18 AND age < 25;
```

#### **Filter Using OR**

```sql
SELECT * FROM students
WHERE age = 20 OR age = 22;
```

#### **Filter Using LIKE**

```sql
SELECT * FROM students
WHERE name LIKE 'A%';
```

#### **Filter Using IN**

```sql
SELECT * FROM students
WHERE age IN (20, 22);
```

---

## **3. Sorting Data Using ORDER BY**

The `ORDER BY` clause sorts the result set.

### **Syntax**

```sql
SELECT column1, column2
FROM table_name
ORDER BY column_name ASC|DESC;
```

### **Examples**

#### **Sort by Age (Ascending – Default)**

```sql
SELECT * FROM students
ORDER BY age;
```

#### **Sort by Age (Descending)**

```sql
SELECT * FROM students
ORDER BY age DESC;
```

#### **Sort by Multiple Columns**

```sql
SELECT * FROM students
ORDER BY age ASC, name DESC;
```

---

## **4. Basic JOIN Operations**

JOINs are used to combine data from multiple tables based on a related column.

---

## **Sample Tables**

### **students**

| student_id | name  | age |
| ---------- | ----- | --- |
| 1          | Alice | 20  |
| 2          | Bob   | 22  |

### **enrollments**

| enroll_id | student_id | course  |
| --------- | ---------- | ------- |
| 1         | 1          | DBMS    |
| 2         | 2          | Web Dev |

---

## **4.1 INNER JOIN**

Returns only matching records from both tables.

### **Syntax**

```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### **Example**

```sql
SELECT students.name, enrollments.course
FROM students
INNER JOIN enrollments
ON students.student_id = enrollments.student_id;
```

---

## **4.2 LEFT JOIN**

Returns all records from the left table and matching records from the right table.

```sql
SELECT students.name, enrollments.course
FROM students
LEFT JOIN enrollments
ON students.student_id = enrollments.student_id;
```

---

## **4.3 RIGHT JOIN**

Returns all records from the right table and matching records from the left table.

```sql
SELECT students.name, enrollments.course
FROM students
RIGHT JOIN enrollments
ON students.student_id = enrollments.student_id;
```

---

## **5. Combined Example**

```sql
SELECT students.name, enrollments.course
FROM students
INNER JOIN enrollments
ON students.student_id = enrollments.student_id
WHERE students.age > 20
ORDER BY students.name;
```

---

## **6. Summary Table**

| Operation      | SQL Keyword |
| -------------- | ----------- |
| Fetch data     | `SELECT`    |
| Filter rows    | `WHERE`     |
| Sort results   | `ORDER BY`  |
| Combine tables | `JOIN`      |

---

## ✅ **Key Points for Lab / Exam**

* `WHERE` filters rows **before** sorting
* `ORDER BY` sorts the final result
* `INNER JOIN` shows matching records only
* `LEFT JOIN` includes unmatched left table records

---


