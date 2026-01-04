# Session 12 – Authentication Protocols, FIDO & Zero Trust
---

## 1. Authentication Protocols

### 1.1 Definition

An **authentication protocol** defines the **rules and message exchanges** used to verify identity between entities over a network.

**MCQ Line:**

> Authentication protocols prevent **credential replay**

---

### 1.2 Common Authentication Protocols (High MCQ Weight)

| Protocol | Usage                       |
| -------- | --------------------------- |
| PAP      | Plain-text authentication   |
| CHAP     | Challenge–response          |
| MS-CHAP  | Microsoft variant           |
| Kerberos | Ticket-based authentication |
| RADIUS   | Centralized AAA             |
| TACACS+  | Network device auth         |

---

### 1.3 PAP (Password Authentication Protocol)

* Sends password in **plain text**
* Least secure

**MCQ Line:**

> PAP is **insecure**

---

### 1.4 CHAP (Challenge Handshake Authentication Protocol)

* Uses **challenge–response**
* Password not transmitted
* Periodic re-authentication

---

### 1.5 Kerberos (Very High MCQ Weight)

**Definition:**
A **ticket-based authentication protocol** using **symmetric key cryptography** and a **trusted third party**.

**Key Components**

* KDC (Key Distribution Center)

  * AS (Authentication Server)
  * TGS (Ticket Granting Server)

**MCQ Line:**

> Kerberos uses **tickets**, not passwords

---

### 1.6 RADIUS & TACACS+

| Feature    | RADIUS     | TACACS+         |
| ---------- | ---------- | --------------- |
| Function   | AAA        | AAA             |
| Encryption | Partial    | Full            |
| Usage      | ISP, Wi-Fi | Network devices |

---

## 2. FIDO Authentication

### 2.1 Definition

**FIDO (Fast IDentity Online)** is a **passwordless authentication standard** based on **public key cryptography**.

**MCQ Line:**

> FIDO eliminates **passwords**

---

### 2.2 FIDO Components

* User device (Authenticator)
* Client
* Server

---

### 2.3 FIDO Standards

| Standard | Description        |
| -------- | ------------------ |
| U2F      | Second-factor auth |
| UAF      | Passwordless       |
| FIDO2    | WebAuthn + CTAP    |

---

### 2.4 How FIDO Works (Exam Steps)

1. User registers authenticator
2. Key pair generated on device
3. Public key stored on server
4. Authentication via challenge-response
5. Private key never leaves device

---

### 2.5 Advantages of FIDO

* Phishing resistant
* No shared secrets
* Strong cryptography
* Device-bound keys

---

## 3. Zero Trust Architecture (ZTA)

### 3.1 Definition

**Zero Trust Architecture** assumes **no implicit trust**—even inside the network.

**MCQ Line:**

> Zero Trust = **Never trust, always verify**

---

### 3.2 Core Principles

* Verify explicitly
* Least privilege access
* Assume breach
* Continuous authentication

---

### 3.3 Zero Trust Components

* Identity & access management (IAM)
* Device verification
* Network segmentation
* Continuous monitoring

---

### 3.4 ZTA vs Traditional Security

| Feature          | Traditional     | Zero Trust     |
| ---------------- | --------------- | -------------- |
| Trust            | Perimeter-based | Identity-based |
| Internal traffic | Trusted         | Verified       |
| Access           | Static          | Dynamic        |

---

## 4. Relationship Between Topics (MCQ Insight)

* Authentication protocols → **How identity is verified**
* FIDO → **Modern passwordless authentication**
* Zero Trust → **Architecture enforcing continuous auth**

---

## 5. Important MCQ Facts

* Kerberos uses **symmetric keys**
* FIDO uses **public key cryptography**
* Zero Trust removes perimeter trust
* PAP sends passwords in plain text
* RADIUS supports AAA

---

## 6. Common Exam Traps

* ❌ FIDO stores private keys on server
* ❌ Zero Trust trusts internal network
* ❌ Kerberos uses public key crypto
* ✔ FIDO private key stays on device
* ✔ Kerberos is symmetric

---

## 7. Lab Mapping (Session 12)

| Lab Task          | Tool             |
| ----------------- | ---------------- |
| Kerberos auth     | Active Directory |
| FIDO demo         | Security keys    |
| Zero Trust policy | Cloud IAM        |

---

## 8. Corrections / Best Practices

* Replace passwords with FIDO
* Combine Zero Trust with MFA
* Use Kerberos in enterprise SSO
* Monitor continuously

---
