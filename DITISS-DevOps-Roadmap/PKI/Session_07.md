# Session 7 – PKI Fundamentals
---

## 1. Public Key Infrastructure (PKI)

### 1.1 Definition

**PKI** is a framework of **policies, procedures, hardware, software, and cryptographic techniques** used to manage **digital certificates and public-key encryption**.

**MCQ Line:**

> PKI enables **secure key management and trust**

---

### 1.2 Core Objectives of PKI

* Authentication
* Integrity
* Confidentiality
* Non-repudiation

---

### 1.3 PKI Components (High MCQ Weight)

| Component                   | Role                         |
| --------------------------- | ---------------------------- |
| Certificate Authority (CA)  | Issues & signs certificates  |
| Registration Authority (RA) | Verifies identity            |
| Digital Certificate         | Binds identity to public key |
| Public & Private Keys       | Cryptographic operations     |
| Certificate Repository      | Stores certificates          |
| CRL / OCSP                  | Certificate revocation       |

---

## 2. Digital Signature

### 2.1 Definition

A **digital signature** is a cryptographic technique used to **verify the authenticity and integrity of a message or document** and provide **non-repudiation**.

**MCQ Line:**

> Digital signatures ensure **integrity + authentication + non-repudiation**

---

### 2.2 How Digital Signature Works (Exam Steps)

1. Sender computes **hash** of message
2. Hash is encrypted using **sender’s private key**
3. Encrypted hash = **Digital Signature**
4. Receiver decrypts using **sender’s public key**
5. Receiver compares computed hash

---

### 2.3 Algorithms Used

* RSA
* DSA
* ECDSA

---

### 2.4 Properties of Digital Signature

| Property        | Supported |
| --------------- | --------- |
| Authentication  | ✅         |
| Integrity       | ✅         |
| Confidentiality | ❌         |
| Non-repudiation | ✅         |

---

### 2.5 Applications

* Software signing
* Email security
* Legal documents
* Online transactions

---

## 3. Digital Certificate

### 3.1 Definition

A **digital certificate** is an **electronic credential** issued by a **Certificate Authority (CA)** that **binds a public key to an identity**.

**MCQ Line:**

> Digital certificates establish **trust**

---

### 3.2 Certificate Contents (X.509)

* Subject name
* Public key
* Issuer (CA)
* Serial number
* Validity period
* Digital signature of CA

---

### 3.3 Types of Digital Certificates

* SSL/TLS certificates
* Code signing certificates
* Email certificates
* Client certificates

---

### 3.4 Certificate Format

| Feature  | Value     |
| -------- | --------- |
| Standard | **X.509** |
| Encoding | DER / PEM |
| Issuer   | CA        |

---

### 3.5 Role of CA

* Identity verification
* Certificate issuance
* Certificate revocation
* Trust establishment

---

## 4. Digital Signature vs Digital Certificate (Very High MCQ Weight)

| Feature   | Digital Signature           | Digital Certificate    |
| --------- | --------------------------- | ---------------------- |
| Purpose   | Verify message authenticity | Verify identity        |
| Issued by | User / entity               | Certificate Authority  |
| Key used  | Private key                 | Public key             |
| Ensures   | Integrity & non-repudiation | Trust & authentication |
| Format    | Attached to message         | X.509                  |

---

## 5. Trust in PKI

### 5.1 Chain of Trust

* Root CA → Intermediate CA → End-entity certificate

**MCQ Line:**

> Trust flows from **Root CA**

---

### 5.2 Certificate Validation Steps

1. Verify CA signature
2. Check validity period
3. Check revocation status (CRL/OCSP)
4. Verify chain of trust

---

## 6. Security Issues in PKI

* Compromised CA
* Fake certificates
* Poor key management
* Expired certificates

---

## 7. Important MCQ Facts

* Digital signature ≠ Encryption
* Certificates use **public key cryptography**
* X.509 is certificate standard
* CA is trusted third party
* Signature provides non-repudiation

---

## 8. Common Exam Traps

* ❌ Digital signature ensures confidentiality
* ❌ Certificate encrypts data
* ❌ Hashing requires key
* ✔ Signature uses private key
* ✔ Certificate binds identity to key

---

## 9. Corrections / Best Practices

* Use **SHA-256+** with signatures
* Verify certificate chain
* Use **OCSP** for real-time revocation
* Protect private keys using HSM

---

## 10. Lab Mapping (Session 7)

| Lab Task               | Tool    |
| ---------------------- | ------- |
| Certificate creation   | OpenSSL |
| Signature verification | OpenSSL |
| CSR generation         | PKCS#10 |

---
