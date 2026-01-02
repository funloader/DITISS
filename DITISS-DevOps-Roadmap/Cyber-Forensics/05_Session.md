# SESSION 5 – ENCODING, ENCRYPTION, HASHING & DATA INTEGRITY

---

## **1. Encoding and Encryption**

### **Concept Overview**

* Encoding and encryption are **NOT the same**
* Very common **MCQ confusion area**

---

### **Encoding**

#### **Definition**

* Conversion of data from one format to another **for compatibility or representation**
* **No security objective**

#### **Key Characteristics**

* Reversible **without a key**
* Publicly known algorithms

#### **Examples**

* ASCII
* Unicode
* Base64

📌 **MCQ Trap**

* Encoding ≠ security
* Encoding does **not** protect confidentiality

---

### **Encryption**

#### **Definition**

* Transforming data into **ciphertext** to prevent unauthorized access

#### **Key Characteristics**

* Requires **key/password**
* Provides **confidentiality**

---

### **Types of Encryption**

| Type       | Key Usage             | Examples  |
| ---------- | --------------------- | --------- |
| Symmetric  | Same key              | AES, DES  |
| Asymmetric | Public & Private keys | RSA, ECC  |
| Hybrid     | Both combined         | TLS / SSL |

📌 **MCQ Trap**

* Encryption ≠ hashing
* Encryption is **reversible with key**

---

## **2. The Hex Editor**

### **Definition**

* Tool to **view and edit binary data** in hexadecimal format

---

### **Key Features**

1. Hex & ASCII side-by-side view
2. Byte-level editing
3. Search & replace patterns
4. File structure analysis
5. Checksum / hash calculation
6. Disk & memory inspection
7. Byte-by-byte file comparison
8. Scripting / automation (advanced)

---

### **Uses in Forensics**

* Examine raw data
* Detect hidden / deleted content
* Analyze file headers
* Malware & reverse engineering

📌 **MCQ Trap**

* Hex editor works at **byte level**, not file level

---

## **3. Files (Forensic Perspective)**

### **Key Forensic File Components**

* File content
* File metadata

  * Creation time
  * Modification time
  * Access time
* File headers & footers
* File system allocation

---

### **Forensic Importance**

* Detect tampering
* Recover deleted files
* Identify file type mismatches

📌 **MCQ Trap**

* File extension ≠ actual file type
* Header determines true file type

---

## **4. Hashing**

### **Definition**

* One-way mathematical function converting data into **fixed-length hash value**

---

### **Key Characteristics**

* One-way (irreversible)
* Same input → same output
* Small change → large hash change (avalanche effect)

---

### **Common Hash Algorithms**

* MD5 (128-bit)
* SHA-1
* SHA-256
* SHA-512

📌 **MCQ Trap**

* Hashing ≠ encryption
* Hashing does **not** use keys

---

## **5. Hashing D/Ls (Hashing Digital Evidence)**

### **Purpose**

* Verify **integrity** of digital evidence

### **When Hashing is Done**

* Before acquisition
* After acquisition
* After analysis

---

### **Use in Forensics**

* Evidence authentication
* Detect alteration
* Chain of custody support

📌 **MCQ Trap**

* Hash mismatch = evidence modified

---

## **6. MD5 Hash Collisions**

### **Definition**

* Two different inputs producing **same MD5 hash**

---

### **Key Facts**

* MD5 produces 128-bit hash
* First practical collision shown in **2004**
* Proven insecure

---

### **Impact**

* Fake files with same hash
* Digital signature forgery
* Certificate authority attacks

📌 **MCQ Trap**

* MD5 is **not reliable** for security
* Still sometimes used for **non-cryptographic integrity checks**

---

## **7. Hash Collisions (General)**

### **Definition**

* When two different inputs generate the **same hash value**

---

### **Why It Matters**

* Breaks integrity assurance
* Compromises authentication
* Affects digital signatures

---

### **Collision Resistance**

* Strong hash functions make collisions **computationally infeasible**

📌 **MCQ Trap**

* Collision resistance ≠ preimage resistance

---

## **8. Bit Rot**

### **Definition**

* **Gradual data corruption** due to physical or environmental factors

---

### **Causes**

* Aging storage media
* Magnetic decay
* Cosmic radiation
* Hardware faults

---

### **Forensic Impact**

* Data corruption
* Hash mismatches
* Evidence degradation over time

---

### **Prevention**

* Regular integrity checks
* Redundancy
* Backups
* Error-correcting codes (ECC)

📌 **MCQ Trap**

* Bit rot is **unintentional**, not tampering

---

## **Important Facts / Points for MCQs**

* Encoding is reversible without key
* Encryption requires key
* Hashing is one-way
* MD5 is broken
* Hex editor works at byte level
* Bit rot causes silent corruption

---

## **MCQ Pointers / Exam Traps**

* Encoding vs Encryption vs Hashing
* MD5 vs SHA-256
* Hash collision vs bit rot
* Hex editor vs file viewer
* File extension vs file header
* Integrity vs confidentiality

---

## **Corrections / Improvements / Suggested Substitutions**

1. **MD5 Usage**

   * Replace MD5 with **SHA-256** for forensic integrity
2. **Terminology**

   * Use *“hash verification”* instead of *hash comparison*
3. **Clarification**

   * Hashing DLs = hashing **digital evidence**, not downloads
4. **Exam Tip**

   * Hexadecimal ≠ encryption ≠ encoding
