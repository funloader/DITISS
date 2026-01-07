Below are **PG-DITISS Session 6 & 7 MCQ-oriented notes**, **strictly aligned with the given syllabus points** and **derived from standard VPN concepts referenced/implicit in NDC notes (tunneling, secure communication, confidentiality, integrity)**, carefully **structured, corrected, and optimized for exam use**.

---

# **Session 6 & 7 – VPN (Virtual Private Network) (PG-DITISS)**

---

## 1. **Concept Overview**

A **VPN (Virtual Private Network)** provides **secure communication over an untrusted network (Internet)** by using:

* Encryption
* Authentication
* Tunneling

Core idea:

> **VPN creates a secure “private” connection over a public network**

---

## 2. **Key Definitions**

| Term         | Exam-Oriented Definition                          |
| ------------ | ------------------------------------------------- |
| VPN          | Secure encrypted connection over a public network |
| Tunneling    | Encapsulation of one protocol inside another      |
| VPN Protocol | Set of rules for VPN communication                |
| Secure VPN   | VPN using cryptography for security               |
| Trusted VPN  | VPN relying on service provider’s trust           |

---

## 3. **Main Content (Organized from Notes & Syllabus)**

---

## **A. VPN – Introduction**

### **Why VPN is Needed**

* Internet is **untrusted**
* Data in transit is vulnerable to:

  * Eavesdropping
  * Tampering
  * Man-in-the-middle attacks

VPN ensures:

* Confidentiality
* Integrity
* Authentication
* Secure remote access

📌 *VPN is a logical private network, not a physical one*

---

## **B. VPN Protocols & Characteristics**

### **Common VPN Protocols (MCQ-Oriented)**

| Protocol | Key Characteristics                       |
| -------- | ----------------------------------------- |
| IPsec    | Network-layer security, strong encryption |
| SSL/TLS  | Application-layer VPN, browser-based      |
| PPTP     | Fast but weak security                    |
| L2TP     | Often combined with IPsec                 |
| OpenVPN  | SSL-based, open-source                    |

📌 *IPsec is most commonly used for site-to-site VPN*

---

### **IPsec Modes (High MCQ Value)**

| Mode           | Description                |
| -------------- | -------------------------- |
| Tunnel Mode    | Entire IP packet encrypted |
| Transport Mode | Only payload encrypted     |

📌 *Tunnel mode used in site-to-site VPN*

---

### **VPN Characteristics**

* Encryption
* Authentication
* Tunneling
* Data integrity
* Secure key exchange

---

## **C. VPN Functions**

### **Primary Functions of VPN**

1. **Confidentiality**

   * Encryption of data
2. **Authentication**

   * User/device verification
3. **Integrity**

   * Prevents data modification
4. **Secure Tunneling**

   * Safe data transmission
5. **Access Control**

   * Restricts network access

📌 *VPN supports CIA triad in data transmission*

---

## **D. Types of VPN**

### **1. Remote Access VPN**

* Used by individual users
* Connects user → corporate network
* Example: Work-from-home access

---

### **2. Site-to-Site VPN**

* Connects two networks
* Uses gateway devices
* Example: Branch office connectivity

---

### **3. Client-to-Site vs Site-to-Site (MCQ Table)**

| Feature         | Client-to-Site | Site-to-Site |
| --------------- | -------------- | ------------ |
| Users           | Individual     | Network      |
| Mode            | Tunnel         | Tunnel       |
| Common protocol | SSL / IPsec    | IPsec        |

---

## **E. Secure VPN**

### **Secure VPN – Definition**

A **Secure VPN**:

* Uses cryptographic mechanisms
* Ensures confidentiality, integrity & authentication

---

### **Security Mechanisms Used**

* Encryption algorithms (AES, 3DES)
* Hashing (SHA)
* Digital certificates
* Key exchange protocols

📌 *Secure VPN does NOT rely on ISP trust*

---

### **Examples**

* IPsec VPN
* SSL VPN
* OpenVPN

---

## **F. Trusted VPN**

### **Trusted VPN – Definition**

A **Trusted VPN**:

* Provided by a **service provider**
* Security depends on **provider trust**
* No encryption by default

---

### **Characteristics of Trusted VPN**

* Uses MPLS / leased lines
* Relies on ISP isolation
* Lower cryptographic security

📌 *Trusted VPN ≠ Encrypted VPN*

---

### **Secure VPN vs Trusted VPN**

| Feature        | Secure VPN   | Trusted VPN      |
| -------------- | ------------ | ---------------- |
| Encryption     | Yes          | No (default)     |
| Trust model    | Cryptography | Service provider |
| Security level | High         | Moderate         |
| Example        | IPsec VPN    | MPLS VPN         |

---

## 4. **Important Facts / Points for MCQs**

* VPN uses tunneling
* IPsec operates at Network Layer
* Tunnel mode encrypts entire packet
* Secure VPN uses encryption
* Trusted VPN relies on ISP
* SSL VPN works through browsers

---

## 5. **Examples (Exam-Friendly)**

* Work-from-home access → Remote access VPN
* Branch connectivity → Site-to-site VPN
* MPLS-based corporate network → Trusted VPN
* Encrypted Internet VPN → Secure VPN

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Secure VPN ≠ Trusted VPN
* Tunnel mode ≠ Transport mode
* VPN ≠ Firewall
* MPLS ≠ Encrypted VPN
* PPTP ≠ Secure protocol

---

