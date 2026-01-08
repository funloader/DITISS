## 📌 **Session 15 – Web & Proxy Services in Linux (PG-DITISS – COSA)** 🌐🛡️

---

## 🌍 **1️⃣ Configuring the Apache Web Server** 🧩

### 🔹 **Concept Overview**

* **Apache HTTP Server** is an **open-source web server**
* Used to **host websites and web applications**
* Works on **HTTP / HTTPS protocols**
* Most commonly used web server in Linux environments

---

### 📘 **Key Definitions**

* **Web Server:** Software that serves web pages to clients
* **Document Root:** Directory from where web files are served
* **HTTP:** HyperText Transfer Protocol
* **Daemon:** Background service (Apache daemon = `apache2` / `httpd`)

---

### 📚 **Main Content**

#### 🔸 **Apache Package**

* Debian/Ubuntu: `apache2`
* RHEL/CentOS: `httpd`

#### 🔸 **Installation**

```bash
sudo apt install apache2
```

#### 🔸 **Service Management**

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

#### 🔸 **Default Document Root**

* `/var/www/html`

#### 🔸 **Test Apache**

* Browser → `http://localhost`
* Default page confirms Apache is running

---

### 📌 **Important Facts for MCQs**

* Apache listens on **Port 80 (HTTP)**, **443 (HTTPS)**
* Main config file:

  * `/etc/apache2/apache2.conf`
* Site config directory:

  * `/etc/apache2/sites-available/`

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Apache ≠ Application Server
* ✔ Apache is **process-based**
* ✔ `index.html` loads by default
* ✔ Firewall must allow port 80

---

### 🔧 **Corrections / Improvements**

* Apache is often replaced by **Nginx** for high concurrency
* Still heavily used in enterprises & exams

---

---

## 🛡️ **2️⃣ Apache Security & Virtual Hosting** 🔐🏠

---

## 🔐 **A. Apache Security**

### 🔹 **Concept Overview**

* Securing Apache prevents:

  * Unauthorized access
  * Information leakage
  * Attacks (directory listing, banner grabbing)

---

### 📘 **Key Security Measures**

* **Disable Directory Listing**

```apache
Options -Indexes
```

* **Hide Apache Version**

```apache
ServerSignature Off
ServerTokens Prod
```

* **Restrict Access**

```apache
Require all denied
Require ip 192.168.1.0/24
```

* **Run Apache as non-root user**

  * User: `www-data`

---

### 📌 **Important Facts for MCQs**

* Apache runs as **www-data**
* `.htaccess` allows per-directory security
* HTTPS uses **SSL/TLS**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Apache does NOT run permanently as root
* ✔ Root needed only to bind low ports
* ✔ `.htaccess` increases flexibility but reduces performance

---

### 🔧 **Corrections / Improvements**

* Prefer **VirtualHost configs** over `.htaccess`
* Use **firewall + SELinux/AppArmor**

---

---

## 🏠 **B. Virtual Hosting in Apache**

### 🔹 **Concept Overview**

* **Virtual Hosting** allows **multiple websites on one server**
* Types:

  * **Name-based**
  * IP-based (rare now)

---

### 📘 **Key Definitions**

* **Virtual Host:** Logical website configuration
* **ServerName:** Primary domain name
* **ServerAlias:** Additional domain names

---

### 📚 **Main Content**

#### 🔸 **Virtual Host Config File**

```apache
<VirtualHost *:80>
  ServerName site1.com
  DocumentRoot /var/www/site1
</VirtualHost>
```

#### 🔸 **Enable Site**

```bash
a2ensite site1.conf
systemctl reload apache2
```

---

### 📌 **Important Facts for MCQs**

* Name-based virtual hosting is **default**
* Requires **DNS name resolution**
* Configs stored in `sites-available`

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Each site does NOT need separate IP
* ✔ VirtualHost works on same port
* ✔ Reload ≠ Restart (reload preferred)

---

### 🔧 **Corrections / Improvements**

* IP-based hosting used only with SSL legacy setups
* Modern SSL supports name-based hosting (SNI)

---

---

## 🌐 **3️⃣ Configuring the Squid Web Proxy Cache** 🦑

### 🔹 **Concept Overview**

* **Squid** is a **proxy & caching server**
* Used to:

  * Control internet access
  * Improve bandwidth usage
  * Cache frequently accessed content

---

### 📘 **Key Definitions**

* **Proxy Server:** Intermediary between client & internet
* **Caching:** Storing frequently accessed data
* **ACL:** Access Control List

---

### 📚 **Main Content**

#### 🔸 **Installation**

```bash
sudo apt install squid
```

#### 🔸 **Configuration File**

* `/etc/squid/squid.conf`

#### 🔸 **Default Port**

* **3128**

#### 🔸 **Basic ACL Example**

```conf
acl localnet src 192.168.1.0/24
http_access allow localnet
http_access deny all
```

#### 🔸 **Start Squid**

```bash
sudo systemctl start squid
```

---

### 📌 **Important Facts for MCQs**

* Squid is **not a firewall**
* Works at **Application Layer**
* Improves performance via caching

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Squid ≠ NAT
* ✔ Squid uses ACL rules order-wise
* ✔ Deny all must be last rule
* ✔ Transparent proxy possible

---

### 🔧 **Corrections / Improvements**

* HTTPS caching is limited
* Modern setups use Squid mainly for **access control**

---

---

## 🧪 **LAB SECTION – Practical Focus (High Exam Weight)** 🧰

### 🧪 **Apache Lab**

* Install Apache
* Change `index.html`
* Verify via browser
* Create Virtual Hosts
* Enable & reload Apache

### 🧪 **Virtual Hosting Lab**

* Create multiple DocumentRoots
* Configure `ServerName`
* Test using `/etc/hosts`

### 🧪 **Squid Lab**

* Install Squid
* Configure ACL
* Set browser proxy
* Test allowed & denied access

---

## 🎯 **MCQ Rapid Revision Summary**

* Apache → Web Server → Port 80/443
* Virtual Hosting → Multiple sites, same server
* Squid → Proxy + Cache → Port 3128
* Security → Hide version, restrict access
* Reload preferred over restart

---
