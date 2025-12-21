Below are the **SQL statements (MySQL)** using the standard **EMP table**
(`empno, ename, job, mgr, hiredate, sal, comm, deptno`).

---

### 1. Find all **managers** with salary **greater than 1500**

```sql
SELECT *
FROM emp
WHERE job = 'MANAGER'
  AND sal > 1500;
```

---

### 2. List all employees with salary **greater than 1200 and less than 2000**

```sql
SELECT *
FROM emp
WHERE sal > 1200
  AND sal < 2000;
```

---

### 3. List all employees with salary **1600 or 800 or 1900**

```sql
SELECT *
FROM emp
WHERE sal IN (1600, 800, 1900);
```

---

### 4. List all employees with **'R' at the second last position** in name

```sql
SELECT *
FROM emp
WHERE ename LIKE '%R_';
```

---

### 5. List all employees whose name **starts with 'A' and ends with 'N'**

```sql
SELECT *
FROM emp
WHERE ename LIKE 'A%N';
```

---

Below are **MySQL SQL statements** based on the standard **EMP table**
(`empno, ename, job, mgr, hiredate, sal, comm, deptno`).

---

### 1. Employees with salary > 1250 and dept no = 30

```sql
SELECT *
FROM emp
WHERE sal > 1250 AND deptno = 30;
```

---

### 2. Employees with salary >= 1250 and <= 3000

```sql
SELECT *
FROM emp
WHERE sal BETWEEN 1250 AND 3000;
```

---

### 3. Employees with salary > 1250 and < 3000

```sql
SELECT *
FROM emp
WHERE sal > 1250 AND sal < 3000;
```

---

### 4. Employees with salary = 3000 or 1250 or 2500

```sql
SELECT *
FROM emp
WHERE sal IN (3000, 1250, 2500);
```

---

### 5. Employee with name = SMITH

```sql
SELECT *
FROM emp
WHERE ename = 'SMITH';
```

---

### 6. Employees with name starting with S

```sql
SELECT *
FROM emp
WHERE ename LIKE 'S%';
```

---

### 7. Employees with name ending with S

```sql
SELECT *
FROM emp
WHERE ename LIKE '%S';
```

---

### 8. Employees with name containing I at 2nd position

```sql
SELECT *
FROM emp
WHERE ename LIKE '_I%';
```

---

### 9. Name starts with A, ends with N and contains L in between

```sql
SELECT *
FROM emp
WHERE ename LIKE 'A%L%N';
```

---

### 10. Name starts with A, B at 3rd position and P at second last position

```sql
SELECT *
FROM emp
WHERE ename LIKE 'A_B%P_';
```

---

### 11. Name starts with A or S or W

```sql
SELECT *
FROM emp
WHERE ename LIKE 'A%'
   OR ename LIKE 'S%'
   OR ename LIKE 'W%';
```

---

### 12. Max and Min salary for each job

```sql
SELECT job,
       MAX(sal) AS max_sal,
       MIN(sal) AS min_sal
FROM emp
GROUP BY job;
```

---

### 13. Count employees who have not received commission

```sql
SELECT COUNT(*) AS no_commission
FROM emp
WHERE comm IS NULL;
```

---

### 14. Sum of salary of employees in dept no 10

```sql
SELECT SUM(sal) AS total_salary
FROM emp
WHERE deptno = 10;
```

---

### 15. Max and Average salary for each job in every department

```sql
SELECT deptno, job,
       MAX(sal) AS max_sal,
       AVG(sal) AS avg_sal
FROM emp
GROUP BY deptno, job;
```

---

### 16. Max salary for every department where deptno > 15 (sorted)

```sql
SELECT deptno, MAX(sal) AS max_sal
FROM emp
WHERE deptno > 15
GROUP BY deptno
ORDER BY deptno;
```

---

### 17. Sum salary for every department where sum > 3000

```sql
SELECT deptno, SUM(sal) AS total_salary
FROM emp
GROUP BY deptno
HAVING SUM(sal) > 3000;
```

---

### 18. Departments having minimum 5 employees

```sql
SELECT deptno
FROM emp
GROUP BY deptno
HAVING COUNT(*) >= 5;
```

---

### 19. Count employees earning > 2000 in each job

```sql
SELECT job, COUNT(*) AS emp_count
FROM emp
WHERE sal > 2000
GROUP BY job;
```

---

### 20. Display names and jobs in lowercase

```sql
SELECT LOWER(ename), LOWER(job)
FROM emp;
```

---

### 21. Display names padded to length 15 (left padded)

```sql
SELECT LPAD(ename, 15, ' ') AS name,
       job
FROM emp;
```

---

### 22. Min, Max, Avg salary of employees under same manager

```sql
SELECT mgr,
       MIN(sal) AS min_sal,
       MAX(sal) AS max_sal,
       AVG(sal) AS avg_sal
FROM emp
WHERE mgr IS NOT NULL
GROUP BY mgr;
```

---

### 23. Sum & Avg of total earnings (sal + comm)

Employees with sal > 2000 and dept 10 or 20

```sql
SELECT SUM(sal + IFNULL(comm,0)) AS total_earnings,
       AVG(sal + IFNULL(comm,0)) AS avg_earnings
FROM emp
WHERE sal > 2000
  AND deptno IN (10, 20);
```

---

### 24. Employees joined in Aug 1980 with salary >1500 and <2500

```sql
SELECT *
FROM emp
WHERE MONTH(hiredate) = 8
  AND YEAR(hiredate) = 1980
  AND sal BETWEEN 1500 AND 2500;
```

---

### 25. Employees joined in Aug or May or Dec

```sql
SELECT *
FROM emp
WHERE MONTH(hiredate) IN (5, 8, 12);
```

---

### 26. Name & hiredate (dd/mm/yy) for clerks with commission

```sql
SELECT ename,
       DATE_FORMAT(hiredate, '%d/%m/%y') AS hiredate
FROM emp
WHERE job = 'CLERK'
  AND comm IS NOT NULL;
```

---

### 27. Empcode (3–5 chars of name + last 2 chars of job)

```sql
SELECT empno,
       ename,
       job,
       CONCAT(SUBSTRING(ename,3,3), RIGHT(job,2)) AS empcode
FROM emp;
```

---

### 28. Commission with $ and thousand separator

(If null → 0), Name starts with A and ends with N

```sql
SELECT ename,
       FORMAT(IFNULL(comm,0), 0) AS commission
FROM emp
WHERE ename LIKE 'A%N';
```

---

### 29. Remarks based on commission

```sql
SELECT empno, ename, sal, comm,
       CASE
           WHEN comm >= 600 THEN 'Excellent Keep it up'
           WHEN comm < 600 AND comm IS NOT NULL THEN 'Good'
           ELSE 'Need improvement'
       END AS Remark
FROM emp;
```

---

### 30. Department name based on deptno

```sql
SELECT empno, ename, deptno,
       CASE deptno
           WHEN 10 THEN 'HR'
           WHEN 20 THEN 'Admin'
           WHEN 30 THEN 'Accounts'
           ELSE 'Purchase'
       END AS department_name
FROM emp;
```

---


