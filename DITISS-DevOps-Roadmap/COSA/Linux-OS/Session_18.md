# 📘 Session 18: OpenFlow & OpenDaylight Architecture 🌐
---

## 🧠 **1. Introduction to OpenFlow** 🔀

### 📌 **Concept Overview**

* **OpenFlow** is a **southbound protocol** used in **SDN** to enable communication between the **SDN Controller (control plane)** and **network devices (data plane)**.
* It allows the controller to **program flow rules** into switches.

---

### 📖 **Key Definitions**

* **OpenFlow**: An open standard protocol for SDN control
* **Flow Table**: Table in switch storing packet-handling rules
* **Flow Entry**: Match fields + actions + counters
* **Controller**: Central entity managing flows

---

### ⭐ **Why OpenFlow?**

* Removes vendor lock-in
* Enables centralized network control
* Makes networks programmable

---

### 🧠 **Important Facts for MCQs**

* OpenFlow works at **control–data plane interface**
* It does **not replace routing protocols**
* It enables **flow-based forwarding**

---

## 🕰️ **2. History and Evolution of OpenFlow** 📈

### 📌 **Evolution Timeline**

| Year      | Event                                    |
| --------- | ---------------------------------------- |
| **2008**  | OpenFlow introduced by Stanford          |
| **2009**  | Version 1.0 released                     |
| **2011**  | Open Networking Foundation (ONF) formed  |
| **Later** | Multiple versions with enhanced features |

---

### 📌 **Motivation Behind OpenFlow**

* Research experimentation on production networks
* Need for flexible, programmable networks
* Separation of control logic from hardware

---

### 🧠 **Important Facts for MCQs**

* OpenFlow is governed by **ONF**
* It was **first implemented in campus networks**
* Designed to work with **commodity switches**

---

### ⚠️ **MCQ Traps**

* ❌ OpenFlow = SDN → False
* ✔ OpenFlow = **protocol used by SDN**

---

## 🔄 **3. Control Plane and Data Plane Separation** 🧩

### 📌 **Concept Overview**

* Traditional networks combine control & forwarding in devices
* SDN (via OpenFlow) **decouples** them

---

### 🧱 **Plane Responsibilities**

| Plane             | Responsibility                      |
| ----------------- | ----------------------------------- |
| **Control Plane** | Decision making (routing, policies) |
| **Data Plane**    | Packet forwarding                   |

---

### 🔗 **Role of OpenFlow**

* Controller installs **flow rules**
* Switch forwards packets based on rules
* If no rule → packet sent to controller

---

### 🧠 **Important Facts for MCQs**

* Separation enables **centralized intelligence**
* Switches become **simple forwarding devices**
* Improves flexibility and automation

---

### ⚠️ **MCQ Traps**

* ❌ Controller forwards packets → False
* ✔ Controller **only programs** switches

---

## 🏗️ **4. OpenDaylight Architecture Overview** 🧠

### 📌 **What is OpenDaylight (ODL)?**

* **OpenDaylight** is an **open-source SDN controller platform**
* Part of the **Linux Foundation**
* Supports multiple southbound protocols (including OpenFlow)

---

### 🧱 **OpenDaylight Architecture Layers**

| Layer                   | Description                      |
| ----------------------- | -------------------------------- |
| **Application Layer**   | Network apps (Firewall, QoS, LB) |
| **Controller Platform** | Core SDN services                |
| **Southbound Plugins**  | OpenFlow, NETCONF, BGP           |
| **Network Devices**     | Switches / Routers               |

---

### 🔌 **Key Components of OpenDaylight**

* **MD-SAL** (Model Driven Service Abstraction Layer)
* **YANG models**
* **Northbound REST APIs**
* **Plugin-based architecture**

---

### 🧠 **Important Facts for MCQs**

* OpenDaylight supports **multi-protocol SDN**
* MD-SAL enables **data & service abstraction**
* Uses **YANG** for data modeling

---

### ⚠️ **MCQ Traps**

* ❌ OpenDaylight = OpenFlow → False
* ✔ OpenDaylight **supports** OpenFlow
* ❌ ODL is hardware → False (software controller)

---

## 📌 **5. Important Facts / Points for MCQs** 📝

* OpenFlow is a **southbound SDN protocol**
* ONF manages OpenFlow standard
* Control plane separated from data plane
* OpenDaylight is **open-source & modular**
* Flow tables define packet treatment

---

## ⚠️ **6. MCQ Pointers / Exam Traps** 🎯

* SDN ≠ OpenFlow
* OpenFlow ≠ routing protocol
* Controller ≠ packet forwarder
* ODL ≠ single-protocol controller
* Flow rule ≠ routing table entry

---
