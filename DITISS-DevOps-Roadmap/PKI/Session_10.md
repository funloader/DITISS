# Session 10 – Public Key Cryptography Standards
---

## 1. Public Key Cryptography Standards (PKCS)

### 1.1 What is PKCS?

**PKCS (Public Key Cryptography Standards)** is a **set of standards developed by RSA Laboratories** to define **formats and methods** for public-key cryptography.

**MCQ Line:**

> PKCS standards ensure **interoperability**

---

## 2. Important PKCS Standards (High MCQ Weight)

### 2.1 PKCS#1 – RSA Cryptography Standard

* Defines **RSA encryption & signature**
* Specifies key formats
* Padding schemes (e.g., OAEP, PSS)

**MCQ Line:**

> PKCS#1 is specific to **RSA**

---

### 2.2 PKCS#5 – Password-Based Cryptography

* Used for **password-based encryption**
* Defines key derivation from passwords
* Example: PBKDF2

---

### 2.3 PKCS#7 – Cryptographic Message Syntax (CMS)

* Format for **signed & encrypted messages**
* Used in **S/MIME**

---

### 2.4 PKCS#8 – Private Key Information Syntax

* Standard format for **storing private keys**
* Supports encryption with password

**MCQ Line:**

> Private keys stored using **PKCS#8**

---

### 2.5 PKCS#10 – Certificate Signing Request (CSR)

* Format for requesting digital certificate
* Contains public key & identity info

---

### 2.6 PKCS#11 – Cryptographic Token Interface

* Interface for **hardware security modules**
* Used with smart cards, USB tokens

---

### 2.7 PKCS#12 – Personal Information Exchange

* Stores **private key + certificate**
* Portable format (.pfx, .p12)

---

## 3. Quick PKCS Summary Table (MCQ Friendly)

| PKCS | Purpose                   |
| ---- | ------------------------- |
| #1   | RSA                       |
| #5   | Password-based crypto     |
| #7   | Signed/encrypted messages |
| #8   | Private key storage       |
| #10  | CSR                       |
| #11  | Crypto token interface    |
| #12  | Key & cert bundle         |

---

## 4. FIPS 140-2

### 4.1 Definition

**FIPS 140-2** is a **US government standard** specifying **security requirements for cryptographic modules**.

**MCQ Line:**

> FIPS 140-2 applies to **cryptographic modules**, not algorithms

---

### 4.2 Purpose of FIPS 140-2

* Ensure cryptographic security
* Certify crypto products
* Used by government & regulated sectors

---

## 5. FIPS 140-2 Security Levels

### Level 1 – Basic Security

* Approved algorithms
* No physical security

### Level 2 – Tamper Evidence

* Tamper-evident seals
* Role-based authentication

### Level 3 – Tamper Resistance

* Tamper-resistant hardware
* Identity-based authentication
* Protected key storage

### Level 4 – Highest Security

* Environmental protection
* Automatic zeroization
* Intrusion detection

**MCQ Line:**

> Level 4 is **most secure**

---

## 6. Comparison of FIPS Levels (High MCQ Weight)

| Level | Physical Security | Authentication     |
| ----- | ----------------- | ------------------ |
| 1     | None              | Basic              |
| 2     | Tamper-evident    | Role-based         |
| 3     | Tamper-resistant  | Identity-based     |
| 4     | Environmental     | Automatic response |

---

## 7. Scope of FIPS 140-2

* Key management
* Algorithm implementation
* Module design
* Physical security
* Self-tests

---

## 8. PKCS vs FIPS (MCQ Comparison)

| Feature      | PKCS             | FIPS 140-2                  |
| ------------ | ---------------- | --------------------------- |
| Developed by | RSA Labs         | US Govt                     |
| Focus        | Crypto formats   | Crypto module security      |
| Applies to   | Software formats | Hardware & software modules |
| Nature       | Standards        | Compliance                  |

---

## 9. Lab Mapping (Session 10)

| Lab Task            | Standard   |
| ------------------- | ---------- |
| CSR generation      | PKCS#10    |
| Private key storage | PKCS#8     |
| Certificate bundle  | PKCS#12    |
| HSM usage           | PKCS#11    |
| Compliance check    | FIPS 140-2 |

---

## 10. Important MCQ Facts

* PKCS ≠ Encryption algorithm
* PKCS#11 used for tokens
* PKCS#12 uses .pfx format
* FIPS 140-2 has **4 levels**
* FIPS applies to modules

---

## 11. Common Exam Traps

* ❌ FIPS defines encryption algorithms
* ❌ PKCS#10 stores private keys
* ❌ PKCS#7 is key storage
* ✔ PKCS#8 stores private keys
* ✔ PKCS#1 is RSA

---

## 12. Corrections / Best Practices

* Use **PBKDF2** for passwords
* Encrypt private keys (PKCS#8)
* Prefer **FIPS-validated modules**
* Regularly audit crypto compliance

---
