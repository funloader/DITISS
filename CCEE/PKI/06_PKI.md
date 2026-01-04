> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
# Session 6: Secure Hashing Methods – 40 MCQs

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

### 2. SHA stands for:

* [ ] Secure Hash Algorithm
* [ ] Symmetric Hash Algorithm
* [ ] Secure HMAC Algorithm
* [ ] Signed Hash Authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Secure Hash Algorithm
💡 SHA is a family of cryptographic hash functions used for data integrity.

</details>

---

### 3. Which of the following is a **key property of a cryptographic hash function**?

* [ ] Encryption reversibility
* [ ] Collision resistance
* [ ] Key exchange
* [ ] Symmetric encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Collision resistance
💡 Hash functions should produce unique outputs for different inputs to prevent collisions.

</details>

---

### 4. HMAC combines:

* [ ] Hash functions with a secret key
* [ ] Symmetric encryption with asymmetric keys
* [ ] Public-key cryptography with hash functions
* [ ] Digital certificates and hashes

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hash functions with a secret key
💡 HMAC uses a secret key and hash function to provide integrity and authentication.

</details>

---

### 5. Which SHA variant produces a **256-bit hash**?

* [ ] SHA-1
* [ ] SHA-256
* [ ] SHA-512
* [ ] SHA-384

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-256
💡 SHA-256 generates a 256-bit output and is widely used in modern cryptography.

</details>

---

### 6. SHA-1 is considered insecure because of:

* [ ] Weak key size
* [ ] Collision vulnerabilities
* [ ] Slow performance
* [ ] Limited hashing output

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Collision vulnerabilities
💡 SHA-1 is prone to collisions and is deprecated for secure applications.

</details>

---

### 7. Which of the following is a property of **cryptographic hash functions**?

* [ ] Reversible
* [ ] Deterministic
* [ ] Requires a key
* [ ] Uses asymmetric encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Deterministic
💡 The same input always produces the same hash output.

</details>

---

### 8. Which of the following ensures **data integrity**?

* [ ] Hash functions
* [ ] Symmetric encryption
* [ ] Asymmetric encryption
* [ ] Digital signatures

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hash functions
💡 Hash functions can detect even small changes in data.

</details>

---

### 9. In HMAC, the **secret key** is used to:

* [ ] Encrypt the message
* [ ] Generate a keyed hash
* [ ] Generate a public key
* [ ] Verify certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Generate a keyed hash
💡 The key ensures that only someone with the key can verify the integrity of the message.

</details>

---

### 10. SHA-512 generates a hash of:

* [ ] 128 bits
* [ ] 256 bits
* [ ] 512 bits
* [ ] 1024 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 512 bits
💡 SHA-512 produces a 512-bit digest.

</details>

---

### 11. Which of the following is NOT a characteristic of a secure hash function?

* [ ] Preimage resistance
* [ ] Collision resistance
* [ ] Key secrecy
* [ ] Avalanche effect

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key secrecy
💡 Hash functions are usually keyless unless used in HMAC; key secrecy is not a property of standard hashes.

</details>

---

### 12. The **avalanche effect** in hashing means:

* [ ] Small change in input changes the hash drastically
* [ ] Hash function can be reversed
* [ ] Output size depends on input size
* [ ] Key is required for hashing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Small change in input changes the hash drastically
💡 This ensures that even minor data changes produce very different hashes.

</details>

---

### 13. HMAC provides:

* [ ] Confidentiality only
* [ ] Integrity and authenticity
* [ ] Non-repudiation
* [ ] Public key distribution

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Integrity and authenticity
💡 HMAC ensures the message has not been altered and comes from a valid source.

</details>

---

### 14. Which of the following is a **collision attack**?

* [ ] Finding two messages with the same hash
* [ ] Cracking symmetric encryption
* [ ] Intercepting network packets
* [ ] Brute-forcing passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Finding two messages with the same hash
💡 Collision attacks exploit weaknesses in hash functions where two inputs produce the same output.

</details>

---

### 15. SHA-3 differs from SHA-2 because:

* [ ] Uses a sponge construction
* [ ] Uses the same Merkle–Damgård structure
* [ ] Is symmetric encryption
* [ ] Produces variable key lengths

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Uses a sponge construction
💡 SHA-3 uses the Keccak sponge function for hashing.

</details>

---

### 16. Which of the following is used in **digital signatures** for integrity?

* [ ] AES
* [ ] HMAC or SHA hash
* [ ] RSA encryption only
* [ ] Diffie-Hellman

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** HMAC or SHA hash
💡 Hashes provide integrity before signing a message.

</details>

---

### 17. SHA-1 produces a hash of:

* [ ] 128 bits
* [ ] 160 bits
* [ ] 256 bits
* [ ] 512 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 160 bits
💡 SHA-1 outputs a 160-bit digest but is considered insecure.

</details>

---

### 18. HMAC requires:

* [ ] Only a hash function
* [ ] Only a secret key
* [ ] Both hash function and secret key
* [ ] A digital certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both hash function and secret key
💡 HMAC combines hashing with a secret key for message authentication.

</details>

---

### 19. Which attack is prevented by HMAC?

* [ ] Eavesdropping
* [ ] Message tampering
* [ ] Man-in-the-middle without key
* [ ] Replay attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Message tampering
💡 HMAC ensures that unauthorized modification of messages is detected.

</details>

---

### 20. The **preimage resistance** property means:

* [ ] Easy to reverse hash function
* [ ] Impossible to find original input from hash
* [ ] Hash output is predictable
* [ ] Two inputs can produce same hash

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Impossible to find original input from hash
💡 Preimage resistance prevents attackers from deducing the input from a hash.

</details>

---

### 21. Which of the following **SHA variants is fastest on 64-bit systems**?

* [ ] SHA-1
* [ ] SHA-224
* [ ] SHA-256
* [ ] SHA-512

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-512
💡 SHA-512 is optimized for 64-bit platforms.

</details>

---

### 22. The **HMAC process** includes which of the following steps?

* [ ] XOR key with ipad and opad
* [ ] Hashing the concatenated result
* [ ] Both of the above
* [ ] Only key padding

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both of the above
💡 HMAC uses inner and outer padding with hashing for authentication.

</details>

---

### 23. HMAC is widely used in:

* [ ] TLS/SSL
* [ ] IPSec
* [ ] API authentication
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 HMAC provides integrity and authentication in many protocols.

</details>

---

### 24. Collision resistance in SHA-2 prevents:

* [ ] Finding two messages with same hash
* [ ] Brute-forcing passwords
* [ ] Eavesdropping
* [ ] Man-in-the-middle

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Finding two messages with same hash
💡 This property ensures unique hashes for different messages.

</details>

---

### 25. SHA-3 is standardized by:

* [ ] NIST
* [ ] ISO
* [ ] IEEE
* [ ] IETF

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** NIST
💡 NIST standardized SHA-3 after the Keccak competition.

</details>

---

### 26. Which of the following **cannot be reversed**?

* [ ] Symmetric encryption
* [ ] Hash functions
* [ ] Asymmetric encryption
* [ ] Digital certificates

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Hash functions
💡 Hashing is one-way; original input cannot be retrieved from output.

</details>

---

### 27. HMAC provides **security against**:

* [ ] Key guessing only
* [ ] Message tampering and forgery
* [ ] Replay attacks only
* [ ] Eavesdropping only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Message tampering and forgery
💡 HMAC ensures integrity and authenticity.

</details>

---

### 28. Which property ensures **hash output changes drastically** with small input changes?

* [ ] Preimage resistance
* [ ] Avalanche effect
* [ ] Collision resistance
* [ ] Key secrecy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Avalanche effect
💡 Small changes in input produce significant changes in hash output.

</details>

---

### 29. HMAC uses which of the following operations?

* [ ] XOR with key
* [ ] Inner and outer hashing
* [ ] Both
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Both
💡 HMAC pads the key and hashes inner and outer results for security.

</details>

---

### 30. Which SHA variant produces a 384-bit output?

* [ ] SHA-256
* [ ] SHA-384
* [ ] SHA-512
* [ ] SHA-224

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-384
💡 SHA-384 truncates SHA-512 output to 384 bits.

</details>

---

### 31. Which property ensures it’s hard to find **two inputs with same hash**?

* [ ] Preimage resistance
* [ ] Collision resistance
* [ ] Second preimage resistance
* [ ] Key secrecy

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Collision resistance
💡 This property prevents two distinct messages from producing the same hash.

</details>

---

### 32. HMAC ensures **message authentication** because:

* [ ] The hash is public
* [ ] Only the sender and receiver know the secret key
* [ ] It encrypts messages
* [ ] It signs the message with certificate

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Only the sender and receiver know the secret key
💡 The key ensures that only authorized parties can verify the hash.

</details>

---

### 33. SHA-224 produces a hash of:

* [ ] 224 bits
* [ ] 256 bits
* [ ] 384 bits
* [ ] 512 bits

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** 224 bits
💡 SHA-224 is a truncated version of SHA-256.

</details>

---

### 34. Which of the following is NOT an application of HMAC?

* [ ] Email integrity
* [ ] API authentication
* [ ] Symmetric encryption key generation
* [ ] TLS/SSL message authentication

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Symmetric encryption key generation
💡 HMAC provides authentication and integrity, not key generation.

</details>

---

### 35. Which attack exploits **hash collisions**?

* [ ] Birthday attack
* [ ] Replay attack
* [ ] Man-in-the-middle
* [ ] Brute-force key attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Birthday attack
💡 Birthday attacks find two inputs producing the same hash.

</details>

---

### 36. SHA-2 family includes:

* [ ] SHA-1, SHA-224, SHA-256
* [ ] SHA-224, SHA-256, SHA-384, SHA-512
* [ ] SHA-1, SHA-256, SHA-512
* [ ] SHA-3 only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-224, SHA-256, SHA-384, SHA-512
💡 SHA-2 is a family of secure hash algorithms.

</details>

---

### 37. Which hash property ensures it’s hard to find **a different input with same hash as known input**?

* [ ] Preimage resistance
* [ ] Second preimage resistance
* [ ] Collision resistance
* [ ] Avalanche effect

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Second preimage resistance
💡 Second preimage resistance prevents an attacker from finding another input with the same hash as a given input.

</details>

---

### 38. Which HMAC input is concatenated first?

* [ ] Outer padded key with hash
* [ ] Inner padded key with message
* [ ] Message only
* [ ] Key only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Inner padded key with message
💡 Inner padding is concatenated with message before hashing.

</details>

---

### 39. Which of the following is considered **collision-resistant and secure** for current applications?

* [ ] SHA-1
* [ ] SHA-256
* [ ] MD5
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** SHA-256
💡 SHA-256 is currently secure and widely recommended.

</details>

---

### 40. HMAC is **resistant to collision attacks** because:

* [ ] Key is secret and hash is applied twice
* [ ] Hash function is symmetric
* [ ] It uses SHA-1 only
* [ ] Hash output is reversible

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key is secret and hash is applied twice
💡 Double hashing with a secret key prevents collision exploitation.

</details>

---
