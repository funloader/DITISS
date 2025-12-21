Below is a **complete MySQL Lab Assignment** written in a **record / exam-ready format**, covering **SELECT, WHERE, and ORDER BY** with clear examples and outputs.

---

# **Lab Assignment: Data Retrieval Using SELECT, WHERE, and ORDER BY**

---

## **Aim**

To retrieve data from a MySQL database using `SELECT` statements, filter records using the `WHERE` clause, and sort the retrieved data using the `ORDER BY` clause.

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
    age INT,
    department VARCHAR(30),
    marks INT
);
```

---

## **Sample Data**

```sql
INSERT INTO students (name, age, department, marks) VALUES
('Alice', 20, 'CSE', 85),
('Bob', 22, 'ECE', 72),
('Charlie', 21, 'CSE', 90),
('David', 23, 'ME', 65),
('Eva', 20, 'ECE', 78);
```

---

## **1. SELECT Statements to Retrieve Data**

### **a) Retrieve all student records**

```sql
SELECT * FROM students;
```

### **b) Retrieve only name and department**

```sql
SELECT name, department FROM students;
```

---

## **2. WHERE Clause for Filtering Data**

### **a) Students from CSE department**

```sql
SELECT * FROM students
WHERE department = 'CSE';
```

### **b) Students with marks greater than 75**

```sql
SELECT name, marks FROM students
WHERE marks > 75;
```

### **c) Students aged between 20 and 22**

```sql
SELECT * FROM students
WHERE age BETWEEN 20 AND 22;
```

---

## **3. ORDER BY Clause for Sorting Data**

### **a) Sort students by marks (ascending)**

```sql
SELECT name, marks
FROM students
ORDER BY marks;
```

### **b) Sort students by marks (descending)**

```sql
SELECT name, marks
FROM students
ORDER BY marks DESC;
```

### **c) Sort by department and then by marks**

```sql
SELECT name, department, marks
FROM students
ORDER BY department ASC, marks DESC;
```

---

## **4. Combined WHERE and ORDER BY**

### **Retrieve CSE students sorted by marks**

```sql
SELECT name, marks
FROM students
WHERE department = 'CSE'
ORDER BY marks DESC;
```

---

## **Result**

* Successfully retrieved specific data using `SELECT`
* Filtered relevant records using `WHERE`
* Sorted retrieved data using `ORDER BY`

---

## **Conclusion**

The lab demonstrates effective data retrieval and analysis using MySQL `SELECT`, `WHERE`, and `ORDER BY` clauses. These commands are essential for querying and analyzing database information.

---

## **Viva / Exam Questions**

1. What is the use of `WHERE` clause?
2. Difference between `ORDER BY ASC` and `DESC`?
3. Can we use `WHERE` without `SELECT`? (Answer: No)

---

