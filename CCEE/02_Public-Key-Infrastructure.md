> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

### 1. Enter the protocol and port that must be specified within an interface ACL to allow a management connection to be terminated on the router:

* [ ] TCP 443
* [ ] UDP 500
* [ ] TCP 22
* [ ] UDP 4500

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** UDP 500
💡 UDP port 500 is used for ISAKMP/IKE Phase 1 management connections, and must be allowed in an interface ACL for proper VPN setup.

</details>

---

### 2. If you omit a parameter in an ISAKMP/IKE Phase 1 policy, a default value is used. Which of the following is **not** a default value?

* [ ] MD5
* [ ] DES
* [ ] DH group 1
* [ ] RSA signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MD5
💡 SHA-1 is the default HMAC function if omitted; MD5 is **not** the default.

</details>

---

### 3. What is the default lifetime of data Security Associations (SAs) if not overridden?

* [ ] 300 seconds
* [ ] 600 seconds
* [ ] 3,600 seconds
* [ ] 86,400 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3,600 seconds
💡 Data SAs default to a 3,600-second lifetime unless explicitly overridden in the configuration.

</details>

---

### 4. What is the default mode for a transform set if omitted?

* [ ] Transport
* [ ] Transform
* [ ] Symmetrical
* [ ] Tunnel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunnel
💡 Tunnel mode is the default transform set mode for site-to-site IPSec VPNs.

</details>

---

### 5. Which of the following is **not required** in a crypto map entry?

* [ ] Crypto ACL
* [ ] Router's local IP address
* [ ] Transform set name
* [ ] Connection method: manual or dynamic (ISAKMP/IKE)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Router's local IP address
💡 The remote peer's IP address must be specified, not the local router’s IP address.

</details>

---

### 6. Which of the following traffic is **dropped** when using static crypto maps and IPSec?

* [ ] Inbound traffic that is protected and matches a crypto ACL entry
* [ ] Inbound traffic that doesn't match a crypto ACL entry
* [ ] Inbound traffic that matches a crypto ACL entry and is in clear text
* [ ] Outbound traffic that matches a crypto ACL and is already protected by IPSec

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inbound traffic that matches a crypto ACL entry and is in clear text
💡 Routers drop inbound traffic that matches a crypto ACL but is unencrypted to enforce IPSec protection.

</details>

---

### 7. What state will a management connection be in if it is successfully set up?

* [ ] MM_NO_STATE
* [ ] QM_IDLE
* [ ] MM_SA_SETUP
* [ ] MM_KEY_AUTH

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** QM_IDLE
💡 QM_IDLE indicates the management connection has successfully negotiated the Phase 2 SAs.

</details>

---

### 8. Which debug crypto isakmp output indicates a **failed policy negotiation**?

* [ ] %CRYPTO-6-IKMP_SA_NOT_OFFERED: Remote peer responded with attribute not offered
* [ ] %CRYPTO-6-IKMP_SA_NOT_AUTH: Cannot accept Quick Mode exchange if SA is not authenticated
* [ ] IPSec(validate_transform_proposal): proxy identities not supported
* [ ] IPSEC(validate_proposal): invalid local address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** %CRYPTO-6-IKMP_SA_NOT_OFFERED: Remote peer responded with attribute not offered
💡 This indicates that the remote peer did not offer the expected attributes, causing negotiation to fail.

</details>

---

### 9. What crypto map command is used to specify the crypto ACL to use?

* [ ] set transform-set
* [ ] match address
* [ ] set address
* [ ] set crypto-acl

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** match address
💡 The `match address` command in the crypto map specifies which ACL defines the traffic to be protected by IPSec.

</details>

---

### 10. In creating an ISAKMP/IKE Phase 1 policy with preshared keys, which of the following commands sets the preshared key for peer 192.1.1.1?

* [ ] crypto key generate rsa 1024
* [ ] crypto isakmp key 0 abc123 address 192.1.1.1
* [ ] crypto isakmp policy 100 authentication pre-share
* [ ] crypto transform-set 3des

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** crypto isakmp key 0 abc123 address 192.1.1.1
💡 This command binds the preshared key `abc123` to the specified peer IP for Phase 1 authentication.

</details>

---

### 11. Atbash is an example of a ____________________

* [ ] Substitution Cipher
* [ ] Transposition Cipher
* [ ] All of the above
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Substitution Cipher
💡 Atbash is a classical monoalphabetic substitution cipher where each letter is mapped to its reverse in the alphabet.

</details>

---

### 12. ______________ cipher replaces bits, characters, or blocks of characters with different bits, characters, or blocks.

* [ ] Substitution
* [ ] XORing
* [ ] Transposition
* [ ] Transportation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Substitution
💡 Substitution ciphers replace the original elements with other symbols or values.

</details>

---

### 13. Who is known as the Father of Modern Cryptography?

* [ ] Archie Walls
* [ ] William Frederick Friedman
* [ ] John Warren
* [ ] Donald N Wilber

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** William Frederick Friedman
💡 Friedman was a pioneering cryptographer who contributed to modern cryptographic methods.

</details>

---

### 14. __________ refers to the set of all possible keys that can be used to initialize a cipher.

* [ ] Cryptology
* [ ] Cryptanalysis
* [ ] Key Space
* [ ] Encryption algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key Space
💡 Key space defines the total number of possible keys that a cryptographic algorithm can use.

</details>

---

### 15. A 20-bit key would have a key space of __________________

* [ ] 1,084,572
* [ ] 1,048,578
* [ ] 1,084,576
* [ ] 1,048,576

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1,048,576
💡 Key space = 2^20 = 1,048,576 possible keys.

</details>

---

### 16. The frequency of brute force attacks has increased because:

* [ ] The use of permutations and transpositions in algorithms has increased
* [ ] As algorithms get stronger, they get less complex
* [ ] Processor speed and power has increased
* [ ] Key length reduces over time

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Processor speed and power has increased
💡 Faster computing power allows attackers to attempt more keys per second, making brute force attacks more practical.

</details>

---

### 17. What is the primary purpose of using one-way hashing on user passwords?

* [ ] Minimizes storage requirements
* [ ] Prevents anyone from reading passwords in plaintext
* [ ] Avoids excessive processing by asymmetric algorithms
* [ ] Prevents replay attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Prevents anyone from reading passwords in plaintext
💡 One-way hashing ensures passwords are stored securely and cannot be reversed easily.

</details>

---

### 18. What is the definition of an algorithm's work factor?

* [ ] The time it takes to encrypt and decrypt the same plaintext
* [ ] The time it takes to break the encryption
* [ ] The time it takes to implement 16 rounds of computation
* [ ] The time it takes to apply substitution functions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The time it takes to break the encryption
💡 Work factor quantifies the effort needed to successfully attack a cryptographic algorithm.

</details>

---

### 19. Which of the following is a U.S. federal government algorithm developed for creating secure message digests?

* [ ] Data Encryption Algorithm
* [ ] Digital Signature Standard
* [ ] Secure Hash Algorithm
* [ ] Data Signature Algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secure Hash Algorithm
💡 SHA is a family of cryptographic hash functions standardized by NIST.

</details>

---

### 20. What does DEA stand for?

* [ ] Data Encoding Algorithm
* [ ] Data Encoding Application
* [ ] Data Encryption Algorithm
* [ ] Digital Encryption Algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Encryption Algorithm
💡 DEA is the basis of the DES symmetric-key encryption standard.

</details>

---

### 21. If different keys generate the same ciphertext for the same message, what is this called?

* [ ] Collision
* [ ] Secure hashing
* [ ] MAC
* [ ] Key clustering

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Collision
💡 A collision occurs when two different keys or messages produce the same ciphertext or hash value.

</details>

---

### 22. What does DES stand for?

* [ ] Data Encryption System
* [ ] Data Encryption Standard
* [ ] Data Encoding Standard
* [ ] Data Encryption Signature

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Encryption Standard
💡 DES is a symmetric-key algorithm for encrypting data in blocks.

</details>

---

### 23. Many countries restrict the use or exportation of cryptographic systems because:

* [ ] Without standards, there would be interoperability issues
* [ ] The systems can be used against local populations
* [ ] Criminals could use encryption to avoid detection
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Cryptography restrictions are imposed for national security, interoperability, and crime prevention.

</details>

---

### 24. Which of the following is true about data encryption to protect data?

* [ ] It verifies integrity and accuracy
* [ ] It requires careful key management
* [ ] It does not require system resources
* [ ] It requires keys to be escrowed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It requires careful key management
💡 Effective encryption requires secure handling and storage of keys to maintain security.

</details>

---

### 25. Which of the following is not a property of a one-way hash function?

* [ ] Converts message of arbitrary length into fixed-length value
* [ ] Computationally infeasible to find message from digest
* [ ] Impossible or rare to derive same digest from two messages
* [ ] Converts message of fixed length to arbitrary-length value

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Converts message of fixed length to arbitrary-length value
💡 One-way hashes always produce fixed-length outputs.

</details>

---

### 26. The generation of keys using random values is referred to as Key Derivation Functions (KDFs). Which value is **not commonly used**?

* [ ] Hashing values
* [ ] Asymmetric values
* [ ] Salts
* [ ] Passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric values
💡 KDFs typically use salts, passwords, or hash values to generate strong cryptographic keys.

</details>

---

### 27. What is the goal of cryptanalysis?

* [ ] To determine the strength of an algorithm
* [ ] To increase substitution in algorithms
* [ ] To decrease transposition in algorithms
* [ ] To determine permutations used

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To determine the strength of an algorithm
💡 Cryptanalysis studies cryptographic systems to find weaknesses or vulnerabilities.

</details>

---

### 28. How many bits make up the effective length of the DES key?

* [ ] 56
* [ ] 64
* [ ] 32
* [ ] 16

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 56
💡 DES uses a 64-bit key, but 8 bits are used for parity, leaving 56 effective bits.

</details>

---

### 29. Who was involved in developing the first public key algorithm?

* [ ] Adi Shamir
* [ ] Ross Anderson
* [ ] Bruce Schneier
* [ ] Martin Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Martin Hellman
💡 Hellman, along with Diffie, developed the first public key cryptography system.

</details>

---

### 30. Which of the following uses a symmetric key and a hashing algorithm?

* [ ] HMAC
* [ ] Triple-DES
* [ ] ISAKMP-OAKLEY
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HMAC
💡 HMAC combines a secret key with a hash function to provide integrity and authentication.

</details>

---

### 31. The word Cryptography is derived from the Greek word _____________, meaning "hidden, secret".

* [ ] Krios
* [ ] Kyros
* [ ] Kerberos
* [ ] Kryptos

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kryptos
💡 “Kryptos” in Greek means secret or hidden.

</details>

---

### 32. DES performs how many rounds of permutation and substitution?

* [ ] 16
* [ ] 32
* [ ] 64
* [ ] 56

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 16
💡 DES applies 16 rounds of Feistel structure processing.

</details>

---

### 33. Kerckhoffs principle states that _____________

* [ ] The keyspace should be public
* [ ] The algorithm should be public
* [ ] The key should be public
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The algorithm should be public
💡 Security should rely only on secrecy of the key, not the algorithm.

</details>

---

### 34. In symmetric algorithms, if 100 people need to communicate securely with each other, how many keys are required?

* [ ] 3,820
* [ ] 4,480
* [ ] 4,950
* [ ] 3,480

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 4,950
💡 For N users: Number of keys = N*(N-1)/2 = 100*99/2 = 4,950.

</details>

---

### 35. Which of the following best describes a certificate authority (CA)?

* [ ] Issues private keys and algorithms
* [ ] Validates encryption processes
* [ ] Verifies encryption keys
* [ ] Issues digital certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Issues digital certificates
💡 CAs validate identities and issue certificates binding identities to public keys.

</details>

---

### 36. Simple substitution and transposition ciphers are vulnerable to:

* [ ] Ping of Death
* [ ] Frequency Analysis
* [ ] Denial of Service
* [ ] SQL Injection

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Frequency Analysis
💡 Classic ciphers can be broken by analyzing letter or symbol frequencies.

</details>

---

### 37. Which cryptosystem is based on the difficulty of factoring large numbers into primes?

* [ ] ECC
* [ ] RSA
* [ ] DES
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA relies on the hardness of prime factorization.

</details>

---

### 38. ___________ is mono-alphabetic substitution while ___________ is not.

* [ ] Caesar, Vigenere
* [ ] Vigenere, Caesar
* [ ] MD4, MD5
* [ ] MD5, MD4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Caesar, Vigenere
💡 Caesar cipher is mono-alphabetic; Vigenere uses multiple alphabets.

</details>

---

### 39. What would indicate that a message had been modified?

* [ ] Public key altered
* [ ] Private key altered
* [ ] Message digest altered
* [ ] Message encrypted properly

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Message digest altered
💡 Hash functions detect modifications by producing different digests.

</details>

---

### 40. Which of the following describes the difference between DES and RSA?

* [ ] DES is symmetric, RSA is asymmetric
* [ ] DES is asymmetric, RSA is symmetric
* [ ] Both are hashing algorithms
* [ ] DES creates keys, RSA encrypts messages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES is symmetric, RSA is asymmetric
💡 DES uses the same key for encryption/decryption; RSA uses a key pair.

</details>

---
