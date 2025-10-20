# ☁️ Infrastructure as Code: Terraform — Session 23

**Duration:** 2 Theory Hours + 4 Lab Hours
**Module:** DevOps (CDAC PG-DITISS)
**Objective:** To introduce **Infrastructure as Code (IaC)** concepts, focusing on **Terraform** for provisioning and managing cloud resources like AWS.

---

## 📘 **Theory Checklist**

### 💻 Introduction to Infrastructure as Code (IaC) and Terraform
- [x] Introduction to **Infrastructure as Code (IaC)**.
- [x] Understand how Terraform fits into the IaC landscape.
- [x] Setting Up the Terraform Environment.

---

### ⚙️ Terraform Configuration Management
- [x] Principles of **Writing and Organizing Terraform Configuration Files**.
- [x] Utilizing **variables** and **outputs** for dynamic and reusable configurations.
- [x] Understanding **Terraform State Management**.

---

### 🗄️ State Management and Reusability
- [x] Introduction to **Terraform Modules** and **Reusability**.
- [x] Managing the Terraform state using a remote backend (e.g., AWS S3).

---

## 🧪 **Lab Assignments**

### 1. Setting Up the Terraform Environment (Initial Provisioning)
- [x] **Install Terraform** on a local machine.
- [x] **Configure AWS credentials** for Terraform to interact with AWS services.
- [x] Create and apply a basic Terraform configuration to **provision an EC2 instance in AWS**.

---

### 2. Writing and Organizing Configuration Files
- [x] Write a configuration file to provision a **VPC, subnet, and an EC2 instance** within the subnet.
- [x] Use **variables and outputs** to make the configuration more dynamic and reusable.
- [x] Apply the configuration and verify the resources are created in AWS.

---

### 3. Terraform State Management and Modules
- [x] Create a **Terraform module** for provisioning an EC2 instance with a security group.
- [x] Use the module in a Terraform configuration to provision **multiple EC2 instances** in different subnets.
- [x] Manage the Terraform state using a **remote backend** (e.g., AWS S3) to enable collaboration and state sharing.

---

## 🧰 **Tools & Platforms**
- ☁️ **Terraform**
- 🌐 **AWS** (Amazon Web Services)
- 🖥️ **Command Line Interface (CLI)**
- 📝 **HCL** (HashiCorp Configuration Language)

---

## 🎯 **Learning Outcomes**
By completing this session, you will:
- ✅ Be proficient in setting up the Terraform environment and connecting to a cloud provider (AWS).
- ✅ Be able to write, organize, and apply Terraform configurations for provisioning fundamental cloud infrastructure components (VPC, EC2).
- ✅ Understand and implement best practices for state management and code reusability using modules.

---

📚 **Reference:**
*Cloud Computing Black Book, Kogent Learning, Kailash, (Wiley), 2024*
