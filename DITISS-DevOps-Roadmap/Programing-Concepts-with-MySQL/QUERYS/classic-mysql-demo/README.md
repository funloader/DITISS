# 💾 Classic MySQL Demo Database

This repository contains the SQL script (`demobldmysql.sql`) used to create a classic employee (EMP), department (DEPT), and salary grade (SALGRADE) database schema.

## 🚀 Getting Started

Follow these steps to set up the database using the MySQL command-line client.

### Step 1: Connect to MySQL

Open your terminal or command prompt and connect to your MySQL server:

```
mysql -u [your_username] -p
```
### Step 2: Create and Select a Database

Create a new database (e.g., classic_demo) and select it for use:
```
CREATE DATABASE classic_demo;
USE classic_demo;
```
### Step 3: Run the SQL Script

Use the SOURCE command, providing the full path to the demobldmysql.sql file you downloaded:
```
SOURCE /path/to/demobldmysql.sql;
```
### Step 4: Verify the Data

After the script runs, you can verify the tables and data with simple SELECT statements:

View Employees and Departments (Join)
To see the core relationship (Employee and their Department):
```
SELECT
    e.ENAME,
    e.JOB,
    d.DNAME,
    d.LOC
FROM
    EMP e
JOIN
    DEPT d ON e.DEPTNO = d.DEPTNO;
```
### Q.Calculated Annual Salaries

The calculation logic is: 
$$\text{Total Annual Salary} = ( \text{Monthly Salary} \times 12 ) + ( \text{Adjusted Monthly Commission} \times 12 )$$

The SQL query to calculate the annual salary is:
```
SELECT
    ENAME,
    (SAL * 12) + (COALESCE(COMM, 0) * 12) AS Total_Annual_Salary
FROM
    EMP;
```
In a MySQL database, you would use the COALESCE or IFNULL function to treat any NULL (no commission) values in the COMM column as a zero, ensuring they don't break the arithmetic.
