> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

### 1. Which of the following inputs are required to create a PKCS#12 (.p12) file for a user using OpenSSL?

* [ ] Digital certificate of issuer only
* [ ] Digital certificate of user only
* [ ] Digital certificate of user and private key of user
* [ ] Digital certificate of issuer and private key of issuer

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital certificate of user and private key of user
💡 A PKCS#12 file bundles the user's certificate and corresponding private key (optionally CA certificates).

</details>

---

### 2. Which of the following algorithms does NOT provide key exchange functionality?

* [ ] RSA
* [ ] Elliptic Curve Diffie-Hellman
* [ ] Diffie-Hellman
* [ ] DSS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DSS
💡 DSS (Digital Signature Standard) is used for digital signatures, not key exchange.

</details>

---

### 3. Which of the following formats is specifically designed to securely store private keys?

* [ ] PEM
* [ ] DER
* [ ] JKS
* [ ] TXT

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** JKS
💡 Java KeyStore (JKS) is explicitly designed to securely store private keys and certificates.

</details>

---

### 4. The Caesar Cipher is an example of which cryptographic technique?

* [ ] Symmetric
* [ ] Asymmetric
* [ ] Transposition
* [ ] Steganography

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric
💡 Caesar cipher uses the same key for encryption and decryption.

</details>

---

### 5. What is the standard format used for digital certificates?

* [ ] X.500
* [ ] .crt
* [ ] X.509
* [ ] PEM

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** X.509
💡 X.509 defines the structure and format of digital certificates.

</details>

---

### 6. Encryption is a ________ function whereas hashing is a ________ function.

* [ ] One-way, Two-way
* [ ] One-way, One-way
* [ ] Two-way, One-way
* [ ] Two-way, Two-way

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Two-way, One-way
💡 Encryption is reversible; hashing is not.

</details>

---

### 7. Encrypting a message digest with a private key produces a:

* [ ] Digital certificate
* [ ] Encrypted hash
* [ ] Digital signature
* [ ] Message authentication code

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signature
💡 Digital signatures are created by encrypting a hash with the sender’s private key.

</details>

---

### 8. A Certificate Revocation List (CRL) contains:

* [ ] Public keys of users
* [ ] Private keys of users
* [ ] Email addresses of revoked users
* [ ] Serial numbers of revoked certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Serial numbers of revoked certificates
💡 CRLs identify revoked certificates by their serial numbers.

</details>

---

### 9. A Certificate Signing Request (CSR) contains:

* [ ] Private key and user credentials
* [ ] Only user credentials
* [ ] Public key and user credentials
* [ ] Only the private key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key and user credentials
💡 A CSR never contains a private key.

</details>

---

### 10. Which of the following is NOT a licensed Certifying Authority (CA) in India?

* [ ] eMudhra
* [ ] nCode
* [ ] SafeScrypt
* [ ] DigiCert

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DigiCert
💡 DigiCert is not licensed as an Indian Root CA.

</details>

---

### 11. What is the block size of plaintext used in the AES algorithm?

* [ ] 64 bits
* [ ] 120 bits
* [ ] 128 bits
* [ ] 256 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 128 bits
💡 AES always operates on 128-bit blocks.

</details>

---

### 12. Which pair of Linux commands produces the same SHA-1 message digest?

* [ ] md4sum, md5sum
* [ ] sha1sum, shasum
* [ ] sha256sum, sha1sum
* [ ] md5sum, sha1sum

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** sha1sum, shasum
💡 Both commands compute SHA-1 by default.

</details>

---

### 13. Which cryptographic algorithms are commonly used in SSL/TLS?

* [ ] DES only
* [ ] RSA only
* [ ] AES and RSA
* [ ] MD5 only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AES and RSA
💡 TLS uses RSA for key exchange/authentication and AES for encryption.

</details>

---

### 14. How many servers are involved in Kerberos authentication?

* [ ] 1
* [ ] 2
* [ ] 3
* [ ] 4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3
💡 Authentication Server, Ticket Granting Server, and Application Server.

</details>

---

### 15. The security of the Diffie-Hellman algorithm relies on the difficulty of computing:

* [ ] Prime factorization
* [ ] Discrete logarithms
* [ ] Hash collisions
* [ ] Elliptic curves

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Discrete logarithms
💡 DH security is based on the discrete logarithm problem.

</details>

---

### 16. Which statement about OCSP and CRL is TRUE?

* [ ] CRL provides real-time certificate validation
* [ ] OCSP requires downloading the entire revocation list
* [ ] CRL must be frequently updated to remain current
* [ ] OCSP stores private keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** CRL must be frequently updated to remain current
💡 This is the primary limitation of CRLs.

</details>

---

### 17. Which IPSec mode protects the entire IP packet?

* [ ] Transport
* [ ] Tunnel
* [ ] Application
* [ ] Session

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunnel
💡 Tunnel mode encapsulates the entire IP packet.

</details>

---

### 18. Which IPSec protocol provides authentication but no encryption?

* [ ] SSL
* [ ] ESP
* [ ] AH
* [ ] TLS

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AH
💡 Authentication Header provides integrity and authentication only.

</details>

---

### 19. Which security service ensures a sender cannot deny sending a message?

* [ ] Confidentiality
* [ ] Integrity
* [ ] Authentication
* [ ] Non-repudiation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Non-repudiation
💡 Digital signatures provide non-repudiation.

</details>

---

### 20. Which of the following is an example of a stream cipher?

* [ ] AES
* [ ] DSA
* [ ] SHA-256
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC4
💡 RC4 is a classic stream cipher.

</details>

---

### 21. Why would a certificate be added to a Certificate Revocation List (CRL)?

* [ ] Certificate was publicly available
* [ ] Private key was compromised
* [ ] Certificate expired normally
* [ ] Public key length increased

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Private key was compromised
💡 Compromise of the private key invalidates trust.

</details>

---

### 22. Which of the following is NOT an encryption algorithm?

* [ ] AES
* [ ] DES
* [ ] RSA
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Diffie-Hellman
💡 Diffie-Hellman is a key exchange algorithm.

</details>

---

### 23. What key length is NOT supported by AES?

* [ ] 128 bits
* [ ] 192 bits
* [ ] 256 bits
* [ ] 512 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 512 bits
💡 AES supports only 128, 192, and 256-bit keys.

</details>

---

### 24. Which protocol provides authentication and/or encryption for packets at the IP layer?

* [ ] SSL
* [ ] PGP
* [ ] ESP
* [ ] SMTP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ESP
💡 ESP (Encapsulating Security Payload) provides encryption, integrity, and optional authentication at the IP layer.

</details>

---

### 25. The combination of key exchange, hash, and encryption algorithms defines a ________ in SSL/TLS.

* [ ] Protocol list
* [ ] Suite of protocols
* [ ] Cipher suite
* [ ] Encryption profile

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cipher suite
💡 A cipher suite specifies the algorithms used for a TLS session.

</details>

---

### 26. To exchange encrypted e-mail messages using PGP, a user must have:

* [ ] Only a public key
* [ ] Only a private key
* [ ] Both public and private keys
* [ ] A digital certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both public and private keys
💡 PGP uses asymmetric cryptography for secure email exchange.

</details>

---

### 27. Which protocol provides security services for data generated at the application layer?

* [ ] IPSec
* [ ] SSL/TLS
* [ ] ICMP
* [ ] ARP

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSL/TLS
💡 SSL/TLS secures application-layer protocols such as HTTP, SMTP, and FTP.

</details>

---

### 28. Which security service ensures that data has not been altered in transit?

* [ ] Confidentiality
* [ ] Integrity
* [ ] Authentication
* [ ] Non-repudiation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Integrity
💡 Integrity ensures data remains unchanged during transmission.

</details>

---

### 29. Anomaly-based and signature-based detection techniques are associated with which security system?

* [ ] Firewall
* [ ] Router
* [ ] IDS
* [ ] VPN

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** IDS
💡 Intrusion Detection Systems use both anomaly and signature-based detection.

</details>

---

### 30. Which of the following is an example of a stream cipher?

* [ ] AES
* [ ] DSA
* [ ] SHA-256
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC4
💡 RC4 encrypts data one byte at a time, making it a stream cipher.

</details>

---

### 31. What does OCSP stand for in public key infrastructure?

* [ ] Online Certificate Service Provider
* [ ] Open Certificate Security Protocol
* [ ] Online Certificate Status Protocol
* [ ] Open Cryptographic Standards Program

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Online Certificate Status Protocol
💡 OCSP provides real-time certificate revocation status.

</details>

---

### 32. Which of the following is a disadvantage of asymmetric cryptography?

* [ ] Does not provide confidentiality
* [ ] Slower than symmetric cryptography
* [ ] Cannot support digital signatures
* [ ] Uses only one key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Slower than symmetric cryptography
💡 Asymmetric algorithms are computationally expensive.

</details>

---

### 33. Which AES key size is NOT supported?

* [ ] 128 bits
* [ ] 192 bits
* [ ] 256 bits
* [ ] 512 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 512 bits
💡 AES supports only 128, 192, and 256-bit keys.

</details>

---

### 34. Which term refers specifically to the science of breaking cryptographic systems?

* [ ] Cryptography
* [ ] Cryptology
* [ ] Cryptanalysis
* [ ] Steganography

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cryptanalysis
💡 Cryptanalysis focuses on breaking encryption and codes.

</details>

---

### 35. A secret key used only once for encrypting data is called a:

* [ ] Public key
* [ ] Private key
* [ ] Asymmetric key
* [ ] Session key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Session key
💡 Session keys are temporary and used for a single communication session.

</details>

---

### 36. Which statement is NOT true about SSL/TLS?

* [ ] Provides encryption and integrity
* [ ] Uses public key cryptography
* [ ] Commonly used to secure login pages
* [ ] Provides VPN services by itself

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides VPN services by itself
💡 SSL/TLS is not a VPN technology.

</details>

---

### 37. An attack where the attacker can choose ciphertext and obtain the corresponding plaintext is called:

* [ ] Ciphertext-only attack
* [ ] Known-plaintext attack
* [ ] Chosen-plaintext attack
* [ ] Chosen-ciphertext attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Chosen-ciphertext attack
💡 The attacker selects ciphertexts and analyzes decrypted outputs.

</details>

---

### 38. Kerberos is primarily a(n) __________ protocol.

* [ ] Session initiation
* [ ] Authentication
* [ ] Encryption
* [ ] Key generation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication
💡 Kerberos provides secure authentication using tickets.

</details>

---

### 39. Which of the following statements is TRUE?

* [ ] SHA-256 hashes can be reversed
* [ ] HTTPS protects against keyloggers
* [ ] Digital signatures depend on the signed content
* [ ] Digital certificates contain private keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signatures depend on the signed content
💡 Any modification to the content invalidates the signature.

</details>

---

### 40. Which statement is TRUE?

* [ ] SHA-256 hashes can be reversed easily
* [ ] HTTPS protects against keyloggers
* [ ] Digital signatures depend on the signed content
* [ ] Digital certificates contain private keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signatures depend on the signed content
💡 Any content change invalidates the signature.

</details>

---
