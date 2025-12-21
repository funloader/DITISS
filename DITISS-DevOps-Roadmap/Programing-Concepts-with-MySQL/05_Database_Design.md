Below is a **complete MySQL lab-style explanation** covering **aggregate functions, GROUP BY, HAVING, and subqueries**, written in a **clear, exam- and record-ready format**.

---

# **Lab Assignment: Aggregate Functions, GROUP BY, HAVING, and Subqueries**

---

## **Aim**

To use aggregate functions (`SUM`, `COUNT`, `AVG`), group data using `GROUP BY`, filter grouped data using `HAVING`, and retrieve data using subqueries in MySQL.

---

## **Requirements**

* MySQL Server
* Database: `lab_db`
* Table: `students`

---

## **Table Structure**

```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    department VARCHAR(30),
    marks INT
);
```

---

## **Sample Data**

```sql
INSERT INTO students (name, department, marks) VALUES
('Alice', 'CSE', 85),
('Bob', 'ECE', 72),
('Charlie', 'CSE', 90),
('David', 'ME', 65),
('Eva', 'ECE', 78),
('Frank', 'CSE', 88);
```

---

## **1. Aggregate Functions**

Aggregate functions perform calculations on multiple rows and return a single value.

---

### **a) COUNT – Total number of students**

```sql
SELECT COUNT(*) AS total_students
FROM students;
```

---

### **b) SUM – Total marks of all students**

```sql
SELECT SUM(marks) AS total_marks
FROM students;
```

---

### **c) AVG – Average marks**

```sql
SELECT AVG(marks) AS average_marks
FROM students;
```

---

## **2. GROUP BY Clause**

`GROUP BY` groups rows with the same values in specified columns.

---

### **a) Number of students in each department**

```sql
SELECT department, COUNT(*) AS student_count
FROM students
GROUP BY department;
```

---

### **b) Average marks in each department**

```sql
SELECT department, AVG(marks) AS avg_marks
FROM students
GROUP BY department;
```

---

## **3. HAVING Clause**

`HAVING` is used to filter grouped results (unlike `WHERE`, which filters rows).

---

### **a) Departments with average marks greater than 80**

```sql
SELECT department, AVG(marks) AS avg_marks
FROM students
GROUP BY department
HAVING AVG(marks) > 80;
```

---

### **b) Departments having more than 2 students**

```sql
SELECT department, COUNT(*) AS student_count
FROM students
GROUP BY department
HAVING COUNT(*) > 2;
```

---

## **4. Subqueries (Nested Queries)**

A **subquery** is a query inside another query.

---

### **4.1 Subquery in WHERE Clause**

#### **Students who scored more than the average marks**

```sql
SELECT name, marks
FROM students
WHERE marks > (
    SELECT AVG(marks)
    FROM students
);
```

---

### **4.2 Subquery with IN**

#### **Students from departments with average marks above 80**

```sql
SELECT name, department
FROM students
WHERE department IN (
    SELECT department
    FROM students
    GROUP BY department
    HAVING AVG(marks) > 80
);
```

---

### **4.3 Subquery in SELECT Clause**

```sql
SELECT name,
       marks,
       (SELECT AVG(marks) FROM students) AS overall_average
FROM students;
```

---

## **5. Combined Example**

```sql
SELECT department, COUNT(*) AS student_count, AVG(marks) AS avg_marks
FROM students
GROUP BY department
HAVING AVG(marks) > 75
ORDER BY avg_marks DESC;
```

---

## **Result**

* Calculated total, average, and count values using aggregate functions
* Grouped data using `GROUP BY`
* Filtered grouped data using `HAVING`
* Retrieved data using subqueries

---

## **Conclusion**

Aggregate functions and grouped queries allow efficient data analysis in MySQL. Subqueries enable complex data retrieval by embedding queries within other queries.

---

## **Key Differences**

| Clause   | Purpose        |
| -------- | -------------- |
| WHERE    | Filters rows   |
| GROUP BY | Groups rows    |
| HAVING   | Filters groups |

---

## **Viva / Exam Questions**

1. Difference between `WHERE` and `HAVING`?
2. Can aggregate functions be used without `GROUP BY`?
3. What is a subquery?

---

