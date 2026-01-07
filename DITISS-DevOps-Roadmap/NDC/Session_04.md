# **Session 4 – Wireshark & Packet Analysis (PG-DITISS)**

---

## 1. **Concept Overview**

Session 4 introduces **Wireshark as a network protocol analyzer** and focuses on:

* Capturing network traffic
* Creating **filters for data collection and display**
* **Examining real-world packet captures**

Core idea:

> **Wireshark helps in visibility, troubleshooting, and security analysis of network traffic**

---

## 2. **Key Definitions**

| Term              | Exam-Oriented Definition                                        |
| ----------------- | --------------------------------------------------------------- |
| Wireshark         | A network protocol analyzer used to capture and analyze packets |
| Packet Capture    | Process of recording network traffic                            |
| Capture Filter    | Filter applied before capturing packets                         |
| Display Filter    | Filter applied after packets are captured                       |
| Protocol Analyzer | Tool that decodes protocol headers and payload                  |

---

## 3. **Main Content (Organized from Notes)**

---

## **A. Wireshark**

### **Definition**

**Wireshark** is a:

* Free and open-source
* Network protocol analyzer
* Used for **real-time packet capture and analysis**

---

### **Uses of Wireshark**

* Network troubleshooting
* Performance analysis
* Security monitoring
* Understanding protocol behavior

---

### **Key Features**

* Captures live network traffic
* Supports protocols:

  * Ethernet
  * TCP/IP
  * HTTP
  * DNS
  * UDP
* Shows:

  * Packet headers
  * Payload
  * Metadata (time, size, protocol)
* Supports encrypted traffic analysis (where keys are available)

📌 *Wireshark works mainly at OSI Layers 2–7*

---

## **B. Filters for Data Collection and Display**

Wireshark uses **two types of filters**.

---

### **1. Capture Filters**

**Purpose:**

* Applied **before packet capture**
* Reduce amount of data collected

**Syntax style:**
(BPF – Berkeley Packet Filter)

#### **Common Capture Filter Examples**

| Requirement              | Filter                   |
| ------------------------ | ------------------------ |
| Capture specific host    | `host 192.168.1.100`     |
| Capture TCP traffic      | `tcp`                    |
| Capture UDP traffic      | `udp`                    |
| Capture port 80          | `port 80`                |
| Capture source host      | `src host 192.168.1.100` |
| Capture destination host | `dst host 192.168.1.100` |

📌 *Capture filters improve performance*

---

### **2. Display Filters**

**Purpose:**

* Applied **after capture**
* Used to analyze specific packets

**Syntax style:**
Wireshark-specific expressions

---

#### **Common Display Filter Examples**

| Requirement    | Display Filter                      |
| -------------- | ----------------------------------- |
| Filter by IP   | `ip.addr == 192.168.1.100`          |
| Filter by TCP  | `tcp`                               |
| Filter by UDP  | `udp`                               |
| Filter by port | `tcp.port == 80`                    |
| Source IP      | `ip.src == 192.168.1.100`           |
| Destination IP | `ip.dst == 192.168.1.100`           |
| HTTP keyword   | `http.request.uri contains "login"` |

📌 *Display filters do NOT affect captured data*

---

## **C. Examine Real-World Packet Captures**

### **Steps to Examine Packet Captures**

1. **Open Capture File**

   * File → Open
2. **Overview Analysis**

   * Number of packets
   * Duration
   * Protocols involved
3. **Identify Issues**

   * Retransmissions
   * Duplicate packets
   * Errors
4. **Packet-Level Inspection**

   * Source & destination
   * Protocol
   * Length
   * Timestamp
5. **Apply Filters**

   * Narrow down analysis
6. **Follow Traffic Flow**

   * TCP Stream analysis
7. **Export Data**

   * CSV / JSON formats

---

### **What Can Be Detected Using Wireshark**

* Suspicious traffic
* Network congestion
* Protocol misuse
* Abnormal packet behavior
* Communication patterns

📌 *Wireshark is a visibility tool, not a preventive control*

---

## 4. **Important Facts / Points for MCQs**

* Wireshark = Protocol analyzer
* Capture filter ≠ Display filter
* Capture filter reduces traffic before capture
* Display filter works on already captured data
* TCP stream shows complete session
* Wireshark does not block traffic

---

## 5. **Examples (Exam-Friendly)**

* Filtering only HTTP packets → Display filter
* Capturing only port 80 traffic → Capture filter
* Viewing full client-server communication → TCP stream
* Finding login request → HTTP display filter

---

## 6. **MCQ Pointers / Exam Traps**

⚠️ **Common Confusions**

* Capture filter ≠ Display filter
* Wireshark ≠ IDS / Firewall
* Filtering ≠ Blocking
* TCP filter ≠ Port filter

---
