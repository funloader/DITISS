# Session 6 – Secure Hashing Methods


---

## 1. Secure Hashing – Concept Overview

### 1.1 Hash Function

A **hash function** takes an input of any size and produces a **fixed-length output** called a **hash value / message digest**.

**MCQ Line:**

> Hash functions are **one-way** and **irreversible**

---

### 1.2 Purpose of Secure Hashing

* Data integrity
* Password storage
* Digital signatures
* Message authentication

---

## 2. Properties of Secure Hash Functions (High MCQ Weight)

| Property                    | Meaning                                  |
| --------------------------- | ---------------------------------------- |
| Deterministic               | Same input → same output                 |
| Fixed length                | Output size constant                     |
| Pre-image resistance        | Hash → input infeasible                  |
| Second pre-image resistance | Same hash for different input infeasible |
| Collision resistance        | Two inputs ≠ same hash                   |

---

## 3. SHA – Secure Hash Algorithm

### 3.1 SHA Family Overview

SHA is a family of cryptographic hash functions standardized by **NIST**.

| Algorithm | Output Size | Status      |
| --------- | ----------- | ----------- |
| SHA-0     | 160 bits    | ❌ Withdrawn |
| SHA-1     | 160 bits    | ❌ Broken    |
| SHA-224   | 224 bits    | ✅           |
| SHA-256   | 256 bits    | ✅           |
| SHA-384   | 384 bits    | ✅           |
| SHA-512   | 512 bits    | ✅           |

---

### 3.2 SHA-1 (Exam Caution)

* Produces **160-bit** hash
* Vulnerable to **collision attacks**
* Deprecated since **2017**

**MCQ Line:**

> SHA-1 is **not secure**

---

### 3.3 SHA-2 Family (Important)

Includes:

* SHA-224
* SHA-256
* SHA-384
* SHA-512

**MCQ Line:**

> SHA-256 is widely used in **TLS, Blockchain, Digital signatures**

---

### 3.4 SHA Working (Conceptual Steps)

1. Padding message
2. Appending message length
3. Dividing into blocks
4. Compression function
5. Final hash output

*(No key involved)*

---

### 3.5 SHA Characteristics

| Feature    | SHA           |
| ---------- | ------------- |
| Type       | Hash function |
| Key        | ❌ No          |
| Reversible | ❌ No          |
| Output     | Fixed         |
| Usage      | Integrity     |

---

## 4. HMAC – Hash-based Message Authentication Code

### 4.1 Definition

HMAC is a **keyed hash function** that combines:

* A **secret key**
* A **hash function** (e.g., SHA-256)

**MCQ Line:**

> HMAC provides **integrity + authentication**

---

### 4.2 HMAC Construction

HMAC(K, M) =
`H((K ⊕ opad) || H((K ⊕ ipad) || M))`

*(Formula rarely required; concept is important)*

---

### 4.3 Components of HMAC

* **Secret key**
* **Message**
* **Hash function**
* **ipad & opad constants**

---

### 4.4 Advantages of HMAC

* Resistant to length-extension attacks
* Secure even if hash has weaknesses
* Efficient & fast

---

### 4.5 HMAC vs Hash (MCQ Favorite)

| Feature        | Hash           | HMAC             |
| -------------- | -------------- | ---------------- |
| Key            | ❌ No           | ✅ Yes            |
| Authentication | ❌ No           | ✅ Yes            |
| Integrity      | ✅ Yes          | ✅ Yes            |
| Use case       | Data integrity | Secure messaging |

---

## 5. Applications (Exam-Relevant)

### SHA

* Password hashing
* Digital signatures
* Blockchain (SHA-256)
* File integrity checking

### HMAC

* API authentication
* Secure communication (TLS)
* Message authentication
* Banking systems

---

## 6. Attacks on Hash Functions (Mention)

* Collision attack
* Pre-image attack
* Birthday attack

**MCQ Line:**

> Birthday attack exploits probability of collisions

---

## 7. Important MCQ Facts

* Hash functions use **no key**
* HMAC uses **secret key**
* SHA-1 is insecure
* SHA-256 output = **256 bits**
* Hashing ≠ Encryption

---

## 8. Common Exam Traps

* ❌ Hash ensures confidentiality
* ❌ HMAC is encryption
* ❌ SHA is reversible
* ✔ Hash = integrity
* ✔ HMAC = integrity + authentication

---

## 9. Corrections / Best Practices

* Avoid **SHA-1**
* Use **SHA-256 or higher**
* Never store passwords as plain hash → use salting
* Prefer **HMAC-SHA256**

---

## 10. Lab Mapping (Session 6)

| Lab Task        | Tool         |
| --------------- | ------------ |
| Hash generation | sha256sum    |
| HMAC            | OpenSSL      |
| Integrity check | Hash compare |

---
