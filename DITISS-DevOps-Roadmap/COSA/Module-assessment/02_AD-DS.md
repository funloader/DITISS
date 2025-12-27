## AD DS Multiple-Choice Questions

> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

### 1. Which action is necessary to apply a new schema extension for a custom application in AD DS?

- [ ] Install the application on the primary domain controller first  
- [ ] Modify the forest functional level to support the new schema  
- [ ] Use the Schema Admins group to apply schema changes  

<details>
<summary><strong>Answer</strong></summary>

✅ **Use the Schema Admins group to apply schema changes**  
Only members of the Schema Admins group are authorized to make changes to the AD DS schema.

</details>

---

### 2. You are comparing two schema extension methods for adding new attributes to AD DS. What is the key advantage of using a separate test environment before deployment?

- [ ] Reduces the time needed for deployment across all domains  
- [ ] Ensures that changes do not negatively impact existing AD DS operations  
- [ ] Automatically updates all domain controllers with minimal effort  

<details>
<summary><strong>Answer</strong></summary>

✅ **Ensures that changes do not negatively impact existing AD DS operations**  
Testing schema changes first helps prevent irreversible issues in production.

</details>

---

### 3. Your company is expanding to several new sites globally and needs to ensure high availability of authentication services across all locations. What is the recommended minimum number of domain controllers per geographical region?

- [ ] One domain controller  
- [ ] Two domain controllers  
- [ ] Three domain controllers  

<details>
<summary><strong>Answer</strong></summary>

✅ **Two domain controllers**  
Having at least two domain controllers provides redundancy and ensures authentication availability if one fails.

</details>

---

### 4. You need to extend the AD DS schema to support a new application. What is a critical prerequisite before making these changes?

- [ ] Upgrade all domain controllers to the latest Windows Server version  
- [ ] Convert all read-only domain controllers to writable ones  
- [ ] Ensure that all forest-wide replication is functioning correctly  

<details>
<summary><strong>Answer</strong></summary>

✅ **Ensure that all forest-wide replication is functioning correctly**  
Schema changes are replicated forest-wide, so healthy replication is critical before making changes.

</details>

---

### 5. Which AD DS operations master role is responsible for handling changes to the AD DS schema?

- [ ] RID Master  
- [ ] Domain Naming Master  
- [ ] Schema Master  

<details>
<summary><strong>Answer</strong></summary>

✅ **Schema Master**  
The Schema Master controls all updates and modifications to the AD DS schema.

</details>

---

### 6. What is the primary function of the AD DS global catalog in a multiple-domain forest?

- [ ] It manages DNS services for all domains in the forest  
- [ ] It speeds up searches for objects across different domains in the forest  
- [ ] It contains a complete copy of the AD DS database for all domains  

<details>
<summary><strong>Answer</strong></summary>

✅ **It speeds up searches for objects across different domains in the forest**  
The global catalog stores a partial replica of objects from all domains, enabling fast forest-wide searches.

</details>

---

### 7. Your organization is deploying a new application that requires custom attributes for user accounts in AD DS. Which step is essential to ensure that these new attributes are available across all domain controllers?

- [ ] Install the application on all domain controllers  
- [ ] Modify the AD DS schema to include the new attributes  
- [ ] Create a new domain in the forest for the application  

<details>
<summary><strong>Answer</strong></summary>

✅ **Modify the AD DS schema to include the new attributes**  
Custom attributes must be added to the schema so they can replicate to all domain controllers.

</details>

---

### 8. What is a primary advantage of deploying a Read-Only Domain Controller (RODC) in a branch office?

- [ ] It can host the global catalog role  
- [ ] Enhanced security with a read-only copy of the AD DS database  
- [ ] It reduces the need for regular backups  

<details>
<summary><strong>Answer</strong></summary>

✅ **Enhanced security with a read-only copy of the AD DS database**  
RODCs help protect against credential theft and unauthorized changes in less secure locations.

</details>

---

### 9. What is a consideration when deciding whether to configure all domain controllers as global catalog servers in a multiple-domain forest?

- [ ] Reduction in authentication speed  
- [ ] Potential increase in replication traffic  
- [ ] Requirement for additional hardware resources  

<details>
<summary><strong>Answer</strong></summary>

✅ **Potential increase in replication traffic**  
Global catalog servers replicate partial data from all domains, which can increase replication traffic.

</details>

---

### 10. Your company has developed an in-house application that requires additional attributes for AD DS objects. What is the initial step to integrate these attributes?

- [ ] Upgrade the domain functional level to the latest version  
- [ ] Extend the AD DS schema to include the new attributes  
- [ ] Reconfigure the global catalog to include the new attributes  

<details>
<summary><strong>Answer</strong></summary>

✅ **Extend the AD DS schema to include the new attributes**  
New attributes must be defined in the schema before they can be used.

</details>

---

### 11. Which role must an administrator hold to extend the AD DS schema for a new application?

- [ ] Domain Admins  
- [ ] Schema Admins  
- [ ] Enterprise Admins  

<details>
<summary><strong>Answer</strong></summary>

✅ **Schema Admins**  
Only Schema Admins are permitted to make schema modifications.

</details>

---

### 12. Which AD DS operations master role is responsible for handling changes to the AD DS schema?

- [ ] Domain Naming Master  
- [ ] RID Master  
- [ ] Schema Master  

<details>
<summary><strong>Answer</strong></summary>

✅ **Schema Master**  
All schema updates are processed by the Schema Master FSMO role.

</details>

---

### 13. Which of the following steps should you perform first when installing a new domain controller in an existing AD DS environment?

- [ ] Install the AD DS binaries using Windows Admin Center or Server Manager  
- [ ] Set the forest functional level  
- [ ] Configure the AD DS role using the Active Directory Domain Services Configuration Wizard  

<details>
<summary><strong>Answer</strong></summary>

✅ **Install the AD DS binaries using Windows Admin Center or Server Manager**  
The AD DS role must be installed before configuration and promotion.

</details>

---

### 14. In the event of a domain controller failure, which type of restore allows you to roll back to a known good date and then update from replication partners?

- [ ] System state restore  
- [ ] Authoritative restore  
- [ ] Nonauthoritative restore  

<details>
<summary><strong>Answer</strong></summary>

✅ **Nonauthoritative restore**  
This restore type brings the DC back online and updates data via replication.

</details>

---

### 15. Which method is recommended for implementing custom schema extensions for a new in-house application in AD DS?

- [ ] Apply changes directly to the production environment  
- [ ] Use a test environment to validate changes before applying them to production  
- [ ] Use a third-party tool to automate schema changes  

<details>
<summary><strong>Answer</strong></summary>

✅ **Use a test environment to validate changes before applying them to production**  
Schema changes are permanent and should always be tested first.

</details>

---

### 16. Which AD DS operations master role is responsible for processing changes to the directory schema?

- [ ] PDC Emulator  
- [ ] Domain Naming Master  
- [ ] Schema Master  

<details>
<summary><strong>Answer</strong></summary>

✅ **Schema Master**  
The Schema Master controls all directory schema modifications.

</details>

---
