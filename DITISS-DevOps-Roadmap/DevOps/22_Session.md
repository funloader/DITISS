## ⚙️ **Session 22: Ansible & Configuration Management**

---

### 🧠 **1. Concept Overview**

* **Ansible** is a popular **configuration management and automation tool** used in DevOps.
* Enables **agentless automation**, making it lightweight and easy to use.
* Widely used for **server provisioning, configuration, and application deployment**.

---

### 📖 **2. Key Definitions**

* **Configuration Management:** Process of **maintaining system state consistency**.
* **Ansible:** Open-source automation tool using **SSH** for communication.
* **Playbook:** YAML file defining tasks to be executed on managed nodes.
* **Inventory:** List of managed hosts.
* **Role:** Structured, reusable collection of playbooks and files.

---

### 🧩 **3. Main Content (Organized from Notes)**

---

#### 🔰 **Introduction to Ansible**

* Written in **Python**
* Uses:

  * SSH (Linux)
  * WinRM (Windows)
* No agent required on target systems

**Key Features:**

* Agentless
* Idempotent
* Simple YAML syntax

📌 *Ansible is declarative.*

---

#### 🛠️ **Setting Up Ansible Environment**

* Requires:

  * Control Node (Ansible installed)
  * Managed Nodes (servers to configure)

**Basic Setup Steps:**

* Install Ansible on control node
* Configure SSH access
* Define inventory file

---

#### 🧾 **Ansible Playbooks & YAML Basics**

* Playbooks define:

  * Hosts
  * Tasks
  * Modules

**YAML Characteristics:**

* Indentation-based
* Human-readable
* Key-value format

📌 *YAML is space-sensitive.*

---

#### 🗂️ **Managing Ansible Inventory**

* Inventory defines:

  * Target hosts
* Can be:

  * Static
  * Dynamic

**Inventory Types:**

* Host-based
* Group-based

📌 *Inventory is mandatory.*

---

#### ♻️ **Ansible Roles & Reusability**

* Roles help in:

  * Organizing playbooks
  * Reusing configurations
* Standard role structure:

  * tasks/
  * handlers/
  * files/
  * templates/
  * vars/

📌 *Roles support scalability.*

---

### 🎯 **4. Important Facts / Points for MCQs**

* Ansible is **agentless**
* Uses **YAML**
* Control node ≠ Managed node
* Inventory lists hosts
* Playbook ≠ Role
* Roles increase reusability
* Idempotent tasks avoid repeated changes

---

### 🧪 **5. Examples**

* Playbook → Install Apache
* Inventory → Web servers group
* Role → Common server setup
* YAML → Task definitions

---

### ⚠️ **6. MCQ Pointers / Exam Traps**

* Ansible ≠ Puppet/Chef (agent-based)
* YAML indentation errors
* Inventory ≠ Playbook
* Role ≠ Module
* Control node ≠ Managed node
* Agentless ≠ passwordless (SSH keys used)

---

✅ **Exam Priority Tip:**

> *PG-DITISS MCQs often test Ansible architecture, YAML syntax basics, inventory vs playbook vs roles—focus on definitions and differences.*
