# Session 9 – Aadhaar, e-Sign & Time Stamping Services
---

## 1. Introduction to Aadhaar

### 1.1 What is Aadhaar?

**Aadhaar** is a **12-digit unique identification number** issued to Indian residents by **UIDAI (Unique Identification Authority of India)**.

**MCQ Line:**

> Aadhaar is a **digital identity platform**, not a citizenship proof

---

### 1.2 Core Features of Aadhaar

* Unique identification
* Based on **biometrics + demographics**
* Centralized database
* Paperless & online verification

---

### 1.3 Aadhaar Data Components

| Type        | Examples                 |
| ----------- | ------------------------ |
| Demographic | Name, DOB, Address       |
| Biometric   | Fingerprint, Iris, Photo |

---

### 1.4 Uses of Aadhaar (Exam-Oriented)

* Identity verification
* Authentication services
* Government subsidy delivery
* Digital services access

---

## 2. Aadhaar Authentication

### 2.1 Definition

Aadhaar authentication is the **process of verifying identity** using Aadhaar number and associated data.

---

### 2.2 Types of Aadhaar Authentication

| Type         | Description        |
| ------------ | ------------------ |
| OTP          | One-Time Password  |
| Biometric    | Fingerprint / Iris |
| Demographic  | Name / DOB match   |
| Multi-factor | Combination        |

**MCQ Line:**

> Aadhaar supports **multi-factor authentication**

---

## 3. e-Sign (Electronic Signature)

### 3.1 Definition

**e-Sign** is an **online electronic signature service** in India that allows users to **digitally sign documents using Aadhaar authentication**.

**MCQ Line:**

> e-Sign is a **paperless digital signature service**

---

### 3.2 Legal Validity

* Recognized under **IT Act, 2000**
* Equivalent to physical signature

---

### 3.3 How e-Sign Works (Exam Steps)

1. User initiates document signing
2. Aadhaar-based authentication (OTP / Biometric)
3. e-Sign service provider generates key pair
4. Document digitally signed
5. Signed document returned

---

### 3.4 Key Characteristics of e-Sign

| Feature        | e-Sign         |
| -------------- | -------------- |
| Key storage    | Temporary      |
| Certificate    | Short-lived    |
| Authentication | Aadhaar-based  |
| Hardware token | ❌ Not required |

---

### 3.5 Advantages of e-Sign

* Paperless
* Fast & remote
* Cost-effective
* Legally valid

---

## 4. Aadhaar vs Digital Certificate (MCQ Comparison)

| Feature   | Aadhaar        | Digital Certificate    |
| --------- | -------------- | ---------------------- |
| Purpose   | Identity       | Trust                  |
| Issued by | UIDAI          | CA                     |
| Validity  | Lifetime       | Limited                |
| Usage     | Authentication | Encryption / Signature |

---

## 5. Time Stamping Services (TSS)

### 5.1 Definition

**Time Stamping Services** provide **trusted proof of the date and time** at which a digital document or transaction existed.

**MCQ Line:**

> Time stamping ensures **time integrity**

---

### 5.2 Purpose of Time Stamping

* Proves document existence at specific time
* Prevents back-dating
* Legal & compliance evidence
* Supports non-repudiation

---

## 6. Trusted Time Stamping (TTS)

### 6.1 Definition

**Trusted Time Stamping (TTS)** uses cryptographic techniques to provide **tamper-proof time information**.

---

### 6.2 Working of TTS (Exam Steps)

1. Hash of document generated
2. Sent to Time Stamping Authority (TSA)
3. TSA appends trusted time
4. TSA signs hash + time
5. Time stamp token returned

---

### 6.3 Components

* Time Stamping Authority (TSA)
* Secure clock source
* Digital signature
* Hash function

---

## 7. Network Time Protocol (NTP)

### 7.1 Overview

**NTP** synchronizes clocks over a network but **does not provide trust or non-repudiation**.

**MCQ Line:**

> NTP ≠ Trusted time source

---

## 8. Coordinated Universal Time (UTC)

### 8.1 Definition

**UTC** is the global time standard based on **atomic clocks**.

---

### 8.2 Importance

* Reference for digital time stamps
* Highly accurate
* Globally accepted

---

## 9. Classes of Time Stamping Certificates

| Class   | Usage                  |
| ------- | ---------------------- |
| Class 1 | Low-risk               |
| Class 2 | Financial transactions |
| Class 3 | E-commerce             |
| Class 4 | Government / Military  |

---

## 10. Applications (Exam-Relevant)

### Aadhaar & e-Sign

* Online contracts
* Banking KYC
* Government portals
* Digital document signing

### Time Stamping

* Legal documents
* Financial transactions
* Software release records
* Digital forensics

---

## 11. Important MCQ Facts

* Aadhaar issued by **UIDAI**
* e-Sign uses **Aadhaar authentication**
* e-Sign keys are **temporary**
* TSA provides trusted time
* UTC is most accurate time standard

---

## 12. Common Exam Traps

* ❌ Aadhaar proves citizenship
* ❌ NTP provides trusted time
* ❌ e-Sign requires USB token
* ✔ e-Sign is Aadhaar-based
* ✔ Time stamping prevents repudiation

---

## 13. Lab Mapping (Session 9)

| Lab Task                | Tool              |
| ----------------------- | ----------------- |
| e-Sign demo             | Government portal |
| Time stamp verification | OpenSSL           |
| Hash generation         | SHA utilities     |

---

## 14. Corrections / Best Practices

* Use **TSA-signed timestamps**
* Combine **digital signature + timestamp**
* Avoid relying solely on system time
* Ensure compliance with IT Act

---
