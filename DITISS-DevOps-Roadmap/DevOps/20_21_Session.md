## 🧱 **Session 20 & 21: Version Control, IaC, Containers, Orchestration & Microservices**

---

### 🧠 **1. Concept Overview**

* These sessions focus on **modern DevOps engineering practices**:

  * Version control for code management
  * **Infrastructure as Code (IaC)** for automation
  * Containerization using Docker
  * Container orchestration using Kubernetes & Docker Swarm
  * Deployment of **microservices-based applications**
* Core topics for **CI/CD and cloud-native architectures**.

---

### 📖 **2. Key Definitions**

* **Version Control System (VCS):** System to track and manage changes in code.
* **Infrastructure as Code (IaC):** Managing infrastructure using **code and automation**.
* **Containerization:** Packaging application with dependencies into containers.
* **Container Orchestration:** Automated management of containers.
* **Microservices:** Architectural style where app is built as **small independent services**.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 📂 **Version Control System**

* Tracks:

  * Code changes
  * Collaboration history
* Enables:

  * Rollback
  * Branching
  * Merging

**Types of VCS:**

* Centralized (CVCS)
* Distributed (DVCS)

📌 *Git is most widely used DVCS.*

---

#### 🏗️ **Infrastructure as Code (IaC)**

* Infrastructure is:

  * Defined using configuration files
* Eliminates manual provisioning

**Benefits:**

* Consistency
* Repeatability
* Versioning of infra
* Faster deployments

**Common Tools (Exam Focus):**

* Terraform
* CloudFormation
* Ansible

---

#### 📦 **Containerization with Docker**

* Docker packages:

  * Application
  * Libraries
  * Dependencies

**Key Components:**

* Docker Engine
* Docker Image
* Docker Container
* Dockerfile

📌 *Containers share host OS kernel.*

---

#### ☸️ **Container Orchestration**

##### 🔹 **Kubernetes**

* Open-source container orchestrator
* Manages:

  * Deployment
  * Scaling
  * Networking
  * Self-healing

**Key Features:**

* Auto-scaling
* Auto-healing
* Rolling updates

---

##### 🔹 **Docker Swarm**

* Native clustering for Docker
* Simpler than Kubernetes

**Comparison:**

| Feature        | Kubernetes | Docker Swarm |
| -------------- | ---------- | ------------ |
| Complexity     | High       | Low          |
| Scalability    | Very High  | Moderate     |
| Industry Usage | High       | Low          |

---

#### 🧬 **Microservice Deployment**

* Each service:

  * Deployed independently
  * Runs in its own container
* Communicate via:

  * APIs

**Benefits:**

* Fault isolation
* Independent scaling
* Faster releases

📌 *Containers + Orchestrators are ideal for microservices.*

---

### 🎯 **4. Important Facts / Points for MCQs**

* VCS tracks code history
* IaC = infrastructure via code
* Docker ≠ VM
* Kubernetes supports auto-healing
* Docker Swarm is simpler than Kubernetes
* Microservices ≠ Monolithic apps

---

### 🧪 **5. Examples**

* Git → Version control
* Terraform → IaC
* Docker → Container platform
* Kubernetes → Orchestration
* Microservice → Payment service in e-commerce app

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* IaC ≠ configuration management
* Container ≠ Virtual machine
* Kubernetes ≠ Docker
* Swarm ≠ Kubernetes
* Microservices ≠ SOA (often confused)
* Orchestration ≠ container runtime

---

✅ **Final Exam Tip:**

> *PG-DITISS MCQs often test definitions, comparisons (K8s vs Swarm, VM vs Container), and IaC benefits—focus on one-liners and traps.*
