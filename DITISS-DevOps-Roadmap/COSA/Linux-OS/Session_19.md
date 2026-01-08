## 📘 Session 19: Network Authentication (LDAP & NIS), Apache Clustering & Load Balancer

---

## 🧠 **1. Concept Overview**

* **Network Authentication** allows **centralized user management** across multiple Linux systems.
* **LDAP & NIS** are directory-based authentication mechanisms.
* **Apache Clustering + Load Balancer** improve **availability, scalability, and performance** of web services.
* Widely used in **enterprise Linux server environments**.

---

## 📖 **2. Key Definitions**

* **LDAP (Lightweight Directory Access Protocol):**
  Centralized, hierarchical directory service used for authentication & authorization.
* **NIS (Network Information Service):**
  Legacy centralized authentication system for sharing user/group info.
* **Apache Clustering:**
  Running Apache on multiple servers acting as a single service.
* **Load Balancer:**
  Distributes incoming traffic across multiple backend servers.
* **Directory Server:**
  Stores authentication data (users, groups, passwords).
* **Client:**
  System that authenticates users using LDAP/NIS server.

---

## 🧩 **3. Main Content (Aligned with COSA – Linux)**

---

### 🔐 **A. Network Authentication**

* Used to **avoid local user creation** on every server.
* Enables:

  * Central user database
  * Single point of administration
  * Consistent UID/GID across systems

---

## 🗂️ **B. LDAP (Lightweight Directory Access Protocol)**

### 🔹 LDAP Architecture

* **LDAP Server:** Stores directory information
* **LDAP Client:** Queries server for authentication
* **Protocol:** TCP/IP (Port **389**, LDAPS **636**)

### 🔹 LDAP Components

* **DIT (Directory Information Tree)**
* **DN (Distinguished Name)** – Unique user identity
* **ObjectClass** – Defines attributes of entries

### 🔹 LDAP Authentication Flow

1. User attempts login on client
2. Client queries LDAP server
3. Server validates credentials
4. Access granted/denied

### 🔹 LDAP Configuration (High-Level)

* Install LDAP packages (`openldap`, `ldap-utils`)
* Configure:

  * `/etc/openldap/`
  * `/etc/nsswitch.conf`
  * `/etc/pam.d/`
* Client uses:

  * `nslcd`
  * `pam_ldap`

---

## 🧑‍🤝‍🧑 **C. NIS (Network Information Service)**

### 🔹 NIS Architecture

* **NIS Master Server**
* **NIS Slave Server (optional)**
* **NIS Clients**

### 🔹 NIS Maps

* `passwd.byname`
* `group.byname`
* `hosts.byname`

### 🔹 NIS Authentication Flow

1. Client requests user info
2. NIS server provides UID/GID
3. Authentication performed

### 🔹 NIS Configuration (High-Level)

* Install `ypserv`, `ypbind`
* Setup domain name
* Configure:

  * `/etc/yp.conf`
  * `/etc/nsswitch.conf`
* Start services:

  * `ypserv`
  * `ypbind`

---

## 🌐 **D. Apache Clustering**

### 🔹 Purpose

* High Availability (HA)
* Load sharing
* Fault tolerance

### 🔹 Types

* **Active–Active**
* **Active–Passive**

### 🔹 Apache Cluster Setup

* Multiple Apache servers
* Shared content (NFS / SAN)
* Front-end Load Balancer

---

## ⚖️ **E. Load Balancer**

### 🔹 Function

* Distributes traffic across servers
* Prevents overload

### 🔹 Common Load Balancers

* **Software:** HAProxy, Nginx
* **Hardware:** F5

### 🔹 Load Balancing Algorithms

* Round Robin
* Least Connections
* IP Hash

---

## 🎯 **4. Important Facts / Points for MCQs**

* LDAP uses **port 389**
* LDAPS uses **port 636**
* NIS is also called **YP (Yellow Pages)**
* LDAP is **more secure & scalable** than NIS
* NIS is considered **obsolete**
* Load balancer works at **Layer 4 / Layer 7**
* Apache clustering improves **availability**

---

## 📌 **5. Examples**

* LDAP used in:

  * Corporate login systems
  * Email authentication
* NIS used in:

  * Older UNIX/Linux networks
* Load Balancer:

  * Web hosting platforms
  * Banking portals

---

## ⚠️ **6. MCQ Pointers / Exam Traps**

* LDAP ≠ Database (It is a **directory service**)
* NIS ≠ Secure (No encryption by default)
* Apache Cluster ≠ Load Balancer (LB is separate)
* LDAP stores data in **tree structure**
* NIS domain ≠ DNS domain
* PAM works with **LDAP/NIS for authentication**

---

📚 **Revision Tip:**
For PG-DITISS MCQs, always remember:
👉 **LDAP = Secure, Scalable, Modern**
👉 **NIS = Legacy, Simple, Insecure**

