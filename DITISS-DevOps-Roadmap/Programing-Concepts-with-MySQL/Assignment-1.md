Below are the **MySQL queries** using the classic **EMP table** (columns assumed: `empno, ename, job, sal, comm, deptno`).

---

### 1. List all records with `sal > 2000` and `comm > 200`

```sql
SELECT *
FROM emp
WHERE sal > 2000
  AND comm > 200;
```

---

### 2. List all records with `job = 'CLERK'` or `sal > 2000`

```sql
SELECT *
FROM emp
WHERE job = 'CLERK'
   OR sal > 2000;
```

---

### 3. List all records with `sal = 1250 or 1100 or 2850`

```sql
SELECT *
FROM emp
WHERE sal IN (1250, 1100, 2850);
```

---

### 4. List all employees with `sal > 1250` and `< 2850`

```sql
SELECT *
FROM emp
WHERE sal > 1250
  AND sal < 2850;
```

---

### 5. List all employees with name ends with **AS**

```sql
SELECT *
FROM emp
WHERE ename LIKE '%AS';
```

---

### 6. List all employees with job starts with **C** and ends with **K**

```sql
SELECT *
FROM emp
WHERE job LIKE 'C%K';
```

---

### 7. List all employees with job having

* **L at 3rd position**
* **M at 3rd last position**

```sql
SELECT *
FROM emp
WHERE job LIKE '__L%M__';
```

---

### 8. List all records with `sal` **not equal** to `1250, 1100, 2850`

```sql
SELECT *
FROM emp
WHERE sal NOT IN (1250, 1100, 2850);
```

---

### 9. List all employees with `sal` **NOT (>1250 AND <2850)**

```sql
SELECT *
FROM emp
WHERE NOT (sal > 1250 AND sal < 2850);
```

*(Alternative)*

```sql
SELECT *
FROM emp
WHERE sal NOT BETWEEN 1251 AND 2849;
```

---

### 10. List all employees with job

* starts with **C**
* **E at 3rd position**
* ends with **K**

```sql
SELECT *
FROM emp
WHERE job LIKE 'C_E%K';
```

---

### 11. List all rows with `comm` is NULL

```sql
SELECT *
FROM emp
WHERE comm IS NULL;
```

---

### 12. List all employees with `sal` is NULL and name starts with **S**

```sql
SELECT *
FROM emp
WHERE sal IS NULL
  AND ename LIKE 'S%';
```

---

### 13. List all employees with job containing **5 characters**

```sql
SELECT *
FROM emp
WHERE LENGTH(job) = 5;
```

---

### 14. List all employees with

* name contains **A at 1st position**
* job contains **5 characters**

```sql
SELECT *
FROM emp
WHERE ename LIKE 'A%'
  AND LENGTH(job) = 5;
```

---

