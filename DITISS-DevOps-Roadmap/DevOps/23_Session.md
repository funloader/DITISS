## 🏗️ **Session 23: Infrastructure as Code (IaC) with Terraform**

---

### 🧠 **1. Concept Overview**

* **Infrastructure as Code (IaC)** automates infrastructure provisioning using **declarative code**.
* **Terraform** is a widely used **IaC tool** that provisions infrastructure across **multiple cloud providers**.
* Focus is on **setup, configuration files, state, and reusability**—highly MCQ-relevant.

---

### 📖 **2. Key Definitions**

* **Infrastructure as Code (IaC):** Managing and provisioning infrastructure using **machine-readable configuration files**.
* **Terraform:** Open-source IaC tool by **HashiCorp**.
* **Provider:** Plugin that allows Terraform to interact with APIs (AWS, Azure, GCP).
* **State File:** File that maps Terraform resources to real infrastructure.
* **Module:** Reusable Terraform configuration.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🔰 **Introduction to IaC & Terraform**

* IaC removes **manual configuration**
* Infrastructure becomes:

  * Version-controlled
  * Repeatable
  * Auditable

**Why Terraform?**

* Cloud-agnostic
* Declarative syntax
* Supports lifecycle management

📌 *Terraform uses HCL (HashiCorp Configuration Language).*

---

#### ⚙️ **Setting Up Terraform Environment**

* Components required:

  * Terraform binary
  * Cloud credentials
  * Provider configuration

**Basic Steps (Exam-Oriented):**

* Install Terraform
* Configure provider
* Initialize working directory

📌 *`terraform init` initializes providers.*

---

#### 🧾 **Terraform Configuration Files**

* Written using **.tf** extension
* Common files:

  * `main.tf`
  * `variables.tf`
  * `outputs.tf`

**Key Blocks:**

* provider
* resource
* variable
* output

📌 *Order of files does not matter.*

---

#### 🗂️ **Terraform State Management**

* Terraform maintains **state file** to track resources
* Default file:

  * `terraform.tfstate`

**Functions of State:**

* Maps config to real resources
* Enables:

  * Change detection
  * Dependency management

📌 *State file is critical and sensitive.*

---

#### ♻️ **Terraform Modules & Reusability**

* Modules allow:

  * Code reuse
  * Standardized infrastructure

**Types of Modules:**

* Root module
* Child module

**Benefits:**

* Maintainability
* Scalability
* Reduced duplication

📌 *Modules improve consistency.*

---

### 🎯 **4. Important Facts / Points for MCQs**

* Terraform is **declarative**
* Uses **HCL**, not YAML
* `terraform init` is mandatory
* State file tracks infrastructure
* Terraform is cloud-agnostic
* Modules enable reusability

---

### 🧪 **5. Examples**

* Terraform → Provision AWS EC2
* Module → VPC configuration
* State file → Track deployed resources
* Provider → AWS plugin

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* IaC ≠ configuration management
* Terraform ≠ Ansible
* HCL ≠ JSON/YAML
* State file ≠ backup file
* Module ≠ resource
* Terraform does not manage app code

---

✅ **Exam Priority Tip:**

> *PG-DITISS MCQs frequently test Terraform basics—commands (`init`), state purpose, IaC benefits, and module vs resource differences. Focus on one-liners and traps.*
