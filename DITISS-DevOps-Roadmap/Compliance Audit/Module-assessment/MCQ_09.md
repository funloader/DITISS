> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

---

### 1. What is the primary objective of PCI DSS Requirement 1?

* [ ] A. Encrypt cardholder data at rest
* [ ] B. Install and maintain network security controls
* [ ] C. Implement role-based access control
* [ ] D. Conduct vulnerability scans

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Install and maintain network security controls**
Requirement 1 focuses on firewalls, segmentation, and secure network architecture.

</details>

---

### 2. Network segmentation in PCI DSS primarily helps to:

* [ ] A. Eliminate encryption requirements
* [ ] B. Reduce scope of the Cardholder Data Environment
* [ ] C. Avoid vulnerability scanning
* [ ] D. Remove the need for firewalls

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Reduce scope of the Cardholder Data Environment**
Segmentation limits systems in scope and reduces compliance burden.

</details>

---

### 3. Which of the following environments must be covered under Requirement 1?

* [ ] A. Only on-premise networks
* [ ] B. Only cloud-based environments
* [ ] C. Only virtualized systems
* [ ] D. Cloud, virtualized, and traditional environments

<details>
<summary><strong>Answer</strong></summary>

✅ **D. Cloud, virtualized, and traditional environments**
PCI DSS explicitly includes all modern deployment models.

</details>

---

### 4. PCI DSS Requirement 2 mainly addresses which security weakness?

* [ ] A. Weak encryption algorithms
* [ ] B. Vendor-supplied default configurations
* [ ] C. Missing audit logs
* [ ] D. Lack of malware protection

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Vendor-supplied default configurations**
Default passwords and settings are a major attack vector.

</details>

---

### 5. Which devices are covered under Requirement 2?

* [ ] A. Only servers
* [ ] B. Only routers and switches
* [ ] C. All system components handling card data
* [ ] D. Only firewalls

<details>
<summary><strong>Answer</strong></summary>

✅ **C. All system components handling card data**
Includes routers, switches, servers, and databases.

</details>

---

### 6. Which encryption standard is explicitly recommended for protecting stored cardholder data?

* [ ] A. DES
* [ ] B. 3DES
* [ ] C. AES-128 or AES-256
* [ ] D. RC4

<details>
<summary><strong>Answer</strong></summary>

✅ **C. AES-128 or AES-256**
PCI DSS mandates strong encryption algorithms.

</details>

---

### 7. Which of the following is NOT an approved method to protect stored cardholder data?

* [ ] A. Tokenization
* [ ] B. Truncation
* [ ] C. Hashing
* [ ] D. Base64 encoding

<details>
<summary><strong>Answer</strong></summary>

✅ **D. Base64 encoding**
Encoding is reversible and not a security control.

</details>

---

### 8. Minimum key strength recommended for RSA key management under PCI DSS is:

* [ ] A. RSA 1024
* [ ] B. RSA 1536
* [ ] C. RSA 2048
* [ ] D. RSA 4096 only

<details>
<summary><strong>Answer</strong></summary>

✅ **C. RSA 2048**
RSA 2048 or higher is required for cryptographic security.

</details>

---

### 9. PCI DSS Requirement 4 primarily focuses on:

* [ ] A. Data stored in databases
* [ ] B. Data transmitted across public networks
* [ ] C. Physical access security
* [ ] D. User authentication

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Data transmitted across public networks**
Transmission security is the core of Requirement 4.

</details>

---

### 10. Which protocol version is considered compliant for data transmission?

* [ ] A. SSL 3.0
* [ ] B. TLS 1.0
* [ ] C. TLS 1.1
* [ ] D. TLS 1.2 or higher

<details>
<summary><strong>Answer</strong></summary>

✅ **D. TLS 1.2 or higher**
Older versions are deprecated due to vulnerabilities.

</details>

---

### 11. Encrypting wireless cardholder data transmissions falls under:

* [ ] A. Requirement 3
* [ ] B. Requirement 4
* [ ] C. Requirement 7
* [ ] D. Requirement 9

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 4**
It covers all public and wireless transmissions.

</details>

---

### 12. Requirement 5 mandates protection against malware on:

* [ ] A. Only servers
* [ ] B. Only endpoints
* [ ] C. All vulnerable systems
* [ ] D. Only internet-facing systems

<details>
<summary><strong>Answer</strong></summary>

✅ **C. All vulnerable systems**
Any system susceptible to malware must be protected.

</details>

---

### 13. How often must malware risk assessments be conducted?

* [ ] A. Monthly
* [ ] B. Quarterly
* [ ] C. Annually
* [ ] D. Only after incidents

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Annually**
Annual risk assessments are explicitly required.

</details>

---

### 14. Secure software development practices are addressed under:

* [ ] A. Requirement 3
* [ ] B. Requirement 5
* [ ] C. Requirement 6
* [ ] D. Requirement 11

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 6**
Requirement 6 focuses on secure systems and applications.

</details>

---

### 15. Payment page script security controls are part of:

* [ ] A. Network security
* [ ] B. Secure systems and applications
* [ ] C. Logging and monitoring
* [ ] D. Physical security

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Secure systems and applications**
Introduced strongly in PCI DSS v4.0.

</details>

---

### 16. The principle of “least privilege” is enforced by:

* [ ] A. Requirement 5
* [ ] B. Requirement 6
* [ ] C. Requirement 7
* [ ] D. Requirement 10

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 7**
Access is restricted on a need-to-know basis.

</details>

---

### 17. Role-Based Access Control (RBAC) supports which requirement?

* [ ] A. Requirement 4
* [ ] B. Requirement 7
* [ ] C. Requirement 9
* [ ] D. Requirement 11

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 7**
RBAC enforces controlled access to CHD.

</details>

---

### 18. Access reviews for cardholder data must be performed at least:

* [ ] A. Monthly
* [ ] B. Bi-annually
* [ ] C. Quarterly
* [ ] D. Annually

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Quarterly**
Quarterly reviews ensure access remains appropriate.

</details>

---

### 19. From March 2025 onward, MFA is mandatory for:

* [ ] A. Only administrators
* [ ] B. Only remote users
* [ ] C. All CDE access
* [ ] D. Only third-party vendors

<details>
<summary><strong>Answer</strong></summary>

✅ **C. All CDE access**
This is a key PCI DSS v4.0 change.

</details>

---

### 20. Minimum password length mandated under PCI DSS v4.0 is:

* [ ] A. 8 characters
* [ ] B. 10 characters
* [ ] C. 12 characters
* [ ] D. 16 characters

<details>
<summary><strong>Answer</strong></summary>

✅ **C. 12 characters**
Stronger authentication requirements are enforced.

</details>

---

### 21. Which requirement addresses physical access to server rooms?

* [ ] A. Requirement 7
* [ ] B. Requirement 8
* [ ] C. Requirement 9
* [ ] D. Requirement 10

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 9**
It governs physical security controls.

</details>

---

### 22. Visitor access logs are required under:

* [ ] A. Requirement 9
* [ ] B. Requirement 10
* [ ] C. Requirement 11
* [ ] D. Requirement 12

<details>
<summary><strong>Answer</strong></summary>

✅ **A. Requirement 9**
Physical visitor access must be documented.

</details>

---

### 23. Audit logs must be retained for a minimum of:

* [ ] A. 3 months
* [ ] B. 6 months
* [ ] C. 9 months
* [ ] D. 1 year

<details>
<summary><strong>Answer</strong></summary>

✅ **D. 1 year**
This is explicitly stated in Requirement 10.

</details>

---

### 24. Real-time monitoring is commonly implemented using:

* [ ] A. IDS only
* [ ] B. Antivirus software
* [ ] C. SIEM systems
* [ ] D. Firewalls

<details>
<summary><strong>Answer</strong></summary>

✅ **C. SIEM systems**
SIEM enables correlation and real-time alerts.

</details>

---

### 25. Which activity is mandatory on a quarterly basis?

* [ ] A. Penetration testing
* [ ] B. Internal and external vulnerability scanning
* [ ] C. Risk assessment
* [ ] D. Security awareness training

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Internal and external vulnerability scanning**

</details>

---

### 26. Annual penetration testing falls under:

* [ ] A. Requirement 6
* [ ] B. Requirement 8
* [ ] C. Requirement 10
* [ ] D. Requirement 11

<details>
<summary><strong>Answer</strong></summary>

✅ **D. Requirement 11**

</details>

---

### 27. Quarterly wireless access point scanning is part of:

* [ ] A. Requirement 1
* [ ] B. Requirement 4
* [ ] C. Requirement 11
* [ ] D. Requirement 12

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 11**

</details>

---

### 28. Security awareness training must be conducted:

* [ ] A. Once during onboarding
* [ ] B. Quarterly
* [ ] C. Annually
* [ ] D. Only after incidents

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Annually**

</details>

---

### 29. Incident response procedures are part of:

* [ ] A. Network security
* [ ] B. Logging and monitoring
* [ ] C. Information security policy
* [ ] D. Vulnerability management

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Information security policy**

</details>

---

### 30. Vendor and third-party compliance management belongs to:

* [ ] A. Requirement 7
* [ ] B. Requirement 10
* [ ] C. Requirement 11
* [ ] D. Requirement 12

<details>
<summary><strong>Answer</strong></summary>

✅ **D. Requirement 12**

</details>

---

### 31. A company uses a cloud-based POS system. They store partial card numbers and process full card numbers via an external gateway. Which PCI DSS requirement primarily ensures this data is protected?

* [ ] A. Requirement 2
* [ ] B. Requirement 3
* [ ] C. Requirement 7
* [ ] D. Requirement 10

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 3**
Requirement 3 mandates protecting stored cardholder data via encryption, truncation, or tokenization.

</details>

---

### 32. A merchant failed to change default passwords on new routers and switches before deployment. A security breach occurs. Which PCI DSS requirement was violated?

* [ ] A. Requirement 1
* [ ] B. Requirement 2
* [ ] C. Requirement 6
* [ ] D. Requirement 9

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 2**
Requirement 2 explicitly prohibits the use of vendor-supplied defaults.

</details>

---

### 33. During an audit, a company shows logs of all CHD access, but they are reviewing them only annually. Which PCI DSS principle is being violated?

* [ ] A. Requirement 7 – Access Control
* [ ] B. Requirement 10 – Logging and Monitoring
* [ ] C. Requirement 11 – Testing & Validation
* [ ] D. Requirement 12 – Security Policy

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 10 – Logging and Monitoring**
PCI DSS mandates **automated review of logs and at least quarterly monitoring**, not annual.

</details>

---

### 34. A financial institution implements 10-character passwords for all CDE access. From March 2025 onward, which PCI DSS requirement and change would they be non-compliant with?

* [ ] A. Requirement 7 – RBAC
* [ ] B. Requirement 8 – MFA & password length
* [ ] C. Requirement 12 – Security policy
* [ ] D. Requirement 3 – Data at rest encryption

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 8 – MFA & password length**
v4.0 mandates **minimum 12-character passwords** for all CDE access.

</details>

---

### 35. A merchant scans its wireless access points only after a suspected breach. Which requirement and principle are they failing to implement?

* [ ] A. Requirement 4 – Transmission encryption
* [ ] B. Requirement 5 – Anti-malware
* [ ] C. Requirement 11 – Regular testing & validation
* [ ] D. Requirement 12 – Policy

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 11 – Regular testing & validation**
PCI DSS mandates **quarterly wireless scanning**, not just post-incident.

</details>

---

### 36. A company grants all new employees access to the full cardholder database, but plans to review permissions annually. What type of vulnerability does this violate?

* [ ] A. Unauthorized physical access
* [ ] B. Least privilege principle
* [ ] C. Encryption compliance
* [ ] D. Malware protection

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Least privilege principle**
Requirement 7 requires **need-to-know access** with **periodic reviews (at least quarterly)**.

</details>

---

### 37. During a quarterly review, an auditor finds an outdated antivirus definition on a production server storing cardholder data. Which requirement is affected?

* [ ] A. Requirement 1
* [ ] B. Requirement 5
* [ ] C. Requirement 6
* [ ] D. Requirement 10

<details>
<summary><strong>Answer</strong></summary>

✅ **B. Requirement 5 – Protect against malware**
Anti-malware definitions must be **current on all vulnerable systems**.

</details>

---

### 38. A merchant uses a third-party payment gateway for all transactions but never verifies if the gateway is PCI DSS compliant. Which PCI DSS requirement is being violated?

* [ ] A. Requirement 4
* [ ] B. Requirement 7
* [ ] C. Requirement 12 – Vendor management
* [ ] D. Requirement 10

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirement 12 – Vendor management**
Requirement 12 mandates ensuring **third-party/vendor compliance**.

</details>

---

### 39. A breach occurs in which attackers accessed cardholder data due to a misconfigured firewall. Which requirement directly addresses this risk?

* [ ] A. Requirement 1 – Network security controls
* [ ] B. Requirement 2 – Default passwords
* [ ] C. Requirement 6 – Secure applications
* [ ] D. Requirement 9 – Physical access

<details>
<summary><strong>Answer</strong></summary>

✅ **A. Requirement 1 – Network security controls**
Proper firewall configuration is a core component of Requirement 1.

</details>

---

### 40. A company implements strong encryption for stored data but transmits cardholder data over an unsecured Wi-Fi network. Which requirements are violated?

* [ ] A. Requirement 3 only
* [ ] B. Requirement 4 only
* [ ] C. Requirements 3 & 4
* [ ] D. Requirement 6 only

<details>
<summary><strong>Answer</strong></summary>

✅ **C. Requirements 3 & 4**
Requirement 3 protects stored data, while Requirement 4 mandates encryption **in transit**, including Wi-Fi networks.

</details>

---


