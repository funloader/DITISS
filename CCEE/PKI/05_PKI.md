> [!IMPORTANT]
> AI-generated content The questions and answer choices in this module assessment were generated using AI and reviewed by a human author.
Absolutely! Here’s a set of **40 MCQs from Session 5: Diffie-Hellman Key Exchange, Attacks on Encryption, and Cryptographic Issues** in the **requested MCQ format**, at **medium-to-difficult level** suitable for PG-DITISS / CSE graduates:
### Session 5: Diffie-Hellman & Cryptographic Attacks – 40 MCQs

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

### 2. In **Diffie-Hellman key exchange**, which mathematical operation ensures secure key generation?

* [ ] Modular addition
* [ ] Modular exponentiation
* [ ] Bitwise XOR
* [ ] Factorial calculation

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Modular exponentiation
💡 Diffie-Hellman relies on modular exponentiation for secure computation of shared keys.

</details>

---

### 3. The main security threat to Diffie-Hellman key exchange is:

* [ ] Eavesdropping
* [ ] Man-in-the-middle attack
* [ ] Replay attack
* [ ] Phishing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Man-in-the-middle attack
💡 An attacker can intercept and replace public values to compute shared keys with both parties.

</details>

---

### 4. Which of the following is a **brute-force attack**?

* [ ] Trying all possible keys until the correct one is found
* [ ] Capturing network packets
* [ ] Modifying messages in transit
* [ ] Impersonating a trusted party

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Trying all possible keys until the correct one is found
💡 Brute-force attacks attempt every possible key to decrypt a message.

</details>

---

### 5. Which of the following is an **active attack** on cryptography?

* [ ] Eavesdropping
* [ ] Traffic analysis
* [ ] Man-in-the-middle
* [ ] Key guessing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Man-in-the-middle
💡 Active attacks modify or inject messages in transit, unlike passive monitoring attacks.

</details>

---

### 6. Diffie-Hellman key exchange is primarily used for:

* [ ] Encrypting large files
* [ ] Digital signatures
* [ ] Securely exchanging symmetric keys
* [ ] Hashing passwords

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Securely exchanging symmetric keys
💡 Diffie-Hellman allows two parties to agree on a shared secret over an insecure channel.

</details>

---

### 7. Which of the following is true about **Diffie-Hellman**?

* [ ] It provides authentication by default
* [ ] It only provides confidentiality of the shared key
* [ ] It encrypts messages directly
* [ ] It uses RSA for key exchange

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** It only provides confidentiality of the shared key
💡 Diffie-Hellman establishes a shared secret but does not authenticate participants.

</details>

---

### 8. In Diffie-Hellman, both parties agree on a **public base `g` and prime `p`**. Why are these public?

* [ ] They are secret keys
* [ ] They are used to compute the shared key and do not compromise security
* [ ] They are used to encrypt messages
* [ ] They prevent attacks

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** They are used to compute the shared key and do not compromise security
💡 Even though `g` and `p` are public, the discrete logarithm problem ensures the shared secret remains secure.

</details>

---

### 9. Which of the following is an example of a **ciphertext-only attack**?

* [ ] Attacker only has intercepted ciphertext
* [ ] Attacker has plaintext and ciphertext
* [ ] Attacker can modify messages
* [ ] Attacker injects messages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Attacker only has intercepted ciphertext
💡 Ciphertext-only attacks attempt to recover plaintext or keys using intercepted encrypted messages alone.

</details>

---

### 10. Which of the following attacks is based on knowing some **plaintext-ciphertext pairs**?

* [ ] Ciphertext-only attack
* [ ] Known-plaintext attack
* [ ] Brute-force attack
* [ ] Replay attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Known-plaintext attack
💡 The attacker uses known pairs to deduce the encryption key or decrypt other messages.

</details>

---

### 11. The **discrete logarithm problem** is the security basis for:

* [ ] DES
* [ ] RSA
* [ ] Diffie-Hellman
* [ ] AES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Diffie-Hellman
💡 The difficulty of computing discrete logs ensures Diffie-Hellman’s security.

</details>

---

### 12. Which attack exploits **weak key generation or small key space**?

* [ ] Brute-force attack
* [ ] Man-in-the-middle
* [ ] Replay attack
* [ ] Dictionary attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Brute-force attack
💡 Small keys can be guessed through exhaustive search.

</details>

---

### 13. Which of the following **cryptographic issues** can weaken security?

* [ ] Using outdated algorithms
* [ ] Using short keys
* [ ] Poor randomness in key generation
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Weaknesses in algorithms, keys, or randomness compromise cryptographic strength.

</details>

---

### 14. Replay attacks are mitigated by:

* [ ] Using longer keys
* [ ] Adding timestamps or nonces
* [ ] Using DES
* [ ] Using RSA

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Adding timestamps or nonces
💡 Unique timestamps or nonces prevent replaying old messages.

</details>

---

### 15. A **chosen-ciphertext attack (CCA)** occurs when:

* [ ] The attacker can only observe ciphertext
* [ ] The attacker can choose ciphertexts and obtain corresponding plaintext
* [ ] The attacker knows some plaintext
* [ ] None of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** The attacker can choose ciphertexts and obtain corresponding plaintext
💡 CCA exploits a system’s ability to decrypt attacker-chosen ciphertexts.

</details>

---

### 16. Which is a **major limitation of Diffie-Hellman** without authentication?

* [ ] Cannot share a key
* [ ] Susceptible to man-in-the-middle attacks
* [ ] Requires large prime numbers
* [ ] Slower than AES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Susceptible to man-in-the-middle attacks
💡 Without authentication, DH cannot prevent an attacker from intercepting and modifying public values.

</details>

---

### 17. Key exchange algorithms are classified as:

* [ ] Symmetric
* [ ] Asymmetric
* [ ] Both
* [ ] None

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Asymmetric
💡 Key exchange protocols like DH use asymmetric operations to agree on symmetric keys.

</details>

---

### 18. Which of the following **attacks targets weak random number generators**?

* [ ] Brute-force attack
* [ ] Man-in-the-middle
* [ ] Cryptanalysis based on key prediction
* [ ] Replay attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Cryptanalysis based on key prediction
💡 Predictable random numbers can compromise key security.

</details>

---

### 19. The security of Diffie-Hellman depends on:

* [ ] Factoring large integers
* [ ] Discrete logarithms
* [ ] Symmetric encryption
* [ ] Hash functions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Discrete logarithms
💡 Computing discrete logs is hard, which protects DH key exchange.

</details>

---

### 20. In cryptography, a **birthday attack** is used to:

* [ ] Break hash functions
* [ ] Break symmetric ciphers
* [ ] Break asymmetric keys
* [ ] Capture network traffic

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Break hash functions
💡 Birthday attacks exploit hash collisions to find duplicate hash values.

</details>

---

### 21. Which type of attack **intercepts and alters communication**?

* [ ] Passive
* [ ] Active
* [ ] Brute-force
* [ ] Ciphertext-only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Active
💡 Active attacks modify messages or insert fraudulent data into communication.

</details>

---

### 22. The **prime number `p` in DH** should be:

* [ ] Small for efficiency
* [ ] Large and preferably a safe prime
* [ ] Odd
* [ ] Even

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Large and preferably a safe prime
💡 Large primes prevent attackers from solving the discrete logarithm problem efficiently.

</details>

---

### 23. Which of the following is a **dictionary attack**?

* [ ] Trying every possible key
* [ ] Using a precompiled list of passwords
* [ ] Observing traffic
* [ ] Modifying messages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using a precompiled list of passwords
💡 Dictionary attacks guess passwords using commonly used words or phrases.

</details>

---

### 24. Which of the following ensures **forward secrecy**?

* [ ] Using long-term static keys
* [ ] Using ephemeral session keys
* [ ] Using DES
* [ ] Reusing the same key

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Using ephemeral session keys
💡 Ephemeral keys prevent compromise of past sessions even if long-term keys are exposed.

</details>

---

### 25. In **cryptography, an avalanche effect** refers to:

* [ ] Small input changes causing major output changes
* [ ] Same input giving same output
* [ ] Same output from different keys
* [ ] Unchanged ciphertext

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Small input changes causing major output changes
💡 Avalanche effect ensures that small changes in plaintext or key drastically change ciphertext.

</details>

---

### 26. Which attack tries to **decrypt messages without knowledge of the key**?

* [ ] Ciphertext-only attack
* [ ] Man-in-the-middle
* [ ] Replay attack
* [ ] Phishing

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Ciphertext-only attack
💡 Only the ciphertext is available; the attacker attempts to recover plaintext or key.

</details>

---

### 27. A **weak key** is one that:

* [ ] Cannot be used
* [ ] Produces predictable ciphertext patterns
* [ ] Is always prime
* [ ] Generates secure encryption

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Produces predictable ciphertext patterns
💡 Weak keys reduce cipher strength and make brute-force attacks easier.

</details>

---

### 28. Which of the following **attacks targets reused keys in symmetric encryption**?

* [ ] Replay attack
* [ ] Key reuse attack
* [ ] Brute-force attack
* [ ] Dictionary attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Key reuse attack
💡 Reusing keys can allow attackers to analyze patterns and recover plaintext.

</details>

---

### 29. To secure DH against **MITM attacks**, which technique is used?

* [ ] Larger primes
* [ ] Digital signatures or certificates
* [ ] AES encryption
* [ ] Short keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Digital signatures or certificates
💡 Authentication ensures the shared key is established with the correct party.

</details>

---

### 30. Which of the following **cryptographic issues** can arise from poor implementation?

* [ ] Weak keys
* [ ] Side-channel attacks
* [ ] Predictable random numbers
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Improper implementation can compromise otherwise secure algorithms.

</details>

---

### 31. A **chosen-plaintext attack** assumes the attacker can:

* [ ] Only observe ciphertext
* [ ] Encrypt arbitrary plaintexts and obtain ciphertexts
* [ ] Modify ciphertext
* [ ] Break hash functions

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Encrypt arbitrary plaintexts and obtain ciphertexts
💡 The attacker uses known ciphertexts of chosen plaintexts to deduce the key.

</details>

---

### 32. Diffie-Hellman does not provide:

* [ ] Confidentiality of shared key
* [ ] Authentication
* [ ] Forward secrecy
* [ ] Key exchange

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Authentication
💡 DH only ensures confidentiality of the shared key; authentication must be added separately.

</details>

---

### 33. Man-in-the-middle attacks on DH are prevented by:

* [ ] Using small primes
* [ ] Verifying public keys using digital signatures
* [ ] Shortening key length
* [ ] Using AES

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Verifying public keys using digital signatures
💡 Authentication prevents attackers from intercepting and substituting keys.

</details>

---

### 34. Which of the following attacks is **not applicable to Diffie-Hellman**?

* [ ] MITM
* [ ] Brute-force discrete log
* [ ] Phishing
* [ ] Chosen-plaintext

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Phishing
💡 Phishing targets users, not the DH algorithm itself.

</details>

---

### 35. Which of the following is a **limitation of brute-force attacks**?

* [ ] Requires negligible computation
* [ ] Becomes impractical with large key sizes
* [ ] Always succeeds instantly
* [ ] Works on public keys only

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Becomes impractical with large key sizes
💡 Exponentially large key spaces prevent brute-force attacks from succeeding quickly.

</details>

---

### 36. Which property ensures **cryptographic strength against known attacks**?

* [ ] Strong keys and randomness
* [ ] Small key size
* [ ] Weak algorithm
* [ ] Reused keys

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Strong keys and randomness
💡 Proper key length and unpredictability are critical to security.

</details>

---

### 37. Which of the following is **vulnerable to MITM if unauthenticated**?

* [ ] RSA key exchange
* [ ] Diffie-Hellman key exchange
* [ ] AES encryption
* [ ] SHA-256

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Diffie-Hellman key exchange
💡 Without authentication, DH is susceptible to MITM attacks.

</details>

---

### 38. Which attack targets **cryptographic hash functions**?

* [ ] Birthday attack
* [ ] Replay attack
* [ ] Brute-force key attack
* [ ] Known-plaintext attack

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Birthday attack
💡 Birthday attacks find hash collisions to compromise integrity.

</details>

---

### 39. Which of the following is **true about a key exchange**?

* [ ] Always encrypts messages
* [ ] Establishes a shared secret
* [ ] Signs messages
* [ ] Hashes messages

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** Establishes a shared secret
💡 Key exchange algorithms allow secure sharing of a symmetric key.

</details>

---

### 40. Cryptographic attacks exploit:

* [ ] Weaknesses in algorithms
* [ ] Weaknesses in key management
* [ ] Implementation flaws
* [ ] All of the above

<details>
<summary><strong>Show Answer</strong></summary>

✅ **Correct Answer:** All of the above
💡 Security failures can result from algorithm, key, or implementation weaknesses.

</details>

---
