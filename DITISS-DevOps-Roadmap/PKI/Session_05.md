# Session 5 – Key Exchange, Attacks & Cryptographic Issues
---

## 1. Diffie–Hellman (DH) Key Exchange

### 1.1 Purpose

Diffie–Hellman is a **key exchange protocol**, not an encryption algorithm.
It allows two parties to **securely establish a shared secret** over an insecure channel.

**MCQ Line:**

> Diffie–Hellman solves the **key distribution problem**

---

### 1.2 Basic Characteristics

| Feature        | Diffie–Hellman             |
| -------------- | -------------------------- |
| Type           | Key exchange               |
| Keys           | Shared secret              |
| Security basis | Discrete Logarithm Problem |
| Encryption     | ❌ No                       |
| Authentication | ❌ No (by default)          |
| Used in        | SSL/TLS, VPNs              |

---

### 1.3 Diffie–Hellman Working (Exam Steps)

1. Publicly agree on:

   * Prime number **p**
   * Generator **g**
2. Alice chooses private key **a**

   * Computes **A = gᵃ mod p**
3. Bob chooses private key **b**

   * Computes **B = gᵇ mod p**
4. Exchange **A** and **B**
5. Shared secret:

   * Alice → **K = Bᵃ mod p**
   * Bob → **K = Aᵇ mod p**

**Result:**

> Both get **same shared secret**

---

### 1.4 Variants of Diffie–Hellman

* **DH (Static DH)**
* **Ephemeral DH (DHE)** → Perfect Forward Secrecy
* **Elliptic Curve DH (ECDH)** → Efficient, modern

**MCQ Line:**

> ECDH provides same security with **smaller keys**

---

### 1.5 Limitations of DH

* Vulnerable to **Man-in-the-Middle (MITM)**
* No authentication by default
* Needs digital signatures or certificates

---

## 2. Attacks Against Encryption

### 2.1 Classification of Cryptographic Attacks

#### Based on Attacker’s Knowledge

| Attack Type       | Description                      |
| ----------------- | -------------------------------- |
| Ciphertext-only   | Only ciphertext available        |
| Known-plaintext   | Plaintext–ciphertext pairs known |
| Chosen-plaintext  | Attacker chooses plaintext       |
| Chosen-ciphertext | Attacker chooses ciphertext      |

---

### 2.2 Brute Force Attack

* Tries **all possible keys**
* Success depends on **key length**
* DES vulnerable, AES secure

**MCQ Line:**

> Increasing key size increases brute-force resistance

---

### 2.3 Man-in-the-Middle (MITM) Attack

* Attacker intercepts communication
* Common in **Diffie–Hellman**
* Prevented using:

  * Digital certificates
  * Authentication

---

### 2.4 Replay Attack

* Captures and replays valid messages
* Common in authentication protocols
* Prevention:

  * Timestamps
  * Nonces

---

### 2.5 Side-Channel Attacks

* Exploit **implementation**, not algorithm
* Types:

  * Timing attack
  * Power analysis
  * Electromagnetic analysis

**MCQ Line:**

> Side-channel attacks exploit **physical characteristics**

---

### 2.6 Cryptanalytic Attacks

* Exploit mathematical weaknesses
* Examples:

  * Differential cryptanalysis
  * Linear cryptanalysis

---

### 2.7 Padding Oracle Attack

* Targets block cipher padding
* Common in CBC mode
* Requires error messages

---

## 3. Cryptographic Issues

### 3.1 Key Management Issues

* Key generation
* Secure storage
* Distribution
* Rotation
* Revocation

**MCQ Line:**

> Key management is the **weakest link** in cryptography

---

### 3.2 Weak Key Problems

* Predictable keys
* Reused keys
* Default passwords
* Short key lengths

---

### 3.3 Algorithm Implementation Issues

* Poor random number generation
* Incorrect padding
* Insecure modes (ECB)
* Hard-coded keys

---

### 3.4 Compatibility & Performance Issues

* Encryption overhead
* Legacy system support
* Hardware limitations
* Power consumption (IoT)

---

### 3.5 Legal & Policy Issues

* Export restrictions
* Compliance (FIPS, GDPR)
* National crypto policies

---

### 3.6 Human-Related Issues

* Weak passwords
* Social engineering
* Poor security awareness

---

## 4. Lab-Oriented Mapping (Exam Perspective)

| Lab Topic         | Algorithm / Tool  |
| ----------------- | ----------------- |
| Key exchange      | Diffie–Hellman    |
| File encryption   | AES               |
| Key generation    | OpenSSL           |
| Secure channels   | TLS               |
| Attack simulation | MITM, brute force |

---

## 5. Important MCQ Facts

* DH ≠ Encryption
* DH vulnerable to MITM
* ECDH > DH
* AES resists brute force
* ECB mode is insecure
* Key management is critical

---

## 6. Quick Comparison Table

| Concept        | Purpose                     |
| -------------- | --------------------------- |
| Diffie–Hellman | Key exchange                |
| AES            | Data encryption             |
| RSA            | Key exchange + signatures   |
| ECC            | Efficient asymmetric crypto |

---

## 7. Common Exam Traps

* ❌ DH provides authentication
* ❌ Encryption alone ensures security
* ❌ Longer algorithm name = stronger
* ✔ Key size matters
* ✔ Implementation matters

---

## 8. Corrections / Best Practices

* Use **DHE/ECDHE** instead of static DH
* Avoid **ECB mode**
* Enforce **key rotation**
* Use **hardware security modules (HSMs)**
* Combine crypto with authentication

---

