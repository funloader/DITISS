> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 7: PKI Fundamentals – 40 MCQs
---

### 1. Which of the following is considered a **passive security attack**?

* [ ] Man-in-the-middle
* [ ] Eavesdropping
* [ ] Denial of Service (DoS)
* [ ] Phishing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eavesdropping
💡 Passive attacks monitor communications without altering them, such as eavesdropping or traffic analysis.

</details>

---

### 2. What is the primary purpose of a **digital signature**?

* [ ] Encrypt data for confidentiality
* [ ] Verify the identity of the sender and integrity of the message
* [ ] Generate session keys
* [ ] Authenticate the server only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verify the identity of the sender and integrity of the message
💡 Digital signatures ensure authenticity and prevent tampering.

</details>

---

### 3. A **digital certificate** primarily provides:

* [ ] Encryption for message content
* [ ] Trust between parties over a network
* [ ] Hash of a message
* [ ] Symmetric key distribution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Trust between parties over a network
💡 Digital certificates bind public keys to identities and establish trust.

</details>

---

### 4. Which entity issues **digital certificates**?

* [ ] Network Administrator
* [ ] Certificate Authority (CA)
* [ ] End user
* [ ] Internet Service Provider (ISP)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Certificate Authority (CA)
💡 CAs verify identities and issue certificates in a PKI system.

</details>

---

### 5. Which of the following **cannot be repudiated** when using a digital signature?

* [ ] Signed document
* [ ] Encrypted session key
* [ ] Public certificate
* [ ] Hash algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signed document
💡 Digital signatures provide non-repudiation; the signer cannot deny signing the document.

</details>

---

### 6. Which cryptographic technique is used in **digital signatures**?

* [ ] Symmetric key encryption
* [ ] Asymmetric key cryptography
* [ ] Hash-based message authentication only
* [ ] Steganography

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric key cryptography
💡 Digital signatures use the sender’s private key for signing and public key for verification.

</details>

---

### 7. A digital certificate contains:

* [ ] Public key, owner info, CA signature
* [ ] Private key only
* [ ] Password hash
* [ ] Encrypted session key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key, owner info, CA signature
💡 Certificates include the entity’s public key, identifying information, and CA digital signature.

</details>

---

### 8. Digital signatures provide **integrity** by:

* [ ] Encrypting the message
* [ ] Hashing the message and signing the hash
* [ ] Sharing the public key
* [ ] Generating symmetric keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hashing the message and signing the hash
💡 Any modification in the message will result in a different hash, breaking the signature.

</details>

---

### 9. Which format is used for most digital certificates?

* [ ] X.509
* [ ] PEM
* [ ] DER
* [ ] TXT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** X.509
💡 X.509 defines the standard format for public key certificates.

</details>

---

### 10. A **public key** in a certificate is used to:

* [ ] Encrypt data or verify digital signatures
* [ ] Decrypt the private key
* [ ] Generate HMAC
* [ ] Create a session key only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encrypt data or verify digital signatures
💡 The public key can verify signatures or encrypt data for the owner.

</details>

---

### 11. What ensures that two parties exchanging information are secure?

* [ ] Digital signature
* [ ] Digital certificate
* [ ] Passwords
* [ ] Symmetric keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital certificate
💡 Certificates establish trust between communicating parties.

</details>

---

### 12. Digital signatures are created using:

* [ ] SHA and private key
* [ ] Only symmetric encryption
* [ ] Only public key
* [ ] Random numbers

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA and private key
💡 The hash of a message is encrypted using the sender’s private key to create a signature.

</details>

---

### 13. What is the primary difference between a digital signature and a digital certificate?

* [ ] Signature authenticates a message; certificate establishes trust
* [ ] Signature encrypts data; certificate decrypts data
* [ ] Signature is symmetric; certificate is asymmetric
* [ ] Signature is issued by CA; certificate is created by user

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signature authenticates a message; certificate establishes trust
💡 A signature ensures authenticity of the message, while a certificate binds identity to a public key.

</details>

---

### 14. A certificate is **invalid** if:

* [ ] The CA signature is correct
* [ ] It is expired or revoked
* [ ] Public key is included
* [ ] Hashing algorithm is used

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It is expired or revoked
💡 Expired or revoked certificates should not be trusted.

</details>

---

### 15. Which of the following ensures **non-repudiation**?

* [ ] Symmetric encryption
* [ ] Digital signature
* [ ] Password protection
* [ ] TLS handshake

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signature
💡 Non-repudiation ensures that a sender cannot deny sending a signed message.

</details>

---

### 16. Which PKI component issues and signs certificates?

* [ ] Registration Authority
* [ ] Certificate Authority
* [ ] End User
* [ ] Key Management Server

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Certificate Authority
💡 The CA validates identities and signs certificates.

</details>

---

### 17. Which is used to **verify digital signature authenticity**?

* [ ] Sender’s public key
* [ ] Sender’s private key
* [ ] Receiver’s public key
* [ ] Receiver’s private key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Sender’s public key
💡 The public key of the sender is used to validate the signature.

</details>

---

### 18. PKI stands for:

* [ ] Public Key Infrastructure
* [ ] Private Key Integration
* [ ] Personal Key Identity
* [ ] Public Key Interchange

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public Key Infrastructure
💡 PKI is a framework for managing keys, certificates, and trust.

</details>

---

### 19. Which of the following is **issued after background verification**?

* [ ] Digital signature
* [ ] Digital certificate
* [ ] Public key
* [ ] Session key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital certificate
💡 Certificates require verification by a CA before issuance.

</details>

---

### 20. Digital certificates provide security mainly for:

* [ ] Authentication and encryption
* [ ] Only encryption
* [ ] Only password management
* [ ] Network routing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication and encryption
💡 Certificates authenticate identities and can also facilitate encryption.

</details>

---

### 21. Digital signatures **cannot** ensure:

* [ ] Integrity
* [ ] Non-repudiation
* [ ] Encryption confidentiality
* [ ] Authenticity

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encryption confidentiality
💡 Signatures verify authenticity and integrity but do not encrypt the message.

</details>

---

### 22. Which of the following is part of a digital certificate?

* [ ] Serial number
* [ ] Subject name
* [ ] Issuer name
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates include issuer, subject, serial number, validity period, and public key.

</details>

---

### 23. Which is used to prevent **forgery of documents**?

* [ ] HMAC
* [ ] Digital signature
* [ ] Symmetric encryption
* [ ] VPN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signature
💡 Signing a document ensures it cannot be forged without detection.

</details>

---

### 24. Certificates are commonly used in:

* [ ] SSL/TLS
* [ ] Email encryption
* [ ] Code signing
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates authenticate identities in web, email, and software applications.

</details>

---

### 25. Digital signature verification fails if:

* [ ] Message was modified after signing
* [ ] Correct public key used
* [ ] Correct hash algorithm
* [ ] Sender is trusted

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Message was modified after signing
💡 Any change to the message invalidates the signature.

</details>

---

### 26. Which of the following algorithms is commonly used for **digital signatures**?

* [ ] RSA
* [ ] AES
* [ ] DES
* [ ] MD5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA and ECC are widely used for signing messages.

</details>

---

### 27. Which component of PKI **verifies the identity before certificate issuance**?

* [ ] Registration Authority (RA)
* [ ] Certificate Authority (CA)
* [ ] End user
* [ ] Network Admin

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Registration Authority (RA)
💡 RA validates identities before the CA issues certificates.

</details>

---

### 28. Certificates usually include a **validity period**. Why?

* [ ] To ensure certificate expires and is renewed periodically
* [ ] To encrypt messages
* [ ] To sign hashes
* [ ] To provide private keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To ensure certificate expires and is renewed periodically
💡 Expiration limits risk if a certificate or key is compromised.

</details>

---

### 29. Which of the following provides **trust chain** in PKI?

* [ ] Root CA → Intermediate CA → End Entity
* [ ] Digital signature only
* [ ] Symmetric key hierarchy
* [ ] VPN chain

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA → Intermediate CA → End Entity
💡 The trust chain ensures each certificate is validated by a trusted CA above it.

</details>

---

### 30. PKI helps prevent:

* [ ] Man-in-the-middle attacks
* [ ] Spoofing identities
* [ ] Data tampering
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates and digital signatures protect against multiple attacks.

</details>

---

### 31. Which of the following is **true for a valid digital certificate**?

* [ ] Signed by a trusted CA
* [ ] Public key included
* [ ] Not expired or revoked
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Valid certificates must be properly signed, contain the correct key, and be within validity.

</details>

---

### 32. The CA’s signature on a certificate ensures:

* [ ] Authenticity of certificate
* [ ] Encryption of message
* [ ] Symmetric key distribution
* [ ] Hash collision prevention

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticity of certificate
💡 CA signature confirms that the certificate was issued by a trusted authority.

</details>

---

### 33. Digital certificates **do not contain**:

* [ ] Owner’s public key
* [ ] Owner’s private key
* [ ] Validity period
* [ ] Issuer info

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Owner’s private key
💡 Private keys are kept secret; certificates only include public keys.

</details>

---

### 34. Digital certificates are used in:

* [ ] HTTPS websites
* [ ] VPN connections
* [ ] Code signing
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates authenticate identity in web, VPN, and software code contexts.

</details>

---

### 35. A **self-signed certificate** is:

* [ ] Signed by the user itself
* [ ] Signed by a trusted CA
* [ ] Invalid for any purpose
* [ ] Used in HMAC

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signed by the user itself
💡 Self-signed certificates are not inherently trusted by others unless explicitly added.

</details>

---

### 36. Which of the following is **used for key verification in PKI**?

* [ ] Public key
* [ ] Private key
* [ ] Symmetric key
* [ ] Session key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key
💡 Public keys are used to verify signatures and encrypt messages.

</details>

---

### 37. Which of the following is **mandatory for certificate-based authentication**?

* [ ] Digital certificate
* [ ] Password only
* [ ] Symmetric key
* [ ] PIN only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital certificate
💡 Certificates allow identity verification without passwords.

</details>

---

### 38. Which algorithm can be used for **digital certificate signatures**?

* [ ] RSA
* [ ] ECDSA
* [ ] DSA
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Various asymmetric algorithms are used to sign certificates.

</details>

---

### 39. Certificate revocation is necessary if:

* [ ] Private key is compromised
* [ ] Certificate expired
* [ ] Identity changes
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Certificates must be revoked if any factor undermines their trust.

</details>

---

### 40. The combination of **digital signature and certificate** provides:

* [ ] Confidentiality and integrity
* [ ] Authentication, integrity, and trust
* [ ] Symmetric key distribution
* [ ] Hashing only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication, integrity, and trust
💡 Signatures ensure integrity and authenticity, while certificates provide trust.

</details>

---
