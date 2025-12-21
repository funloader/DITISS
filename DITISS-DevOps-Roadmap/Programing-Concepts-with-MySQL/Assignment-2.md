Below are **MySQL queries** assuming the classic **EMP table** with columns like
`empno, ename, job, mgr, hiredate, sal, comm, deptno`.

---

### 1. Name, Salary, Dept no of employees working in dept 20, 30, 40

```sql
SELECT ename, sal, deptno
FROM emp
WHERE deptno IN (20, 30, 40);
```

---

### 2. Total salary of all employees

**Formula:** `sal + comm + sal*0.10`

```sql
SELECT SUM(sal + IFNULL(comm,0) + sal*0.10) AS total_salary
FROM emp;
```

---

### 3. Name and Job of employees

* Joined **before 1-Jan-1986**
* Salary between **1200 and 2500**
* With user-defined column headers

```sql
SELECT ename AS "Employee Name",
       job AS "Job Title"
FROM emp
WHERE hiredate < '1986-01-01'
  AND sal BETWEEN 1200 AND 2500;
```

---

### 4. Empno, Name, Dept no of employees working under manager **7698**

```sql
SELECT empno, ename, deptno
FROM emp
WHERE mgr = 7698;
```

---

### 5. Name, Job, Salary of employees working in dept 10 and 30

```sql
SELECT ename, job, sal
FROM emp
WHERE deptno IN (10, 30);
```

---

### 6. Display name concatenated with dept code

Column name: **Emp info**

```sql
SELECT CONCAT(ename, ', ', deptno) AS `Emp info`
FROM emp;
```

---

### 7. Employee details who do not have a manager

```sql
SELECT *
FROM emp
WHERE mgr IS NULL;
```

---

### 8. Name, Dept no, Date of joining

* Joined between **1-Jan-1981** and **31-Mar-1983**
* Sort by date of joining (ascending)

```sql
SELECT ename, deptno, hiredate
FROM emp
WHERE hiredate BETWEEN '1981-01-01' AND '1983-03-31'
ORDER BY hiredate ASC;
```

---

### 9. Employee details where job contains word **'AGE'**

```sql
SELECT *
FROM emp
WHERE job LIKE '%AGE%';
```

---

### 11. Employee details where

* Name starts with **A** and ends with **S**
  **OR**
* Name has **N** as 2nd or 3rd character and ends with **N** or **S**

```sql
SELECT *
FROM emp
WHERE (ename LIKE 'A%S')
   OR (ename LIKE '_N%N'
       OR ename LIKE '__N%N'
       OR ename LIKE '_N%S'
       OR ename LIKE '__N%S');
```

---

### 12. Names of employees having **'_'** character in their name

```sql
SELECT ename
FROM emp
WHERE ename LIKE '%\_%' ESCAPE '\';
```

---
