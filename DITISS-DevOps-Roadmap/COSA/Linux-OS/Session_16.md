## 📌 Session 16 – Linux Mail Services (PG-DITISS – COSA) 📧

---

## ✉️ **1️⃣ Understanding E-mail Delivery** 🔄

### 🔹 **Concept Overview**

* E-mail delivery involves **sending, transferring, and retrieving mails**
* Uses **client–server architecture**
* Three core components:

  * **MUA** (Mail User Agent)
  * **MTA** (Mail Transfer Agent)
  * **MDA** (Mail Delivery Agent)

---

### 📘 **Key Definitions**

* **MUA:** Email client (Outlook, Thunderbird, Webmail)
* **MTA:** Transfers mail between servers (**Postfix**, Sendmail)
* **MDA:** Delivers mail to mailbox (Dovecot LDA)
* **SMTP:** Protocol for sending mail
* **POP3 / IMAP:** Protocols for receiving mail

---

### 📚 **Main Content**

#### 🔸 **E-mail Flow (Exam-Important)**

1. User sends mail via **MUA**
2. Mail sent to **MTA (SMTP)**
3. Mail routed to recipient **MTA**
4. Mail stored by **MDA**
5. User retrieves mail via **POP3 / IMAP**

---

### 📌 **Important Facts / Points for MCQs**

* SMTP → **Outgoing mail**
* POP3 / IMAP → **Incoming mail**
* MTA works on **store-and-forward model**
* Mailbox formats: **mbox**, **Maildir**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ SMTP ≠ mail reading protocol
* ✔ IMAP keeps mail on server
* ✔ POP3 downloads mail locally
* ✔ Port 25 is SMTP (default)

---

### 🔧 **Corrections / Improvements**

* Modern SMTP uses **Submission port 587**
* Port 25 often blocked by ISPs

---

---

## 📮 **2️⃣ Postfix Mail Server** 📨

### 🔹 **Concept Overview**

* **Postfix** is a **secure, fast MTA**
* Replaces Sendmail in many systems
* Handles **sending & routing emails**

---

### 📘 **Key Definitions**

* **Mail Queue:** Temporary storage for mail
* **Relay:** Forwarding mail to another server
* **SMTP Daemon:** Listens for mail requests

---

### 📚 **Main Content**

#### 🔸 **Installation**

```bash
sudo apt install postfix
```

#### 🔸 **Configuration Type**

* Internet Site
* System Mail Name → Domain name

#### 🔸 **Key Configuration File**

* `/etc/postfix/main.cf`

#### 🔸 **Important Parameters**

```conf
myhostname = mail.example.com
mydomain = example.com
mydestination = $myhostname, localhost.$mydomain
```

#### 🔸 **Service Control**

```bash
systemctl start postfix
```

---

### 📌 **Important Facts / Points for MCQs**

* Postfix is an **MTA**
* Default SMTP port → **25**
* Mail queue directory → `/var/spool/postfix`

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Postfix ≠ Mail client
* ✔ Postfix does NOT read mail
* ✔ `sendmail` command works with Postfix

---

### 🔧 **Corrections / Improvements**

* TLS & SASL recommended for security
* Postfix supports virtual domains

---

---

## 📥 **3️⃣ Dovecot – IMAP & POP Server** 📬

### 🔹 **Concept Overview**

* **Dovecot** is a **mail access server**
* Allows users to **retrieve emails**
* Supports **POP3 and IMAP**

---

### 📘 **Key Definitions**

* **IMAP:** Server-based mail access
* **POP3:** Download-based mail access
* **Mailbox:** Location where mail is stored

---

### 📚 **Main Content**

#### 🔸 **Installation**

```bash
sudo apt install dovecot-imapd dovecot-pop3d
```

#### 🔸 **Configuration File**

* `/etc/dovecot/dovecot.conf`
* `/etc/dovecot/conf.d/`

#### 🔸 **Mail Location**

```conf
mail_location = maildir:~/Maildir
```

#### 🔸 **Service Control**

```bash
systemctl start dovecot
```

---

### 📌 **Important Facts / Points for MCQs**

* IMAP port → **143**
* POP3 port → **110**
* Secure IMAP → **993**
* Secure POP3 → **995**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ Dovecot ≠ MTA
* ✔ Dovecot requires mail stored by Postfix
* ✔ IMAP supports folder sync

---

### 🔧 **Corrections / Improvements**

* IMAP preferred over POP3
* SSL/TLS strongly recommended

---

---

## 🌐 **4️⃣ SquirrelMail Web Client** 🖥️📧

### 🔹 **Concept Overview**

* **SquirrelMail** is a **web-based email client**
* Written in **PHP**
* Works with **IMAP + SMTP**

---

### 📘 **Key Definitions**

* **Webmail:** Browser-based email access
* **PHP Application:** Runs via Apache

---

### 📚 **Main Content**

#### 🔸 **Installation**

```bash
sudo apt install squirrelmail
```

#### 🔸 **Configuration**

```bash
sudo squirrelmail-configure
```

#### 🔸 **Access URL**

```
http://localhost/squirrelmail
```

---

### 📌 **Important Facts / Points for MCQs**

* Requires **Apache + PHP**
* Uses **Dovecot (IMAP)**
* Uses **Postfix (SMTP)**

---

### ⚠️ **MCQ Pointers / Exam Traps**

* ❌ SquirrelMail ≠ Mail server
* ✔ Webmail = MUA
* ✔ Needs backend mail services

---

## 🧪 **LAB – Practical Configuration Flow** 🧰

### 🧪 **Postfix Lab**

* Install Postfix
* Configure domain
* Send test mail using `mail` command

### 🧪 **Dovecot Lab**

* Enable IMAP / POP3
* Configure Maildir
* Test using telnet / client

### 🧪 **SquirrelMail Lab**

* Install & configure
* Access via browser
* Login using Linux user

---

## 🎯 **Rapid MCQ Revision (High Value)** ✅

| Component    | Role         | Port      |
| ------------ | ------------ | --------- |
| SMTP         | Sending mail | 25 / 587  |
| Postfix      | MTA          | 25        |
| Dovecot      | IMAP/POP     | 143 / 110 |
| SquirrelMail | Webmail      | Browser   |

---
