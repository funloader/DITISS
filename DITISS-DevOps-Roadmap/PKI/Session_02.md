# Session 02 – Basic Encryption Concepts, File Encryption & Encrypted Folders**
---

## 1. Basic Encryption Concepts (Foundation – High MCQ Weight)

### 1.1 What is Encryption?

* **Encryption** is the process of converting **plaintext → ciphertext** using an **encryption algorithm and key**.
* Purpose: **Confidentiality**

**MCQ Line:**

> Encryption ensures **confidentiality**, not integrity or authentication by itself.

---

### 1.2 Core Encryption Components

| Component  | Description               | MCQ Note          |
| ---------- | ------------------------- | ----------------- |
| Plaintext  | Original readable data    | Input             |
| Ciphertext | Encrypted unreadable data | Output            |
| Algorithm  | Mathematical process      | Public            |
| Key        | Secret value              | Must be protected |
| Encryption | Plaintext → Ciphertext    | Sender side       |
| Decryption | Ciphertext → Plaintext    | Receiver side     |

---

### 1.3 Types of Encryption (Conceptual)

| Type       | Key Usage      | Example | MCQ Tip      |
| ---------- | -------------- | ------- | ------------ |
| Symmetric  | Same key       | AES     | Fast         |
| Asymmetric | Public/Private | RSA     | Key exchange |
| Hybrid     | Both           | TLS     | Real-world   |

---

### 1.4 Encryption States (Very Important)

| State           | Description     | Example      |
| --------------- | --------------- | ------------ |
| Data at Rest    | Stored data     | Files, disks |
| Data in Transit | Moving data     | HTTPS        |
| Data in Use     | Being processed | RAM          |

**MCQ Trap:**

> File & folder encryption mainly protect **Data at Rest**.

---

### 1.5 Key Length & Security

* Longer key ⇒ Higher resistance to **brute-force attack**
* Examples:

  * AES-128 → Secure
  * AES-256 → More secure
* Security depends on:

  * Algorithm strength
  * Key length
  * Key management

---

## 2. File Encryption (Major Syllabus Area)

### 2.1 What is File Encryption?

* Encrypts **individual files**
* Only encrypted files are protected, not entire disk

**Use Case:**

* Protect sensitive documents
* Secure file transfer
* Cloud storage security

---

### 2.2 How File Encryption Works

1. User selects file
2. Encryption algorithm applied
3. Secret key/password used
4. Encrypted file created
5. Only authorized user can decrypt

---

### 2.3 Common File Encryption Methods

| Method            | Description              | MCQ Note              |
| ----------------- | ------------------------ | --------------------- |
| Password-based    | Uses user password       | Weak if password weak |
| Key-based         | Uses cryptographic key   | Stronger              |
| Certificate-based | Uses digital certificate | Enterprise use        |

---

### 2.4 File Encryption Tools / Technologies

| Tool                         | Platform       | Notes      |
| ---------------------------- | -------------- | ---------- |
| EFS (Encrypting File System) | Windows (NTFS) | File-level |
| GPG                          | Cross-platform | OpenPGP    |
| VeraCrypt                    | Cross-platform | Containers |
| OpenSSL                      | Cross-platform | CLI-based  |

---

### 2.5 Encrypting File System (EFS – Windows)

* File-level encryption in **NTFS**
* Uses **AES**
* Encryption tied to **user account**

**Limitations (Exam Important):**

* If user account deleted → file inaccessible
* Does NOT protect against:

  * Malware running as same user
  * System admin access

---

### 2.6 Advantages of File Encryption

* Fine-grained control
* Easy to implement
* Less overhead than disk encryption

### 2.7 Disadvantages

* Manual file selection
* Metadata leakage (file name, size)
* Key loss = permanent data loss

---

## 3. Encrypted Folders (Graphical / Using Cipher)

### 3.1 What is Folder Encryption?

* Encrypts **entire directory**
* All files inside folder are automatically encrypted

**MCQ Line:**

> Folder encryption provides **automatic protection** for new files.

---

### 3.2 Folder Encryption vs File Encryption

| Aspect     | File Encryption | Folder Encryption |
| ---------- | --------------- | ----------------- |
| Scope      | Single file     | Entire directory  |
| Automation | Manual          | Automatic         |
| Ease       | Moderate        | Easier            |
| Security   | Medium          | Better            |

---

## 4. Graphical Folder Encryption (GUI-Based)

### 4.1 Characteristics

* Uses **GUI tools**
* User-friendly
* Less technical knowledge required

### 4.2 Examples

| Tool                         | Platform       |
| ---------------------------- | -------------- |
| Windows EFS (Folder level)   | Windows        |
| BitLocker (Folder via drive) | Windows        |
| VeraCrypt Containers         | Cross-platform |

**MCQ Trap:**

> BitLocker is **disk encryption**, not pure folder encryption.

---

### 4.3 Pros & Cons (Graphical)

**Pros**

* Easy to use
* Low learning curve

**Cons**

* Limited customization
* Less transparency
* Not ideal for automation

---

## 5. Folder Encryption Using `cipher` (Command Line)

### 5.1 What is `cipher`?

* Windows command-line utility
* Used with **NTFS**
* Encrypts files/folders using **EFS**

---

### 5.2 Basic `cipher` Commands (MCQ Friendly)

| Command                | Purpose                |
| ---------------------- | ---------------------- |
| `cipher /e foldername` | Encrypt folder         |
| `cipher /d foldername` | Decrypt folder         |
| `cipher /c filename`   | Show encryption status |
| `cipher /w`            | Wipe free disk space   |

**MCQ Note:**

> `cipher` works only on **NTFS**, not FAT32.

---

### 5.3 Features of Cipher-Based Encryption

* Scriptable
* Suitable for automation
* Requires command-line knowledge

---

### 5.4 Graphical vs Cipher-Based Encryption

| Parameter   | Graphical | Cipher |
| ----------- | --------- | ------ |
| Interface   | GUI       | CLI    |
| Automation  | Low       | High   |
| Ease of use | High      | Medium |
| Exam Focus  | Moderate  | High   |

---

## 6. Security Threats Related to File/Folder Encryption

| Threat         | Explanation                |
| -------------- | -------------------------- |
| Key loss       | Permanent data loss        |
| Weak passwords | Brute-force attack         |
| Malware        | Access via same user       |
| Backup issues  | Encrypted backups unusable |

---

## 7. Best Practices (Exam-Oriented)

* Use **strong passwords**
* Backup **encryption keys/certificates**
* Combine with **access control**
* Prefer **AES-based tools**
* Encrypt sensitive data **at rest**

---

## 8. MCQ One-Liners / Rapid Revision

* File encryption protects **data at rest**
* EFS uses **AES**
* Cipher works on **NTFS**
* Folder encryption auto-encrypts new files
* BitLocker ≠ File encryption
* Loss of key = **no recovery**
* Encryption ≠ authentication

---

## 9. Common Exam Traps & Clarifications

* ❌ Encryption alone does not ensure integrity
* ❌ EFS is not disk encryption
* ❌ Cipher does not work on FAT/FAT32
* ✔ Folder encryption reduces human error
* ✔ Command-line tools preferred in enterprise automation

---
