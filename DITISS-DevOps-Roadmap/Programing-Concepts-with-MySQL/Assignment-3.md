Below are **MySQL queries** using **Single Row Functions** and **Group Functions**, based on the standard **EMP table**
(`empno, ename, job, mgr, hiredate, sal, comm, deptno`).

---

## **Single Row Functions**

### 1. List all employees and their email

**Email format:**

* ename → characters **2 to 5**
* job → characters **2 to 4**
* append `@mycompany.com`

```sql
SELECT ename,
       CONCAT(SUBSTRING(ename,2,4),
              SUBSTRING(job,2,3),
              '@mycompany.com') AS email
FROM emp;
```

---

### 2. List all employees who joined in **September**

```sql
SELECT *
FROM emp
WHERE MONTH(hiredate) = 9;
```

---

### 3. Empno, Name, Deptno of employees with **18 or more years of experience**

(Sorted by experience)

```sql
SELECT empno,
       ename,
       deptno,
       TIMESTAMPDIFF(YEAR, hiredate, CURDATE()) AS experience
FROM emp
WHERE TIMESTAMPDIFF(YEAR, hiredate, CURDATE()) >= 18
ORDER BY experience;
```

---

### 4. Employee details who joined on **3rd of any month/year**

```sql
SELECT *
FROM emp
WHERE DAY(hiredate) = 3;
```

---

### 5. Display all employees who joined between **1981 and 1983**

```sql
SELECT *
FROM emp
WHERE YEAR(hiredate) BETWEEN 1981 AND 1983;
```

---

## **Group Functions**

### 6. Highest, Lowest, Total & Average salary for each department

* Rounded to nearest whole number
* Column labels: **Maximum, Minimum, Total, Average**

```sql
SELECT deptno,
       ROUND(MAX(sal)) AS Maximum,
       ROUND(MIN(sal)) AS Minimum,
       ROUND(SUM(sal)) AS Total,
       ROUND(AVG(sal)) AS Average
FROM emp
GROUP BY deptno;
```

---

### 7. Department no and number of managers in each department

(Column label: **Total Number of Managers**)

```sql
SELECT deptno,
       COUNT(DISTINCT mgr) AS `Total Number of Managers`
FROM emp
WHERE mgr IS NOT NULL
GROUP BY deptno;
```

---

### 8. Department number and total salary of **non-managers**

(Only where total salary > 20000)

```sql
SELECT deptno,
       SUM(sal) AS total_salary
FROM emp
WHERE empno NOT IN (SELECT DISTINCT mgr FROM emp WHERE mgr IS NOT NULL)
GROUP BY deptno
HAVING SUM(sal) > 20000;
```

---
