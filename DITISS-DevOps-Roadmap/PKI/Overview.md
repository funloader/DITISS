# 🔐 Public Key Infrastructure (PKI) — Overview

*PG-DITISS • August 2025 Batch*

- **Total Duration: 50 Hours** (30 Theory + 20 Lab)
- **Objective:** Provide in-depth understanding of cryptography, PKI, certificates, authentication models, and securing web/email systems.

---

## 🧭 Module Structure (Session-wise Overview)

### 🧩 Session 1 — Information Security Foundations
- [ ] Information Security Concepts
- [ ] Security Attacks & Threats

---

### 🔐 Session 2 — Basic Encryption Concepts
- [ ] Basics of Encryption
- [ ] File Encryption
- [ ] Encrypting Folders (GUI & cipher command)

---

### 🧮 Session 3 — Cryptographic Fundamentals
- [ ] Symmetric vs Asymmetric Cryptography
- [ ] Cryptographic Ciphers
- [ ] Protocol Basics (history, key generation, ciphering process)

---

### 🔑 Session 4 — Encryption Algorithms
🔸 *Symmetric*
  - DES
  - AES
  - RC5

🔸 *Asymmetric*
  - RSA
  - ECC

---

### 🧭 Session 5 — Key Exchange & Attacks
- [ ] Diffie–Hellman Key Exchange
- [ ] Attacks on Encryption
- [ ] Cryptographic Issues

*Lab (CrypTool)*
- [ ] Symmetric encryption: Caesar, Vernam, DES, RC4, AES, XOR, 3DES…
- [ ] Asymmetric encryption: RSA, ECC

---

### 🧮 Session 6 — Hashing Techniques
- [ ] SHA Family (SHA-1/256/512)
- [ ] HMAC

---

### 🧾 Session 7 — PKI Fundamentals
- [ ] Digital Signatures
- [ ] Digital Certificates

---

### 🏦 Session 8 — CA & Trust Architecture
- [ ] Certificate Authorities (CA)
- [ ] Trust Models
- [ ] Certificate Issuance Workflow
- [ ] Certificate Revocation (CRL / OCSP)
- [ ] Certificate Classes & Types

---

### 🆔 Session 9 — e-Sign & Time-Stamping
- [ ] Aadhaar & e-Sign
- [ ] Time-Stamping Services

**Lab (XCA Tool)**
- [ ] Create Digital Signature
- [ ] Digitally Sign Word & PDF Documents

---

### 📜 Session 10 — PKI Standards
- [ ] PKCS Standards
- [ ] FIPS 140-2

**Lab (XCA Tool)**
- [ ] Create Digital Certificate
- [ ] Create a CA in XCA
- [ ] Issue TLS certificate for: ``https://www.ditiss.local``
- [ ] Import into browser to fix self-signed warning

---

### 🔐 Session 11 — Authentication Techniques
- [ ] Strong Authentication
- [ ] SFA & MFA
- [ ] Single Sign-On (SSO)
- [ ] OpenID, OAuth
- [ ] Graphical Passwords

---

### 🛡 Session 12 — Authentication Protocols
- [ ] Authentication Protocols
- [ ] FIDO Authentication
- [ ] Zero Trust Architecture

---

### 🌐 Session 13 — Securing Web & Email
- [ ] SSL
- [ ] TLS
- [ ] PGP
- [ ] S/MIME

**Lab (OpenSSL)**
- [ ] Create Self-Signed Certificates
- [ ] Build Hierarchical PKI Using OpenSSL
      - Root CA → rtca.pgditiss.local
      - Sub CA → sbca.pgditiss.local
- [ ] Deploy HTTPS site: https://www.pgditiss.local
- [ ] Configure DNS/Name Resolution
- [ ] Access via Windows client

---

### 🏛 Session 14 & 15 — Legal Framework & Directory Services
- [ ] IT Act
- [ ] LDAP / Active Directory
- [ ] Introduction to Blockchain

**Lab**
- [ ] Sign & Encrypt Email using Thunderbird / Outlook
(Using certificates created earlier)

---

### 🎯 End of Module Outcomes

After completing PKI (50 hours), a PG-DITISS student can:

✔ Understand Cryptographic Algorithms
- Symmetric, asymmetric, hashing, HMAC
- Algorithms: DES, AES, RC4, RSA, ECC

✔ Implement Digital Signatures & Certificates
- Create, sign, validate certificates
- Use CA, Sub-CA & trust chains

✔ Deploy PKI in Real Environments
- Build full PKI (Root + Sub CA) on Linux
- Issue TLS certificates for websites
- Secure web servers using OpenSSL & Apache

✔ Apply Authentication Frameworks
- SSO, MFA, OAuth, OpenID
- FIDO & Zero Trust

✔ Secure Documents & Emails
- PGP, S/MIME
- Sign PDFs, Word documents
- Encrypted email communication

✔ Understand Legal & Enterprise Identity Systems
- IT Act & compliance
- LDAP / Active Directory basics
