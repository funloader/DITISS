## 👤👥 **Session 7 – User & Group Management (PG-DITISS)**

---

## 🔹 **1. Concept Overview**

Session 7 focuses on **managing users and groups in Linux**, a core admin task and a **high-frequency MCQ area**:

* User types and IDs
* Group concepts
* User & group management commands
* System files related to users/groups
* **Lab:** Creating, modifying, deleting users and groups

> Content strictly aligned with **COSA-Linux.pdf** (User & Group Management section).

---

## 📘 **2. Key Definitions**

* **User:** An account to access the Linux system.
* **Group:** Collection of users sharing common permissions.
* **UID (User ID):** Unique numeric identifier for a user.
* **GID (Group ID):** Unique numeric identifier for a group.
* **Root User:** Superuser with UID = 0.
* **Service User:** System account used by services (apache, mail, ftp).

---

## 🧩 **3. Main Content (Organized from COSA Notes)**

---

### 👤 **A. Types of Users in Linux**

(from COSA)

1. **Regular User**

   * Created during installation
   * Home directory: `/home/username`
   * Limited privileges

2. **Root User**

   * Superuser
   * UID = **0**
   * Full administrative access

3. **Service User**

   * Used by services (e.g., apache, squid)
   * Improves system security
   * No interactive login (usually)

---

### 👥 **B. Group Concepts**

* Every user belongs to **at least one group**
* Groups simplify permission management
* Users in same group share access rights

**Important COSA Points:**

* A file can have **only one group owner**
* Linux does **not support nested groups**

---

### 🗂️ **C. Important System Files (MCQ Favorite)**

| File          | Purpose                  |
| ------------- | ------------------------ |
| `/etc/passwd` | User account information |
| `/etc/shadow` | Encrypted passwords      |
| `/etc/group`  | Group details            |

**Exam Trap:**
❌ Passwords are **NOT** stored in `/etc/passwd`

---

### 🧑‍💻 **D. User Management Commands**

| Command            | Description            |
| ------------------ | ---------------------- |
| `useradd username` | Create new user        |
| `passwd username`  | Set/change password    |
| `usermod`          | Modify user properties |
| `userdel username` | Delete user            |
| `id username`      | Display UID & GID      |
| `whoami`           | Show current user      |

**Important Options:**

* `userdel -r` → deletes home directory
* `usermod -aG group user` → add user to group

---

### 👥 **E. Group Management Commands**

| Command              | Description          |
| -------------------- | -------------------- |
| `groupadd groupname` | Create group         |
| `groupdel groupname` | Delete group         |
| `groups username`    | Show user’s groups   |
| `newgrp groupname`   | Switch primary group |

---

### 🔑 **F. User–Group Relationship**

* **Primary Group:** Assigned at user creation
* **Secondary Groups:** Additional groups

**Exam One-liner:**
👉 *Primary group controls default file group ownership.*

---

## 📌 **4. Important Facts / Points for MCQs**

* Root UID = **0**
* `/etc/shadow` stores encrypted passwords
* One file → one group owner only
* Service users increase system security
* `groups` command shows group membership
* `newgrp` switches current group

---

## 🧪 **5. Examples**

* Create user:

  ```bash
  useradd tom
  passwd tom
  ```
* Create group:

  ```bash
  groupadd developers
  ```
* Add user to group:

  ```bash
  usermod -aG developers tom
  ```
* Check user info:

  ```bash
  id tom
  ```

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* ❌ `/etc/passwd` does NOT store passwords
* ❌ One file cannot have multiple group owners
* ⚠️ Root ≠ Regular user with sudo
* ⚠️ userdel does NOT delete home directory by default
* ⚠️ Service users usually cannot login

---

* Verify changes using:

  * `id`
  * `groups`
  * `/etc/passwd`, `/etc/group`

---

