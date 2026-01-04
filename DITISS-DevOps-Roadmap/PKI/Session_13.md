# Session 13 – Securing Websites and Emails (SSL, TLS, PGP, S/MIME)
---

## 1. Concept Overview

Securing websites and emails involves using **cryptographic protocols** to ensure:

* **Confidentiality**
* **Integrity**
* **Authentication**
* **Non-repudiation (for emails)**

**Website security → SSL / TLS**
**Email security → PGP / S-MIME**

---

## 2. Key Definitions (Very Important for MCQs)

* **SSL (Secure Sockets Layer):**
  Cryptographic protocol for securing data transmission over networks (now deprecated).

* **TLS (Transport Layer Security):**
  Successor to SSL; provides secure communication over computer networks.

* **PGP (Pretty Good Privacy):**
  Hybrid cryptosystem used to secure email communication.

* **S/MIME (Secure/Multipurpose Internet Mail Extensions):**
  Certificate-based standard for secure email messaging.

---

## 3. Main Content (Organized from Notes)

---

## 3.1 SSL (Secure Sockets Layer)

### Overview

* Developed by **Netscape**
* Used to secure **HTTP → HTTPS**
* Uses **public key cryptography + symmetric encryption**
* **Deprecated** due to vulnerabilities

### SSL Versions (MCQ Favorite)

| Version | Status                   |
| ------- | ------------------------ |
| SSL 2.0 | Insecure                 |
| SSL 3.0 | Insecure (POODLE attack) |

**MCQ Line:**

> SSL is **obsolete** and replaced by TLS

---

### SSL Provides

* Server authentication
* Data confidentiality
* Data integrity

---

## 3.2 TLS (Transport Layer Security)

### Overview

* Standard protocol for **secure web communication**
* Used in **HTTPS, FTPS, SMTP, IMAP**
* Maintained by **IETF**

---

### TLS Versions

| Version | Status      |
| ------- | ----------- |
| TLS 1.0 | Weak        |
| TLS 1.1 | Weak        |
| TLS 1.2 | Secure      |
| TLS 1.3 | Most secure |

---

### TLS Handshake (Exam-Oriented Flow)

1. Client Hello
2. Server Hello + Certificate
3. Key exchange
4. Session key generation
5. Secure communication

**MCQ Line:**

> TLS uses **asymmetric encryption for key exchange** and **symmetric encryption for data**

---

### TLS Advantages Over SSL

* Stronger algorithms
* Better handshake
* Improved performance
* Resistance to known attacks

---

## 3.3 PGP (Pretty Good Privacy)

### Overview

* Developed by **Phil Zimmermann (1991)**
* Used for **email encryption**
* Uses **hybrid encryption**

---

### How PGP Works

1. Message hashed (Integrity)
2. Hash encrypted with sender’s private key (Signature)
3. Message encrypted using symmetric key
4. Symmetric key encrypted using recipient’s public key

---

### PGP Security Services

* Confidentiality
* Authentication
* Integrity
* Non-repudiation

---

### Key Characteristics

* **Web of Trust** model
* No central CA mandatory
* User-managed keys

**MCQ Line:**

> PGP uses **Web of Trust**, not PKI hierarchy

---

## 3.4 S/MIME (Secure MIME)

### Overview

* Email security standard
* Uses **X.509 digital certificates**
* Depends on **PKI and CAs**

---

### S/MIME Services

* Email encryption
* Digital signatures
* Authentication
* Non-repudiation

---

### S/MIME Architecture

* Sender encrypts email using recipient’s public key
* Sender signs email using private key
* Certificate verified using CA chain

---

## 4. Comparison Tables (High MCQ Value)

---

### SSL vs TLS

| Feature   | SSL        | TLS          |
| --------- | ---------- | ------------ |
| Status    | Deprecated | Active       |
| Security  | Weak       | Strong       |
| Developer | Netscape   | IETF         |
| Usage     | Old HTTPS  | Modern HTTPS |

---

### PGP vs S/MIME

| Feature        | PGP            | S/MIME          |
| -------------- | -------------- | --------------- |
| Trust Model    | Web of Trust   | PKI             |
| Certificates   | Optional       | Mandatory       |
| Key Management | User-based     | CA-based        |
| Usage          | Personal email | Corporate email |

---

## 5. Important Facts / Points for MCQs

* HTTPS = HTTP + TLS
* TLS uses **digital certificates**
* SSL is **obsolete**
* PGP invented in **1991**
* S/MIME relies on **X.509 certificates**
* PGP uses **hybrid cryptography**

---

## 6. Examples (If Applicable)

* **Website:**
  `https://bank.com` → Uses **TLS**

* **Email:**
  Outlook corporate email → **S/MIME**
  Personal secure email → **PGP**

---

## 7. MCQ Pointers / Exam Traps

* ❌ SSL is still secure
* ❌ PGP uses centralized CA
* ❌ TLS encrypts entire handshake symmetrically
* ✔ TLS replaces SSL
* ✔ PGP uses Web of Trust
* ✔ S/MIME uses PKI

**Likely MCQ Framing:**

* “Which protocol secures HTTPS?”
* “Which email security uses PKI?”
* “Which protocol is deprecated?”

---

## 8. Corrections / Improvements / Suggested Substitutions

* Replace **SSL** with **TLS 1.2 / TLS 1.3**
* Avoid TLS 1.0 and TLS 1.1
* Use **S/MIME** in enterprise environments
* Use **PGP** where CA infrastructure is unavailable
* Emphasize **hybrid encryption** in PGP (often missed)

---
