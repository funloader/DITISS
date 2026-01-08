## 📘 Session 19: Network Authentication (LDAP & NIS), Apache Clustering & Load Balancer

---

## 🔐 **Network Authentication: LDAP & NIS**

### 1️⃣ **Concept Overview**

* Network authentication allows **centralized user management** across multiple Linux systems.
* **LDAP** and **NIS** are directory-based authentication mechanisms.
* Used in **enterprise networks**, **servers**, and **multi-user environments**.

---

### 2️⃣ **Key Definitions**

* **LDAP (Lightweight Directory Access Protocol):**
  A **directory service protocol** used to access and maintain **distributed directory information**.
* **NIS (Network Information Service):**
  A **client-server directory service** that centrally manages user and system configuration data.

---

### 3️⃣ **Main Content**

#### 🧩 **LDAP**

* Works on **client-server model**
* Stores data in **hierarchical directory structure**
* Uses **DN (Distinguished Name)** for unique identification
* Supports:

  * User authentication
  * Authorization
  * Centralized password management
* Uses **TCP/IP**
* Common LDAP Server:

  * **OpenLDAP**
* Secure LDAP uses **LDAPS (LDAP over SSL/TLS)**

**LDAP Data Structure**

* Directory Information Tree (DIT)
* Entries → Attributes → Values

---

#### 🧩 **NIS**

* Older centralized authentication service
* Uses **NIS server (master/slave)** and **NIS clients**
* Distributes:

  * `/etc/passwd`
  * `/etc/group`
  * `/etc/hosts`
* Uses **YP (Yellow Pages)** protocol
* Domain-based authentication

---

### 4️⃣ **Important Facts / Points for MCQs**

* LDAP is **more secure** than NIS
* NIS **does not encrypt data**
* LDAP supports **SSL/TLS**
* NIS is considered **obsolete** in modern systems
* LDAP supports **scalability & extensibility**
* Default LDAP port:

  * **389 (LDAP)**
  * **636 (LDAPS)**

---

### 5️⃣ **LDAP vs NIS (Very Important Table)**

| Feature        | LDAP           | NIS            |
| -------------- | -------------- | -------------- |
| Security       | High (SSL/TLS) | Low            |
| Data Structure | Hierarchical   | Flat           |
| Scalability    | High           | Low            |
| Encryption     | Supported      | Not supported  |
| Usage          | Modern systems | Legacy systems |

---

### 6️⃣ **MCQ Pointers / Exam Traps**

* ❌ NIS ≠ Secure authentication
* ❌ LDAP is NOT a database (it is a directory service)
* LDAP ≠ Active Directory (AD uses LDAP)
* NIS uses **YP tools**
* LDAP entries are identified by **DN**

---

### 7️⃣ **Corrections / Improvements / Suggested Substitutions**

* NIS should be replaced with **LDAP** in production environments
* Prefer **LDAPS** instead of plain LDAP
* Use **SSSD** with LDAP for modern Linux authentication

---

---

## 🌐 **Apache Clustering**

### 1️⃣ **Concept Overview**

* Apache Clustering allows **multiple Apache servers** to work together.
* Goal:

  * **High Availability**
  * **Scalability**
  * **Fault Tolerance**

---

### 2️⃣ **Key Definitions**

* **Apache HTTP Server:** Open-source web server software.
* **Clustering:** Grouping of servers acting as a single system.

---

### 3️⃣ **Main Content**

* Multiple Apache servers serve the same application
* Requests distributed across nodes
* Often combined with:

  * **Load Balancer**
  * **Shared Storage (NFS)**
* Session management handled using:

  * Sticky sessions
  * Database-backed sessions

---

### 4️⃣ **Important Facts / Points for MCQs**

* Apache alone does NOT provide load balancing
* Apache clustering requires **external load balancer**
* Used in **high traffic websites**
* Improves:

  * Availability
  * Performance

---

### 5️⃣ **Examples**

* E-commerce websites
* Banking portals
* Enterprise applications

---

### 6️⃣ **MCQ Pointers / Exam Traps**

* ❌ Apache Clustering ≠ Apache Module only
* ❌ Clustering ≠ Backup server
* Apache + Load Balancer = Complete clustering solution

---

### 7️⃣ **Corrections / Improvements / Suggested Substitutions**

* Use **Apache + HAProxy** or **Apache + Nginx**
* For sessions, use **Redis / Database-based sessions**

---

---

## ⚖️ **Load Balancer**

### 1️⃣ **Concept Overview**

* Load Balancer distributes incoming traffic across multiple servers.
* Prevents **server overload**
* Improves **performance & reliability**

---

### 2️⃣ **Key Definitions**

* **Load Balancing:** Distribution of network traffic.
* **Backend Servers:** Servers receiving balanced requests.

---

### 3️⃣ **Main Content**

#### 🔁 **Types of Load Balancers**

* **Hardware Load Balancer**
* **Software Load Balancer**

#### 🔁 **Load Balancing Algorithms**

* Round Robin
* Least Connections
* IP Hash

#### 🔁 **Common Load Balancers**

* **HAProxy**
* **Nginx**
* **LVS (Linux Virtual Server)**

---

### 4️⃣ **Important Facts / Points for MCQs**

* Load balancer works at:

  * Layer 4 (Transport)
  * Layer 7 (Application)
* HAProxy is **Layer 4 & 7**
* LVS works at **Layer 4**
* Load balancer increases **availability**, not storage

---

### 5️⃣ **Examples**

* Apache Web Servers behind HAProxy
* Web farm architecture

---

### 6️⃣ **MCQ Pointers / Exam Traps**

* ❌ Load balancer ≠ Firewall
* ❌ Load balancer ≠ Proxy (though some act as both)
* Sticky session required for login-based apps

---

## ✅ **Quick Exam Takeaway**

* **LDAP > NIS** (Security & scalability)
* **Apache Clustering + Load Balancer = High Availability**
* **HAProxy + Apache** is a common PG-DITISS exam scenario

---
