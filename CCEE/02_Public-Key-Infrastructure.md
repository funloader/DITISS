> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
---

### 1. Which protocol and port must be allowed in an interface ACL to permit secure remote management access to a router?

* [ ] TCP 443
* [ ] UDP 500
* [ ] TCP 22
* [ ] UDP 4500

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** TCP 22
💡 TCP port 22 is used by SSH, which provides secure remote management access to routers.

</details>

---

### 2. If a parameter is omitted in an ISAKMP/IKE Phase 1 policy on modern Cisco IOS, which of the following is **not** a default value?

* [ ] DES
* [ ] SHA-1
* [ ] DH group 1
* [ ] MD5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** MD5
💡 Modern Cisco IOS defaults to SHA-1 for hashing; MD5 is no longer the default.

</details>

---

### 3. What is the default lifetime of IPSec data Security Associations (SAs) if not configured?

* [ ] 300 seconds
* [ ] 600 seconds
* [ ] 3,600 seconds
* [ ] 86,400 seconds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 3,600 seconds
💡 IPSec Phase 2 SAs default to a lifetime of 3,600 seconds.

</details>

---

### 4. What is the default IPSec transform mode if not explicitly specified?

* [ ] Transport
* [ ] Symmetric
* [ ] Transform
* [ ] Tunnel

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Tunnel
💡 Tunnel mode is the default and encapsulates the entire IP packet.

</details>

---

### 5. Which of the following is **not required** in a static crypto map configuration?

* [ ] Crypto ACL
* [ ] Transform set name
* [ ] Peer IP address
* [ ] Local router IP address

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Local router IP address
💡 The router’s local address is inferred from the interface.

</details>

---

### 6. Which traffic is dropped when using static crypto maps with IPSec?

* [ ] Encrypted inbound traffic matching the crypto ACL
* [ ] Inbound traffic not matching the crypto ACL
* [ ] Inbound traffic matching the crypto ACL but sent in clear text
* [ ] Outbound encrypted traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inbound traffic matching the crypto ACL but sent in clear text
💡 Traffic that should be protected but arrives unencrypted is dropped.

</details>

---

### 7. Which ISAKMP state indicates that Phase 2 (Quick Mode) negotiation is complete?

* [ ] MM_NO_STATE
* [ ] QM_IDLE
* [ ] MM_SA_SETUP
* [ ] MM_KEY_AUTH

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** QM_IDLE
💡 QM_IDLE indicates successful IPSec SA establishment.

</details>

---

### 8. Which debug message indicates a failed ISAKMP policy negotiation?

* [ ] %CRYPTO-6-IKMP_SA_NOT_OFFERED
* [ ] %CRYPTO-6-IKMP_SA_NOT_AUTH
* [ ] IPSEC(validate_transform_proposal)
* [ ] IPSEC(validate_proposal)

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** %CRYPTO-6-IKMP_SA_NOT_OFFERED
💡 The peers could not agree on policy attributes.

</details>

---

### 9. Which crypto map command specifies the ACL that defines interesting traffic?

* [ ] set transform-set
* [ ] match address
* [ ] set peer
* [ ] set authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** match address
💡 This command links traffic selection to an ACL.

</details>

---

### 10. Which command configures a preshared key for an ISAKMP peer at 192.1.1.1?

* [ ] crypto key generate rsa
* [ ] crypto isakmp key abc123 address 192.1.1.1
* [ ] crypto isakmp policy authentication pre-share
* [ ] crypto transform-set esp-3des

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** crypto isakmp key abc123 address 192.1.1.1
💡 This command binds the preshared key to the peer.

</details>

---

### 11. Atbash is an example of a:

* [ ] Substitution cipher
* [ ] Transposition cipher
* [ ] Stream cipher
* [ ] Block cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Substitution cipher
💡 Atbash maps each letter to its alphabetic opposite.

</details>

---

### 12. Which cipher replaces bits, characters, or blocks with other values?

* [ ] Substitution
* [ ] Transposition
* [ ] Hashing
* [ ] Permutation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Substitution
💡 Substitution changes symbols; transposition changes order.

</details>

---

### 13. Who is known as the father of modern cryptography?

* [ ] Claude Shannon
* [ ] William F. Friedman
* [ ] Whitfield Diffie
* [ ] Bruce Schneier

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** William F. Friedman
💡 Friedman laid foundational work in modern cryptology.

</details>

---

### 14. What term describes the total number of possible keys for a cipher?

* [ ] Cryptanalysis
* [ ] Key space
* [ ] Entropy
* [ ] Algorithm strength

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key space
💡 Larger key spaces increase resistance to brute-force attacks.

</details>

---

### 15. A 20-bit key has a key space of:

* [ ] 1,084,576
* [ ] 1,048,576
* [ ] 1,024,000
* [ ] 1,000,000

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 1,048,576
💡 Key space = 2²⁰.

</details>

---

### 16. Why have brute-force attacks become more feasible?

* [ ] Algorithms are weaker
* [ ] Keys are shorter
* [ ] Increased processing power
* [ ] Reduced encryption rounds

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Increased processing power
💡 Faster CPUs and GPUs allow more key attempts per second.

</details>

---

### 17. Why are passwords stored using one-way hashes?

* [ ] To reduce storage space
* [ ] To prevent plaintext recovery
* [ ] To speed authentication
* [ ] To prevent replay attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** To prevent plaintext recovery
💡 Hashes cannot be feasibly reversed.

</details>

---

### 18. What does an algorithm’s work factor measure?

* [ ] Encryption speed
* [ ] Decryption speed
* [ ] Effort required to break it
* [ ] Number of rounds used

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Effort required to break it
💡 Higher work factor means stronger security.

</details>

---

### 19. Which U.S. standard defines secure hash functions?

* [ ] DSS
* [ ] DEA
* [ ] SHA
* [ ] DSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA
💡 SHA is standardized by NIST.

</details>

---

### 20. What does DEA stand for?

* [ ] Data Encryption Algorithm
* [ ] Digital Encryption Algorithm
* [ ] Data Encoding Algorithm
* [ ] Digital Encoding Algorithm

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Encryption Algorithm
💡 DEA underlies the DES standard.

</details>

---

### 21. When multiple keys produce the same ciphertext for the same plaintext, this is called:

* [ ] Collision
* [ ] Key clustering
* [ ] Hash overlap
* [ ] Key exhaustion

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key clustering
💡 Key clustering weakens encryption by reducing uniqueness.

</details>

---

### 22. What does DES stand for?

* [ ] Data Encryption System
* [ ] Data Encryption Standard
* [ ] Digital Encryption Standard
* [ ] Data Encoding Standard

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Data Encryption Standard
💡 DES is a symmetric block cipher.

</details>

---

### 23. Why do some governments regulate cryptographic systems?

* [ ] Criminal misuse concerns
* [ ] National security
* [ ] Interoperability
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Regulations balance security, commerce, and law enforcement.

</details>

---

### 24. Which statement about encryption is true?

* [ ] It guarantees integrity
* [ ] It requires careful key management
* [ ] It eliminates access control
* [ ] It requires key escrow

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It requires careful key management
💡 Key protection is critical to encryption security.

</details>

---

### 25. Which is NOT a property of a one-way hash function?

* [ ] Fixed-length output
* [ ] Preimage resistance
* [ ] Collision resistance
* [ ] Variable-length output

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Variable-length output
💡 Hashes always produce fixed-length digests.

</details>

---

### 26. Which input is NOT commonly used by key derivation functions?

* [ ] Passwords
* [ ] Salts
* [ ] Master keys
* [ ] Asymmetric keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric keys
💡 KDFs typically derive keys from symmetric secrets.

</details>

---

### 27. What is the primary goal of cryptanalysis?

* [ ] Improve encryption speed
* [ ] Recover plaintext or keys without authorization
* [ ] Increase key length
* [ ] Design algorithms

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Recover plaintext or keys without authorization
💡 Cryptanalysis seeks to break cryptographic protections.

</details>

---

### 28. What is the effective key length of DES?

* [ ] 64 bits
* [ ] 56 bits
* [ ] 48 bits
* [ ] 32 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 56 bits
💡 8 bits are used for parity.

</details>

---

### 29. Who co-developed the first public key cryptosystem?

* [ ] Adi Shamir
* [ ] Martin Hellman
* [ ] Bruce Schneier
* [ ] Ron Rivest

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Martin Hellman
💡 Hellman and Diffie introduced public key cryptography.

</details>

---

### 30. Which uses a secret key combined with a hash function?

* [ ] RSA
* [ ] Triple-DES
* [ ] HMAC
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HMAC
💡 HMAC ensures integrity and authentication.

</details>

---

### 31. The word cryptography comes from the Greek word meaning “hidden”:

* [ ] Kyros
* [ ] Kerberos
* [ ] Kryptos
* [ ] Krypto

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Kryptos

</details>

---

### 32. How many rounds does DES use?

* [ ] 8
* [ ] 16
* [ ] 32
* [ ] 64

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 16

</details>

---

### 33. Kerckhoffs’ principle states that:

* [ ] The key must be public
* [ ] The algorithm must be public
* [ ] The system must be secret
* [ ] Keys must be escrowed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The algorithm must be public

</details>

---

### 34. How many symmetric keys are needed for 100 users to communicate securely?

* [ ] 3,820
* [ ] 4,480
* [ ] 4,950
* [ ] 5,000

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 4,950

</details>

---

### 35. What is the role of a Certificate Authority (CA)?

* [ ] Encrypt data
* [ ] Issue digital certificates
* [ ] Generate private keys
* [ ] Store passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Issue digital certificates

</details>

---

### 36. Classical substitution ciphers are vulnerable to:

* [ ] SQL injection
* [ ] Frequency analysis
* [ ] Denial of service
* [ ] Buffer overflow

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Frequency analysis

</details>

---

### 37. Which cryptosystem relies on integer factorization?

* [ ] DES
* [ ] ECC
* [ ] RSA
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA

</details>

---

### 38. Which cipher is monoalphabetic?

* [ ] Caesar
* [ ] Vigenère
* [ ] AES
* [ ] DES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Caesar

</details>

---

### 39. What indicates that a message was modified?

* [ ] Encryption used
* [ ] Message digest changed
* [ ] Public key changed
* [ ] Ciphertext length changed

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Message digest changed

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
