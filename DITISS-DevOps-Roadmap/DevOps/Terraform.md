# 🧭 Infrastructure as Code (IaC) — Terraform (Session 23)

**Duration:** 2 Theory Hours + 4 Lab Hours  
**Module:** DevOps (CDAC PG-DITISS)  
**Objective:**  
To introduce **Infrastructure as Code (IaC)** concepts, focusing on **Terraform** for provisioning and managing cloud infrastructure efficiently.

---

## 📘 **Theory Checklist**

### 💻 Introduction to Infrastructure as Code (IaC) and Terraform
- [x] Understand the concept and importance of **Infrastructure as Code (IaC)**.  
- [x] Explore Terraform’s role in the IaC ecosystem.  
- [x] Learn how to set up and configure the Terraform environment.  

---

### ⚙️ Terraform Configuration Management
- [x] Learn how to **write and organize Terraform configuration files**.  
- [x] Use **variables** and **outputs** to make configurations dynamic and reusable.  
- [x] Understand **Terraform State Management** and its purpose.  

---

### 🗄️ State Management and Reusability
- [x] Create and manage **Terraform Modules** for reusability.  
- [x] Manage **Terraform state** with remote backends (e.g., AWS S3) for collaboration and versioning.  

---

## 🧪 **Lab Assignments**

### 1️⃣ Setting Up the Terraform Environment
- [x] Install Terraform on a local machine.  
- [x] Configure **AWS credentials** to enable cloud interactions.  
- [x] Write a simple Terraform configuration to **provision an EC2 instance** on AWS.  

---

### 2️⃣ Writing and Organizing Configuration Files
- [x] Write configuration files to create a **VPC, subnet, and EC2 instance**.  
- [x] Use **variables and outputs** for flexible configuration.  
- [x] Apply and verify created resources in the AWS Management Console.  

---

### 3️⃣ State Management and Modules
- [x] Develop a **Terraform module** for EC2 instance creation with security groups.  
- [x] Reuse the module to provision multiple EC2 instances in different subnets.  
- [x] Manage **Terraform state** using AWS S3 as a remote backend.  

---

## 🧰 **Tools & Platforms**
| Category | Tools |
|-----------|-------|
| IaC | Terraform |
| Cloud Provider | AWS |
| CLI | AWS CLI, Terraform CLI |
| Configuration Language | HCL (HashiCorp Configuration Language) |
| Backend | AWS S3 (Remote State) |

---

## 🎯 **Learning Outcomes**
By completing this session, you will:
- ✅ Understand the principles of **Infrastructure as Code (IaC)**.  
- ✅ Set up and manage Terraform for cloud provisioning.  
- ✅ Write modular and reusable Terraform code.  
- ✅ Implement **remote state management** and collaborate effectively in teams.  

---

## ✍️ **Personal Notes**
> Use this section to record your own Terraform workflows, scripts, or troubleshooting notes.

```bash
# Example commands
terraform init
terraform plan
terraform apply
terraform destroy
