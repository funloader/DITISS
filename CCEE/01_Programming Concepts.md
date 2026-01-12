> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# SET 01

---

### 1. Which MySQL function returns the current date and time in the server?

* [ ] CURDATE()
* [ ] NOW()
* [ ] CURTIME()
* [ ] DATE()

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NOW()
💡 `NOW()` returns the current date and time in `YYYY-MM-DD HH:MM:SS` format. `CURDATE()` returns only the date, and `CURTIME()` returns only the time.

</details>

---

### 2. What type of database management system is MySQL?

* [ ] Object-oriented
* [ ] Hierarchical
* [ ] Relational
* [ ] Network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Relational
💡 MySQL is a relational database management system (RDBMS) that stores data in structured tables with relationships among them.

</details>

---

### 3. MySQL is open source and freely available.

* [ ] True
* [ ] False

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** True
💡 MySQL is released under the GNU General Public License, making it free to use and modify.

</details>

---

### 4. In which programming language is MySQL primarily written?

* [ ] Python
* [ ] C/C++
* [ ] Java
* [ ] COBOL

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** C/C++
💡 MySQL server is implemented in C and C++ for performance and system-level access.

</details>

---

### 5. What is the function of the `SHOW TABLES` command in MySQL?

* [ ] Displays all tables across all databases on the server
* [ ] Displays all tables in the currently selected database
* [ ] Displays only the structure of a specific table
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Displays all tables in the currently selected database
💡 `SHOW TABLES` lists the tables that exist in the database selected via `USE database_name`.

</details>

---

### 6. Who is considered the "Father of MySQL"?

* [ ] Michael Widenius
* [ ] Bill Joy
* [ ] Stephanie Wall
* [ ] Sigmund Velin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Michael Widenius
💡 Michael "Monty" Widenius is the primary developer of MySQL.

</details>

---

### 7. Which replication type is natively supported by MySQL?

* [ ] Multiple-master replication
* [ ] Master-to-slave replication
* [ ] Single file-based clustering
* [ ] MySQL does not support replication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Master-to-slave replication
💡 MySQL supports master-slave replication where one server acts as master and others as slaves. Multi-source replication is also possible in recent versions.

</details>

---

### 8. Which command should be used to revoke privileges granted to a MySQL user?

* [ ] REVOKE
* [ ] UNDO
* [ ] UNGRANT
* [ ] DELETE

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** REVOKE
💡 `REVOKE` removes previously granted privileges from a user in MySQL.

</details>

---

### 9. What is the maximum length of a CHAR column in MySQL?

* [ ] 255 bytes
* [ ] 65,535 bytes
* [ ] 256 bytes
* [ ] None of the mentioned

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 255 bytes
💡 `CHAR` columns can store a fixed-length string up to 255 characters. Longer storage requires `VARCHAR` or `TEXT`.

</details>

---

### 10. What is the maximum length of a VARCHAR column in MySQL?

* [ ] Up to 65,535 bytes
* [ ] Up to 256 bytes
* [ ] Up to 65,567 bytes
* [ ] None of the mentioned

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Up to 65,535 bytes
💡 `VARCHAR` can store variable-length strings up to 65,535 bytes, depending on row size and character set.

</details>

---

### 11. In Oracle, which datatype is used to declare variable-length character columns?

* [ ] VARCHAR
* [ ] VARCHAR3
* [ ] VARCHAR2
* [ ] None of the mentioned

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** VARCHAR2
💡 `VARCHAR2` is the standard Oracle datatype for variable-length strings. `VARCHAR` is reserved but behaves differently across versions.

</details>

---

### 12. Which of the following are commonly used RDBMS?

* [ ] Oracle
* [ ] MySQL
* [ ] HeidiSQL
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Oracle and MySQL are RDBMS. HeidiSQL is a client tool for managing RDBMS.

</details>

---

### 13. Which SQL command is used to create a new table in a database?

* [ ] CREATE TABLE
* [ ] BUILD TABLE
* [ ] GENERATE TABLE
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CREATE TABLE
💡 `CREATE TABLE` is the standard SQL command to define a new table along with its columns, data types, and constraints.

</details>

---

### 14. In MariaDB, what does the name "Maria" represent?

* [ ] Maria is the nickname of Widenius
* [ ] Maria is the name of Widenius' younger daughter
* [ ] Maria is the name of Widenius' wife
* [ ] There is no specific reason

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Maria is the name of Widenius' younger daughter
💡 MariaDB was named after Monty Widenius’ daughter, following the naming convention of MySQL being named after his other daughter, My.

</details>

---

### 15. In terms of performance, how does MariaDB compare to MySQL?

* [ ] MariaDB is faster than MySQL
* [ ] MySQL is faster than MariaDB
* [ ] Both have similar performance
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MariaDB is faster than MySQL
💡 MariaDB includes performance improvements, additional storage engines, and optimizations over MySQL in many workloads.

</details>

---

### 16. Which command is used to create a new database in MariaDB?

* [ ] CREATE DB
* [ ] CREATE ST DATABASE
* [ ] CREATE DATABASE
* [ ] CREATE NEW DATABASE

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CREATE DATABASE
💡 `CREATE DATABASE database_name;` is the standard command in SQL to create a new database.

</details>

---

### 17. Which command retrieves the list of existing databases in MariaDB?

* [ ] USE DATABASES
* [ ] SHOW DB
* [ ] GET DATABASES
* [ ] SHOW DATABASES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHOW DATABASES
💡 `SHOW DATABASES;` lists all databases available on the MariaDB server.

</details>

---

### 18. Which command is used to select a specific database for operations in MariaDB?

* [ ] SELECT
* [ ] WORKON
* [ ] USE
* [ ] USE DATABASE

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** USE
💡 `USE database_name;` sets the current database context for subsequent queries.

</details>

---

### 19. Which command deletes an existing database in MariaDB?

* [ ] DROP DATABASES
* [ ] DROP DB
* [ ] REMOVE DATABASE
* [ ] DROP DATABASE

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DROP DATABASE
💡 `DROP DATABASE database_name;` permanently deletes a database and all its contents.

</details>

---

### 20. What is the default port number used by MySQL/MariaDB?

* [ ] 3307
* [ ] 3306
* [ ] 3308
* [ ] 3309

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3306
💡 The default TCP port for MySQL and MariaDB is 3306, though it can be changed in configuration files.

</details>

---

### 21. Which statement is used to assign or change the password for an existing MariaDB user account?

* [ ] PASSWORD
* [ ] USER PASSWORD
* [ ] SET PASSWORD
* [ ] SET USER PASSWORD

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SET PASSWORD
💡 `SET PASSWORD FOR 'user'@'host' = 'newpassword';` changes the password for an existing account.

</details>

---

### 22. Which SQL statement is used to modify existing data in a table?

* [ ] UPDATE
* [ ] ALTER
* [ ] CHANGE
* [ ] MODIFY

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UPDATE
💡 `UPDATE table_name SET column=value WHERE condition;` modifies existing records. `ALTER` changes table structure, not data.

</details>

---

### 23. The `TO_CHAR()` function in SQL can convert which of the following to a string?

* [ ] date
* [ ] datetime
* [ ] time
* [ ] timestamp
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 `TO_CHAR()` converts various temporal types into formatted strings for display or reporting purposes.

</details>

---

### 24. Which types of joins are supported in MariaDB/MySQL?

* [ ] Left Join
* [ ] Inner Join
* [ ] Outer Join
* [ ] Right Join
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 MariaDB/MySQL support all standard join types: INNER, LEFT, RIGHT, and FULL OUTER (via workarounds).

</details>

---

### 25. Is a semicolon (`;`) necessary at the end of every SQL query in MySQL?

* [ ] True
* [ ] False

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** True
💡 The semicolon terminates SQL statements, allowing multiple queries to be executed sequentially. It is required in command-line interfaces and scripts.

</details>

---
