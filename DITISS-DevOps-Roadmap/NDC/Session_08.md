# **Session 8 – Hybrid VPN, IPsec Modes & Advanced VPN Concepts (PG-DITISS)**

---

## 1. **Concept Overview**

Session 8 builds on VPN fundamentals and focuses on:

* **Hybrid VPN architecture**
* **IPsec in detail**
* **Tunnel vs Transport mode**
* **IPv6 VPN**
* **Split Tunnel vs Full Tunnel VPN**

Core idea:

> **VPN architectures and modes decide security level, performance, and traffic flow**

---

## 2. **Key Definitions**

| Term           | Exam-Oriented Definition                         |
| -------------- | ------------------------------------------------ |
| Hybrid VPN     | Combination of Secure VPN and Trusted VPN        |
| IPsec          | Suite of protocols for securing IP communication |
| Tunnel Mode    | Entire IP packet is encrypted                    |
| Transport Mode | Only payload is encrypted                        |
| IPv6 VPN       | VPN supporting IPv6 addressing                   |
| Split Tunnel   | VPN routes selective traffic                     |
| Full Tunnel    | VPN routes all traffic                           |

---

## 3. **Main Content (Organized as per Syllabus)**

---

## **A. Hybrid VPN**

### **Hybrid VPN – Definition**

A **Hybrid VPN**:

* Combines features of:

  * **Secure VPN (encryption-based)**
  * **Trusted VPN (ISP-based)**
* Uses **trusted backbone + encrypted tunnels**

📌 *Balances performance and security*

---

### **Characteristics of Hybrid VPN**

* Encryption over trusted networks
* Reduced cost compared to pure secure VPN
* Used in large enterprise networks
* Common in MPLS + IPsec deployments

---

### **Hybrid VPN Architecture**

* ISP provides MPLS backbone
* IPsec tunnels used for sensitive data
* Trust + cryptography combined

📌 *Hybrid VPN ≠ Pure IPsec VPN*

---

## **B. IPsec**

---

### **IPsec – Definition**

**IPsec (Internet Protocol Security)** is:

* A **network-layer security protocol suite**
* Used to secure IP communications

📌 *IPsec operates at OSI Layer 3*

---

### **IPsec Core Components (High MCQ Value)**

| Component                            | Function                     |
| ------------------------------------ | ---------------------------- |
| AH (Authentication Header)           | Integrity & authentication   |
| ESP (Encapsulating Security Payload) | Encryption, integrity        |
| IKE                                  | Key exchange & SA management |
| SA (Security Association)            | Security agreement           |

📌 *ESP is more commonly used than AH*

---

## **C. Tunnel Mode vs Transport Mode**

---

### **1. Tunnel Mode**

**Definition:**

* Entire original IP packet is encrypted
* New IP header added

**Used in:**

* Site-to-site VPN
* Gateway-to-gateway VPN

---

### **2. Transport Mode**

**Definition:**

* Only payload encrypted
* Original IP header remains visible

**Used in:**

* Host-to-host VPN

---

### **Tunnel vs Transport Mode (MCQ Table)**

| Feature          | Tunnel Mode   | Transport Mode |
| ---------------- | ------------- | -------------- |
| Encryption scope | Entire packet | Payload only   |
| New IP header    | Yes           | No             |
| Common usage     | Site-to-site  | Host-to-host   |
| Security level   | Higher        | Lower          |

📌 *Tunnel mode is default for VPN gateways*

---

## **D. IPv6 VPN**

---

### **IPv6 VPN – Concept**

An **IPv6 VPN**:

* Supports IPv6 addressing
* Secures IPv6 traffic using VPN protocols

---

### **Why IPv6 VPN?**

* IPv4 exhaustion
* Larger address space
* Built-in IPsec support in IPv6

📌 *IPsec is mandatory in IPv6 specification (conceptual MCQ point)*

---

### **IPv6 VPN Characteristics**

* Uses IPsec / SSL
* Supports dual-stack environments
* Ensures secure IPv6 communication

---

## **E. Split Tunnel vs Full Tunnel VPN**

---

### **1. Split Tunnel VPN**

**Definition:**

* Only **corporate traffic** goes through VPN
* Internet traffic goes directly

**Advantages:**

* Reduced bandwidth usage
* Better performance

**Disadvantages:**

* Lower security
* Risk of data leakage

---

### **2. Full Tunnel VPN**

**Definition:**

* **All traffic** goes through VPN
* Includes Internet access

**Advantages:**

* High security
* Complete traffic monitoring

**Disadvantages:**

* Increased latency
* Higher bandwidth usage

---

### **Split vs Full Tunnel (MCQ Table)**

| Feature         | Split Tunnel | Full Tunnel |
| --------------- | ------------ | ----------- |
| Traffic routing | Partial      | All         |
| Security        | Lower        | Higher      |
| Bandwidth usage | Less         | More        |
| Performance     | Better       | Slower      |

📌 *Full tunnel preferred in high-security environments*

---

## 4. **Important Facts / Points for MCQs**

* Hybrid VPN = Secure + Trusted
* IPsec works at Network Layer
* ESP provides encryption
* Tunnel mode encrypts entire packet
* IPv6 supports IPsec by design
* Split tunneling reduces bandwidth

---

## 5. **Examples (Exam-Friendly)**

* MPLS + IPsec → Hybrid VPN
* Branch connectivity → IPsec Tunnel mode
* End-to-end host encryption → Transport mode
* Corporate laptop VPN → Split / Full tunnel
* IPv6 corporate network → IPv6 VPN

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Hybrid VPN ≠ Trusted VPN
* AH ≠ ESP
* Tunnel mode ≠ Transport mode
* IPv6 VPN ≠ IPv4 VPN
* Split tunnel ≠ Secure by default

---

