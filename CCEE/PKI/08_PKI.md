> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 8: Certificate Authority & Certificate Management 40 MCQs

---

### 1. Which of the following entities is responsible for issuing digital certificates?

* [ ] Registration Authority (RA)
* [ ] Certificate Authority (CA)
* [ ] End User
* [ ] Network Administrator

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Certificate Authority (CA)
💡 The CA verifies identities and issues digital certificates in a PKI system.

</details>

---

### 2. What is the primary role of a **Registration Authority (RA)**?

* [ ] Issue certificates directly
* [ ] Verify the identity of certificate applicants
* [ ] Encrypt messages
* [ ] Generate private keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verify the identity of certificate applicants
💡 RA performs identity verification before passing requests to the CA for issuance.

</details>

---

### 3. In a **CA Trust Model**, the trust chain starts from:

* [ ] End Entity
* [ ] Root CA
* [ ] Intermediate CA
* [ ] Client

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA
💡 Root CA is pre-installed and forms the top of the trust hierarchy.

</details>

---

### 4. Which of the following best describes **certificate issuance**?

* [ ] Signing the certificate with the applicant's private key
* [ ] CA creating, signing, and distributing a certificate after verification
* [ ] Encrypting messages between two parties
* [ ] Generating symmetric keys for the network

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CA creating, signing, and distributing a certificate after verification
💡 The CA issues certificates after verifying the applicant’s identity.

</details>

---

### 5. Certificate revocation is performed when:

* [ ] A certificate expires
* [ ] A private key is compromised
* [ ] An organization’s ownership changes
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Revocation maintains PKI security if a certificate is no longer trustworthy.

</details>

---

### 6. Which protocol allows **real-time checking** of certificate revocation?

* [ ] SSL
* [ ] TLS
* [ ] OCSP
* [ ] HTTPS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OCSP
💡 Online Certificate Status Protocol provides real-time revocation status.

</details>

---

### 7. What is a **Certificate Revocation List (CRL)**?

* [ ] A list of trusted CAs
* [ ] A list of revoked certificates issued by a CA
* [ ] A public key repository
* [ ] A key exchange protocol

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** A list of revoked certificates issued by a CA
💡 CRL allows clients to check which certificates are no longer valid.

</details>

---

### 8. In PKI, the **trust chain** is validated using:

* [ ] Client’s private key
* [ ] Root CA’s public key
* [ ] Symmetric session key
* [ ] HMAC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA’s public key
💡 Each certificate is verified using the issuer’s public key, ultimately linking to a trusted root CA.

</details>

---

### 9. A **Domain Validated (DV) certificate** validates:

* [ ] The organization only
* [ ] Ownership of the domain only
* [ ] User identity
* [ ] Server IP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ownership of the domain only
💡 DV certificates confirm that the requester controls the domain.

</details>

---

### 10. Which type of certificate provides the **highest level of authentication**?

* [ ] DV
* [ ] OV
* [ ] EV
* [ ] Class 1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** EV (Extended Validation)
💡 EV certificates require rigorous verification of the organization and domain.

</details>

---

### 11. Which certificate class is used for **high-risk websites**?

* [ ] Class 1
* [ ] Class 2
* [ ] Class 3
* [ ] Class 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Class 3
💡 Class 3 certificates involve physical verification and organization identity checks.

</details>

---

### 12. Which certificate is typically used for **email encryption**?

* [ ] Code Signing Certificate
* [ ] DV Certificate
* [ ] S/MIME Certificate
* [ ] SSL Certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** S/MIME Certificate
💡 S/MIME uses certificates to encrypt and sign email messages.

</details>

---

### 13. Certificate signing by a CA guarantees:

* [ ] Confidentiality of the data
* [ ] Authenticity of the certificate
* [ ] Integrity of all messages in the network
* [ ] Symmetric key distribution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticity of the certificate
💡 CA signature proves that the certificate is issued by a trusted authority.

</details>

---

### 14. Which of the following **cannot be used as a reason for certificate revocation**?

* [ ] Key compromise
* [ ] Affiliation change
* [ ] Expiry of certificate
* [ ] Public key validation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key validation
💡 Validation of public key is part of issuance; it is not a revocation reason.

</details>

---

### 15. The **Trust Model** in PKI ensures:

* [ ] Symmetric encryption
* [ ] Hierarchical verification of certificates
* [ ] VPN tunnel creation
* [ ] Password strength enforcement

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hierarchical verification of certificates
💡 Trust is propagated from root CAs to intermediate CAs and end entities.

</details>

---

### 16. What is the role of an **Intermediate CA**?

* [ ] Issue root certificates
* [ ] Bridge trust between root CA and end entities
* [ ] Encrypt data
* [ ] Generate HMAC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Bridge trust between root CA and end entities
💡 Intermediate CAs reduce direct exposure of root CA and manage certificate issuance.

</details>

---

### 17. A certificate is considered **invalid** if:

* [ ] Signed by trusted CA
* [ ] Public key matches private key
* [ ] It has been revoked
* [ ] It contains the organization name

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It has been revoked
💡 Revoked certificates must not be trusted.

</details>

---

### 18. **Online Certificate Status Protocol (OCSP)** is preferred over CRL because:

* [ ] It reduces network traffic and gives real-time status
* [ ] It encrypts messages
* [ ] It provides multi-factor authentication
* [ ] It generates certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It reduces network traffic and gives real-time status
💡 OCSP avoids downloading the entire CRL for revocation checks.

</details>

---

### 19. Which type of certificate verifies both **organization and domain**?

* [ ] DV
* [ ] OV
* [ ] EV
* [ ] Class 1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** OV (Organization Validated)
💡 OV certificates validate the organization and domain for medium-risk transactions.

</details>

---

### 20. Root CA public keys are typically **pre-installed** in:

* [ ] Web browsers and operating systems
* [ ] Individual laptops only
* [ ] Network routers
* [ ] Firewalls

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Web browsers and operating systems
💡 Root CAs are trusted by default through pre-installed certificates.

</details>

---

### 21. Which component ensures that **end users trust the certificate**?

* [ ] Root CA signature
* [ ] Passwords
* [ ] Symmetric key
* [ ] IP address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA signature
💡 Trust propagates from a known trusted root CA to all certificates.

</details>

---

### 22. Which of the following is **NOT a type of certificate**?

* [ ] Domain Validated
* [ ] Organization Validated
* [ ] Extended Validation
* [ ] Symmetric Key Certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric Key Certificate
💡 Certificates are based on public key infrastructure, not symmetric keys.

</details>

---

### 23. Certificate classes are based on:

* [ ] Level of verification
* [ ] Symmetric key strength
* [ ] Hashing algorithm used
* [ ] Cipher block size

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Level of verification
💡 Class 1-3 certificates differ by how much identity verification the CA performs.

</details>

---

### 24. Which of the following statements is **true about CRL**?

* [ ] CRL is updated in real-time
* [ ] CRL contains all certificates ever issued
* [ ] CRL lists revoked certificates
* [ ] CRL encrypts user data

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CRL lists revoked certificates
💡 CRL is a periodically updated list of invalid certificates.

</details>

---

### 25. Which certificate type is **used for code signing**?

* [ ] DV
* [ ] OV
* [ ] Code Signing Certificate
* [ ] EV

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Code Signing Certificate
💡 Code signing certificates verify that software originates from a trusted source.

</details>

---

### 26. Certificate issuance includes which of the following steps?

* [ ] Key pair generation
* [ ] Identity verification
* [ ] Certificate signing
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificate issuance involves key generation, verification, and signing.

</details>

---

### 27. Which of the following ensures that **two communicating parties can trust each other**?

* [ ] Digital certificate
* [ ] Hash function
* [ ] VPN
* [ ] Firewall

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital certificate
💡 Certificates authenticate entities to establish trust.

</details>

---

### 28. EV certificates are typically used in:

* [ ] E-commerce and banking websites
* [ ] Personal blogs
* [ ] Internal servers only
* [ ] Social media

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** E-commerce and banking websites
💡 EV certificates provide high trust for high-value transactions.

</details>

---

### 29. Which type of certificate is issued **based solely on email validation**?

* [ ] Class 1
* [ ] Class 2
* [ ] Class 3
* [ ] Class 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Class 1
💡 Class 1 is for low-risk scenarios and validates only the email address.

</details>

---

### 30. Intermediate CAs help in:

* [ ] Reducing root CA exposure
* [ ] Issuing certificates
* [ ] Forming trust chains
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Intermediate CAs bridge trust and manage certificate issuance.

</details>

---

### 31. Which certificate class involves **physical verification of the organization**?

* [ ] Class 1
* [ ] Class 2
* [ ] Class 3
* [ ] Class 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Class 3
💡 Physical verification is required for high-risk certificates.

</details>

---

### 32. Which of the following is a key **advantage of using OCSP** over CRL?

* [ ] Faster revocation checks
* [ ] Requires downloading entire list
* [ ] Encrypts messages
* [ ] Provides hashing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Faster revocation checks
💡 OCSP allows real-time verification without downloading the full CRL.

</details>

---

### 33. Certificates can be revoked due to:

* [ ] Key compromise
* [ ] Employee leaving organization
* [ ] Domain change
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Any event that invalidates trust requires revocation.

</details>

---

### 34. A **trust anchor** is:

* [ ] Root CA certificate
* [ ] End entity certificate
* [ ] Symmetric key
* [ ] HMAC key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA certificate
💡 Trust anchor is the root CA used to validate certificate chains.

</details>

---

### 35. Which certificate type is used **only for code authentication**?

* [ ] SSL
* [ ] Email
* [ ] Code Signing
* [ ] DV

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Code Signing
💡 Verifies software integrity and publisher authenticity.

</details>

---

### 36. What happens if a client uses a **revoked certificate**?

* [ ] Communication fails or is insecure
* [ ] Data is encrypted successfully
* [ ] HMAC validates the message
* [ ] Nothing happens

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Communication fails or is insecure
💡 Revoked certificates are no longer trusted and should not be used.

</details>

---

### 37. Which of the following **does not require CA verification**?

* [ ] Self-signed certificate
* [ ] EV certificate
* [ ] OV certificate
* [ ] Class 3 certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Self-signed certificate
💡 Self-signed certificates are created without CA involvement.

</details>

---

### 38. The **root CA certificate** is typically:

* [ ] Publicly trusted
* [ ] Secret
* [ ] Expired
* [ ] Revoked

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Publicly trusted
💡 Root CA certificates are pre-installed in browsers and OS for trust.

</details>

---

### 39. Trust in PKI is established via:

* [ ] Public key hierarchy
* [ ] Password complexity
* [ ] Symmetric encryption only
* [ ] Firewalls

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key hierarchy
💡 PKI uses hierarchical trust chains from root CA to end entities.

</details>

---

### 40. Which of the following is a **mandatory field** in X.509 certificates?

* [ ] Issuer name
* [ ] Validity period
* [ ] Public key
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates must include issuer, validity period, and public key to be valid.

</details>

---
