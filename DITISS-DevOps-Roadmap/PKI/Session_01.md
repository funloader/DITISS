# Session 01 : Information Security – Core Concepts, Mechanisms, Attacks & Threats
---

## 1. Concept Overview

**Information Security (InfoSec)** deals with protecting information and information systems from **unauthorized access, misuse, disclosure, disruption, modification, or destruction**.
It uses **cryptography, authentication, access control, and security protocols** to mitigate **security attacks and threats**.

---

## 2. Key Definitions (MCQ One-Liners)

* **Information Security:** Protection of information to ensure **CIA triad**.
* **Cryptography:** Art and science of securing information using mathematical techniques.
* **Plaintext:** Original readable data.
* **Ciphertext:** Encrypted, unreadable data.
* **Encryption:** Conversion of plaintext to ciphertext.
* **Decryption:** Conversion of ciphertext to plaintext.
* **Key:** Secret value controlling encryption/decryption.
* **Cryptanalysis:** Art of breaking encryption.
* **Cryptology:** Cryptography + Cryptanalysis.

---

## 3. Main Content (Organized & Exam-Focused)

### A. Goals / Security Services of Information Security (Very Important)

| Security Service    | Purpose                         | MCQ Keyword       |
| ------------------- | ------------------------------- | ----------------- |
| **Confidentiality** | Prevent unauthorized disclosure | Encryption        |
| **Integrity**       | Detect data modification        | Hash, MAC         |
| **Authentication**  | Verify identity                 | Certificates      |
| **Non-repudiation** | Prevent denial of action        | Digital Signature |

---

### B. Cryptography Basics (InfoSec Foundation)

#### 1. Types of Encryption

| Type           | Keys Used        | Examples      | MCQ Note       |
| -------------- | ---------------- | ------------- | -------------- |
| **Symmetric**  | Same key         | AES, DES, RC5 | Faster         |
| **Asymmetric** | Public + Private | RSA, ECC      | Slower         |
| **Hybrid**     | Both             | TLS, SSL, PGP | Most practical |

---

#### 2. Symmetric Algorithms (Exam Facts)

* **DES**

  * Key size: **56 bits**
  * Block size: **64 bits**
  * Structure: **Feistel network**
  * Status: ❌ **Insecure (brute force)**

* **AES**

  * Key sizes: **128 / 192 / 256 bits**
  * Block size: **128 bits**
  * Standardized by **NIST (2001)**
  * Status: ✅ **Secure & widely used**

* **RC5**

  * Variable block & key size
  * Designed by **Ron Rivest (1994)**
  * Research/benchmark use

---

#### 3. Asymmetric Algorithms

* **RSA**

  * Invented: **1977**
  * Security based on: **Integer factorization**
  * Used in: **SSL/TLS, Digital Signature**

* **ECC**

  * Security based on: **ECDLP**
  * Smaller keys, higher efficiency
  * **256-bit ECC ≈ 3072-bit RSA**

* **Diffie–Hellman**

  * Purpose: **Key exchange**
  * Vulnerable to: **MITM attack**
  * Mitigation: Certificates / PKI

---

### C. Hashing & Message Integrity

* **SHA Family**

  * SHA-1 ❌ (Broken – collision attack 2017)
  * SHA-2 / SHA-3 ✅ Secure
* **HMAC**

  * Keyed hash
  * Protects against **length-extension attack**
  * Used in **TLS, IPsec**

---

### D. Digital Signature vs Digital Certificate (High MCQ Weight)

| Feature   | Digital Signature          | Digital Certificate       |
| --------- | -------------------------- | ------------------------- |
| Purpose   | Message authenticity       | Identity trust            |
| Uses      | Integrity, Non-repudiation | Authentication            |
| Based on  | Hash + Private key         | PKI                       |
| Format    | Attached to document       | **X.509**                 |
| Issued by | Signer                     | **Certificate Authority** |

---

### E. Certificate Authority (CA) & Trust Model

* CA issues, manages, revokes certificates
* Trust via **Chain of Trust**
* Root CA → Intermediate CA → End Entity
* Revocation methods:

  * **CRL** (List based, heavy)
  * **OCSP** (Real-time, lightweight)

---

### F. Authentication Mechanisms (Threat Mitigation)

#### 1. Authentication Factors

* Something you **know** → Password
* Something you **have** → Token
* Something you **are** → Biometrics

#### 2. Types

| Type | Factors | Security  |
| ---- | ------- | --------- |
| SFA  | 1       | Weak      |
| 2FA  | 2       | Strong    |
| MFA  | ≥2      | Strongest |

---

### G. Single Sign-On (SSO)

* Login once, access many systems
* Protocols:

  * **Kerberos**
  * **SAML**
  * **OAuth 2.0**
  * **OpenID Connect**
* Risk: **Single Point of Failure**

---

### H. Modern Authentication & Security Models

* **FIDO**

  * Passwordless
  * Public-key based
  * Resistant to phishing
* **Zero Trust Architecture**

  * “Never trust, always verify”
  * Least privilege
  * Continuous monitoring

---

### I. Securing Communication (Critical Exam Area)

#### SSL vs TLS

| Aspect   | SSL            | TLS             |
| -------- | -------------- | --------------- |
| Status   | Deprecated     | Active          |
| Security | Weak           | Strong          |
| Use      | HTTPS (legacy) | HTTPS (current) |

* TLS uses **Hybrid Encryption**
* Provides: Authentication, Confidentiality, Integrity

---

### J. Email Security

| Standard   | Usage            |
| ---------- | ---------------- |
| **PGP**    | Personal email   |
| **S/MIME** | Enterprise email |

---

### K. Directory Services

* **LDAP:** Protocol
* **Active Directory:** Microsoft implementation
* Used for **AAA (Authentication, Authorization, Accounting)**

---

### L. Blockchain (Threat-Resistant Ledger)

* Decentralized, immutable ledger
* Uses: Cryptocurrency, Supply Chain
* Types:

  * Public
  * Private
  * Consortium

---

## 4. Important Facts / Points for MCQs

* AES → **Symmetric**
* RSA → **Asymmetric**
* SHA → **Integrity**
* Digital Signature → **Non-repudiation**
* OCSP → **Real-time revocation**
* ECC → **Smaller key, same security**
* Zero Trust → **No implicit trust**

---

## 5. Examples (Exam-Friendly)

* HTTPS → TLS + Digital Certificate
* Online Banking → MFA + Encryption
* Email Signing → Digital Signature
* VPN → Diffie-Hellman + AES

---

## 6. MCQ Pointers / Exam Traps

* ❌ SHA ≠ Encryption (It’s hashing)
* ❌ Digital Certificate ≠ Digital Signature
* ❌ OAuth ≠ Authentication (Authorization only)
* ✔ ECC more efficient than RSA
* ✔ CRL vs OCSP confusion common
* ✔ DES insecure due to key length

---

## 7. Corrections / Improvements / Suggested Substitutions

1. **SHA-1 should not be recommended** → Use SHA-256 / SHA-3
2. **SSL terminology outdated** → Prefer TLS
3. **DES not secure** → Replace with AES
4. **Birthday attack** applies mainly to **hash functions**, not encryption
5. **Non-repudiation** mainly via **Digital Signature**, not encryption
6. Graphical passwords → usability issues, not universally “more secure”

---
