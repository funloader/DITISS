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

Below is a **complete MySQL Lab Assignment** written in a **formal lab-record format**, focused specifically on **aggregate functions, GROUP BY, and HAVING**.

---

# **Lab Assignment: Aggregate Functions, GROUP BY, and HAVING**

---

## **Aim**

To perform calculations on dataset columns using aggregate functions (`SUM`, `COUNT`, `AVG`), group data using the `GROUP BY` clause, and filter grouped data using the `HAVING` clause in MySQL.

---

## **Requirements**

* MySQL Server
* Database: `lab_db`
* Table: `employees`

---

## **Table Structure**

```sql
CREATE TABLE employees (
    emp_id INT PRIMARY KEY AUTO_INCREMENT,
    emp_name VARCHAR(50),
    department VARCHAR(30),
    salary INT
);
```

---

## **Sample Data**

```sql
INSERT INTO employees (emp_name, department, salary) VALUES
('Alice', 'HR', 40000),
('Bob', 'IT', 55000),
('Charlie', 'IT', 60000),
('David', 'HR', 42000),
('Eva', 'Finance', 50000),
('Frank', 'IT', 58000);
```

---

## **1. Aggregate Functions**

### **a) COUNT – Total number of employees**

```sql
SELECT COUNT(*) AS total_employees
FROM employees;
```

---

### **b) SUM – Total salary of all employees**

```sql
SELECT SUM(salary) AS total_salary
FROM employees;
```

---

### **c) AVG – Average salary**

```sql
SELECT AVG(salary) AS average_salary
FROM employees;
```

---

## **2. GROUP BY Clause**

### **a) Number of employees in each department**

```sql
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department;
```

---

### **b) Average salary by department**

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department;
```

---

### **c) Total salary by department**

```sql
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department;
```

---

## **3. HAVING Clause**

### **a) Departments with average salary greater than 50,000**

```sql
SELECT department, AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;
```

---

### **b) Departments having more than 2 employees**

```sql
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department
HAVING COUNT(*) > 2;
```

---

## **4. Combined GROUP BY and HAVING Example**

```sql
SELECT department,
       COUNT(*) AS employee_count,
       AVG(salary) AS avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 45000;
```

---

## **Result**

* Calculated total, average, and count values using aggregate functions
* Grouped records based on department
* Filtered grouped data using aggregate conditions

---

## **Conclusion**

Aggregate functions combined with `GROUP BY` and `HAVING` clauses enable effective data analysis in MySQL. They are essential for summarizing and filtering grouped information in real-world applications.

---

## **Key Difference**

| Clause | Usage          |
| ------ | -------------- |
| WHERE  | Filters rows   |
| HAVING | Filters groups |

---

## **Viva / Exam Questions**

1. Why can’t aggregate functions be used in `WHERE`?
2. What is the purpose of `GROUP BY`?
3. Can `HAVING` be used without `GROUP BY`?

---
