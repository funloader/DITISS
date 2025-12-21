Below is the **correct SQL (MySQL-style)** to create the **Student, Course, and Marks tables**, along with a **small correction explanation** (important for exams/interviews).

---

## Practice creating following tables

```sql
create table mydept_DBDA
(
deptid number primary key,
dname varchar2(20) not null unique,
dloc varchar2(20)
)

insert into mydept_DBDA values(30,'Purchase','Mumbai');

create table myemployee
(
empno number(5) primary key,
fname varchar2(15) not null,
mname varchar2(15),
lname varchar2(15) not null,
sal number(9,2) check(sal >=1000),
doj date default sysdate,
passportnum varchar2(15) unique,

deptno number constraint fk_deptno references mydept_DBDA(deptid) on delete
cascade
)
```

---

---

## 1. Create **MYDEPT_DBDA** table

```sql
CREATE TABLE mydept_DBDA
(
    deptid NUMBER PRIMARY KEY,
    dname  VARCHAR2(20) NOT NULL UNIQUE,
    dloc   VARCHAR2(20)
);
```

### Insert sample data

```sql
INSERT INTO mydept_DBDA
VALUES (30, 'Purchase', 'Mumbai');
```

---

## 2. Create **MYEMPLOYEE** table

```sql
CREATE TABLE myemployee
(
    empno       NUMBER(5) PRIMARY KEY,
    fname       VARCHAR2(15) NOT NULL,
    mname       VARCHAR2(15),
    lname       VARCHAR2(15) NOT NULL,
    sal         NUMBER(9,2) CHECK (sal >= 1000),
    doj         DATE DEFAULT SYSDATE,
    passportnum VARCHAR2(15) UNIQUE,
    deptno      NUMBER,
    CONSTRAINT fk_deptno
        FOREIGN KEY (deptno)
        REFERENCES mydept_DBDA(deptid)
        ON DELETE CASCADE
);
```

---

## 3. Sample insert into **MYEMPLOYEE**

```sql
INSERT INTO myemployee
(empno, fname, mname, lname, sal, passportnum, deptno)
VALUES
(1001, 'Amit', NULL, 'Sharma', 25000, 'P12345', 30);
```

---

## 🔑 Key Concepts (Very Important)

* `PRIMARY KEY` → uniquely identifies records
* `NOT NULL` → mandatory column
* `UNIQUE` → no duplicate values allowed
* `CHECK (sal >= 1000)` → enforces salary rule
* `DEFAULT SYSDATE` → auto assigns date of joining
* `FOREIGN KEY … ON DELETE CASCADE` → deletes employee rows when department is deleted

---

---

## Create following tables Student, Course

```sql
Student (sid,sname) ---------------- sid ---primary key
Course(cid,cname)-------------- cid ---primary key

Marks(studid,coursed,marks)
Sample data for marks table
studid,courseid,marks
1 1 99
1 3 98
2 1 95
2 2 97

create table marks(
studid number,
courseid number,
marks number,
constraint pk primary key(studid,courseid),
constraint fk_sid foreign key (studid) references student(sid) on delete set null,
constraint fk_cid foreign key (courseid) references course(cid)
)
```

---

---

## 1. Create **Student** table

```sql
CREATE TABLE student (
    sid INT PRIMARY KEY,
    sname VARCHAR(50)
);
```

---

## 2. Create **Course** table

```sql
CREATE TABLE course (
    cid INT PRIMARY KEY,
    cname VARCHAR(50)
);
```

---

## 3. Create **Marks** table

⚠ **Important note:**

* A column that is part of a **PRIMARY KEY cannot be NULL**
* Therefore, **ON DELETE SET NULL** is **not allowed** on `studid` because it is part of the primary key

So we must use **ON DELETE CASCADE** (correct & valid).

### ✅ Correct version

```sql
CREATE TABLE marks (
    studid INT,
    courseid INT,
    marks INT,
    CONSTRAINT pk_marks PRIMARY KEY (studid, courseid),
    CONSTRAINT fk_sid FOREIGN KEY (studid)
        REFERENCES student(sid)
        ON DELETE CASCADE,
    CONSTRAINT fk_cid FOREIGN KEY (courseid)
        REFERENCES course(cid)
);
```

---

## 4. Insert sample data into **Marks**

```sql
INSERT INTO marks VALUES (1, 1, 99);
INSERT INTO marks VALUES (1, 3, 98);
INSERT INTO marks VALUES (2, 1, 95);
INSERT INTO marks VALUES (2, 2, 97);
```

---

## 🔑 Summary (Exam-ready points)

* `sid` and `cid` → **Primary Keys**
* `marks` → **Composite Primary Key (studid, courseid)**
* **ON DELETE SET NULL ❌ not allowed** with primary key columns
* Use **ON DELETE CASCADE ✅**

