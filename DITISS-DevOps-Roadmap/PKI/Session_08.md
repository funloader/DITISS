# Session 8 – Certificate Authority & Certificate Management
---

## 1. Certificate Authority (CA)

### 1.1 Definition

A **Certificate Authority (CA)** is a **trusted third party** that **issues, signs, manages, and revokes digital certificates**.

**MCQ Line:**

> CA binds **identity ↔ public key**

---

### 1.2 Functions of CA (High MCQ Weight)

* Identity verification
* Certificate issuance
* Certificate renewal
* Certificate revocation
* Publishing CRL
* Maintaining trust

---

### 1.3 Types of CAs

| Type            | Description                    |
| --------------- | ------------------------------ |
| Root CA         | Top-level, self-signed         |
| Intermediate CA | Issued by Root CA              |
| Issuing CA      | Issues end-entity certificates |

**MCQ Line:**

> Root CA is **implicitly trusted**

---

## 2. Trust Model

### 2.1 Definition

The **Trust Model** defines **how trust is established and validated** among entities in a PKI environment.

---

### 2.2 CA Trust Model (Chain of Trust)

* Hierarchical trust structure
* Trust flows from **Root CA → End Entity**

**MCQ Line:**

> Trust is established through **certificate chain**

---

### 2.3 Types of Trust Models

| Model        | Description                         |
| ------------ | ----------------------------------- |
| Hierarchical | Single root, multiple intermediates |
| Web of Trust | Peer-based (PGP)                    |
| Bridge Trust | Multiple PKIs interconnected        |

---

### 2.4 Trust Verification Steps

1. Verify CA digital signature
2. Validate certificate chain
3. Check certificate validity
4. Check revocation status

---

## 3. Certificate Issuance Process

### 3.1 Definition

Certificate issuance is the **process of generating, validating, signing, and distributing** a digital certificate.

---

### 3.2 Certificate Issuance Steps (Very High MCQ Weight)

1. **Certificate Request (CSR)**
   – Contains public key & identity info
2. **Identity Verification**
   – Performed by CA or RA
3. **Certificate Creation**
   – X.509 certificate generated
4. **Certificate Signing**
   – Signed using CA’s private key
5. **Certificate Distribution**
   – Delivered to requester / repository

**MCQ Line:**

> CSR format = **PKCS#10**

---

## 4. Certificate Revocation

### 4.1 Definition

Certificate revocation is the **process of invalidating a certificate before expiry**.

---

### 4.2 Reasons for Revocation

* Private key compromise
* Certificate misuse
* Employee termination
* Certificate issued incorrectly

---

### 4.3 Certificate Revocation List (CRL)

| Feature   | CRL                  |
| --------- | -------------------- |
| Type      | Offline list         |
| Issued by | CA                   |
| Contains  | Revoked certificates |
| Drawback  | High bandwidth       |

**MCQ Line:**

> CRL is periodically downloaded

---

### 4.4 Online Certificate Status Protocol (OCSP)

| Feature   | OCSP                     |
| --------- | ------------------------ |
| Type      | Online protocol          |
| Status    | Real-time                |
| Response  | Good / Revoked / Unknown |
| Advantage | Low bandwidth            |

**MCQ Line:**

> OCSP provides **real-time certificate status**

---

### 4.5 CRL vs OCSP (High MCQ Weight)

| Feature  | CRL     | OCSP                 |
| -------- | ------- | -------------------- |
| Mode     | Offline | Online               |
| Size     | Large   | Small                |
| Response | List    | Certificate-specific |
| Speed    | Slow    | Fast                 |

---

## 5. Types and Classes of Certificates

### 5.1 Certificate Types (Usage-Based)

| Type                        | Purpose               |
| --------------------------- | --------------------- |
| DV (Domain Validated)       | Website encryption    |
| OV (Organization Validated) | Business identity     |
| EV (Extended Validation)    | High trust            |
| Code Signing                | Software authenticity |
| Email Certificate           | Secure email          |

---

### 5.2 Certificate Classes (Verification Level)

| Class   | Verification Level  | Risk   |
| ------- | ------------------- | ------ |
| Class 1 | Email/domain        | Low    |
| Class 2 | Organization        | Medium |
| Class 3 | Extended + physical | High   |

---

### 5.3 MCQ Distinction

* **Types** → Purpose
* **Classes** → Level of verification

---

## 6. Important MCQ Facts

* CA is trusted third party
* X.509 is certificate standard
* PKCS#10 used for CSR
* Root CA is self-signed
* OCSP > CRL for real-time checks

---

## 7. Common Exam Traps

* ❌ CRL provides real-time status
* ❌ OCSP stores list of revoked certs
* ❌ Root CA certificate is unsigned
* ✔ Root CA is self-signed
* ✔ OCSP reduces bandwidth usage

---

## 8. Corrections / Best Practices

* Use **OCSP stapling**
* Limit Root CA usage
* Use Intermediate CAs
* Monitor certificate expiry
* Enforce key protection

---

## 9. Lab Mapping (Session 8)

| Lab Task       | Tool    |
| -------------- | ------- |
| CSR generation | OpenSSL |
| CRL check      | OpenSSL |
| OCSP query     | OpenSSL |

---

