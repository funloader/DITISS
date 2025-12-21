Below is a **complete, lab-ready explanation of MySQL Security and User Management**, suitable for **assignments, exams, and lab records**.

---

# **Security and User Management in MySQL**

---

## **Aim**

To understand and implement security mechanisms in MySQL by creating users, assigning privileges, revoking permissions, and managing secure access to databases.

---

## **1. MySQL User Accounts**

In MySQL, a user account is defined by:

```text
'username'@'hostname'
```

Example:

```text
'admin'@'localhost'
```

---

## **2. Creating a MySQL User**

### **Syntax**

```sql
CREATE USER 'username'@'host' IDENTIFIED BY 'password';
```

### **Example**

```sql
CREATE USER 'secure_user'@'localhost' IDENTIFIED BY 'Secure@123';
```

---

## **3. Granting Privileges**

Privileges control what actions a user can perform.

---

### **3.1 Grant All Privileges on a Database**

```sql
GRANT ALL PRIVILEGES ON lab_db.* TO 'secure_user'@'localhost';
FLUSH PRIVILEGES;
```

---

### **3.2 Grant Specific Privileges**

```sql
GRANT SELECT, INSERT ON lab_db.students
TO 'secure_user'@'localhost';
```

---

### **Common Privileges**

| Privilege | Description             |
| --------- | ----------------------- |
| SELECT    | Read data               |
| INSERT    | Add new data            |
| UPDATE    | Modify data             |
| DELETE    | Remove data             |
| CREATE    | Create tables/databases |
| DROP      | Delete tables/databases |
| ALL       | Full access             |

---

## **4. Viewing User Privileges**

```sql
SHOW GRANTS FOR 'secure_user'@'localhost';
```

---

## **5. Revoking Privileges**

### **Syntax**

```sql
REVOKE privilege ON database.table FROM 'username'@'host';
```

### **Example**

```sql
REVOKE DELETE ON lab_db.students
FROM 'secure_user'@'localhost';
```

---

## **6. Changing User Password**

```sql
ALTER USER 'secure_user'@'localhost'
IDENTIFIED BY 'NewSecure@456';
```

---

## **7. Dropping a User**

⚠️ Permanently removes the user account.

```sql
DROP USER 'secure_user'@'localhost';
```

---

## **8. Role Management (MySQL 8.0+)**

### **Create a Role**

```sql
CREATE ROLE 'readonly_role';
```

### **Grant Privileges to Role**

```sql
GRANT SELECT ON lab_db.* TO 'readonly_role';
```

### **Assign Role to User**

```sql
GRANT 'readonly_role' TO 'secure_user'@'localhost';
```

### **Activate Role**

```sql
SET DEFAULT ROLE 'readonly_role' TO 'secure_user'@'localhost';
```

---

## **9. Best Practices for MySQL Security**

✔ Use strong passwords
✔ Follow **least privilege principle**
✔ Avoid using root for applications
✔ Use separate users for different applications
✔ Regularly review and revoke unused privileges
✔ Enable SSL for remote access

---

## **10. Example Lab Task**

```sql
-- Create user
CREATE USER 'report_user'@'localhost' IDENTIFIED BY 'Report@123';

-- Grant read-only access
GRANT SELECT ON lab_db.* TO 'report_user'@'localhost';

-- Check privileges
SHOW GRANTS FOR 'report_user'@'localhost';
```

---

## **Result**

* Successfully created MySQL users
* Assigned and revoked privileges
* Implemented secure access control

---

## **Conclusion**

MySQL Security and User Management ensures controlled access to databases by defining users, privileges, and roles. Proper user management is critical for protecting sensitive data and maintaining database integrity.

---

## **Viva / Exam Questions**

1. What is the principle of least privilege?
2. Difference between `GRANT` and `REVOKE`?
3. Why should root access be restricted?

---


Just tell me 🙂

