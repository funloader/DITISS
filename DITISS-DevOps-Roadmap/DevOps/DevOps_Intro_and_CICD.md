# ⚙️ DevOps Introduction and CI/CD Pipelines — Sessions 15 & 16

**Duration:** 4 Theory Hours + Lab Assignment
**Module:** DevOps (CDAC PG-DITISS)
**Objective:** To introduce the core concepts, principles, and phases of DevOps, and gain hands-on experience with container technology like Docker for implementing CI/CD pipelines.

---

## 📘 **Theory Checklist**

### 🚀 Introduction to DevOps
- [x] **Introduction to DevOps** (definition, cultural shift, and business drivers).
- [x] Understanding the **DevOps ecosystem** (tools, practices, and people).
- [x] Explore the **DevOps phases** (Plan, Code, Build, Test, Release, Deploy, Operate, Monitor).

---

### 🧩 DevOps Principles and Models
- [x] Study the **CAMS model** (Culture, Automation, Lean, Measurement, Sharing).
- [x] Understanding **Kaizen** (continuous improvement) in a DevOps context.
- [x] Concepts of **Immutable deployment** (replacing, not changing, running infrastructure).

---

### 🐳 Core Technologies
- [x] Introduction to **CI/CD Pipelines** and their automation benefits.
- [x] Understanding **IAM** (Identity and Access Management) in the context of pipeline security.
- [x] Overview of **LXC** (Linux Containers) and its relation to modern containerization.
- [x] Deep dive into **Docker** (container platform).
- [x] Introduction to **KVM** (Kernel-based Virtual Machine) as a hypervisor technology.

---

## 🧪 **Lab Assignments**

### 1. Docker Container Creation and Management
- [x] **Create an httpd container** running on port **8000**. Name the container as `web5`. Do not map any directory.
- [x] Create an **"index.html"** file and **copy this file inside the container**.
- [x] Check if the website displays your webpage (via the exposed port).
- [x] **Modify the "index.html" file** and copy it inside the container again.
- [x] Check if the website is updated or not (demonstrating container immutability vs. volume mapping).

---

### 2. Docker Image Creation via Dockerfile
- [x] Create a **C program (exe)** and test the program on the base machine.
- [x] Create an **image using a Dockerfile** to execute this exe program. Give the image name as `"Name: v1"`.
- [x] Try the above steps with a program that **requires user input**.

---

## 🧰 **Tools & Platforms**
- ⚙️ **Docker**
- 🖥️ **Linux OS** (for LXC/KVM concepts)
- 💻 **C Programming Language** (for simple executable deployment)

---

## 🎯 **Learning Outcomes**
By completing this session, you will:
- ✅ Articulate the cultural, automation, and measurement components of DevOps (CAMS model).
- ✅ Understand the function of a CI/CD pipeline and its components.
- ✅ Be able to create, run, and interact with basic Docker containers (httpd).
- ✅ Be able to write a simple Dockerfile to package and execute a custom application (C program).

---
