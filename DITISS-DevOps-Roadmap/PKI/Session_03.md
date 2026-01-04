# Session 03 – Cryptographic Fundamentals, Ciphers & Protocols
---

## 1. Cryptographic Fundamentals (High-Weight Concepts)

### 1.1 What is Cryptography?

* Science of securing information using **mathematical algorithms**
* Provides **confidentiality, integrity, authentication, non-repudiation**

**MCQ Line:**

> Cryptography is a **preventive security control**.

---

### 1.2 Cryptographic Objectives

| Objective       | Achieved Using    | MCQ Tip              |
| --------------- | ----------------- | -------------------- |
| Confidentiality | Encryption        | Symmetric/Asymmetric |
| Integrity       | Hash, MAC         | SHA                  |
| Authentication  | Certificates      | PKI                  |
| Non-repudiation | Digital Signature | Private key          |

---

### 1.3 Cryptographic Primitives (Exam Favorite)

| Primitive         | Purpose                     |
| ----------------- | --------------------------- |
| Encryption        | Confidentiality             |
| Hash Function     | Integrity                   |
| MAC               | Integrity + Authentication  |
| Digital Signature | Integrity + Non-repudiation |
| Key Exchange      | Secure key sharing          |

---

### 1.4 Key Concepts

* **Kerckhoffs’s Principle:** Algorithm can be public; **key must be secret**
* **Confusion:** Hides relationship between key & ciphertext
* **Diffusion:** Spreads plaintext statistics

**MCQ Trap:**

> Confusion & diffusion are properties of **block ciphers**, not hash functions.

---

## 2. Cryptographic Ciphers

### 2.1 Classification of Ciphers

| Basis     | Types                        |
| --------- | ---------------------------- |
| Key usage | Symmetric / Asymmetric       |
| Operation | Block / Stream               |
| Function  | Substitution / Transposition |

---

## 3. Symmetric Cryptographic Ciphers

### 3.1 Characteristics

* Same key for encryption & decryption
* Fast & efficient
* Key distribution problem

---

### 3.2 Block vs Stream Ciphers

| Feature           | Block Cipher | Stream Cipher   |
| ----------------- | ------------ | --------------- |
| Unit              | Fixed block  | Bit/byte stream |
| Example           | AES          | RC4             |
| Speed             | Moderate     | Very fast       |
| Error propagation | High         | Low             |

---

### 3.3 Important Symmetric Algorithms (MCQ Core)

#### 3.3.1 DES

* Key size: **56 bits**
* Block size: **64 bits**
* Structure: **Feistel**
* Status: ❌ Insecure

---

#### 3.3.2 3DES

* DES applied **3 times**
* Key size: **168 bits**
* Status: ❌ Slow & deprecated

---

#### 3.3.3 AES (Most Important)

* Key sizes: **128 / 192 / 256**
* Block size: **128 bits**
* Structure: **Substitution-Permutation Network**
* Status: ✅ Secure

**MCQ Line:**

> AES is **not Feistel-based**.

---

#### 3.3.4 RC4

* Stream cipher
* Used in **WEP, early TLS**
* Status: ❌ Broken

---

### 3.4 Modes of Operation (Very Important)

| Mode | Feature                  | MCQ Note           |
| ---- | ------------------------ | ------------------ |
| ECB  | No IV                    | ❌ Insecure         |
| CBC  | Uses IV                  | Error propagation  |
| CFB  | Stream-like              | Self-synchronizing |
| OFB  | No error propagation     | Needs sync         |
| GCM  | Authenticated encryption | Fast & secure      |

**MCQ Trap:**

> ECB leaks patterns.

---

## 4. Asymmetric Cryptographic Ciphers

### 4.1 Characteristics

* Uses **Public & Private key**
* Slower than symmetric
* Solves key distribution problem

---

### 4.2 Major Asymmetric Algorithms

#### 4.2.1 RSA

* Invented: **1977**
* Security: **Integer factorization**
* Used for: Encryption, Signature, Key exchange

---

#### 4.2.2 Diffie–Hellman

* Purpose: **Key exchange**
* Problem: **Discrete Logarithm**
* Vulnerable to: **MITM**

---

#### 4.2.3 Elliptic Curve Cryptography (ECC)

* Based on **ECDLP**
* Smaller keys, same security
* Used in: TLS, Mobile devices

---

### 4.3 Symmetric vs Asymmetric (MCQ Table)

| Feature     | Symmetric       | Asymmetric   |
| ----------- | --------------- | ------------ |
| Speed       | Fast            | Slow         |
| Keys        | Single          | Key pair     |
| Scalability | Poor            | Good         |
| Use         | Data encryption | Key exchange |

---

## 5. Cryptographic Protocols

*(History, Usage, Key Generation, Ciphering)*

---

## 5.1 SSL / TLS (Most Important Protocol)

### History

* SSL → Developed by **Netscape**
* TLS → IETF standardized version
* SSL deprecated, TLS active

---

### Usage

* Secure web communication (**HTTPS**)
* Provides:

  * Confidentiality
  * Integrity
  * Authentication

---

### Key Generation (Handshake Summary)

1. ClientHello
2. ServerHello
3. Certificate exchange
4. Key exchange (RSA / DH / ECDHE)
5. Session key generated
6. Secure communication begins

---

### Ciphering Message

* **Asymmetric** → Key exchange
* **Symmetric (AES)** → Data transfer
* **HMAC** → Integrity

**MCQ Line:**

> TLS uses **hybrid encryption**.

---

## 5.2 IPsec

### Usage

* Network-layer security
* Used in **VPNs**

### Modes

| Mode      | Purpose            |
| --------- | ------------------ |
| Transport | End-to-end         |
| Tunnel    | Gateway-to-gateway |

### Protocols

* **AH:** Integrity & authentication
* **ESP:** Confidentiality + Integrity

---

## 5.3 Kerberos

### History

* Developed by **MIT**
* Uses **symmetric cryptography**

### Usage

* Network authentication
* Time-based tickets

### Key Points

* Uses **KDC**
* Requires time synchronization

---

## 5.4 PGP (Pretty Good Privacy)

### Usage

* Secure email
* Uses **hybrid encryption**

### Components

* Symmetric key (message)
* Asymmetric key (key exchange)
* Hash (integrity)

---

## 5.5 SSH (Secure Shell)

### Usage

* Secure remote login
* Port **22**

### Features

* Encryption
* Authentication
* Integrity

---

## 6. Protocol Comparison (MCQ Gold)

| Protocol | Layer       | Primary Use    |
| -------- | ----------- | -------------- |
| TLS      | Application | Web security   |
| IPsec    | Network     | VPN            |
| SSH      | Application | Remote access  |
| Kerberos | Application | Authentication |
| PGP      | Application | Email          |

---

## 7. Common Exam Traps

* ❌ TLS ≠ Symmetric only
* ❌ RSA is not used for bulk data
* ❌ ECB is not secure
* ✔ ECC ≠ RSA
* ✔ IPsec works at Network layer

---

## 8. Rapid MCQ One-Liners

* AES → Symmetric block cipher
* RSA → Asymmetric
* DH → Key exchange
* TLS → Hybrid encryption
* ECB → Pattern leakage
* GCM → Authenticated encryption
* Kerberos → Ticket-based auth

---

## 9. Summary for Revision

* Cryptography = math-based security
* Symmetric → fast, key problem
* Asymmetric → slow, scalable
* Protocols combine both
* TLS & IPsec are exam favorites

---
