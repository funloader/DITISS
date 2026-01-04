> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.

# Session 3: Cryptographic Fundamentals, Ciphers & Protocols – 40 MCQs

---

### 1. Which of the following is considered a **passive security attack**?

* [ ] Man-in-the-middle
* [ ] Eavesdropping
* [ ] Denial of Service (DoS)
* [ ] Phishing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Eavesdropping
💡 Passive attacks monitor or listen to communications without altering them, such as eavesdropping or traffic analysis.

</details>

---

### 2. Which of the following **does not provide confidentiality** by itself?

* [ ] AES
* [ ] RSA
* [ ] SHA-256
* [ ] DES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-256
💡 SHA-256 is a hash function used for integrity verification, not for encryption.

</details>

---

### 3. Which type of cipher **encrypts data in fixed-size blocks**?

* [ ] Stream cipher
* [ ] Block cipher
* [ ] One-time pad
* [ ] Caesar cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Block cipher
💡 Block ciphers encrypt fixed-size blocks (e.g., 64-bit or 128-bit) of plaintext at a time.

</details>

---

### 4. Which of the following is an example of a **stream cipher**?

* [ ] AES
* [ ] RC4
* [ ] DES
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC4
💡 RC4 encrypts data one byte at a time, making it a stream cipher.

</details>

---

### 5. Symmetric key encryption uses:

* [ ] One key for encryption and a different key for decryption
* [ ] Two keys: public and private
* [ ] One key for both encryption and decryption
* [ ] No key at all

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** One key for both encryption and decryption
💡 Symmetric encryption uses a single secret key for both encryption and decryption.

</details>

---

### 6. Which of the following is **asymmetric encryption**?

* [ ] DES
* [ ] AES
* [ ] RSA
* [ ] RC5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA uses a public key for encryption and a private key for decryption.

</details>

---

### 7. Which of the following is the **primary purpose of a cryptographic protocol**?

* [ ] Encrypt large files
* [ ] Define rules for secure communication
* [ ] Generate random numbers
* [ ] Store passwords securely

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Define rules for secure communication
💡 Cryptographic protocols establish secure methods for exchanging information.

</details>

---

### 8. Which symmetric algorithm was **widely used before AES**?

* [ ] DES
* [ ] RSA
* [ ] ECC
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** DES
💡 DES (Data Encryption Standard) was replaced due to small key size vulnerabilities.

</details>

---

### 9. Which of the following is a **characteristic of asymmetric encryption**?

* [ ] Faster than symmetric encryption
* [ ] Same key used for encryption and decryption
* [ ] Uses public and private key pair
* [ ] Cannot be used for digital signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses public and private key pair
💡 Asymmetric encryption involves two mathematically related keys for encryption and decryption.

</details>

---

### 10. The main advantage of **hybrid cryptography** is:

* [ ] Uses only symmetric encryption
* [ ] Combines speed of symmetric and security of asymmetric
* [ ] Requires no keys
* [ ] Provides anonymity

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Combines speed of symmetric and security of asymmetric
💡 Hybrid encryption uses symmetric keys for data and asymmetric encryption for key exchange.

</details>

---

### 11. Which of the following **protocols is used to exchange keys securely**?

* [ ] AES
* [ ] DES
* [ ] Diffie-Hellman
* [ ] SHA-1

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Diffie-Hellman
💡 Diffie-Hellman allows two parties to agree on a shared secret key over an insecure channel.

</details>

---

### 12. Which of the following is **true about block ciphers**?

* [ ] Encrypts data bit by bit
* [ ] Encrypts data in blocks of fixed length
* [ ] Cannot use padding
* [ ] Is slower than asymmetric encryption always

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encrypts data in blocks of fixed length
💡 Block ciphers process plaintext in fixed-size blocks, e.g., AES-128 encrypts 128-bit blocks.

</details>

---

### 13. Which of the following is a **weakness of symmetric key cryptography**?

* [ ] Requires secure key distribution
* [ ] Can provide digital signatures
* [ ] Always slower than asymmetric encryption
* [ ] Cannot encrypt files

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Requires secure key distribution
💡 Symmetric encryption requires both parties to have the same secret key securely distributed.

</details>

---

### 14. Which of the following **hash functions** is commonly used in cryptographic protocols?

* [ ] AES
* [ ] DES
* [ ] SHA-2
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-2
💡 SHA-2 is used to verify message integrity in cryptographic protocols.

</details>

---

### 15. Which asymmetric algorithm is **based on factoring large prime numbers**?

* [ ] AES
* [ ] RSA
* [ ] DES
* [ ] RC5

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RSA
💡 RSA’s security relies on the difficulty of factoring large prime numbers.

</details>

---

### 16. Which cipher uses a **variable key size and number of rounds**?

* [ ] DES
* [ ] RC5
* [ ] AES
* [ ] RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** RC5
💡 RC5 is flexible with block size, key size, and number of encryption rounds.

</details>

---

### 17. What does a **cryptographic protocol** primarily protect against?

* [ ] Unauthorized access
* [ ] Man-in-the-middle attacks
* [ ] Eavesdropping
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Protocols define secure methods for communication, protecting against multiple attack types.

</details>

---

### 18. Which of the following **is NOT a property of cryptographic protocols**?

* [ ] Confidentiality
* [ ] Integrity
* [ ] Availability
* [ ] Authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Availability
💡 Cryptographic protocols focus on confidentiality, integrity, and authentication, not system uptime.

</details>

---

### 19. Which of the following is **true about RSA encryption**?

* [ ] Uses a single secret key
* [ ] Faster than AES for large data
* [ ] Public key encrypts, private key decrypts
* [ ] Cannot be used in digital signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Public key encrypts, private key decrypts
💡 RSA uses a public-private key pair for encryption and decryption.

</details>

---

### 20. What is the **main advantage of asymmetric encryption over symmetric encryption**?

* [ ] Faster encryption
* [ ] Uses a single key
* [ ] Simplifies key distribution
* [ ] Can encrypt large files efficiently

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Simplifies key distribution
💡 Asymmetric encryption allows secure communication without prior exchange of secret keys.

</details>

---

### 21. Which of the following is **true about symmetric key length**?

* [ ] Longer keys are less secure
* [ ] Longer keys are more secure
* [ ] Key length does not affect security
* [ ] Only 56-bit keys are secure

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Longer keys are more secure
💡 Longer keys increase the number of possible combinations, making brute-force attacks harder.

</details>

---

### 22. Which asymmetric cipher is based on **elliptic curves**?

* [ ] AES
* [ ] ECC
* [ ] DES
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ECC
💡 ECC (Elliptic Curve Cryptography) is an asymmetric encryption method using elliptic curve mathematics.

</details>

---

### 23. Which of the following is **true about one-time pad**?

* [ ] Provides perfect secrecy if key is random and as long as plaintext
* [ ] Can be reused for multiple messages
* [ ] Is asymmetric
* [ ] Is a block cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Provides perfect secrecy if key is random and as long as plaintext
💡 One-time pad is theoretically unbreakable if keys are random, used only once, and equal in length to the message.

</details>

---

### 24. Which of the following **cannot provide message integrity**?

* [ ] Hash function
* [ ] HMAC
* [ ] Symmetric encryption alone
* [ ] Digital signature

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric encryption alone
💡 Symmetric encryption ensures confidentiality but not integrity by itself.

</details>

---

### 25. Which cryptographic primitive is **used in digital signatures**?

* [ ] Symmetric encryption
* [ ] Asymmetric encryption
* [ ] Hash functions
* [ ] Both asymmetric encryption and hash functions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both asymmetric encryption and hash functions
💡 Digital signatures use a hash of the message encrypted with a private key.

</details>

---

### 26. Which of the following is a **common key generation method**?

* [ ] Random number generator
* [ ] Password hashing
* [ ] Eavesdropping
* [ ] Man-in-the-middle

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Random number generator
💡 Cryptographic keys must be generated using secure random number generators.

</details>

---

### 27. Which of the following **ensures that encrypted messages cannot be altered**?

* [ ] Symmetric encryption alone
* [ ] Digital signature
* [ ] One-time pad
* [ ] Stream cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signature
💡 Digital signatures provide integrity and non-repudiation for messages.

</details>

---

### 28. Which asymmetric algorithm is **efficient for mobile devices** due to smaller key sizes?

* [ ] RSA
* [ ] ECC
* [ ] DES
* [ ] AES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ECC
💡 ECC provides comparable security to RSA with much smaller key sizes, suitable for resource-constrained devices.

</details>

---

### 29. Which of the following **cryptographic operations is reversible**?

* [ ] Hashing
* [ ] Encryption
* [ ] HMAC
* [ ] Message digest

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encryption
💡 Encryption can be reversed using the appropriate key; hashing is irreversible.

</details>

---

### 30. Which of the following **attacks tries to deduce the key by analyzing ciphertext patterns**?

* [ ] Brute-force attack
* [ ] Ciphertext-only attack
* [ ] Known-plaintext attack
* [ ] Man-in-the-middle

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ciphertext-only attack
💡 Ciphertext-only attacks analyze patterns in encrypted messages to recover the key.

</details>

---

### 31. Which of the following is **true for Feistel ciphers** like DES?

* [ ] Encrypts using substitution-permutation
* [ ] Requires key pair for asymmetric encryption
* [ ] Uses hash functions for encryption
* [ ] Cannot be decrypted

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encrypts using substitution-permutation
💡 Feistel networks use multiple rounds of substitution and permutation for block encryption.

</details>

---

### 32. Which of the following is a **standard asymmetric encryption key size** for RSA?

* [ ] 128-bit
* [ ] 256-bit
* [ ] 2048-bit
* [ ] 64-bit

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 2048-bit
💡 RSA commonly uses 2048-bit or higher keys for secure communication.

</details>

---

### 33. Which of the following **ensures both confidentiality and authentication**?

* [ ] Symmetric encryption
* [ ] Asymmetric encryption with digital signatures
* [ ] Hashing alone
* [ ] Ciphertext-only encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric encryption with digital signatures
💡 Encrypting with the recipient’s public key ensures confidentiality; signing with sender’s private key ensures authentication.

</details>

---

### 34. Which of the following is **true about cryptographic keys**?

* [ ] Longer keys always slow down asymmetric encryption
* [ ] Keys must be generated randomly for security
* [ ] Symmetric keys do not require secrecy
* [ ] Public keys must remain private

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Keys must be generated randomly for security
💡 Cryptographically secure keys require randomness to resist attacks.

</details>

---

### 35. Which of the following **provides non-repudiation**?

* [ ] Symmetric encryption
* [ ] Digital signature
* [ ] One-time pad
* [ ] Stream cipher

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signature
💡 Digital signatures prevent the sender from denying the message.

</details>

---

### 36. Which of the following **encryption schemes uses rounds of substitution and permutation**?

* [ ] AES
* [ ] RSA
* [ ] ECC
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** AES
💡 AES applies multiple rounds of substitution and permutation for strong encryption.

</details>

---

### 37. Which of the following is **true about asymmetric key exchange**?

* [ ] Requires pre-shared secret
* [ ] Can securely exchange keys over insecure channel
* [ ] Cannot be used in digital signatures
* [ ] Uses a single shared key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Can securely exchange keys over insecure channel
💡 Asymmetric algorithms like Diffie-Hellman allow secure key exchange without prior secret sharing.

</details>

---

### 38. Which of the following **cryptosystems is suitable for mobile wallets**?

* [ ] RSA with 4096-bit keys
* [ ] ECC with 256-bit keys
* [ ] DES with 56-bit keys
* [ ] RC4

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** ECC with 256-bit keys
💡 ECC provides strong security with small key sizes, ideal for resource-constrained mobile devices.

</details>

---

### 39. Which protocol **ensures secure message exchange using symmetric keys and integrity checks**?

* [ ] SSL/TLS
* [ ] AES alone
* [ ] SHA alone
* [ ] Diffie-Hellman alone

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SSL/TLS
💡 TLS uses symmetric encryption for data and HMAC for integrity verification.

</details>

---

### 40. Which of the following **attacks can compromise symmetric key cryptography if the key is weak**?

* [ ] Brute-force attack
* [ ] Eavesdropping
* [ ] Man-in-the-middle
* [ ] Replay attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Brute-force attack
💡 Weak symmetric keys can be guessed via exhaustive search (brute-force) attacks.

</details>

---
