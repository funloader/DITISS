> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

### 1. Alice needs to transfer her personal certificate and private key securely from one system to another to use in Thunderbird for S/MIME email. Which file type should she create using OpenSSL, and what inputs are required?

* [ ] PEM file containing only the user’s certificate
* [ ] DER file containing only the private key
* [ ] PKCS#12 (.p12) file containing the user’s certificate and private key
* [ ] PKCS#7 file containing only the issuer’s certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** PKCS#12 (.p12) file containing the user’s certificate and private key
💡 PKCS#12 files bundle a user’s certificate and private key into a single file for secure transport. This is typically used for importing/exporting certificates between systems or applications like email clients.

</details>

---

### 2. In Cryptool, which symmetric cipher uses a simple substitution based on a fixed key value?

* [ ] Caesar Cipher
* [ ] AES
* [ ] RSA
* [ ] Vernam Cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Caesar Cipher
💡 Caesar Cipher shifts letters by a fixed number in the alphabet and is a basic symmetric encryption technique.

</details>

---

### 3. Which of the following is true about the Vernam Cipher in Cryptool?

* [ ] It is a block cipher
* [ ] It uses a one-time pad and provides perfect secrecy if the key is random and as long as the plaintext
* [ ] It is an asymmetric cipher
* [ ] It is vulnerable to frequency analysis even with a long key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It uses a one-time pad and provides perfect secrecy if the key is random and as long as the plaintext
💡 Vernam Cipher is theoretically unbreakable when the key is truly random and as long as the message.

</details>

---

### 4. When using DES in Cryptool, what is the block size used?

* [ ] 32 bits
* [ ] 64 bits
* [ ] 128 bits
* [ ] 56 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 64 bits
💡 DES is a symmetric block cipher with a 64-bit block size and a 56-bit key.

</details>

---

### 5. Triple DES (3DES) increases security by:

* [ ] Using a single DES key three times
* [ ] Using three DES keys in encrypt-decrypt-encrypt (EDE) sequence
* [ ] Increasing block size to 192 bits
* [ ] Converting DES to an asymmetric algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using three DES keys in encrypt-decrypt-encrypt (EDE) sequence
💡 Triple DES applies DES three times with different keys to enhance security.

</details>

---

### 6. In Cryptool, which of the following is a stream cipher?

* [ ] DES
* [ ] AES
* [ ] RC4
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC4
💡 RC4 is a symmetric stream cipher that encrypts data byte-by-byte.

</details>

---

### 7. In RSA asymmetric encryption, the public key is used to:

* [ ] Encrypt data
* [ ] Decrypt data
* [ ] Sign a message
* [ ] Generate a symmetric key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encrypt data
💡 The public key encrypts messages; the private key decrypts. Signing uses the private key.

</details>

---

### 8. In ECC (Elliptic Curve Cryptography), which parameter is essential for key generation?

* [ ] Prime factor
* [ ] Curve equation and base point
* [ ] Symmetric key
* [ ] Modulus only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Curve equation and base point
💡 ECC keys are derived from a chosen elliptic curve and a base point on that curve.

</details>

---

### 9. When digitally signing a PDF using XCA, which is mandatory?

* [ ] Recipient's public key
* [ ] Signer’s private key and certificate
* [ ] CA root certificate only
* [ ] Symmetric encryption key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signer’s private key and certificate
💡 The private key signs the document; the certificate helps verify the signature.

</details>

---

### 10. What is the first step to create a CA in XCA for issuing certificates?

* [ ] Issue certificate to server
* [ ] Import root certificate
* [ ] Create a root CA
* [ ] Export CA key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create a root CA
💡 A root CA establishes a trust chain to issue subordinate certificates.

</details>

---

### 11. Importing a self-signed certificate into a browser removes which warning?

* [ ] Certificate not trusted
* [ ] Expired certificate warning
* [ ] Host mismatch warning
* [ ] Private key mismatch warning

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Certificate not trusted
💡 Adding a self-signed certificate to the trust store marks it as trusted.

</details>

---

### 12. Which OpenSSL command generates a self-signed certificate with a private key?

* [ ] `openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem`
* [ ] `openssl genrsa -aes256 -out key.pem 2048`
* [ ] `openssl verify -CAfile ca.pem cert.pem`
* [ ] `openssl pkcs12 -export -in cert.pem -inkey key.pem`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `openssl req -x509 -newkey rsa:2048 -keyout key.pem -out cert.pem`
💡 This creates a self-signed X.509 certificate and a new private key.

</details>

---

### 13. In a hierarchical PKI, which certificate issues `www.pgditiss.local`’s certificate?

* [ ] Root CA
* [ ] Subordinate CA
* [ ] Self-signed server certificate
* [ ] Client certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Subordinate CA
💡 The Subordinate CA signs server certificates in a trust hierarchy.

</details>

---

### 14. What is the purpose of a CRL in PKI?

* [ ] Issuing new certificates
* [ ] Revoking compromised or expired certificates
* [ ] Encrypting email
* [ ] Signing web content

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Revoking compromised or expired certificates
💡 CRL (Certificate Revocation List) tracks certificates no longer trusted.

</details>

---

### 15. Why is DNS configuration important when accessing `https://www.pgditiss.local`?

* [ ] To enable SMTP encryption
* [ ] To resolve hostname to server IP
* [ ] To encrypt the certificate
* [ ] To generate key pair

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To resolve hostname to server IP
💡 DNS ensures browsers can locate the server by its FQDN for HTTPS connections.

</details>

---

### 16. Which OpenSSL tool creates a Certificate Signing Request (CSR)?

* [ ] `openssl req`
* [ ] `openssl genrsa`
* [ ] `openssl x509`
* [ ] `openssl pkcs12`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `openssl req`
💡 The `req` command generates CSRs for submission to a CA.

</details>

---

### 17. In S/MIME email encryption, which algorithms are typically used?

* [ ] RSA for symmetric encryption
* [ ] DES for asymmetric encryption
* [ ] AES or Triple DES for message content, RSA for key exchange
* [ ] MD5 for content encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AES or Triple DES for message content, RSA for key exchange
💡 S/MIME uses hybrid encryption: symmetric encryption for content and asymmetric encryption for the session key.

</details>

---

### 18. Which XCA option generates a website certificate?

* [ ] Create personal key
* [ ] Create end-entity certificate
* [ ] Create root certificate
* [ ] Generate CSR only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Create end-entity certificate
💡 End-entity certificates are used by servers and clients to establish trust.

</details>

---

### 19. Which hashing algorithm is commonly used for digital signatures in XCA?

* [ ] AES
* [ ] DES
* [ ] SHA-256
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-256
💡 SHA-256 generates a hash of the document, which is then signed with the private key.

</details>

---

### 20. What is the key difference between symmetric and asymmetric encryption?

* [ ] Symmetric uses public/private keys, asymmetric uses a single key
* [ ] Symmetric uses a single shared key, asymmetric uses public/private key pairs
* [ ] Symmetric is slower than asymmetric always
* [ ] Asymmetric cannot be used for digital signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric uses a single shared key, asymmetric uses public/private key pairs
💡 Symmetric encryption is faster, asymmetric enables secure key distribution and signing.

</details>

---

### 21. In OpenSSL, which command verifies a certificate against a CA certificate?

* [ ] `openssl genrsa -out key.pem 2048`
* [ ] `openssl verify -CAfile ca.pem cert.pem`
* [ ] `openssl req -new -key key.pem -out csr.pem`
* [ ] `openssl x509 -in cert.pem -text -noout`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `openssl verify -CAfile ca.pem cert.pem`
💡 This command checks whether a certificate is trusted by verifying it against the CA certificate.

</details>

---

### 22. In hierarchical PKI, what is the correct order of certificate issuance?

* [ ] Server → Sub CA → Root CA
* [ ] Sub CA → Server → Root CA
* [ ] Root CA → Sub CA → Server
* [ ] Root CA → Server → Sub CA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA → Sub CA → Server
💡 The Root CA signs the Subordinate CA, which then signs the end-entity (server) certificate.

</details>

---

### 23. Which of the following is true about self-signed certificates in OpenSSL?

* [ ] They are signed by their own private key
* [ ] They are always trusted by default in browsers
* [ ] They require a subordinate CA to be valid
* [ ] They cannot be used for email encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They are signed by their own private key
💡 Self-signed certificates are not trusted by default; they must be added manually to the trust store.

</details>

---

### 24. When digitally signing a document in XCA, which must match?

* [ ] Certificate validity period
* [ ] CA key usage
* [ ] Signer’s private key corresponds to the certificate used
* [ ] Subject alternative name

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Signer’s private key corresponds to the certificate used
💡 Only the private key paired with the certificate can create a valid digital signature.

</details>

---

### 25. In Cryptool, XOR cipher is classified as:

* [ ] Asymmetric block cipher
* [ ] Symmetric stream cipher
* [ ] Public key encryption
* [ ] Hashing algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric stream cipher
💡 XOR encrypts bitwise using a key stream; it is symmetric and operates like a stream cipher.

</details>

---

### 26. Which is a major advantage of ECC over RSA?

* [ ] Smaller key size for similar security
* [ ] Easier to implement without libraries
* [ ] Works only for symmetric encryption
* [ ] Requires no public/private key pair

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Smaller key size for similar security
💡 ECC achieves comparable security to RSA with smaller keys, making it efficient for constrained systems.

</details>

---

### 27. When creating an HTTPS server, which certificate is installed on the server?

* [ ] Server certificate issued by Subordinate CA
* [ ] Root CA certificate only
* [ ] Sub CA private key only
* [ ] Client certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server certificate issued by Subordinate CA
💡 The server uses the end-entity certificate signed by the subordinate CA for HTTPS connections.

</details>

---

### 28. When sending an encrypted email, what ensures the recipient can decrypt it?

* [ ] Sender’s private key
* [ ] Recipient’s public key
* [ ] Sender’s public key
* [ ] Random symmetric key only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Recipient’s public key
💡 The email content is encrypted with a symmetric key, which is then encrypted with the recipient’s public key.

</details>

---

### 29. Which key usage is required for a CA certificate?

* [ ] Digital signature only
* [ ] Certificate signing and CRL signing
* [ ] Key encipherment only
* [ ] Content encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Certificate signing and CRL signing
💡 CA certificates must sign other certificates and manage revocation lists.

</details>

---

### 30. Which OpenSSL command generates a new private key and CSR in one step?

* [ ] `openssl req -new -newkey rsa:2048 -keyout key.pem -out csr.pem`
* [ ] `openssl x509 -req -in csr.pem -signkey key.pem -out cert.pem`
* [ ] `openssl genrsa -out key.pem 2048`
* [ ] `openssl pkcs12 -export -in cert.pem -inkey key.pem`

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** `openssl req -new -newkey rsa:2048 -keyout key.pem -out csr.pem`
💡 This command creates a private key and CSR simultaneously.

</details>

---

### 31. In hierarchical PKI, OCSP is used for:

* [ ] Issuing new certificates
* [ ] Checking revocation status in real-time
* [ ] Encrypting messages
* [ ] Signing emails

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Checking revocation status in real-time
💡 OCSP provides immediate verification of certificate validity compared to CRLs.

</details>

---

### 32. AES in Cryptool is considered:

* [ ] Stream cipher with variable block size
* [ ] Symmetric block cipher with fixed 128-bit block size
* [ ] Asymmetric cipher with 256-bit keys
* [ ] Hash function

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric block cipher with fixed 128-bit block size
💡 AES encrypts 128-bit blocks with keys of 128, 192, or 256 bits.

</details>

---

### 33. To trust a self-signed certificate in a browser, you must:

* [ ] Generate a CSR
* [ ] Import the certificate into the browser’s trusted root store
* [ ] Use OpenSSL to verify the certificate
* [ ] Encrypt browser cache

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Import the certificate into the browser’s trusted root store
💡 Browsers only trust certificates in their root stores; self-signed certificates must be added manually.

</details>

---

### 34. Digital signatures in XCA provide:

* [ ] Authenticity, integrity, and non-repudiation
* [ ] Content encryption
* [ ] Replacement of certificates
* [ ] Only email protection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authenticity, integrity, and non-repudiation
💡 Digital signatures verify the sender and ensure the content hasn’t been altered.

</details>

---

### 35. In OpenSSL, the `-days` option sets:

* [ ] Key size
* [ ] Validity period of the certificate
* [ ] Encryption algorithm
* [ ] Serial number

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Validity period of the certificate
💡 The `-days` option determines how long the certificate is valid from the creation date.

</details>

---

### 36. A primary advantage of PKI for email encryption is:

* [ ] Eliminates passwords
* [ ] Ensures secure key exchange and message integrity
* [ ] Encrypts only attachments
* [ ] Works without certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ensures secure key exchange and message integrity
💡 PKI allows safe symmetric key distribution and digital signatures for verification.

</details>

---

### 37. When creating a Subordinate CA in XCA, which certificate signs it?

* [ ] Server certificate
* [ ] Root CA certificate
* [ ] Client certificate
* [ ] Self-signed end-entity certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Root CA certificate
💡 The root CA signs subordinate CA certificates to establish the trust chain.

</details>

---

### 38. When setting up HTTPS in Apache using OpenSSL, which files are essential?

* [ ] Server certificate, server private key, CA certificate chain
* [ ] Only server private key
* [ ] Only self-signed certificate
* [ ] Client certificate only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Server certificate, server private key, CA certificate chain
💡 Apache needs the certificate, private key, and optionally the chain to establish trust.

</details>

---

### 39. In S/MIME labs, which algorithm hashes email content before signing?

* [ ] AES
* [ ] SHA-256
* [ ] RC4
* [ ] DES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-256
💡 Hashing ensures content integrity; the hash is encrypted with the sender’s private key.

</details>

---

### 40. What is the role of a Certificate Authority (CA)?

* [ ] Issues, signs, and manages certificates
* [ ] Generates symmetric keys for users
* [ ] Encrypts email content automatically
* [ ] Hosts websites

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Issues, signs, and manages certificates
💡 The CA validates identities and signs certificates to establish trust in PKI systems.

</details>

---
