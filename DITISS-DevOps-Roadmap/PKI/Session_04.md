# Session 4 – Symmetric & Asymmetric Key Encryption
---

## 1. Concept Overview

Encryption algorithms are broadly classified into:

* **Symmetric Key Encryption** → Same key for encryption & decryption
* **Asymmetric Key Encryption** → Public–Private key pair

**MCQ Priority:**

> Algorithm type, key size, structure, security status, use-case

---

## 2. Key Definitions

* **Symmetric Encryption:** Uses a single shared secret key
* **Asymmetric Encryption:** Uses mathematically related key pair
* **Block Cipher:** Encrypts fixed-size blocks of data
* **Key Length:** Size of cryptographic key in bits
* **Feistel Network:** Encryption structure using repeated rounds

---

## 3. Symmetric Key Encryption

### 3.1 General Characteristics

* Fast & efficient
* Used for **bulk data encryption**
* Key distribution is a major challenge

---

## 4. DES (Data Encryption Standard)

### 4.1 Basic Details (High MCQ Weight)

| Feature        | DES                 |
| -------------- | ------------------- |
| Type           | Symmetric           |
| Cipher Type    | Block cipher        |
| Block size     | **64 bits**         |
| Key size       | **56 bits**         |
| Structure      | **Feistel Network** |
| Rounds         | **16**              |
| Developed by   | IBM                 |
| Adopted by     | US Govt (1977)      |
| Current status | ❌ Insecure          |

---

### 4.2 DES Working (MCQ-Oriented)

* Plaintext split into **64-bit blocks**
* Each round uses a **48-bit subkey**
* Uses **substitution & permutation**
* Final swap after last round

**MCQ Line:**

> DES uses **same algorithm** for encryption & decryption (key order reversed)

---

### 4.3 Weakness of DES

* Short key length → **Brute-force attack**
* Successfully broken in **1998**

---

## 5. AES (Advanced Encryption Standard)

### 5.1 Basic Details

| Feature     | AES                                  |
| ----------- | ------------------------------------ |
| Type        | Symmetric                            |
| Cipher Type | Block cipher                         |
| Block size  | **128 bits**                         |
| Key sizes   | **128 / 192 / 256 bits**             |
| Structure   | **Substitution–Permutation Network** |
| Selected by | NIST                                 |
| Year        | **2001**                             |
| Status      | ✅ Secure                             |

---

### 5.2 AES Internal Operations (Exam Favorite)

Each round consists of:

1. **SubBytes**
2. **ShiftRows**
3. **MixColumns**
4. **AddRoundKey**

**MCQ Trap:**

> AES is **NOT Feistel-based**

---

### 5.3 Advantages of AES

* Strong security
* High performance
* Hardware & software friendly
* Widely standardized

---

### 5.4 AES Modes (Mention Only)

* ECB ❌
* CBC
* CTR
* GCM ✅ (Authenticated Encryption)

---

## 6. RC5 (Rivest Cipher 5)

### 6.1 Key Characteristics

| Feature    | RC5                       |
| ---------- | ------------------------- |
| Designer   | Ronald Rivest             |
| Year       | 1994                      |
| Type       | Symmetric                 |
| Block size | Variable (32/64/128 bits) |
| Key size   | Variable (0–2040 bits)    |
| Rounds     | Variable (0–255)          |
| Structure  | Feistel-like              |
| Status     | Limited use               |

---

### 6.2 RC5 Highlights

* Simple & flexible design
* Uses:

  * XOR
  * Addition
  * Bit rotations

**MCQ Line:**

> RC5 supports **variable parameters**

---

## 7. Asymmetric Key Encryption

### 7.1 General Characteristics

* Uses **key pairs**
* Slower than symmetric
* Used for:

  * Key exchange
  * Digital signatures
  * Authentication

---

## 8. RSA (Rivest–Shamir–Adleman)

### 8.1 Basic Details

| Feature         | RSA                                 |
| --------------- | ----------------------------------- |
| Type            | Asymmetric                          |
| Invented        | **1977**                            |
| Based on        | **Integer factorization**           |
| Keys            | Public & Private                    |
| Common key size | 2048 / 3072 bits                    |
| Uses            | Encryption, Signature, Key exchange |

---

### 8.2 RSA Key Generation (MCQ Steps)

1. Choose primes **p, q**
2. Compute **n = p × q**
3. Compute **φ(n)**
4. Choose **e**
5. Compute **d**
6. Public key → (e, n)
7. Private key → (d, n)

---

### 8.3 RSA Limitations

* Slow
* Large key sizes
* Not used for bulk data

**MCQ Line:**

> RSA is mainly used for **key exchange**, not data encryption

---

## 9. ECC (Elliptic Curve Cryptography)

### 9.1 Basic Details

| Feature        | ECC                        |
| -------------- | -------------------------- |
| Type           | Asymmetric                 |
| Security basis | **ECDLP**                  |
| Key size       | Small                      |
| Example        | 256-bit ECC ≈ 3072-bit RSA |
| Usage          | TLS, Mobile, IoT           |

---

### 9.2 Advantages of ECC

* Smaller keys
* Faster computation
* Low power consumption
* High security per bit

---

## 10. Symmetric vs Asymmetric (MCQ Comparison)

| Feature     | Symmetric       | Asymmetric   |
| ----------- | --------------- | ------------ |
| Speed       | Fast            | Slow         |
| Keys        | Single          | Key pair     |
| Scalability | Poor            | Good         |
| Usage       | Data encryption | Key exchange |
| Examples    | AES, DES        | RSA, ECC     |

---

## 11. Important Facts / Points for MCQs

* DES key = **56 bits**
* AES block size = **128 bits**
* AES ≠ Feistel
* RSA security = **Factorization**
* ECC security = **Discrete log**
* RC5 = Variable parameters

---

## 12. Examples (Exam-Oriented)

* Disk encryption → **AES**
* SSL/TLS key exchange → **RSA / ECC**
* Mobile devices → **ECC**

---

## 13. MCQ Pointers / Exam Traps

* ❌ DES is not secure
* ❌ RSA is not symmetric
* ❌ AES block size is NOT variable
* ✔ ECC gives same security with smaller keys
* ✔ RC5 parameters are configurable

---

## 14. Corrections / Improvements / Suggested Substitutions

* DES should be referred as **deprecated**, not obsolete
* RC5 is **rarely deployed**, mainly academic
* Use **AES-GCM** instead of AES-ECB
* Prefer **ECC over RSA** for modern systems
* Avoid small RSA key sizes (<2048 bits)

---
